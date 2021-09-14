---
description: Especifica si el códec debe intentar detectar bordes de marco ruidosos y quitarlos.
ms.assetid: fdb4f3a8-1447-4e1e-a208-0f9b717f7626
title: MFPKEY_NOISEEDGEREMOVAL propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30acd92bae7693d0714e42d6b4f832a521557bf2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268892"
---
# <a name="mfpkey_noiseedgeremoval-property"></a>Propiedad \_ MFPKEY NOISEEDGEREMOVAL

Especifica si el códec debe intentar detectar bordes de marco ruidosos y quitarlos.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCNoiseEdgeRemoval

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="default-value"></a>Valor predeterminado

false

## <a name="remarks"></a>Observaciones

Un borde de marco ruidoso suele ser los datos del intervalo de espacio en blanco vertical (VBI) de un fotograma de televisión de difusión. La VBI es las primeras 21 líneas de digitalización del marco de televisión. Estas líneas de examen no contienen datos de vídeo: contienen datos sobre la difusión. Cuando una tarjeta de captura registra una señal de televisión, la VBI normalmente se quita del marco. La detección y corrección de borde ruidosos realizadas por el códec solo puede corregir un borde que tenga tres o menos líneas de ruido. Si el vídeo capturado contiene más de tres líneas ruidosas, hay un problema con el hardware que se usa para capturar el vídeo.

Si el códec se establece para quitar los bordes ruidosos, duplica las líneas adyacentes al borde ruidoso para rellenar el marco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




