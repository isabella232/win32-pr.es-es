---
title: Método enable de la clase SystemRestore
description: Habilita la supervisión en una unidad determinada.
ms.assetid: f3140f6d-d190-46a4-8587-c2e928ac8ecf
keywords:
- Habilitar la restauración del sistema de métodos
- Habilitar método Restaurar sistema, clase SystemRestore
- SystemRestore Class System Restore, enable (método)
topic_type:
- apiref
api_name:
- SystemRestore.Enable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090aa01b4028a7146ea1d7f271ba4390f43ca260
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714597"
---
# <a name="enable-method-of-the-systemrestore-class"></a>Método enable de la clase SystemRestore

Habilita la supervisión en una unidad determinada.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Enable(
  [in] String Drive
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Unidad* \[ de de\]
</dt> <dd>

Unidad que se va a habilitar. La cadena de unidad debe tener el formato "C: \\ ". Si este parámetro es la unidad del sistema o una cadena vacía (""), se supervisan todas las unidades.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. De lo contrario, el método devuelve uno de los códigos de error COM definidos en WinError. h.

## <a name="remarks"></a>Observaciones

El método **enable** no espera a que la supervisión se habilite completamente antes de que se devuelva, ya que esto puede tardar unos minutos. En su lugar, se devuelve inmediatamente después de iniciar el servicio de restauración del sistema y el controlador de filtro.

Para habilitar Restaurar sistema en una unidad que no es del sistema, primero debe habilitar Restaurar sistema en la unidad del sistema.

Este método produce un error en modo seguro.

## <a name="examples"></a>Ejemplos


```VB
'Enable Method of the SystemRestore Class
'Enables monitoring on a particular drive.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else 
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
If (obj.Enable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                         |
| Espacio de nombres<br/>                | Raíz \\ predeterminada<br/>                                                          |
| MOF<br/>                      | <dl> <dt>MOF</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





