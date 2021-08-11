---
description: Especifica la duración del eco que el algoritmo de cancelación de eco acústico (AEC) puede controlar, en milisegundos.
ms.assetid: d451b90f-7ef7-4f66-be83-aca93e3ad894
title: MFPKEY_WMAAECMA_FEATR_ECHO_LENGTH propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4b8f22b87622c00c296f194cb7ba618c55b04901ac30ce216d7387e2e04033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242032"
---
# <a name="mfpkey_wmaaecma_featr_echo_length-property"></a>Propiedad MFPKEY \_ WMAAECMA \_ FEATR \_ ECHO \_ LENGTH

Especifica la duración del eco que el algoritmo de cancelación de eco acústico (AEC) puede controlar, en milisegundos.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

256

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentarios

El algoritmo de AEC usa un filtro adaptable cuya longitud viene determinada por la duración del eco. Se recomienda que las aplicaciones usen uno de los siguientes valores:

-   128
-   256
-   512
-   1024

El valor predeterminado es 256 milisegundos, lo que es suficiente para la mayoría de los entornos de oficina y hogar. Antes de establecer esta propiedad, debe establecer la propiedad [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) en VARIANT \_ TRUE.

El DSP usa esta propiedad solo cuando el procesamiento de AEC está habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
