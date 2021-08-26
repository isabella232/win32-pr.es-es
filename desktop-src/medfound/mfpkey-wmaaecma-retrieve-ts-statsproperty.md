---
description: Especifica si el DSP de captura de voz almacena las estadísticas de marca de tiempo en el registro.
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: MFPKEY_WMAAECMA_RETRIEVE_TS_STATS (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c28f9812bb5f1324fcb1153b84f5a6704c7481c8356073fd02b8d95b57a8e497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953505"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a>MFPKEY \_ WMAAECMA \_ RETRIEVE \_ TS \_ STATS Property

Especifica si el DSP de captura de voz almacena las estadísticas de marca de tiempo en el registro.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="default-value"></a>Valor predeterminado

VARIANT \_ FALSE

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentarios

Los algoritmos de cancelación de eco acústico (AEC) dependen de marcas de tiempo precisas en las secuencias de audio. En realidad, las marcas de tiempo suelen ser más complejas y los distintos dispositivos de audio pueden presentar diferentes tasas de varianza y desviación. Cuando AEC está habilitado, el DSP recopila estadísticas sobre las marcas de tiempo y usa esta información para compensar las imprecisiones.

Si el valor de esta propiedad es VARIANT TRUE, el DSP guarda las \_ estadísticas que recopila en el registro. La próxima vez que el DSP realice AEC con el mismo par de dispositivos de audio, leerá la información estadística del registro, lo que permite que el DSP se ejecute de forma más eficaz.

Si establece el valor de esta propiedad en VARIANT TRUE y usa el DSP en modo de filtro, también debe establecer la propiedad \_ GUID [MFPKEY \_ WMAAECMA \_ DEVICEPAIR. \_ ](mfpkey-wmaaecma-devicepair-guidproperty.md) En el modo de origen, esto no es necesario.

El valor predeterminado de esta propiedad es VARIANT \_ FALSE. El DSP usa esta propiedad solo cuando el procesamiento de AEC está habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
