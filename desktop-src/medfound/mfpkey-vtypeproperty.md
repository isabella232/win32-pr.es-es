---
description: Especifica la lógica que el códec usará para detectar vídeo de origen entrelazado.
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: Propiedad MFPKEY_VTYPE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e95bab3120e60a2faa1a3be47c6459205f5f34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908386"
---
# <a name="mfpkey_vtype-property"></a>\_Propiedad VTYPE de MFPKEY

Especifica la lógica que el códec usará para detectar vídeo de origen entrelazado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCVType

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Esta propiedad se puede establecer en uno de los valores siguientes.



| Value | Descripción                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | El códec usará la lógica de detección estándar de tipo de marco.                                                                                 |
| 1     | El códec tratará todos los fotogramas de vídeo de origen como fotogramas entrelazados.                                                                          |
| 2     | El códec tratará todos los fotogramas de vídeo de origen como campos de vídeo entrelazado.                                                                 |
| 3     | El códec determinará automáticamente si los fotogramas de vídeo de entrada son fotogramas entrelazados o campos de vídeo entrelazado.                      |
| 4     | El códec determinará automáticamente si los fotogramas de vídeo de entrada son fotogramas progresivos, fotogramas entrelazados o campos de vídeo entrelazado. |



 

Esta propiedad determina el método de codificación de imágenes que se usa para la codificación de vídeo progresiva o entrelazada.

Si no se especifica ningún tipo de vídeo, el códec utilizará la codificación de tramas progresiva para las sesiones de codificación progresiva y la codificación entrelazada de campo para las sesiones de codificación entrelazada. El tipo de sesión de codificación de vídeo (progresivo o entrelazado) se establece mediante la [propiedad \_ INTERLACEDCODINGENABLED de MFPKEY](mfpkey-interlacedcodingenabledproperty.md) .

> [!Note]  
> La propiedad [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) debe establecerse en Variant \_ true para producir una salida entrelazada; de lo contrario, el establecimiento de la \_ propiedad MPFKEY VTYPE no tendrá ningún efecto.

 

Cuando se está codificando el vídeo entrelazado, es posible especificar varios métodos de codificación de imágenes. Normalmente, la manera más eficaz de codificar vídeo entrelazado es usar el método entrelazado de campo (2). Si el vídeo de origen contiene muy poco movimiento, el método entrelazado de fotogramas (1) o el método de marco/campo automático (2) podrían ser más adecuados.

Al codificar contenido mixto (que contiene fotogramas progresivos y entrelazados), es mejor usar el método automático de valor Frame/Field/progresivo (4).

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

 

 




