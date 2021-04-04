---
description: El experto debe implementar la función Register Expert. Monitor de red llama a la función Register Expert para obtener información sobre el experto.
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: Registrar función de devolución de llamada experta (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908697"
---
# <a name="register-expert-callback-function"></a>Registrar función de devolución de llamada experta

El experto debe implementar la función **Register** Expert. Monitor de red llama a la función **Register** Expert para obtener información sobre el experto.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pExpertInfo* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**EXPERTENUMINFO**](expertenuminfo.md) que monitor de red asigna. El experto rellena la estructura con toda la información solicitada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es **true** y la función devuelve la información solicitada.

Si la función no se realiza correctamente, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

El miembro de la **versión** de la estructura [**EXPERTENUMINFO**](expertenuminfo.md) debe ser cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




