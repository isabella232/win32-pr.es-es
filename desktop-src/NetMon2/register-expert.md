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
ms.openlocfilehash: 1203682e82b01b7665c9661c3f58c14bbf2cd479cac62c72a64505b0e25feaa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889575"
---
# <a name="register-expert-callback-function"></a>Registrar función de devolución de llamada de experto

El experto debe implementar la **función register** expert. Monitor de red llama a la **función de experto Register** para obtener información sobre el experto.

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

## <a name="remarks"></a>Comentarios

El **miembro Version** de la estructura [**EXPERTENUMINFO**](expertenuminfo.md) debe ser cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




