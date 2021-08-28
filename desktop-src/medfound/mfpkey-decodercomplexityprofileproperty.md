---
description: Especifica el perfil de complejidad del contenido codificado.
ms.assetid: 2e238d31-98b2-4c79-96b0-9e6949010a73
title: MFPKEY_DECODERCOMPLEXITYPROFILE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca206357a3f3a396ac6d07ea16a1b72bc245c641095a5523e46139dfd6af7f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604225"
---
# <a name="mfpkey_decodercomplexityprofile-property"></a>Propiedad DECODERCOMPLEXITYPROFILE de MFPKEY \_

Especifica el perfil de complejidad del contenido codificado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCDecoderComplexityProfile

## <a name="data-type"></a>Tipo de datos

**VT \_ BSTR**

## <a name="remarks"></a>Comentarios

Solo puede leer este valor una vez completada la codificación.

En el caso del audio, esta propiedad tiene uno de los valores siguientes.



| Valor | Descripción                                                                                    |
|-------|------------------------------------------------------------------------------------------------|
| "L1"  | Codificación estándar con una frecuencia de muestreo de 44,1 KHz y una velocidad de bits máxima de 161 Kbps.         |
| "L2"  | Codificación estándar con velocidades de muestreo de hasta 48 KHz y una velocidad de bits máxima de 161 Kbps.         |
| "L3"  | Codificación estándar con velocidades de muestreo de hasta 48 KHz y una velocidad de bits máxima de 385 Kbps.         |
| "M0a" | Professional codificación con velocidades de muestreo de hasta 48 KHz y velocidades de bits entre 48 y 192 Kbps.  |
| "M0b" | Professional codificación con velocidades de muestreo de hasta 48 KHz y una velocidad de bits máxima de 192 Kbps.      |
| "M1"  | Professional codificación con velocidades de muestreo de hasta 48 KHz y una velocidad de bits máxima de 384 Kbps.      |
| "M2"  | Professional codificación con velocidades de muestreo de hasta 96 KHz y una velocidad de bits máxima de 768 Kbps.      |
| "M3"  | Professional codificación con velocidades de muestreo de hasta 96 KHz y una velocidad de bits máxima de 1,5 Mbps.      |
| "N1"  | Codificación sin pérdida con velocidades de muestreo de hasta 48 KHz y un máximo de 2 canales.                |
| "N2"  | Codificación sin pérdida con velocidades de muestreo de hasta 96 KHz y un máximo de 6 canales (5,1 envolvente). |
| "N3"  | Codificación sin pérdida con velocidades de muestreo de hasta 96 KHz y un máximo de 8 canales (7,1 envolvente). |



 

Para el vídeo, esta propiedad tiene uno de los siguientes valores:



| Value | Descripción                                                                       |
|-------|-----------------------------------------------------------------------------------|
| "AP"  | perfil avanzado (disponible solo en el códec Windows de perfil avanzado de Media Video 9) |
| "CP"  | ya no se admite                                                               |
| "MP"  | perfil principal                                                                      |
| "SP"  | perfil simple                                                                    |



 

Para el contenido de vídeo, puede solicitar un nivel de perfil estableciendo [MFPKEY \_ DECODERCOMPLEXITYREQUESTED antes](mfpkey-decodercomplexityrequestedproperty.md) de comenzar la codificación. El códec intentará codificar dentro de los parámetros del nivel de complejidad solicitado, pero las demás opciones que configure tendrán prioridad. Siempre debe comprobar el valor del perfil de complejidad real después de la codificación en caso de que no se pueda respetar la solicitud.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




