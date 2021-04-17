---
description: Especifica la duración del eco que el algoritmo de cancelación del eco acústico (AEC) puede controlar, en milisegundos.
ms.assetid: d451b90f-7ef7-4f66-be83-aca93e3ad894
title: Propiedad MFPKEY_WMAAECMA_FEATR_ECHO_LENGTH (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d66f7dcc4764447495e0f3ae55d2d038c2a8d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696698"
---
# <a name="mfpkey_wmaaecma_featr_echo_length-property"></a>\_Propiedad de \_ longitud de \_ eco \_ del MFPKEY de WMAAECMA

Especifica la duración del eco que el algoritmo de cancelación del eco acústico (AEC) puede controlar, en milisegundos.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

256

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

El algoritmo AEC usa un filtro adaptable cuya longitud viene determinada por la duración del eco. Se recomienda que las aplicaciones usen uno de los siguientes valores:

-   128
-   256
-   512
-   1024

El valor predeterminado es 256 milisegundos, que es suficiente para la mayoría de los entornos de oficina y de casa. Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.

El DSP usa esta propiedad solo cuando el procesamiento de AEC está habilitado.

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

 

 
