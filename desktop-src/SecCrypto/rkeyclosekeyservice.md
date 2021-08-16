---
description: No se admite la función RKeyCloseKeyService.
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: Función RKeyCloseKeyService (Rkeysvcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyCloseKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 5c7a075cf4869e350d90e278d009098cf4716d6518b1970c15b8b8264c93cd22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900560"
---
# <a name="rkeyclosekeyservice-function"></a>Función RKeyCloseKeyService

No **se admite la función RKeyCloseKeyService.**

**Windows Server 2003:** La **función RKeyCloseKeyService** cierra un identificador de servicio clave abierto por una llamada anterior a la [**función RKeyOpenKeyService.**](rkeyopenkeyservice.md) Tenga en cuenta que este comportamiento ha cambiado con Windows Server 2003 con Service Pack 1 (SP1).

## <a name="syntax"></a>Sintaxis


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hKeySvcCli* \[ En\]
</dt> <dd>

Un [**identificador KEYSVCC \_ HANDLE**](keysvcc-handle.md) abierto previamente [**por RKeyOpenKeyService**](rkeyopenkeyservice.md). Este valor no puede ser **NULL.**

</dd> <dt>

*pReserved* \[ in, out\]
</dt> <dd>

Reservado. Establezca este valor en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es S \_ OK.

Si se produce un error en la función, el valor devuelto es **un ULONG** que indica el error.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> </dl>

 

 




