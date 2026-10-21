# node-banana: narration transcript

The spoken narration of `architecture-explainer.html` (commit `8929b7a`), in order, with the time each line starts. The voice is Kokoro `af_heart`, rendered locally. In the page, the same lines form the transcript beside the animation (click a line to jump there) and the captions.

## 1. A local node editor for AI media (0:00–0:14)

**0:00** Node Banana is a node editor for AI media, running on your own machine.

**0:05** Press Run, and the graph calls AI providers with your own key.

**0:10** The image comes back to the node that asked for it.

## 2. Who owns what (0:14–0:42)

**0:15** In the browser, you wire typed nodes on a canvas; a store runs them.

**0:20** Executors do each node's work; the recorder uploads each output.

**0:25** On the server, the generate route picks a provider; an adapter makes the call.

**0:30** The asset library keeps every output on disk; workflows save as files.

**0:36** An agent chat builds and edits workflows on your Claude Code or Codex login.

## 3. One Run, end to end (0:42–1:13)

**0:43** The canvas catches Cmd/Ctrl+Enter.

**0:46** runBatch repeats the run as often as you set.

**0:49** The store runs inputs first, then the image executor.

**0:52** The node shows a spinner and calls the server.

**0:55** The route picks Gemini, preferring your Settings key.

**0:58** The adapter calls Gemini, retrying brief errors, and the image comes back.

**1:04** The recorder takes the image, returning an ID.

**1:07** The node shows the image and keeps its ID.

**1:10** Meanwhile, the upload lands on disk.

## 4. What survives a crash (1:13–1:38)

**1:14** Saves write a temp file, then rename it into place.

**1:17** Outputs and their record files, called sidecars, land the same way.

**1:22** In the web app, a crash loses the request, unsaved edits and queued uploads.

**1:28** No run resumes; the library reloads from sidecars, the graph from a saved file.

**1:33** The desktop app can restore your session, but never resends a request.

## 5. Three decisions that shape it (1:38–2:03)

**1:39** First, your Settings key rides each request, in a header.

**1:43** Other sites can't call the server to spend your credits.

**1:46** Second, every output is saved; the browser mints its ID.

**1:50** So a retried upload gets back the same record.

**1:53** Third, the agent edits but can't start a run, so a planted prompt can't spend credits.

**1:59** It offers a Run button; only your press starts the run.

## 6. Reading the tree (2:03–2:19)

**2:04** The API folder holds the server routes and adapters.

**2:08** Components and the store, with its executors, run in the browser.

**2:12** Lib holds the recorder, the on-disk library and the agent.

**2:16** Last, the server guard (server.js) and the desktop app (electron/).

## 7. The whole system (2:19–2:29)

**2:19** You press Run; the store runs the graph and an executor calls the route.

**2:23** An adapter calls the model, and the output is saved to disk.
