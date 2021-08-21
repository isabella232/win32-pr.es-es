---
title: Método Disable de la clase SystemRestore
description: Deshabilita la supervisión en una unidad determinada.
ms.assetid: 2ad37dd4-7d80-4697-9dbb-abb329a34ff7
keywords:
- Deshabilitar el método Restaurar sistema
- Deshabilitar método Restaurar sistema , clase SystemRestore
- SystemRestore class Restaurar sistema , Disable (método)
topic_type:
- apiref
api_name:
- SystemRestore.Disable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a05d53ee13e2f06c2f4765d2947f49a417ed798965406185619dfce207cf76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452926"
---
# <a name="disable-method-of-the-systemrestore-class"></a>Método Disable de la clase SystemRestore

Deshabilita la supervisión en una unidad determinada.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Disable(
  [in] String Drive
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Unidad* \[ En\]
</dt> <dd>

Unidad que se va a deshabilitar. La cadena de unidad debe tener el formato "C: \\ ". Si este parámetro es la unidad del sistema o una cadena vacía (""), no se supervisa ninguna unidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es S \_ OK. De lo contrario, el método devuelve uno de los códigos de error COM definidos en WinError.h.

## <a name="examples"></a>Ejemplos


```VB
'Disable Method of the SystemRestore Class
'Disables monitoring on a particular drive.
Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.Disable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                         |
| Espacio de nombres<br/>                | Raíz \\ predeterminada<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





