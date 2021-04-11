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
# <a name="drm_baselicenseacqurl"></a>\_BASELICENSEACQURL DRM

El **atributo \_ BaseLicenseAcqURL de DRM** contiene una dirección URL base parcial a la que una aplicación de reproductor debe navegar para obtener una licencia para el contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ BaseLicenseAcqURL

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Se trata de una propiedad de lectura y escritura opcional que se establece y recupera mediante [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Se proporciona para permitir que los sistemas de distribución de licencias usen rutas de acceso relativas en las propiedades de la dirección URL de adquisición de licencias.

Después de establecer esta propiedad, todas las direcciones URL de adquisición de licencias parciales en encabezados de contenido tendrán la dirección URL base agregada al principio de la dirección URL parcial para formar una dirección URL completa a la que navegar la aplicación de reproducción. La llamada a **IWMDRMReader:: GetDRMProperty** para **DRM \_ BaseLicenseAcqURL** solo funcionará en la misma sesión que se estableció. La propiedad no se almacena en el encabezado de contenido; es dinámica y solo se almacena la dirección URL relativa en el contenido.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




