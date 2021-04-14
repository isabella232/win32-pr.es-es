---
title: DRM_LicenseAcqURL
description: El \_ atributo LicenseAcqURL de DRM contiene la dirección de una página web a la que la aplicación cliente puede desplazarse para obtener una licencia de contenido para el contenido de la versión 7 de DRM.
ms.assetid: bee29e39-ded8-439d-9164-fc318cb535c0
keywords:
- DRM_LicenseAcqURL formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231efc4334a4d893b4bdd1e7545bd50b1bed2a5c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104533004"
---
# <a name="drm_licenseacqurl"></a>\_LICENSEACQURL DRM

El **atributo \_ LicenseAcqURL de DRM** contiene la dirección de una página web a la que la aplicación cliente puede desplazarse para obtener una licencia de contenido para el contenido de la versión 7 de DRM.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ LicenseAcqURL

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Este atributo se puede establecer mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Se puede recuperar el mismo atributo de archivo mediante [**DRM \_ DRMHeader \_ LicenseAcqURL**](drm-drmheader-licenseacqurl.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




