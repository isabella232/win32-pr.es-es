---
title: DRM_DRMHeader_LicenseAcqURL
description: El atributo DRMHeader LicenseAcqURL de DRM contiene la dirección URL de adquisición \_ de licencia para una licencia drm versión \_ 7.
ms.assetid: 00c788b4-b291-4df5-9926-0badc7357faf
keywords:
- DRM_DRMHeader_LicenseAcqURL windows Media Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c394df01703befbb17c61b340b8ea4239740ac3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467087"
---
# <a name="drm_drmheader_licenseacqurl"></a>DRM \_ DRMHeader \_ LicenseAcqURL

El **atributo \_ DRMHeader \_ LicenseAcqURL de DRM** contiene la dirección URL de adquisición de licencia para una licencia drm versión 7.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL

## <a name="data-type"></a>Tipo de datos

**CADENA DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Observaciones

Este atributo solo está presente con el contenido de la versión 7 de DRM. Se puede recuperar con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Para establecer la dirección URL de adquisición de licencias en el archivo mediante [**IWMDRMWriter::SetDRMAttribute,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) debe usar la propiedad [**\_ LicenseAcqURL de DRM.**](drm-licenseacqurl.md)

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




