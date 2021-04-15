---
description: Configuración del escritor ASF
ms.assetid: 5708c4a0-6197-4a42-adfd-01c6dfe86302
title: Configuración del escritor ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a6dfc1827743dce946188ebf9e050226b5c484
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666121"
---
# <a name="configuring-the-asf-writer"></a><span data-ttu-id="66456-103">Configuración del escritor ASF</span><span class="sxs-lookup"><span data-stu-id="66456-103">Configuring the ASF Writer</span></span>

<span data-ttu-id="66456-104">Cuando se crea el filtro de [escritura ASF de WM](wm-asf-writer-filter.md) , se configura automáticamente con el \_ perfil 256Video de V80 de WMProfile \_ .</span><span class="sxs-lookup"><span data-stu-id="66456-104">When the [WM ASF Writer](wm-asf-writer-filter.md) filter is created, it is configured automatically with the WMProfile\_V80\_256Video profile.</span></span> <span data-ttu-id="66456-105">Este perfil usa los códecs Windows Media Audio y Windows Media Video versión 8, que no son tan recientes como los códecs de la serie Windows Media 9.</span><span class="sxs-lookup"><span data-stu-id="66456-105">This profile uses the Windows Media Audio and Windows Media Video version 8 codecs, which are not as recent as the Windows Media 9 Series codecs.</span></span> <span data-ttu-id="66456-106">Se recomienda crear un perfil personalizado que use los códecs de la serie Windows Media 9 y configurar el escritor ASF de WM con el perfil personalizado, tal y como se describe en [configuración de perfiles y otras propiedades de archivo ASF](configuring-profiles-and-other-asf-file-properties.md).</span><span class="sxs-lookup"><span data-stu-id="66456-106">It is recommended to create a custom profile that uses the Windows Media 9 Series codecs, and configure the WM ASF Writer with the custom profile, as described in [Configuring Profiles and Other ASF File Properties](configuring-profiles-and-other-asf-file-properties.md).</span></span> <span data-ttu-id="66456-107">Debe agregar el filtro de escritor ASF de WM al gráfico de filtro antes de configurar el filtro, y configurar el filtro antes de conectarlo a cualquier otro filtro.</span><span class="sxs-lookup"><span data-stu-id="66456-107">You must add the WM ASF Writer filter to the filter graph before configuring the filter, and configure the filter before connecting it to any other filters.</span></span>

<span data-ttu-id="66456-108">Todos los datos de entrada deben tener una marca de tiempo y todos los pin de entrada deben estar conectados para poder ejecutar o pausar el filtro.</span><span class="sxs-lookup"><span data-stu-id="66456-108">All input data must be time-stamped, and all input pins must be connected before the filter can be run or paused.</span></span> <span data-ttu-id="66456-109">Por lo tanto, si configura el filtro con un perfil que tiene una secuencia de audio y una secuencia de vídeo, el filtro creará un PIN de entrada de audio y vídeo, y ambos PIN deben estar conectados para poder ejecutar el filtro.</span><span class="sxs-lookup"><span data-stu-id="66456-109">Therefore, if you configure the filter with a profile that has an audio stream and a video stream, the filter will create an audio and a video input pin, and both pins must be connected before the filter can be run.</span></span> <span data-ttu-id="66456-110">Dado que el SDK de Windows Media Format requiere que una secuencia de audio funcione, el escritor ASF de WM siempre debe tener un PIN de audio de entrada, incluso si se trata de un flujo ficticio, es decir, una secuencia de audio silenciada y de velocidad de bits baja.</span><span class="sxs-lookup"><span data-stu-id="66456-110">Because the Windows Media Format SDK requires an audio stream to work, the WM ASF Writer must always have an input audio pin, even if it is for a dummy stream—that is, a muted, low-bit-rate audio stream.</span></span>

<span data-ttu-id="66456-111">Agregar extensiones de unidad de datos</span><span class="sxs-lookup"><span data-stu-id="66456-111">Adding Data Unit Extensions</span></span>

<span data-ttu-id="66456-112">Puede configurar una secuencia de perfil para las extensiones de unidad de datos, como los códigos de tiempo SMPTE, antes o después de que se conecte el filtro, siempre que siga este orden de operaciones:</span><span class="sxs-lookup"><span data-stu-id="66456-112">You can configure a profile stream for data unit extensions, such as SMPTE time codes, either before or after the filter is connected, as long as you follow this order of operations:</span></span>

1.  <span data-ttu-id="66456-113">Agregue una o más extensiones de unidad de datos a la secuencia mediante **IWMStreamConfig2:: AddDataUnitExtension**.</span><span class="sxs-lookup"><span data-stu-id="66456-113">Add one or more data unit extensions to the stream using **IWMStreamConfig2::AddDataUnitExtension**.</span></span>
2.  <span data-ttu-id="66456-114">Llame a **IWMProfile:: ReconfigStream** para actualizar el perfil.</span><span class="sxs-lookup"><span data-stu-id="66456-114">Call **IWMProfile::ReconfigStream** to update the profile.</span></span>
3.  <span data-ttu-id="66456-115">Llame a [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) con el objeto de perfil actualizado.</span><span class="sxs-lookup"><span data-stu-id="66456-115">Call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) with the updated profile object.</span></span>
4.  <span data-ttu-id="66456-116">Busque el PIN de entrada de vídeo y llame a su método [**IAMWMBufferPass:: SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) para registrar la interfaz [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="66456-116">Find the video input pin, and call its [**IAMWMBufferPass::SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) method to register your application-defined [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

<span data-ttu-id="66456-117">Cuando se ejecute el gráfico, se llamará al método [**IAMWMBufferPassCallback:: Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) para cada fotograma y podrá obtener y establecer propiedades en el ejemplo mediante sus métodos de interfaz **INSSBuffer3** .</span><span class="sxs-lookup"><span data-stu-id="66456-117">When the graph runs, your [**IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) method will be called for each frame, and you will be able to get and set properties on the sample using its **INSSBuffer3** interface methods.</span></span>

> [!Note]  
> <span data-ttu-id="66456-118">En algunos escenarios de uso intensivo del procesador, como el Telecine inverso, el escritor ASF de WM puede requerir más búferes de salida de los que pueden admitir algunos filtros de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="66456-118">In some processor-intensive scenarios such as inverse telecine, the WM ASF Writer may require more output buffers than some downstream filters can support.</span></span> <span data-ttu-id="66456-119">Por ejemplo, el descodificador de DV no aceptará más de un búfer para su PIN de salida y se aplica lo mismo para el descompresor de AVI en determinadas condiciones.</span><span class="sxs-lookup"><span data-stu-id="66456-119">The DV Decoder, for example, will not accept more than one buffer for its output pin and the same is true for the AVI Decompressor in certain conditions.</span></span> <span data-ttu-id="66456-120">Si surgen problemas al intentar conectarse a estos filtros o, posiblemente, al ejecutar el gráfico, puede que sea necesario escribir un filtro intermediario que acepte cualquier número de búferes en su PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="66456-120">If you encounter problems when attempting to connect to these filters, or possibly when running the graph, it may be necessary to write an intermediary filter that accepts any number of buffers on its output pin.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="66456-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66456-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66456-122">Crear archivos ASF en DirectShow</span><span class="sxs-lookup"><span data-stu-id="66456-122">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



