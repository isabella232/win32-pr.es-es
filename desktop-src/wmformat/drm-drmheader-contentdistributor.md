---
title: DRM_DRMHeader_ContentDistributor
description: El \_ atributo ContentDistributor de DRM DRMHeader \_ contiene una cadena identificar el distribuidor de contenido.
ms.assetid: ea9ae7ba-35cc-4e86-995c-9abcdae48f9c
keywords:
- DRM_DRMHeader_ContentDistributor formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2494f80e612e03f9d25372d38e875c1df814fd7d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105714335"
---
# <a name="drm_drmheader_contentdistributor"></a><span data-ttu-id="48658-104">\_ContentDistributor DRMHEADER \_ DRM</span><span class="sxs-lookup"><span data-stu-id="48658-104">DRM\_DRMHeader\_ContentDistributor</span></span>

<span data-ttu-id="48658-105">El **atributo \_ \_ ContentDistributor de DRM DRMHeader** contiene una cadena identificar el distribuidor de contenido.</span><span class="sxs-lookup"><span data-stu-id="48658-105">The **DRM\_DRMHeader\_ContentDistributor** attribute contains a string identifiying the content distributor.</span></span>

## <a name="global-constant"></a><span data-ttu-id="48658-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="48658-106">Global Constant</span></span>

<span data-ttu-id="48658-107">g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor</span><span class="sxs-lookup"><span data-stu-id="48658-107">g\_wszWMDRM\_DRMHeader\_ContentDistributor</span></span>

## <a name="data-type"></a><span data-ttu-id="48658-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="48658-108">Data Type</span></span>

<span data-ttu-id="48658-109">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="48658-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="48658-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48658-110">Remarks</span></span>

<span data-ttu-id="48658-111">El identificador de contenido es opcional y está determinado únicamente por el creador del contenido.</span><span class="sxs-lookup"><span data-stu-id="48658-111">The content ID is optional and is determined solely by the content creator.</span></span> <span data-ttu-id="48658-112">El objeto de escritor no hace nada con este atributo.</span><span class="sxs-lookup"><span data-stu-id="48658-112">The writer object does nothing with this attribute.</span></span> <span data-ttu-id="48658-113">Este atributo solo está presente con el contenido de la versión 7 de DRM.</span><span class="sxs-lookup"><span data-stu-id="48658-113">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="48658-114">Se puede establecer mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="48658-114">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="48658-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="48658-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48658-116">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="48658-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




