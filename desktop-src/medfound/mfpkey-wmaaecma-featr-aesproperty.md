---
description: Especifica cuántas veces el DSP de captura de voz realiza la supresión de eco acústico (AES) en la señal residual.
ms.assetid: 409b40f8-38eb-49f7-be30-348ab5cdd33a
title: MFPKEY_WMAAECMA_FEATR_AES propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e842bc3064b431437d8bbdfab06c0081ecdb49a8c38288ba4adb78648363c71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242042"
---
# <a name="mfpkey_wmaaecma_featr_aes-property"></a>Propiedad \_ AES MFPKEY WMAAECMA \_ FEATR \_

Especifica cuántas veces el DSP de captura de voz realiza la supresión de eco acústico (AES) en la señal residual.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentarios

El DSP de captura de voz puede realizar AES en la señal residual después de la cancelación del eco. Esta propiedad puede tener el valor 0, 1 o 2. El valor predeterminado es 0. Antes de establecer esta propiedad, debe establecer la propiedad [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) en VARIANT \_ TRUE.

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

 

 
