---
description: Especifica el perfil de complejidad del contenido codificado.
ms.assetid: 2e238d31-98b2-4c79-96b0-9e6949010a73
title: Propiedad MFPKEY_DECODERCOMPLEXITYPROFILE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39544830a0a05e21779a637da61d3bcb310fcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908793"
---
# <a name="mfpkey_decodercomplexityprofile-property"></a>\_Propiedad DECODERCOMPLEXITYPROFILE de MFPKEY

Especifica el perfil de complejidad del contenido codificado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCDecoderComplexityProfile

## <a name="data-type"></a>Tipo de datos

**VT \_ BSTR**

## <a name="remarks"></a>Observaciones

Este valor solo se puede leer una vez completada la codificación.

En el caso de audio, esta propiedad tiene uno de los valores siguientes.



| Value | Descripción                                                                                    |
|-------|------------------------------------------------------------------------------------------------|
| Nivel  | Codificación estándar con una velocidad de muestreo de 44,1 KHz y una velocidad de bits máxima de 161 kbps.         |
| L2  | Codificación estándar con velocidades de muestreo de hasta 48 KHz y una velocidad de bits máxima de 161 kbps.         |
| Caché  | Codificación estándar con velocidades de muestreo de hasta 48 KHz y una velocidad de bits máxima de 385 kbps.         |
| "M0a" | Codificación profesional con velocidades de muestreo de hasta 48 KHz y velocidades de bits entre 48 y 192 kbps.  |
| "M0b" | Codificación profesional con velocidades de muestreo de hasta 48 KHz y una velocidad de bits máxima de 192 kbps.      |
| Conector  | Codificación profesional con velocidades de muestreo de hasta 48 KHz y una velocidad de bits máxima de 384 Kbps.      |
| ²  | Codificación profesional con velocidades de muestreo de hasta 96 KHz y una velocidad de bits máxima de 768 kbps.      |
| M3  | Codificación profesional con velocidades de muestreo de hasta 96 KHz y una velocidad de bits máxima de 1,5 Mbps.      |
| N1  | Codificación sin pérdida con velocidades de muestreo de hasta 48 KHz y un máximo de 2 canales.                |
| N2  | Codificación sin pérdida con velocidades de muestreo de hasta 96 KHz y un máximo de 6 canales (5,1 envolvente). |
| N3  | Codificación sin pérdida con velocidades de muestreo de hasta 96 KHz y un máximo de 8 canales (7,1 envolvente). |



 

En el caso de vídeo, esta propiedad tiene uno de los siguientes valores:



| Value | Descripción                                                                       |
|-------|-----------------------------------------------------------------------------------|
| AISLAMIENTO  | perfil avanzado (disponible solo en códec de perfil avanzado de Windows Media Video 9) |
| CP  | ya no se admite                                                               |
| MP  | Perfil principal                                                                      |
| DAÑADO  | Perfil simple                                                                    |



 

Para el contenido de vídeo, puede solicitar un nivel de perfil estableciendo [MFPKEY \_ DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) antes de comenzar la codificación. El códec intentará codificar dentro de los parámetros del nivel de complejidad solicitado, pero los demás valores de configuración que configure tendrán prioridad. Siempre debe comprobar el valor del perfil de complejidad real después de la codificación en caso de que no se pueda respetar la solicitud.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




