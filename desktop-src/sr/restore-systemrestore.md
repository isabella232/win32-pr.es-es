---
title: Método restore de la clase SystemRestore
description: Inicia una restauración del sistema.
ms.assetid: ca4aa97b-fa59-407d-b127-951d46932c33
keywords:
- Restore Method Restaurar sistema
- Restore Method System Restore, clase SystemRestore
- Clase SystemRestore System Restore, método restore
topic_type:
- apiref
api_name:
- SystemRestore.Restore
api_location:
- Root\\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b7747b710801718d9b169c8999c51dd30cefde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801382"
---
# <a name="restore-method-of-the-systemrestore-class"></a>Método restore de la clase SystemRestore

Inicia una restauración del sistema. El autor de la llamada debe forzar el reinicio del sistema. La restauración real se produce durante el reinicio.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Restore(
  [in] uint32 SequenceNumber
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SequenceNumber* \[ de\]
</dt> <dd>

Número de secuencia del punto de restauración. Para determinar el número de secuencia de un punto de restauración específico, enumere todos los puntos de restauración en el sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. De lo contrario, el método devuelve uno de los códigos de error COM definidos en WinError. h.

## <a name="examples"></a>Ejemplos


```VB
'Restore Method of the SystemRestore Class
'Initiates a system restore. The caller must 
'force a system reboot. The actual restoration 
'occurs during the reboot.
Set Args = wscript.Arguments
RpNum = Args.item(0)
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
if obj.Restore(RpNum) <> 0 Then
    wscript.Echo "Restore failed"
End If
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
for each OpSys in OpSysSet
    OpSys.Reboot()
next
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                         |
| Espacio de nombres<br/>                | Raíz \\ \\ predeterminada<br/>                                                        |
| MOF<br/>                      | <dl> <dt>MOF</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





