---
title: Acerca de los complementos de conversión
description: Acerca de los complementos de conversión
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Windows Media Player, Complementos de conversión
- Complementos de Windows Media Player, conversión
- complementos, conversión
- Complementos de conversión, acerca de
- Formato ASF
- ASF (formato de sistemas avanzados)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6e2a8fa41b657a593dc03082f871503b53eba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773590"
---
# <a name="about-conversion-plug-ins"></a><span data-ttu-id="f3e14-109">Acerca de los complementos de conversión</span><span class="sxs-lookup"><span data-stu-id="f3e14-109">About Conversion Plug-ins</span></span>

<span data-ttu-id="f3e14-110">Puede crear un complemento de Media Player de Windows para convertir archivos multimedia digitales creados con tecnologías no proporcionadas por Microsoft, en formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="f3e14-110">You can create a Windows Media Player plug-in to convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).</span></span>

<span data-ttu-id="f3e14-111">Los complementos de conversión son objetos del modelo de objetos componentes (COM) que se empaquetan y distribuyen como archivos ejecutables (. exe).</span><span class="sxs-lookup"><span data-stu-id="f3e14-111">Conversion plug-ins are Component Object Model (COM) objects that are packaged and distributed as executable (.exe) files.</span></span> <span data-ttu-id="f3e14-112">Windows Media Player crea una instancia de los complementos de conversión para convertir formatos de medios digitales de terceros en los escenarios siguientes:</span><span class="sxs-lookup"><span data-stu-id="f3e14-112">Windows Media Player instantiates conversion plug-ins to convert third-party digital media formats in the following scenarios:</span></span>

-   <span data-ttu-id="f3e14-113">El contenido multimedia digital se copia en el equipo desde un dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="f3e14-113">Digital media content is copied to the computer from a portable device.</span></span>
-   <span data-ttu-id="f3e14-114">El contenido multimedia digital se agrega a la biblioteca mediante **IWMPMediaCollection:: Add**.</span><span class="sxs-lookup"><span data-stu-id="f3e14-114">Digital media content is added to the library by using **IWMPMediaCollection::add**.</span></span>
-   <span data-ttu-id="f3e14-115">El contenido multimedia digital se agrega a la biblioteca mediante la característica de búsqueda de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f3e14-115">Digital media content is added to the library by using the search feature of Windows Media Player.</span></span>
-   <span data-ttu-id="f3e14-116">La característica de supervisión de carpetas de Windows Media Player agrega el contenido multimedia digital a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f3e14-116">Digital media content is added to the library by the folder monitoring feature of Windows Media Player.</span></span>
-   <span data-ttu-id="f3e14-117">El contenido multimedia digital se agrega a la lista de sincronización cuando el usuario arrastra y coloca un archivo.</span><span class="sxs-lookup"><span data-stu-id="f3e14-117">Digital media content is added to the sync list when the user drags and drops a file.</span></span>

<span data-ttu-id="f3e14-118">Después de que Windows Media Player crea una instancia de un complemento de conversión, el complemento debe convertir el archivo proporcionado en ASF o WMA y agregar los metadatos pertinentes.</span><span class="sxs-lookup"><span data-stu-id="f3e14-118">After Windows Media Player creates an instance of a conversion plug-in, the plug-in must convert the supplied file to ASF or WMA and add relevant metadata.</span></span> <span data-ttu-id="f3e14-119">(No use el complemento de conversión para transcodificar el archivo). A continuación, el complemento debe copiar el archivo convertido en la carpeta especificada y devolver la ruta de acceso al nuevo archivo a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f3e14-119">(Do not use the conversion plug-in to transcode the file.) The plug-in must then copy the converted file to the specified folder and return the path to the new file to Windows Media Player.</span></span>

<span data-ttu-id="f3e14-120">Los complementos de conversión deben implementar la interfaz **IWMPConvert** .</span><span class="sxs-lookup"><span data-stu-id="f3e14-120">Conversion plug-ins must implement the **IWMPConvert** interface.</span></span> <span data-ttu-id="f3e14-121">Consulte [referencia de programación de complementos de conversión](conversion-plug-ins-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f3e14-121">See [Conversion Plug-ins Programming Reference](conversion-plug-ins-programming-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3e14-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3e14-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3e14-123">**Acerca del proceso de conversión**</span><span class="sxs-lookup"><span data-stu-id="f3e14-123">**About the Conversion Process**</span></span>](about-the-conversion-process.md)
</dt> <dt>

[<span data-ttu-id="f3e14-124">**Agregar metadatos a archivos convertidos**</span><span class="sxs-lookup"><span data-stu-id="f3e14-124">**Adding Metadata to Converted Files**</span></span>](adding-metadata-to-converted-files.md)
</dt> <dt>

[<span data-ttu-id="f3e14-125">**Complementos de conversión de Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="f3e14-125">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




