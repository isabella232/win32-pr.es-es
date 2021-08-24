---
title: DRM_BaseLicenseAcqURL
description: El atributo BaseLicenseAcqURL de DRM contiene una dirección URL base parcial a la que una aplicación de reproductor debe navegar para obtener una \_ licencia para el contenido.
ms.assetid: 9acaac44-81b2-467c-9510-023fbb47dd04
keywords:
- DRM_BaseLicenseAcqURL windows Media Format
topic_type:
- apiref
api_name:
- DRM_BaseLicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77827068ee8a491cd732b28e5b8d60e1868ec66c04c72156f08358dd7d3751d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659005"
---
# <a name="drm_baselicenseacqurl"></a>DRM \_ BaseLicenseAcqURL

El **atributo \_ BaseLicenseAcqURL de DRM** contiene una dirección URL base parcial a la que una aplicación de reproductor debe navegar para obtener una licencia para el contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ BaseLicenseAcqURL

## <a name="data-type"></a>Tipo de datos

**CADENA DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Se trata de una propiedad de lectura y escritura opcional que se establece y recupera mediante [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Se proporciona para permitir que los sistemas de distribución de licencias usen rutas de acceso relativas en las propiedades de la dirección URL de adquisición de licencias.

Después de establecer esta propiedad, todas las direcciones URL de adquisición de licencias parciales de los encabezados de contenido tendrán la dirección URL base agregada al frente de la dirección URL parcial para formar una dirección URL completa a la que navegar la aplicación del reproductor. Llamar **a IWMDRMReader::GetDRMProperty** para **DRM \_ BaseLicenseAcqURL** solo funcionará en la misma sesión que se estableció. La propiedad no se almacena en el encabezado de contenido; es dinámico y solo la dirección URL relativa se almacena en el contenido.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




