---
title: Usar comandos de script
description: Usar comandos de script
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- SDK de Windows Media Format, comandos de script
- Advanced Systems Format (ASF), comandos de script
- ASF (formato de sistemas avanzados), comandos de script
- scripts, comandos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2e840a677e58a1be528e84e4ed1b4be7fe3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075805"
---
# <a name="using-script-commands"></a><span data-ttu-id="6c557-107">Usar comandos de script</span><span class="sxs-lookup"><span data-stu-id="6c557-107">Using Script Commands</span></span>

<span data-ttu-id="6c557-108">El SDK de Windows Media Format admite el uso de comandos de script para comunicar acciones de aplicación en archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="6c557-108">The Windows Media Format SDK supports the use of script commands to communicate application actions in ASF files.</span></span> <span data-ttu-id="6c557-109">Cada comando de script se compone de dos cadenas, la primera cadena es el tipo de comando, la segunda son los datos del comando.</span><span class="sxs-lookup"><span data-stu-id="6c557-109">Each script command is made up of two strings, the first string is the type of command, the second is the command data.</span></span> <span data-ttu-id="6c557-110">Por ejemplo, puede usar el tipo de script "URL" y pasar una dirección URL de Internet válida como datos del comando.</span><span class="sxs-lookup"><span data-stu-id="6c557-110">For example, you can use the script type "URL" and pass a valid Internet URL as the command data.</span></span> <span data-ttu-id="6c557-111">Cuando una aplicación de lectura que admite comandos de script de tipo "URL" recibe este comando, abrirá la dirección especificada en una ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="6c557-111">When a reading application that supports script commands of type "URL" receives this command, it will open the specified address in a browser window.</span></span>

<span data-ttu-id="6c557-112">El SDK de Windows Media Format proporciona dos opciones para entregar el script en archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="6c557-112">The Windows Media Format SDK provides two options for delivering script in ASF files.</span></span> <span data-ttu-id="6c557-113">Puede crear una secuencia de script o puede incluir comandos de script en el encabezado del archivo.</span><span class="sxs-lookup"><span data-stu-id="6c557-113">You can create a script stream or you can include script commands in the header of the file.</span></span> <span data-ttu-id="6c557-114">Los flujos de script son útiles porque los comandos de script se entregan en el orden temporal de presentación.</span><span class="sxs-lookup"><span data-stu-id="6c557-114">Script streams are useful because the script commands are delivered in presentation time order.</span></span> <span data-ttu-id="6c557-115">Si usa comandos de script en el encabezado de archivo, la aplicación tendrá que recuperar todos los comandos de script antes de iniciar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="6c557-115">If you use script commands in the file header, your application will need to retrieve all of the script commands before starting playback.</span></span> <span data-ttu-id="6c557-116">Debe realizar un seguimiento de los tiempos de presentación de los comandos de script y responder a ellos en el momento adecuado.</span><span class="sxs-lookup"><span data-stu-id="6c557-116">You must keep track of the presentation times of script commands and respond to them at the right time.</span></span>

<span data-ttu-id="6c557-117">En las secciones siguientes se describe cómo incluir comandos de script en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="6c557-117">The following sections describe how to include script commands in an ASF file.</span></span>



| <span data-ttu-id="6c557-118">Sección</span><span class="sxs-lookup"><span data-stu-id="6c557-118">Section</span></span>                                                                                                                | <span data-ttu-id="6c557-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c557-119">Description</span></span>                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="6c557-120">Para usar una secuencia de script</span><span class="sxs-lookup"><span data-stu-id="6c557-120">To Use a Script Stream</span></span>](to-use-a-script-stream.md)                                                                   | <span data-ttu-id="6c557-121">Describe cómo incluir comandos de script en una secuencia de scripts.</span><span class="sxs-lookup"><span data-stu-id="6c557-121">Describes how to include script commands in a script stream.</span></span> |
| [<span data-ttu-id="6c557-122">Para agregar datos de script al encabezado</span><span class="sxs-lookup"><span data-stu-id="6c557-122">To Add Script Data to the Header</span></span>](to-add-script-data-to-the-header.md)                                               | <span data-ttu-id="6c557-123">Describe cómo incluir comandos de script en el encabezado de archivo.</span><span class="sxs-lookup"><span data-stu-id="6c557-123">Describes how to include script commands in the file header.</span></span> |
| [<span data-ttu-id="6c557-124">Usar comandos de script compatibles con Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="6c557-124">Using Script Commands Supported by Windows Media Player</span></span>](using-script-commands-supported-by-windows-media-player.md) | <span data-ttu-id="6c557-125">Describe los comandos de script utilizados por Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="6c557-125">Describes the script commands used by Windows Media Player.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="6c557-126">En versiones anteriores del SDK de Windows Media Format, las secuencias de comandos se usaban para abrir direcciones web correspondientes al contenido de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="6c557-126">In previous versions of the Windows Media Format SDK, script streams were used to open Web addresses corresponding to the content of an ASF file.</span></span> <span data-ttu-id="6c557-127">Ahora puede usar secuencias web para trabajar con páginas web sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="6c557-127">You can now use Web streams to work with synchronized Web pages.</span></span> <span data-ttu-id="6c557-128">Para obtener más información,</span><span class="sxs-lookup"><span data-stu-id="6c557-128">For more information.</span></span> <span data-ttu-id="6c557-129">vea [secuencias web](web-streams.md).</span><span class="sxs-lookup"><span data-stu-id="6c557-129">see [Web Streams](web-streams.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6c557-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6c557-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c557-131">**Comandos de script**</span><span class="sxs-lookup"><span data-stu-id="6c557-131">**Script Commands**</span></span>](script-commands.md)
</dt> <dt>

[<span data-ttu-id="6c557-132">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="6c557-132">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




