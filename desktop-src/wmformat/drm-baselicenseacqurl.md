---
title: DRM_BaseLicenseAcqURL
description: El \_ atributo BaseLicenseAcqURL de DRM contiene una dirección URL base parcial a la que una aplicación de reproductor debe navegar para obtener una licencia para el contenido.
ms.assetid: 9acaac44-81b2-467c-9510-023fbb47dd04
keywords:
- DRM_BaseLicenseAcqURL formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_BaseLicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 128a65eb51d9051243dd439e208207aaf98d5caf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149076"
---
# <a name="drm_baselicenseacqurl"></a><span data-ttu-id="3ac7f-104">\_BASELICENSEACQURL DRM</span><span class="sxs-lookup"><span data-stu-id="3ac7f-104">DRM\_BaseLicenseAcqURL</span></span>

<span data-ttu-id="3ac7f-105">El **atributo \_ BaseLicenseAcqURL de DRM** contiene una dirección URL base parcial a la que una aplicación de reproductor debe navegar para obtener una licencia para el contenido.</span><span class="sxs-lookup"><span data-stu-id="3ac7f-105">The **DRM\_BaseLicenseAcqURL** attribute contains a partial, base URL to which a player application must navigate to obtain a license for the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="3ac7f-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="3ac7f-106">Global Constant</span></span>

<span data-ttu-id="3ac7f-107">g \_ wszWMDRM \_ BaseLicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="3ac7f-107">g\_wszWMDRM\_BaseLicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="3ac7f-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3ac7f-108">Data Type</span></span>

<span data-ttu-id="3ac7f-109">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="3ac7f-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="3ac7f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ac7f-110">Remarks</span></span>

<span data-ttu-id="3ac7f-111">Se trata de una propiedad de lectura y escritura opcional que se establece y recupera mediante [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="3ac7f-111">This is an optional read-write property that is set and retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="3ac7f-112">Se proporciona para permitir que los sistemas de distribución de licencias usen rutas de acceso relativas en las propiedades de la dirección URL de adquisición de licencias.</span><span class="sxs-lookup"><span data-stu-id="3ac7f-112">It is provided to enable license distribution systems to use relative paths in the license acquisition URL properties.</span></span>

<span data-ttu-id="3ac7f-113">Después de establecer esta propiedad, todas las direcciones URL de adquisición de licencias parciales en encabezados de contenido tendrán la dirección URL base agregada al principio de la dirección URL parcial para formar una dirección URL completa a la que navegar la aplicación de reproducción.</span><span class="sxs-lookup"><span data-stu-id="3ac7f-113">After setting this property, all partial license acquisition URLs in content headers will have the base URL added to the front of the partial URL to form a full URL for the player application to navigate to.</span></span> <span data-ttu-id="3ac7f-114">La llamada a **IWMDRMReader:: GetDRMProperty** para **DRM \_ BaseLicenseAcqURL** solo funcionará en la misma sesión que se estableció.</span><span class="sxs-lookup"><span data-stu-id="3ac7f-114">Calling **IWMDRMReader::GetDRMProperty** for **DRM\_BaseLicenseAcqURL** will only work only in the same session as it was set.</span></span> <span data-ttu-id="3ac7f-115">La propiedad no se almacena en el encabezado de contenido; es dinámica y solo se almacena la dirección URL relativa en el contenido.</span><span class="sxs-lookup"><span data-stu-id="3ac7f-115">The property is not stored in the content header; it is dynamic, and only the relative URL is stored in the content.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ac7f-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ac7f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ac7f-117">**Propiedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="3ac7f-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




