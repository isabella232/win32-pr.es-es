---
description: Especifica la estructura DEDATOX que describe el contenido de audio de entrada.
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: MFPKEY_WMAENC_ORIGWAVEFORMAT propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3475e5578124b8f0a762beddf713f701a5695110
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474079"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a>Propiedad MFPKEY \_ WMAENC \_ ORIGWAVEFORMAT

Especifica la estructura [**DEDATOX**](/previous-versions/dd757713(v=vs.85)) que describe el contenido de audio de entrada.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACOriginalWaveFormat

## <a name="data-type"></a>Tipo de datos

VT \_ ARRAY \| VT \_ UI1 [**(WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) como una matriz de bytes)

## <a name="remarks"></a>Observaciones

Al transcodificación Windows contenido basado en Audio multimedia a una velocidad de bits inferior, puede pasar la estructura [**DEFORMATEX**](/previous-versions/dd757713(v=vs.85)) del contenido al códec para permitir que el códec optimice sus algoritmos. Esta característica, denominada recompresión inteligente, proporciona mejores resultados que descomprimir el contenido y, a continuación, devolver los ejemplos de PCM reconstruidos a través del códec.

Al pasar la [**estructura DESATEX,**](/previous-versions/dd757713(v=vs.85)) incluya los bytes adicionales al final de la estructura especificada por **ELATEX.cbSize**.

El codificador de audio solo acepta entradas y salidas para las que el número de canales, bits por muestra y frecuencia de muestreo son idénticos. Solo puede transcodificar contenido a una velocidad de bits inferior dentro de esos parámetros. En cualquier caso, debe descodificar el contenido y pasar los ejemplos sin comprimir como entrada al codificador. Al establecer esta propiedad se proporciona al codificador información sobre el procesamiento que ya se ha realizado en el contenido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
