---
description: Especifica los coeficientes de subconjuntos proporcionados por el autor para descodificar el audio multicanal para menos canales de los que contiene la secuencia codificada.
ms.assetid: f6737c05-4b39-4209-9985-9402b28cf316
title: Propiedad MFPKEY_WMADEC_FOLDDOWN_MATRIX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92cb2495863d319c7f755d7d72f475ccf1eda75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715539"
---
# <a name="mfpkey_wmadec_folddown_matrix-property"></a>\_Propiedad MFPKEY WMADEC \_ FOLDDOWN \_ Matrix

Especifica los coeficientes de subconjuntos proporcionados por el autor para descodificar el audio multicanal para menos canales de los que contiene la secuencia codificada.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACFoldDownXToYChannels

g \_ wszWMACFoldXToYChannelsZ

## <a name="data-type"></a>Tipo de datos

**\_Matriz VT \| VT \_ I4**

## <a name="remarks"></a>Observaciones

Un descodificador de audio puede actuar como un objeto multimedia de DirectX (DMO) o como una transformación de Media Foundation (MFT). Para obtener información sobre cuándo un descodificador actúa como DMO o MFT, consulte las páginas de referencia de códecs individuales en [objetos de códec](codecobjects.md).

Cuando se usa un descodificador como DMO, el descodificador puede realizar un repliegue de canal y se pueden enumerar los tipos de medios de salida plegados mediante una llamada a [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).

Cuando se usa un descodificador como MFT, el descodificador de forma predeterminada no realizará ningún repliegue y no ofrecerá tipos de medios de salida plegados. Un descodificador que actúe como MFT solo realizará un repliegue si los coeficientes de subconjunto personalizado se establecen mediante la propiedad de **\_ \_ \_ matriz MFPKEY WMADEC FOLDDOWN** .

Si la propiedad MFPKEY de la **\_ matriz de WMADEC \_ FOLDDOWN \_** no se establece en la MFT del descodificador de audio y desea realizar un repliegue, puede usar (como MFT) el procesador de señal digital de remuestreador de audio.

El valor de esta propiedad es una cadena que contiene coeficientes de repliegue en una lista separada por comas de valores enteros. La lista debe contener un número de enteros para cada canal en el contenido codificado igual al número de canales en el contenido descodificado.

Si el coeficiente es cero, el valor que se va a utilizar en la cadena debe ser "-2147483648"; en caso contrario, el valor se calcula con la ecuación: 20 \* 65536 \* log10 (x).

Los coeficientes se enumeran en el orden de máscara de canal, tal como se define en las constantes de máscara de canal que se incluyen en el archivo de encabezado mmreg. h. Por lo tanto, los dos primeros valores de un subconjunto de canal de 6 a 2 representan las partes del canal de salida de la izquierda y el canal de salida derecho que se compone del canal izquierdo central en el flujo de 6 canales.

Debe establecer esta propiedad solo si los valores de plegamiento proporcionados por el autor se conservan con el contenido codificado. De lo contrario, deje que el descodificador realice sus propios cálculos.

Actualmente, el códec Windows Media Audio 10 Professional solo admite la reducción vertical de dos canales.

Si la propiedad [MFPKEY \_ WMADEC \_ SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) está establecida en **\_ envolved DSSPEAKER**, el códec omitirá los coeficientes de subconjuntos proporcionados por el autor y se doblará a una señal de 2 canales que puede ser procesada por el descodificador de matriz del receptor. Esto permite que los equipos envolventes entreguen cuatro canales. Este modo solo se admite si el origen es 5,1. El códec solo puede doblar 8 canales a 2 canales.

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

 

 
