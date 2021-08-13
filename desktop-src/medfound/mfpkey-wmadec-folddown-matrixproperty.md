---
description: Especifica los coeficientes desplegables proporcionados por el autor para descodificar audio multicanal para menos canales de los que contiene la secuencia codificada.
ms.assetid: f6737c05-4b39-4209-9985-9402b28cf316
title: MFPKEY_WMADEC_FOLDDOWN_MATRIX propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb1b9eb1259c2a8c23f7b993699e1c51f17c09636afd7d19de23ce033fd269fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463165"
---
# <a name="mfpkey_wmadec_folddown_matrix-property"></a>Propiedad MFPKEY \_ WMADEC \_ FOLDDOWN \_ MATRIX

Especifica los coeficientes desplegables proporcionados por el autor para descodificar audio multicanal para menos canales de los que contiene la secuencia codificada.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACFoldDownXToYChannels

g \_ wszWMACFoldXToYChannelsZ

## <a name="data-type"></a>Tipo de datos

**VT \_ ARRAY \| VT \_ I4**

## <a name="remarks"></a>Observaciones

Un descodificador de audio puede actuar como un objeto multimedia DirectX (DMO) o como un Media Foundation transformación (MFT). Para obtener información sobre cuándo un descodificador actúa como un DMO o un MFT, vea las páginas de referencia de códecs individuales en [Objetos de códec](codecobjects.md).

Cuando se usa un descodificador como un DMO, el descodificador puede realizar el plegado del canal hacia abajo y puede enumerar los tipos de medios de salida plegados llamando a [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).

Cuando se usa un descodificador como MFT, el descodificador de forma predeterminada no realizará ningún plegado y no ofrecerá tipos de medios de salida plegados hacia abajo. Un descodificador que actúa como MFT realizará el plegado hacia abajo solo si se establecen coeficientes de plegado personalizados mediante la propiedad **\_ MFPKEY WMADEC \_ FOLDDOWN \_ MATRIX.**

Si la propiedad **\_ MFPKEY WMADEC \_ FOLDDOWN \_ MATRIX** no está establecida en el descodificador de audio MFT y desea realizar un plegado hacia abajo, puede usar (como MFT) el procesador de señal digital Audio Resampler.

El valor de esta propiedad es una cadena que contiene coeficientes desplegables en una lista separada por comas de valores enteros. La lista debe contener un número de enteros para cada canal del contenido codificado igual al número de canales del contenido descodificado.

Si el coeficiente es cero, el valor que se va a usar en la cadena debe ser "-2147483648"; de lo contrario, el valor se calcula mediante la ecuación: 20 \* 65536 \* log10(x).

Los coeficientes se enumeran en el orden de la máscara de canal, tal como se define en las constantes de máscara de canal que se incluyen en el archivo de encabezado mmreg.h. Por lo tanto, los dos primeros valores de un canal de 6 a 2 desplegable representan las partes del canal de salida izquierdo y el canal de salida derecho que se constituyen en el canal central izquierdo en la secuencia de 6 canales.

Debe establecer esta propiedad solo si los valores desplegables proporcionados por el autor se conservan con el contenido codificado. De lo contrario, deje que el descodificador realice sus propios cálculos.

El códec Windows Media Audio 10 Professional actualmente solo admite el plegado a dos canales.

Si la propiedad [MFPKEY \_ WMADEC \_ SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) se establece en **DSSPEAKER \_ SURROUND,** el códec omitirá los coeficientes de plegado proporcionados por el autor y se plegará a una señal de 2 canales que puede procesar el descodificador de matriz del receptor. Esto permite que los equipos envolventes entreguen cuatro canales. Este modo solo se admite si el origen es 5.1. El códec solo puede plegar 8 canales a 2 canales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
