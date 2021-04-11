---
description: Especifica si el códec debe intentar detectar bordes de fotogramas ruidosos y quitarlos.
ms.assetid: fdb4f3a8-1447-4e1e-a208-0f9b717f7626
title: Propiedad MFPKEY_NOISEEDGEREMOVAL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30acd92bae7693d0714e42d6b4f832a521557bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276314"
---
# <a name="mfpkey_noiseedgeremoval-property"></a>\_Propiedad NOISEEDGEREMOVAL de MFPKEY

Especifica si el códec debe intentar detectar bordes de fotogramas ruidosos y quitarlos.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCNoiseEdgeRemoval

## <a name="data-type"></a>Tipo de datos

VT \_ bool

## <a name="default-value"></a>Valor predeterminado

false

## <a name="remarks"></a>Observaciones

Un borde de marco ruidoso suele ser el intervalo de espacio en blanco (VBI) vertical de un fotograma de televisión de difusión. VBI son las 21 primeras líneas de análisis del fotograma de televisión. Estas líneas de análisis no contienen datos de vídeo, sino que contienen datos sobre la difusión. Cuando una tarjeta de captura graba una señal de televisión, el VBI normalmente se quita del fotograma. La detección y corrección de bordes ruidosos realizadas por el códec solo puede corregir un borde que tenga tres o menos líneas de ruido. Si el vídeo capturado contiene más de tres líneas ruidosos, hay un problema con el hardware que se usa para capturar el vídeo.

Si el códec está configurado para quitar bordes ruidosos, duplica líneas adyacentes al borde ruidoso para rellenar el fotograma.

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

 

 




