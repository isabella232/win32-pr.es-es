---
title: Método GetLastRestoreStatus de la clase SystemRestore
description: Recupera el estado de la última restauración del sistema.
ms.assetid: 03f9fd71-9f20-428e-bdca-4692e838581a
keywords:
- Método GetLastRestoreStatus Restaurar sistema
- Método GetLastRestoreStatus Restaurar sistema, clase SystemRestore
- SystemRestore Class System Restore, GetLastRestoreStatus método
topic_type:
- apiref
api_name:
- SystemRestore.GetLastRestoreStatus
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd1ef0e62f7874bb92f3c8e9ecec7b62a1b3ff3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705115"
---
# <a name="getlastrestorestatus-method-of-the-systemrestore-class"></a>Método GetLastRestoreStatus de la clase SystemRestore

Recupera el estado de la última restauración del sistema.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetLastRestoreStatus();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores de estado.



| Valor devuelto                                                                 | Descripción                                  |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>0</dt> </dl> | Error en la última restauración.<br/>          |
| <dl> <dt>1</dt> </dl> | La última restauración se realizó correctamente.<br/>  |
| <dl> <dt>2</dt> </dl> | Se interrumpió la última restauración.<br/> |



 

## <a name="examples"></a>Ejemplos


```VB
'GetLastRestoreStatus Method of the SystemRestore Class
'Retrieves the status of the last system restore.
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
stat = obj.GetLastRestoreStatus()
If stat = 0 Then
    wscript.Echo "Failed"
ElseIf stat = 1 Then 
    wscript.Echo "Success"
ElseIf stat = 2 Then
    wscript.Echo "Interrrupted"
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

 

 





