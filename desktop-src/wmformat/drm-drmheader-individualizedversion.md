---
title: DRM_DRMHeader_IndividualizedVersion
description: El \_ atributo DRMHeaderIndividualizedVersion de DRM contiene la versión individualizada mínima necesaria para reproducir el archivo.
ms.assetid: 2ac24660-8b7a-4dba-9f9f-ad8b13a22f5c
keywords:
- DRM_DRMHeader_IndividualizedVersion formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 167065f99a72245c6d7cc677ce24fa1ff96dec84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105714329"
---
# <a name="drm_drmheader_individualizedversion"></a><span data-ttu-id="c4e40-104">\_IndividualizedVersion DRMHEADER \_ DRM</span><span class="sxs-lookup"><span data-stu-id="c4e40-104">DRM\_DRMHeader\_IndividualizedVersion</span></span>

<span data-ttu-id="c4e40-105">El **atributo \_ DRMHeaderIndividualizedVersion de DRM** contiene la versión individualizada mínima necesaria para reproducir el archivo.</span><span class="sxs-lookup"><span data-stu-id="c4e40-105">The **DRM\_DRMHeaderIndividualizedVersion** attribute contains the minimum individualized version required to play back the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c4e40-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="c4e40-106">Global Constant</span></span>

<span data-ttu-id="c4e40-107">g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="c4e40-107">g\_wszWMDRM\_DRMHeader\_IndividualizedVersion</span></span>

## <a name="data-type"></a><span data-ttu-id="c4e40-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c4e40-108">Data Type</span></span>

<span data-ttu-id="c4e40-109">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="c4e40-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="c4e40-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4e40-110">Remarks</span></span>

<span data-ttu-id="c4e40-111">Este atributo solo está presente con el contenido de la versión 7 de DRM.</span><span class="sxs-lookup"><span data-stu-id="c4e40-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="c4e40-112">Se puede recuperar con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="c4e40-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="c4e40-113">Para establecer la versión individualizada (también denominada versión de seguridad) en el archivo mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , debe usar la [**propiedad \_ IndividualizedVersion de DRM**](drm-individualizedversion.md) .</span><span class="sxs-lookup"><span data-stu-id="c4e40-113">To set the individualized version (also called the security version) on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_IndividualizedVersion**](drm-individualizedversion.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4e40-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4e40-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4e40-115">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="c4e40-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




