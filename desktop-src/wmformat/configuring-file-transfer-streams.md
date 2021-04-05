---
title: Configuración de secuencias de transferencia de archivos
description: Configuración de secuencias de transferencia de archivos
ms.assetid: faed54ae-9e80-492a-9602-e726bdb3b54a
keywords:
- flujos, configurar secuencias de transferencia de archivos
- códecs, configurar secuencias de transferencia de archivos
- flujos de transferencia de archivos
- secuencias, extensiones de unidad de datos
- códecs, extensiones de unidad de datos
- extensiones de unidad de datos, secuencias de transferencia de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fac7d2270da82f1f9e82ed9123611ae608dd3c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077353"
---
# <a name="configuring-file-transfer-streams"></a><span data-ttu-id="2d775-109">Configuración de secuencias de transferencia de archivos</span><span class="sxs-lookup"><span data-stu-id="2d775-109">Configuring File Transfer Streams</span></span>

<span data-ttu-id="2d775-110">Las secuencias de transferencia de archivos no requieren ninguna configuración especial en la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) .</span><span class="sxs-lookup"><span data-stu-id="2d775-110">File transfer streams do not require any special settings in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="2d775-111">Requieren una extensión de unidad de datos para asociar un nombre de archivo a cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2d775-111">They do require a data unit extension to associate a file name with each sample.</span></span> <span data-ttu-id="2d775-112">Para enviar un nombre con ejemplos de transferencia de archivos, debe implementar un sistema de extensión de unidad de datos para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2d775-112">To send a name with file transfer samples, you must implement a data unit extension system for the stream.</span></span>

<span data-ttu-id="2d775-113">Para establecer una extensión de unidad de datos para la secuencia, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2d775-113">To set a data unit extension for the stream, perform the following steps:</span></span>

1.  <span data-ttu-id="2d775-114">Obtenga un puntero a la interfaz [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) del objeto de configuración de la secuencia llamando a **IWMStreamConfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="2d775-114">Obtain a pointer to the [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
2.  <span data-ttu-id="2d775-115">Agregue una extensión de unidad de datos para la secuencia mediante una llamada a [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="2d775-115">Add a data unit extension for the stream by calling [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) as follows:</span></span>
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="2d775-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d775-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d775-117">**Configuración común para todos los flujos**</span><span class="sxs-lookup"><span data-stu-id="2d775-117">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="2d775-118">**Configuración de tipos de flujo arbitrarios**</span><span class="sxs-lookup"><span data-stu-id="2d775-118">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="2d775-119">**Secuencias de archivo**</span><span class="sxs-lookup"><span data-stu-id="2d775-119">**File Streams**</span></span>](file-streams.md)
</dt> </dl>

 

 




