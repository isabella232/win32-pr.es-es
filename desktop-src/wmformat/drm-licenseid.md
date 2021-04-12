---
title: DRM_LicenseID
description: La \_ propiedad LicenseID de DRM contiene una cadena recuperada de la licencia asociada al archivo abierto que identifica de forma única esa licencia.
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- DRM_LicenseID formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d9174e364e186056e63375b8ed322875dfb868
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358710"
---
# <a name="drm_licenseid"></a><span data-ttu-id="91e53-104">\_LICENSEID DRM</span><span class="sxs-lookup"><span data-stu-id="91e53-104">DRM\_LicenseID</span></span>

<span data-ttu-id="91e53-105">La **propiedad \_ LicenseID de DRM** contiene una cadena recuperada de la licencia asociada al archivo abierto que identifica de forma única esa licencia.</span><span class="sxs-lookup"><span data-stu-id="91e53-105">The **DRM\_LicenseID** property contains a string retrieved from the license associated with the currently open file that uniquely identifies that license.</span></span>

## <a name="global-constant"></a><span data-ttu-id="91e53-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="91e53-106">Global Constant</span></span>

<span data-ttu-id="91e53-107">g \_ wszWMDRM \_ LicenseID</span><span class="sxs-lookup"><span data-stu-id="91e53-107">g\_wszWMDRM\_LicenseID</span></span>

## <a name="data-type"></a><span data-ttu-id="91e53-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="91e53-108">Data Type</span></span>

<span data-ttu-id="91e53-109">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="91e53-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="91e53-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91e53-110">Remarks</span></span>

<span data-ttu-id="91e53-111">Este atributo solo está presente con el contenido de la versión 7 de DRM.</span><span class="sxs-lookup"><span data-stu-id="91e53-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="91e53-112">Se puede establecer mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="91e53-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

<span data-ttu-id="91e53-113">El identificador de licencia se almacena en una licencia, no en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="91e53-113">The license ID is stored in a license, not in an ASF file.</span></span> <span data-ttu-id="91e53-114">Cada licencia individual tiene un identificador único que se asigna mediante el generador de licencias en el momento en que se crea la licencia.</span><span class="sxs-lookup"><span data-stu-id="91e53-114">Each individual license has a unique ID which is assigned by the license generator at the time the license is created.</span></span> <span data-ttu-id="91e53-115">Por ejemplo, si obtiene dos licencias para el mismo contenido, cada una tendrá un atributo LicenseID diferente.</span><span class="sxs-lookup"><span data-stu-id="91e53-115">For example, if you obtain two licenses for the same content, each one will have a different LicenseID attribute.</span></span> <span data-ttu-id="91e53-116">Normalmente, las aplicaciones no tienen necesidad de recuperar este valor.</span><span class="sxs-lookup"><span data-stu-id="91e53-116">Typically, applications have no need to retrieve this value.</span></span>

## <a name="see-also"></a><span data-ttu-id="91e53-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="91e53-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91e53-118">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="91e53-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




