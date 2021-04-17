---
description: Especifica si el DSP de la captura de voz almacena las estadísticas de la marca de tiempo en el registro.
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: Propiedad MFPKEY_WMAAECMA_RETRIEVE_TS_STATS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8e4efad8def035c7282e3ade8045bdbfd7e34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696690"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a>MFPKEY \_ WMAAECMA \_ recuperar \_ la \_ propiedad de estadísticas de TS

Especifica si el DSP de la captura de voz almacena las estadísticas de la marca de tiempo en el registro.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ bool

## <a name="default-value"></a>Valor predeterminado

VARIANTE \_ false

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

Los algoritmos de cancelación del eco acústico (AEC) dependen de las marcas de tiempo precisas en las secuencias de audio. En realidad, las marcas de tiempo suelen ser imperfectas y los distintos dispositivos de audio pueden presentar diferentes tasas de varianza y de desplazamiento. Cuando AEC está habilitado, el DSP recopila estadísticas sobre las marcas de tiempo y usa esta información para compensar las imprecisiones.

Si el valor de esta propiedad es VARIANT \_ true, el DSP guarda las estadísticas que recopila en el registro. La próxima vez que el DSP realice el AEC usando el mismo par de dispositivos de audio, leerá la información estadística del registro, lo que permite que el DSP funcione de forma más eficaz.

Si establece el valor de esta propiedad en VARIANT \_ true y usa el DSP en modo de filtro, también debe establecer la propiedad [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) . En el modo de origen, esto no es necesario.

El valor predeterminado de esta propiedad es VARIANT \_ false. El DSP usa esta propiedad solo cuando el procesamiento de AEC está habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
