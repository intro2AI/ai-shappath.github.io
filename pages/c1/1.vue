<template>
	<div class="page">
		<NuxtLink to="/" class="close">CLOSE</NuxtLink>
		<header class="">
			<div class="title">
				<div class="univers -type-l">
					Large Language Model capabilities
				</div>
				<div class="questions">
					<div v-for="(q, i) in questions" class="question">
						{{ q }}
					</div>
				</div>
			</div>
			<LayoutMap></LayoutMap>
		</header>
		
		<main>
			<div class="content">
				<img 
				src="https://d2w9rnfcy7mm78.cloudfront.net/17023232/original_6076caf38d78aceedbb6713051e4a9ed.gif?1656415167?bc=0" 
				alt="GIF" 
				style="width: 100%; height: auto; aspect-ratio: 1/1;"
				/>
				<p>
				<p class="citation">
					Artist: Andre do Amaral, via <a href='https://savee.it/i/vJsv7N5/' target="_blank" rel="noopener noreferrer" style='text-decoration: underline;'>Savee.it</a><br/>
				</p>




				<br />
					In this chapter we will immerse ourselves into Generative AI Chatbots, also known as Large Language Models (LLMs).
					We will understand through examples - what LLMs are, the kinds of tasks they are capable of doing, and how you can fit LLMs into workflows and processes in your domain of interest.<br />
					Keywords: Prompt Engineering("we program the LLM using prompts"), Chain of thought prompting, In-context-learning, 
				<br />
				</p>
				
				<p><br/><br/>
				<a href='https://www.perplexity.ai/' target="_blank" rel="noopener noreferrer" style='text-decoration: underline;'>Perplexity</a>: faster search and research<br/><br/>
				<a href='https://claude.ai/new' target="_blank" rel="noopener noreferrer" style='text-decoration: underline;'>Claude</a>: For chatting and "translating" one thing into another<br/><br/>
				<a href='https://goblin.tools/' target="_blank" rel="noopener noreferrer" style='text-decoration: underline;'>Goblin Tools</a>: A set of very useful tools<br/><br/>
				<a href='https://build.nvidia.com/nvidia/nemotron-4-mini-hindi-4b-instruct' target="_blank" rel="noopener noreferrer" style='text-decoration: underline;'>Nemotron Hindi</a>: A Language Model tailored for the Hindi Language<br/><br/>
				<a href='https://huggingface.co/l3cube-pune/marathi-gpt-gemma-7b' target="_blank" rel="noopener noreferrer" style='text-decoration: underline;'>Gemma Marathi</a>: A Language Model tailored for the Marathi Language<br/><br/>
				<a href='https://huggingface.co/l3cube-pune/marathi-sentiment-md' target="_blank" rel="noopener noreferrer" style='text-decoration: underline;'>MahaSent-MD</a>: Marathi sentiment analysis<br/><br/>
				<a href='https://huggingface.co/spaces/BlinkDL/RWKV-Gradio-1' target="_blank" rel="noopener noreferrer" style='text-decoration: underline;'>RWKV-x060-World</a>:  Sequence model for 100+ languages<br/><br/>
				<a href='https://notebooklm.google/' target="_blank" rel="noopener noreferrer" style='text-decoration: underline;'>NotebookLM</a>: For chatting with books and webpages<br/><br/>
				<a href='https://aistudio.google.com/prompts/new_chat' target="_blank" rel="noopener noreferrer" style='text-decoration: underline;'>Google AI Studio</a>: for quick fine-tuning<br/><br/>
				<a href='https://gemini.google.com/gems/view' target="_blank" rel="noopener noreferrer" style='text-decoration: underline;'>Google Gemini</a>: Sync across your Google Workspace<br/><br/>
				<a href='https://www.deeplearning.ai/short-courses/practical-multi-ai-agents-and-advanced-use-cases-with-crewai/' target="_blank" rel="noopener noreferrer" style='text-decoration: underline;'>CrewAI Multi Agent Systems</a>: Automate complex tasks which take in fuzzy inputs<br/><br/>
				<a href='https://concepts.engine.study/' target="_blank" rel="noopener noreferrer" style='text-decoration: underline;'>Colourful Concepts</a>: drag and combine concepts<br/><br/>
				<a href='https://clay.thoughtandcraft.com/' target="_blank" rel="noopener noreferrer" style='text-decoration: underline;'>Clay</a>: roaming in sentence space<br/><br/>
				<a href='https://textfx.withgoogle.com/' target="_blank" rel="noopener noreferrer" style='text-decoration: underline;'>TextFx</a>: AI-powered tools for rappers, writers, and wordsmiths><br/><br/>
				<a href='https://www.aitudes.com/' target="_blank" rel="noopener noreferrer" style='text-decoration: underline;'>Aititudes</a>: Small AI tools for writing<br/><br/>
				</p>
			</div>
		</main>
		<ElementsNavigation :current="currentRoute.path"></ElementsNavigation>
	</div>
</template>

<script setup>
	definePageMeta({
		layout: 'default',
	})

	const { width } = useWindowSize()

	const { currentRoute } = useRouter()
	const questions = await getQuestions(currentRoute.value.path)

	// onMounted(() => {
	// 	const paragraphs = document.querySelectorAll('p')
	// 	countParagraphs(paragraphs, currentRoute.value.path)
	// })
</script>
