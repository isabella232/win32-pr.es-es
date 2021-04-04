---
title: DRM_DRMHeader_LicenseAcqURL
description: El \_ atributo DRMHeader de DRM \_ LicenseAcqURL contiene la dirección URL de adquisición de licencias para una licencia de DRM versión 7.
ms.assetid: 00c788b4-b291-4df5-9926-0badc7357faf
keywords:
- DRM_DRMHeader_LicenseAcqURL formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c394df01703befbb17c61b340b8ea4239740ac3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077312"
---
# <a name="drm_drmheader_licenseacqurl"></a>\_LicenseAcqURL DRMHEADER \_ DRM

El **atributo \_ DRMHeader \_ de DRM LicenseAcqURL** contiene la dirección URL de adquisición de licencias para una licencia de DRM versión 7.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Este atributo solo está presente con el contenido de la versión 7 de DRM. Se puede recuperar con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Para establecer la dirección URL de adquisición de licencias en el archivo mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , debe usar la propiedad [**\_ LicenseAcqURL de DRM**](drm-licenseacqurl.md) .

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




