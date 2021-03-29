---
title: Extensiones de unidad de datos
description: Extensiones de unidad de datos
ms.assetid: f95de189-0449-4b88-aba3-7b19f385c8fe
keywords:
- Windows Media Format SDK, extensiones de unidad de datos
- Advanced Systems Format (ASF), extensiones de unidad de datos
- ASF (formato de sistemas avanzados), extensiones de unidad de datos
- SDK de Windows Media Format, sistemas de extensión de carga
- Advanced Systems Format (ASF), sistemas de extensión de carga útil
- ASF (formato de sistemas avanzados), sistemas de extensión de carga útil
- extensiones de unidad de datos, acerca de
- extensiones de unidad de carga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8ed5c9db82d0002648148ca14bd7f94baa9029
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788763"
---
# <a name="data-unit-extensions"></a><span data-ttu-id="169c9-111">Extensiones de unidad de datos</span><span class="sxs-lookup"><span data-stu-id="169c9-111">Data Unit Extensions</span></span>

<span data-ttu-id="169c9-112">El SDK de Windows Media Format permite complementar los datos de ejemplos con *extensiones de unidad de datos*, también denominados sistemas de extensión de carga.</span><span class="sxs-lookup"><span data-stu-id="169c9-112">The Windows Media Format SDK enables you to supplement data in samples with *data unit extensions*, also called payload extension systems.</span></span> <span data-ttu-id="169c9-113">En esta documentación se usa el término "extensiones de unidad de datos" para mantener la coherencia con los nombres de método como [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span><span class="sxs-lookup"><span data-stu-id="169c9-113">This documentation uses the term "data unit extensions" in order to remain consistent with method names such as [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span></span> <span data-ttu-id="169c9-114">Una extensión de unidad de datos es un par nombre-valor que se adjunta al ejemplo en la sección de datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="169c9-114">A data unit extension is a name/value pair that is attached to the sample in the data section of the file.</span></span> <span data-ttu-id="169c9-115">Puede tener acceso a los datos extendidos mediante los métodos del objeto de búfer cuando el lector recupera el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="169c9-115">You can access the extended data using methods of the buffer object when the sample is retrieved by the reader.</span></span>

<span data-ttu-id="169c9-116">Puede crear extensiones de unidad de datos para sus propias especificaciones, pero hay varios tipos predefinidos y compatibles con los objetos de este SDK.</span><span class="sxs-lookup"><span data-stu-id="169c9-116">You can create data unit extensions to your own specifications, but several types are predefined and supported by the objects of this SDK.</span></span> <span data-ttu-id="169c9-117">Estas extensiones estándar se utilizan para proporcionar datos adicionales para los nombres de archivo (en scripts y secuencias Web), datos de código de tiempo SMPTE, relación de aspecto de píxeles no cuadrado, duración y tipo de entrelazado.</span><span class="sxs-lookup"><span data-stu-id="169c9-117">These standard extensions are used to provide additional data for file names (in script and Web streams), SMPTE time code data, non-square pixel aspect ratio, duration, and type of interlacing.</span></span>

<span data-ttu-id="169c9-118">Para usar las extensiones de unidad de datos, debe configurar la secuencia para aceptarlas y, a continuación, agregar extensiones a cada ejemplo de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="169c9-118">To use data unit extensions, you must configure the stream to accept them, and then add extensions to each sample for that stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="169c9-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="169c9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="169c9-120">**Características de archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="169c9-120">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="169c9-121">**Configuración de extensiones de unidades de datos**</span><span class="sxs-lookup"><span data-stu-id="169c9-121">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="169c9-122">**Configuración de las extensiones de unidad de datos**</span><span class="sxs-lookup"><span data-stu-id="169c9-122">**Setting Data Unit Extensions**</span></span>](setting-data-unit-extensions.md)
</dt> </dl>

 

 




