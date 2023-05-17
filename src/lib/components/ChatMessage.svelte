<script lang="ts">
	import type { ChatCompletionRequestMessageRoleEnum } from 'openai'
	export let type: ChatCompletionRequestMessageRoleEnum
	export let message: string
</script>

<div class="chat {type === 'user' ? 'chat-end' : 'chat-start'} justify-end">
	<div class="chat-image avatar">
		<div class="w-10 rounded-full">
			<img
			    src="{type === 'user' ? 'https://img.icons8.com/?size=512&id=8nVspI3zH2dt&format=png' : 'https://img.icons8.com/?size=512&id=D45ofLrj1Mp5&format=png'}"
				alt="{type} avatar"
			/>
		</div>
	</div>
	<div class="chat-header">
		{type === 'user' ? 'Me' : 'Bot'}
	</div>
	<div class="chat-bubble {type === 'user' ? 'chat-bubble-primary' : 'chat-bubble-secondary'}">
		{message}
	</div>
</div>
