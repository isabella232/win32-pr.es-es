---
description: El experto debe implementar la función register expert. Monitor de red llama a la función register expert para obtener información sobre el experto.
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: Registrar función de devolución de llamada de experto (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 085d5c59b17b10949ad39d07354906f40e123988
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074096"
---
# <a name="register-expert-callback-function"></a>Registrar función de devolución de llamada de experto

El experto debe implementar la **función register** expert. Monitor de red llama a **la función register** expert para obtener información sobre el experto.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pEinfo* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura EXPERTENUMINFO**](expertenuminfo.md) que Monitor de red asigna. El experto rellena la estructura con toda la información solicitada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es **TRUE** y la función devuelve la información solicitada.

Si la función no se realiza correctamente, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Observaciones

El **miembro Version** de la estructura [**EXPERTENUMINFO**](expertenuminfo.md) debe ser cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




