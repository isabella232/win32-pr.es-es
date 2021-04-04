---
description: No se admite la función RKeyCloseKeyService.
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: Función RKeyCloseKeyService (Rkeysvcc. h)
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
ms.openlocfilehash: 3a35362876c067de011ec69a858e20150308cbd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907977"
---
# <a name="rkeyclosekeyservice-function"></a>RKeyCloseKeyService función)

No se admite la función **RKeyCloseKeyService** .

**Windows Server 2003:** La función **RKeyCloseKeyService** cierra un identificador del servicio de claves abierto por una llamada anterior a la función [**RKeyOpenKeyService**](rkeyopenkeyservice.md) . Tenga en cuenta que este comportamiento ha cambiado con Windows Server 2003 con Service Pack 1 (SP1).

## <a name="syntax"></a>Sintaxis


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hKeySvcCli* \[ de\]
</dt> <dd>

Identificador [**de \_ controlador de KEYSVCC**](keysvcc-handle.md) abierto previamente por [**RKeyOpenKeyService**](rkeyopenkeyservice.md). Este valor no puede ser **null**.

</dd> <dt>

*conservado* \[ in, out\]
</dt> <dd>

Reservado. Establezca este valor en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es S \_ OK.

Si se produce un error en la función, el valor devuelto es un **ULong** que indica el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> </dl>

 

 




