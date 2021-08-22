---
description: El tipo de datos KEYSVCC \_ HANDLE define un identificador de servicio de claves. Las funciones RKeyOpenKeyService y RKeyCloseKeyService usan un identificador KEYSVCC \_ HANDLE.
ms.assetid: d0fd5184-5c8e-4f96-9ff1-8abd6f718d05
title: KEYSVCC_HANDLE (Rkeysvcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32e34285c6291cb7cb87aeb9095e5261b43999b0eefa82e33704719e7673f1b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515955"
---
# <a name="keysvcc_handle"></a>IDENTIFICADOR \_ KEYSVCC

El **tipo de datos KEYSVCC \_ HANDLE** define un identificador de servicio de claves. Las funciones [**RKeyOpenKeyService**](rkeyopenkeyservice.md) y [**RKeyCloseKeyService**](rkeyclosekeyservice.md) usan un identificador **KEYSVCC \_** HANDLE.


```C++
typedef void* KEYSVCC_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 




