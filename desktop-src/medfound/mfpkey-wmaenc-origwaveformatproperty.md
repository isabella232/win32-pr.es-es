---
description: Especifica la estructura WAVEFORMATEX que describe el contenido de audio de entrada.
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: Propiedad MFPKEY_WMAENC_ORIGWAVEFORMAT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3475e5578124b8f0a762beddf713f701a5695110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276227"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a>\_ \_ Propiedad ORIGWAVEFORMAT de MFPKEY WMAENC

Especifica la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) que describe el contenido de audio de entrada.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACOriginalWaveFormat

## <a name="data-type"></a>Tipo de datos

VT \_ array \| VT \_ UI1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) como una matriz de bytes)

## <a name="remarks"></a>Observaciones

Al transcodificar contenido basado en Windows Media Audio a una velocidad de bits más baja, puede pasar la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) del contenido al códec para permitir que el códec optimice sus algoritmos. Esta característica, denominada recompresión inteligente, proporciona mejores resultados que descomprimir el contenido y, a continuación, volver a alimentar los ejemplos de PCM reconstruidos a través del códec.

Al pasar la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) , incluya cualquier byte adicional al final de la estructura especificada por **WAVEFORMATEX. cbSize**.

El codificador de audio solo acepta entradas y salidas para las que el número de canales, bits por muestra y velocidad de muestreo son idénticos. Puede transcodificar contenido solo a una velocidad de bits menor dentro de esos parámetros. En cualquier caso, debe descodificar el contenido y pasar los ejemplos sin comprimir como entrada al codificador. Al establecer esta propiedad, se proporciona al codificador alguna información sobre el procesamiento que ya se ha realizado en el contenido.

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

 

 
