---
description: Especifica si el codificador genera entradas de fotograma ficticias en la secuencia de bits para fotogramas duplicados.
ms.assetid: dc09cecb-98c0-40bb-9e5d-f4661bf98522
title: MFPKEY_PRODUCEDUMMYFRAMES propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cb8f186c885e9cc150ab194bdadd01403a37b423b30bf6009b173819d27dfa9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939895"
---
# <a name="mfpkey_producedummyframes-property"></a>Propiedad MFPKEY \_ PRODUCEDUMMYFRAMES

Especifica si el codificador genera entradas de fotograma ficticias en la secuencia de bits para fotogramas duplicados.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCProduceDummyFrames

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="default-value"></a>Valor predeterminado

VARIANT \_ FALSE

## <a name="remarks"></a>Comentarios

Si este valor es VARIANT FALSE, el códec no colocará ningún dato en la \_ secuencia de bits para fotogramas duplicados.

Los fotogramas ficticios pueden ser importantes en aplicaciones donde se conservan los números de fotograma. Un ejemplo común es cuando se mantienen los códigos de tiempo de SMPTE para el contenido codificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




