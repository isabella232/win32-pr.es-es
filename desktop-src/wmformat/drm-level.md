---
title: DRM_Level
description: '\_El nivel DRM es un atributo de licencia que el SDK de formato de Windows Media establece al crear una licencia local para los archivos protegidos con DRM versión 1.'
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- DRM_Level formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3177197b9c149c2fca2c7678a8fe03c6b412e2d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358711"
---
# <a name="drm_level"></a><span data-ttu-id="978f5-104">Nivel de DRM \_</span><span class="sxs-lookup"><span data-stu-id="978f5-104">DRM\_Level</span></span>

<span data-ttu-id="978f5-105">**DRM \_ Level** es un atributo de licencia que el SDK de formato de Windows Media establece cuando crea una licencia local para archivos protegidos con DRM versión 1.</span><span class="sxs-lookup"><span data-stu-id="978f5-105">**DRM\_Level** is a license attribute that the Windows Media Format SDK sets when it creates a local license for files protected with DRM version 1.</span></span> <span data-ttu-id="978f5-106">Contiene el nivel de seguridad que la aplicación que realiza la llamada debe tener para tener acceso al contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="978f5-106">It contains the security level that the calling application must have to access the content in the file.</span></span> <span data-ttu-id="978f5-107">El valor predeterminado es 150.</span><span class="sxs-lookup"><span data-stu-id="978f5-107">The default value is 150.</span></span>

## <a name="global-constant"></a><span data-ttu-id="978f5-108">Constante global</span><span class="sxs-lookup"><span data-stu-id="978f5-108">Global Constant</span></span>

<span data-ttu-id="978f5-109">\_nivel g wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="978f5-109">g\_wszWMDRM\_Level</span></span>

## <a name="data-type"></a><span data-ttu-id="978f5-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="978f5-110">Data Type</span></span>

<span data-ttu-id="978f5-111">**tipo de WMT \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="978f5-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="978f5-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="978f5-112">Remarks</span></span>

<span data-ttu-id="978f5-113">El nivel de seguridad de DRM de una aplicación viene determinado por la biblioteca wmstubdrm determinada a la que se vincula en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="978f5-113">An application's DRM security level is determined by the particular wmstubdrm library that it links to at compile time.</span></span> <span data-ttu-id="978f5-114">Para obtener más información sobre estos niveles de seguridad, consulte [obtención de la biblioteca DRM necesaria](obtaining-the-required-drm-library.md).</span><span class="sxs-lookup"><span data-stu-id="978f5-114">For more information on these security levels, see [Obtaining the Required DRM Library](obtaining-the-required-drm-library.md).</span></span> <span data-ttu-id="978f5-115">Use [**IWMHeaderInfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) para establecer esta propiedad al proteger los archivos ASF con DRM versión 1.</span><span class="sxs-lookup"><span data-stu-id="978f5-115">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property when protecting ASF files with DRM version 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="978f5-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="978f5-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="978f5-117">**Propiedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="978f5-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




