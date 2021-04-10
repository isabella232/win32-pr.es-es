---
description: Atributos del escritor de receptor
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: Atributos del escritor de receptor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23dbca06c3ff1a4ac80b8e68413fdd0816d71a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155316"
---
# <a name="sink-writer-attributes"></a><span data-ttu-id="cdbbf-103">Atributos del escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="cdbbf-103">Sink Writer Attributes</span></span>

<span data-ttu-id="cdbbf-104">Los siguientes atributos se pueden usar para inicializar el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="cdbbf-104">The following attributes can be used to initialize the sink writer.</span></span>



| <span data-ttu-id="cdbbf-105">Atributo</span><span class="sxs-lookup"><span data-stu-id="cdbbf-105">Attribute</span></span>                                                                                  | <span data-ttu-id="cdbbf-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="cdbbf-106">Description</span></span>                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdbbf-107">\_baja \_ latencia de MF</span><span class="sxs-lookup"><span data-stu-id="cdbbf-107">MF\_LOW\_LATENCY</span></span>](mf-low-latency.md)                                                     | <span data-ttu-id="cdbbf-108">Habilita el procesamiento de baja latencia.</span><span class="sxs-lookup"><span data-stu-id="cdbbf-108">Enables low-latency processing.</span></span>                                                                                                                                                                                                    |
| [<span data-ttu-id="cdbbf-109">MF \_ ReadWrite \_ deshabilitar \_ convertidores</span><span class="sxs-lookup"><span data-stu-id="cdbbf-109">MF\_READWRITE\_DISABLE\_CONVERTERS</span></span>](mf-readwrite-disable-converters.md)                  | <span data-ttu-id="cdbbf-110">Habilita o deshabilita las conversiones de formato del escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="cdbbf-110">Enables or disables format conversions by the sink writer.</span></span>                                                                                                                                                                         |
| [<span data-ttu-id="cdbbf-111">MF \_ ReadWrite \_ habilitar \_ \_ transformaciones de hardware</span><span class="sxs-lookup"><span data-stu-id="cdbbf-111">MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS</span></span>](mf-readwrite-enable-hardware-transforms.md) | <span data-ttu-id="cdbbf-112">Permite al escritor del receptor usar transformaciones de Media Foundation basadas en hardware (MFTs).</span><span class="sxs-lookup"><span data-stu-id="cdbbf-112">Enables the sink writer to use hardware-based Media Foundation transforms (MFTs).</span></span>                                                                                                                                                  |
| [<span data-ttu-id="cdbbf-113">\_devolución de \_ \_ llamada asincrónica de escritor del receptor MF \_</span><span class="sxs-lookup"><span data-stu-id="cdbbf-113">MF\_SINK\_WRITER\_ASYNC\_CALLBACK</span></span>](mf-sink-writer-async-callback.md)                     | <span data-ttu-id="cdbbf-114">Contiene un puntero a la interfaz de devolución de llamada de la aplicación para el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="cdbbf-114">Contains a pointer to the application's callback interface for the sink writer.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="cdbbf-115">\_limitación de \_ \_ deshabilitación de escritor de receptor MF \_</span><span class="sxs-lookup"><span data-stu-id="cdbbf-115">MF\_SINK\_WRITER\_DISABLE\_THROTTLING</span></span>](mf-sink-writer-disable-throttling.md)             | <span data-ttu-id="cdbbf-116">Especifica si el escritor del receptor limita la velocidad de los datos entrantes.</span><span class="sxs-lookup"><span data-stu-id="cdbbf-116">Specifies whether the sink writer limits the rate of incoming data.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="cdbbf-117">\_CONTAINERTYPE de TRANSCODIFICACIÓN MF \_</span><span class="sxs-lookup"><span data-stu-id="cdbbf-117">MF\_TRANSCODE\_CONTAINERTYPE</span></span>](mf-transcode-containertype.md)                             | <span data-ttu-id="cdbbf-118">Especifica el tipo de contenedor del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="cdbbf-118">Specifies the container type of the output file.</span></span>                                                                                                                                                                                   |
| [<span data-ttu-id="cdbbf-119">\_Atributo de \_ desbloqueo FIELDOFUSE de MFT \_</span><span class="sxs-lookup"><span data-stu-id="cdbbf-119">MFT\_FIELDOFUSE\_UNLOCK\_Attribute</span></span>](mft-fieldofuse-unlock-attribute.md)                  | <span data-ttu-id="cdbbf-120">Contiene un puntero [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , que se usa para desbloquear una MFT con restricciones de campo de uso.</span><span class="sxs-lookup"><span data-stu-id="cdbbf-120">Contains an [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer, which is used to unlock an MFT with field-of-use restrictions.</span></span> <span data-ttu-id="cdbbf-121">Para obtener más información, consulte el [campo de restricciones de uso](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="cdbbf-121">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> |
| [<span data-ttu-id="cdbbf-122">\_Administrador de \_ D3D del escritor de receptores MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="cdbbf-122">MF\_SINK\_WRITER\_D3D\_MANAGER</span></span>](mf-sink-writer-d3d-manager.md)                           | <span data-ttu-id="cdbbf-123">Use este atributo para proporcionar un dispositivo Direct3D para cualquier codificador de vídeo o receptor de medios cargados por el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="cdbbf-123">Use this attribute to provide a Direct3D device for any video encoders or media sinks loaded by the sink writer.</span></span>                                                                                                                   |



 

<span data-ttu-id="cdbbf-124">Utilice estos atributos con los siguientes métodos y funciones:</span><span class="sxs-lookup"><span data-stu-id="cdbbf-124">Use these attributes with the following methods and functions:</span></span>

-   [<span data-ttu-id="cdbbf-125">**IMFReadWriteClassFactory::CreateInstanceFromObject**</span><span class="sxs-lookup"><span data-stu-id="cdbbf-125">**IMFReadWriteClassFactory::CreateInstanceFromObject**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [<span data-ttu-id="cdbbf-126">**IMFReadWriteClassFactory::CreateInstanceFromURL**</span><span class="sxs-lookup"><span data-stu-id="cdbbf-126">**IMFReadWriteClassFactory::CreateInstanceFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [<span data-ttu-id="cdbbf-127">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="cdbbf-127">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="cdbbf-128">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="cdbbf-128">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

<span data-ttu-id="cdbbf-129">Para usar cualquiera de estos atributos, llame primero a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un nuevo almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="cdbbf-129">To use any of these attributes, first call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span> <span data-ttu-id="cdbbf-130">A continuación, use la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para establecer los atributos deseados en el almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="cdbbf-130">Then use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface to set the desired attributes on the attribute store.</span></span> <span data-ttu-id="cdbbf-131">Pase el puntero **IMFAttributes** al parámetro *pAttributes* de cualquiera de los métodos o funciones enumerados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="cdbbf-131">Pass the **IMFAttributes** pointer to the *pAttributes* parameter of any of the methods or functions listed previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdbbf-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cdbbf-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdbbf-133">**IMFSinkWriter**</span><span class="sxs-lookup"><span data-stu-id="cdbbf-133">**IMFSinkWriter**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[<span data-ttu-id="cdbbf-134">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cdbbf-134">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



