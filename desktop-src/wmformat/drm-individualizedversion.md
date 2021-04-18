---
title: DRM_IndividualizedVersion
description: El \_ atributo IndividualizedVersion de DRM se almacena en el encabezado DRM y contiene la versión individual y mínima necesaria para tener acceso al contenido.
ms.assetid: ed3e165c-c6b0-4eea-be79-a715abd4dd0a
keywords:
- DRM_IndividualizedVersion formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ecde48ef3d68e30116cdd7fc8a77179f2282c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358714"
---
# <a name="drm_individualizedversion"></a><span data-ttu-id="d2b32-104">\_INDIVIDUALIZEDVERSION DRM</span><span class="sxs-lookup"><span data-stu-id="d2b32-104">DRM\_IndividualizedVersion</span></span>

<span data-ttu-id="d2b32-105">El **atributo \_ IndividualizedVersion de DRM** se almacena en el encabezado DRM y contiene la versión individual y mínima necesaria para tener acceso al contenido.</span><span class="sxs-lookup"><span data-stu-id="d2b32-105">The **DRM\_IndividualizedVersion** attribute is stored in the DRM header and contains the minimum individualized version required to access the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d2b32-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="d2b32-106">Global Constant</span></span>

<span data-ttu-id="d2b32-107">g \_ wszWMDRM \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="d2b32-107">g\_wszWMDRM\_IndividualizedVersion</span></span>

## <a name="data-type"></a><span data-ttu-id="d2b32-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d2b32-108">Data Type</span></span>

<span data-ttu-id="d2b32-109">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d2b32-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="d2b32-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2b32-110">Remarks</span></span>

<span data-ttu-id="d2b32-111">Este atributo solo está presente con el contenido de la versión 7 de DRM.</span><span class="sxs-lookup"><span data-stu-id="d2b32-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="d2b32-112">Se puede establecer mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="d2b32-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="d2b32-113">Se puede recuperar el mismo atributo de archivo mediante [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md).</span><span class="sxs-lookup"><span data-stu-id="d2b32-113">The same file attribute can be retrieved using [**DRM\_DRMHeader\_IndividualizedVersion**](drm-drmheader-individualizedversion.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d2b32-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2b32-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2b32-115">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="d2b32-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




