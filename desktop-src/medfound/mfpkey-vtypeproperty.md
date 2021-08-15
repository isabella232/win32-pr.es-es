---
description: Especifica la lógica que usará el códec para detectar vídeo de origen entrelazado.
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: MFPKEY_VTYPE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f406f0bc91e3431672c2b7f92cc544273e2a64403017a22eb4567054cef0155
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973344"
---
# <a name="mfpkey_vtype-property"></a>Propiedad VTYPE de MFPKEY \_

Especifica la lógica que usará el códec para detectar vídeo de origen entrelazado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCVType

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Comentarios

Esta propiedad puede establecerse en uno de los valores siguientes.



| Valor | Descripción                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | El códec usará la lógica de detección de tipo de marco estándar.                                                                                 |
| 1     | El códec tratará todos los fotogramas de vídeo de origen como fotogramas entrelazados.                                                                          |
| 2     | El códec tratará todos los fotogramas de vídeo de origen como campos de vídeo entrelazado.                                                                 |
| 3     | El códec determinará automáticamente si los fotogramas de vídeo de entrada son fotogramas entrelazados o campos de vídeo entrelazado.                      |
| 4     | El códec determinará automáticamente si los fotogramas de vídeo de entrada son fotogramas progresivas, fotogramas entrelazados o campos de vídeo entrelazado. |



 

Esta propiedad determina el método de codificación de imágenes usado para la codificación de vídeo progresiva o entrelazada.

Si no se especifica ningún tipo de vídeo, el códec usará la codificación de fotogramas progresiva para las sesiones de codificación progresiva y la codificación entrelazada de campos para las sesiones de codificación entrelazadas. El tipo de sesión de codificación de vídeo (progresiva o entrelazada) se establece mediante la propiedad [ \_ MFPKEY INTERLACEDCODINGENABLED.](mfpkey-interlacedcodingenabledproperty.md)

> [!Note]  
> La propiedad [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) debe establecerse en VARIANT TRUE para generar una salida entrelazada; de lo contrario, establecer la propiedad \_ MPFKEY VTYPE no tendrá \_ ningún efecto.

 

Cuando se codifica el vídeo entrelazado, es posible especificar varios métodos de codificación de imágenes. Normalmente, la manera más eficaz de codificar vídeo entrelazado es usar el método entrelazado de campo (2). Si el vídeo de origen contiene muy poco movimiento, el método entrelazado de fotogramas (1) o el método de marco/campo automático (2) podrían ser más adecuados.

Al codificar contenido mixto (que contiene fotogramas progresivas e entrelazados), es mejor usar el valor marco automático, campo o método progresista (4).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




