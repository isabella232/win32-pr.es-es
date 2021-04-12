---
title: DRM_DRMHeader_KeyID
description: El \_ \_ atributo de ID. de clave de DRMHEADER de DRM contiene el identificador de clave para el archivo.
ms.assetid: cf9fe829-8473-4dd5-9a99-48b709fec0d8
keywords:
- DRM_DRMHeader_KeyID formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebbf2f548725309717993bf29e48de2bf78ed17
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358690"
---
# <a name="drm_drmheader_keyid"></a><span data-ttu-id="7000e-104">ID. de DRMHeader de DRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="7000e-104">DRM\_DRMHeader\_KeyID</span></span>

<span data-ttu-id="7000e-105">El atributo de ID. de clave de **\_ \_ DRMHeader de DRM** contiene el identificador de clave para el archivo.</span><span class="sxs-lookup"><span data-stu-id="7000e-105">The **DRM\_DRMHeader\_KeyID** attribute contains the key ID for the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="7000e-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="7000e-106">Global Constant</span></span>

<span data-ttu-id="7000e-107">\_wszWMDRM \_ DRMHeader ID. de cuenta \_</span><span class="sxs-lookup"><span data-stu-id="7000e-107">g\_wszWMDRM\_DRMHeader\_KeyID</span></span>

## <a name="data-type"></a><span data-ttu-id="7000e-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7000e-108">Data Type</span></span>

<span data-ttu-id="7000e-109">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="7000e-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="7000e-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7000e-110">Remarks</span></span>

<span data-ttu-id="7000e-111">Este atributo solo está presente con el contenido de la versión 7 de DRM.</span><span class="sxs-lookup"><span data-stu-id="7000e-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="7000e-112">Se puede recuperar con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="7000e-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="7000e-113">Para establecer el identificador de clave en el archivo mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , debe usar la propiedad ID. de clave de [**DRM \_**](drm-keyid.md) .</span><span class="sxs-lookup"><span data-stu-id="7000e-113">To set the key ID on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_KeyID**](drm-keyid.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="7000e-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="7000e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7000e-115">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="7000e-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




