---
title: Comandos de script
description: Comandos de script
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- SDK de Windows Media Format, comandos de script
- Advanced Systems Format (ASF), comandos de script
- ASF (formato de sistemas avanzados), comandos de script
- SDK de Windows Media Format, secuencias de scripts
- Advanced Systems Format (ASF), secuencias de scripts
- ASF (formato de sistemas avanzados), secuencias de scripts
- Windows Media Format SDK, secuencias
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- scripts, comandos
- scripts, secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57ab446a216624dc8f844f54298aeeaee358ac3
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078574"
---
# <a name="script-commands"></a><span data-ttu-id="88920-114">Comandos de script</span><span class="sxs-lookup"><span data-stu-id="88920-114">Script Commands</span></span>

<span data-ttu-id="88920-115">Los comandos de script admitidos por el SDK de Windows Media Format son pares de cadena de valor y nombre simple.</span><span class="sxs-lookup"><span data-stu-id="88920-115">The script commands supported by the Windows Media Format SDK are simple name and value string pairs.</span></span> <span data-ttu-id="88920-116">Por ejemplo, un comando de script común es "URL", que usa Windows Media Player y otras aplicaciones de reproducción para abrir páginas Web.</span><span class="sxs-lookup"><span data-stu-id="88920-116">For example, a common script command is "URL", which is used by Windows Media Player and other playing applications to open Web pages.</span></span> <span data-ttu-id="88920-117">La otra mitad del par de scripts para el comando "URL" contiene un localizador uniforme de recursos (URL) válido, como `https://www.adatum.com` .</span><span class="sxs-lookup"><span data-stu-id="88920-117">The other half of the script pair for "URL" command contains a valid uniform resource locator (URL), such as `https://www.adatum.com`.</span></span> <span data-ttu-id="88920-118">Los objetos de este SDK no proporcionan compatibilidad para ningún comando específico; la aplicación debe incluir lógica para controlar los comandos que use.</span><span class="sxs-lookup"><span data-stu-id="88920-118">No support is provided by the objects of this SDK for any specific commands; your application must include logic to handle whatever commands you use.</span></span> <span data-ttu-id="88920-119">Puede usar los comandos admitidos por Windows Media Player para mantener la compatibilidad con la mayoría de los reproductores.</span><span class="sxs-lookup"><span data-stu-id="88920-119">You can use the commands supported by Windows Media Player to maintain compatibility with most players.</span></span>

<span data-ttu-id="88920-120">Los comandos de script se pueden entregar de una de estas dos maneras: en una secuencia de script o en el encabezado de archivo.</span><span class="sxs-lookup"><span data-stu-id="88920-120">Script commands can be delivered in one of two ways: in a script stream or in the file header.</span></span>

## <a name="script-streams"></a><span data-ttu-id="88920-121">Secuencias de script</span><span class="sxs-lookup"><span data-stu-id="88920-121">Script Streams</span></span>

<span data-ttu-id="88920-122">Puede enviar comandos de script en su propia secuencia en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="88920-122">You can deliver script commands in their own stream in an ASF file.</span></span> <span data-ttu-id="88920-123">Cada ejemplo de una secuencia de script contiene las dos cadenas del par nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="88920-123">Each sample in a script stream contains the two strings of the name/value pair.</span></span> <span data-ttu-id="88920-124">La ventaja de usar un flujo de script es que los comandos se entregarán en el momento correcto de la presentación.</span><span class="sxs-lookup"><span data-stu-id="88920-124">The advantage of using a script stream is that the commands will be delivered at the correct presentation time.</span></span>

## <a name="script-commands-in-the-file-header"></a><span data-ttu-id="88920-125">Comandos de script en el encabezado de archivo</span><span class="sxs-lookup"><span data-stu-id="88920-125">Script Commands in the File Header</span></span>

<span data-ttu-id="88920-126">Los comandos de script pueden incluirse en el encabezado de archivo para su recuperación en el momento de la reproducción.</span><span class="sxs-lookup"><span data-stu-id="88920-126">Script commands can be included in the file header for retrieval at the time of playback.</span></span> <span data-ttu-id="88920-127">La aplicación de reproducción es responsable de ejecutar los comandos de script en el momento adecuado.</span><span class="sxs-lookup"><span data-stu-id="88920-127">The playing application is responsible for executing the script commands at the proper time.</span></span> <span data-ttu-id="88920-128">La ventaja de usar comandos de script en el encabezado de archivo es que todos los comandos de script están disponibles antes de empezar a recibir ejemplos.</span><span class="sxs-lookup"><span data-stu-id="88920-128">The advantage of using script commands in the file header is that all of the script commands are available before beginning to receive samples.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88920-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88920-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88920-130">**Características de archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="88920-130">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="88920-131">**Usar comandos de script**</span><span class="sxs-lookup"><span data-stu-id="88920-131">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




