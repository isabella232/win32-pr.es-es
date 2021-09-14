---
description: Especifica si el DSP de captura de voz almacena las estadísticas de marca de tiempo en el registro.
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: MFPKEY_WMAAECMA_RETRIEVE_TS_STATS propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8e4efad8def035c7282e3ade8045bdbfd7e34d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363787"
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

## <a name="remarks"></a>Observaciones

Los algoritmos de cancelación de eco acústico (AEC) dependen de marcas de tiempo precisas en las secuencias de audio. En realidad, las marcas de tiempo suelen ser más complejas y los distintos dispositivos de audio pueden presentar diferentes tasas de varianza y desviación. Cuando AEC está habilitado, el DSP recopila estadísticas sobre las marcas de tiempo y usa esta información para compensar las imprecisiones.

Si el valor de esta propiedad es VARIANT TRUE, el DSP guarda las \_ estadísticas que recopila en el registro. La próxima vez que el DSP realice AEC con el mismo par de dispositivos de audio, leerá la información estadística del registro, lo que permite que el DSP se ejecute de forma más eficaz.

Si establece el valor de esta propiedad en VARIANT TRUE y usa el DSP en modo de filtro, también debe establecer la propiedad \_ GUID [MFPKEY \_ WMAAECMA \_ DEVICEPAIR. \_ ](mfpkey-wmaaecma-devicepair-guidproperty.md) En el modo de origen, esto no es necesario.

El valor predeterminado de esta propiedad es VARIANT \_ FALSE. El DSP usa esta propiedad solo cuando el procesamiento de AEC está habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
