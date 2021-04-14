---
title: Configuración de las extensiones de unidad de datos
description: Configuración de las extensiones de unidad de datos
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- Advanced Systems Format (ASF), extensiones de unidad de datos
- ASF (formato de sistemas avanzados), extensiones de unidad de datos
- extensiones de unidad de datos, configuración
- secuencias, extensiones de unidad de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822a05a6e6bcbb9f0101d32eed05f2b6c5c68dc8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104533046"
---
# <a name="setting-data-unit-extensions"></a><span data-ttu-id="3c232-107">Configuración de las extensiones de unidad de datos</span><span class="sxs-lookup"><span data-stu-id="3c232-107">Setting Data Unit Extensions</span></span>

<span data-ttu-id="3c232-108">Algunas secuencias están configuradas para usar las extensiones de unidad de datos para asociar datos complementarios a ejemplos individuales.</span><span class="sxs-lookup"><span data-stu-id="3c232-108">Some streams are configured to use data unit extensions to associate supplementary data with individual samples.</span></span> <span data-ttu-id="3c232-109">Para obtener más información acerca de los ejemplos extendidos, consulte [extensiones de unidad de datos](data-unit-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="3c232-109">For more information about extended samples, see [Data Unit Extensions](data-unit-extensions.md).</span></span>

<span data-ttu-id="3c232-110">La mayoría de los sistemas de extensión de unidad de datos requieren una extensión en cada ejemplo de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="3c232-110">Most data unit extension systems require an extension on every sample in the stream.</span></span> <span data-ttu-id="3c232-111">Si no proporciona una extensión del tamaño correcto, el escritor rechazará el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3c232-111">If you do not provide an extension of the correct size, the writer will reject the sample.</span></span>

<span data-ttu-id="3c232-112">Para agregar datos extendidos a un ejemplo, use el método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="3c232-112">To add extended data to a sample, use the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="3c232-113">Puede obtener información sobre las extensiones de unidad de datos configuradas en una secuencia mediante los métodos [**IWMStreamConfig2:: GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) y [**IWMStreamConfig2:: GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) .</span><span class="sxs-lookup"><span data-stu-id="3c232-113">You can get information about the data unit extensions configured on a stream by using the [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) and [**IWMStreamConfig2::GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c232-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c232-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c232-115">**Configuración de extensiones de unidades de datos**</span><span class="sxs-lookup"><span data-stu-id="3c232-115">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="3c232-116">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="3c232-116">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




