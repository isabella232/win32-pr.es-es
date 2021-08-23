---
description: El archivo GetOwner&\# 8194; El método de clase WMI recupera el nombre de usuario y el nombre de dominio en los que se ejecuta el proceso.
ms.assetid: bbd6d22b-ca54-42f3-8098-d3034048ec4d
ms.tgt_platform: multiple
title: Método GetOwner de la Win32_Process clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwner
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2fe91ef581490ab15869fa45c299c9e172c01df9d689a4fcd1546cbbf84621ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760445"
---
# <a name="getowner-method-of-the-win32_process-class"></a>Método GetOwner de la clase Process de Win32 \_

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwner** recupera el nombre de usuario y el nombre de dominio en los que se ejecuta el proceso.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetOwner(
  [out] string User,
  [out] string Domain
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Usuario* \[ out\]
</dt> <dd>

Devuelve el nombre de usuario del propietario de este proceso.

</dd> <dt>

*Dominio* \[ out\]
</dt> <dd>

Devuelve el nombre de dominio con el que se ejecuta este proceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero (0) para indicar que se ha correcto. Cualquier otro número indica que hubo un error. Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Finalización correcta** (0)
</dt> <dt>

**Acceso denegado** (2)
</dt> <dt>

**Privilegios insuficientes** (3)
</dt> <dt>

**Error desconocido** (8)
</dt> <dt>

**Ruta de acceso no encontrada** (9)
</dt> <dt>

**Parámetro no válido** (21)
</dt> <dt>

**Otros** (22 4294967295)
</dt> </dl>

## <a name="examples"></a>Ejemplos

[Monitor Process CPU Pct by Name with Owner](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) El ejemplo de VBScript recopila el porcentaje de uso de CPU o procesador y busca el propietario del proceso.

El [archivo Get all servers that a list of users is logged onto](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) PowerShell sample querys WMI for the owner of all explorer.exe processes (Obtener todos los servidores que una lista de usuarios ha iniciado sesión en El ejemplo de PowerShell consulta WMI para el propietario de todos los explorer.exe procesos).

En el siguiente ejemplo de código de VBScript se obtiene el propietario de cada proceso en ejecución.


```VB
strComputer = "."
Set colProcesses = GetObject("winmgmts:" & _
   "{impersonationLevel=impersonate}!\\" & strComputer & _
   "\root\cimv2").ExecQuery("Select * from Win32_Process")

For Each objProcess in colProcesses

    Return = objProcess.GetOwner(strNameOfUser)
    If Return <> 0 Then
        Wscript.Echo "Could not get owner info for process " & _  
            objProcess.Name & VBNewLine _
            & "Error = " & Return
    Else 
        Wscript.Echo "Process " _
            & objProcess.Name & " is owned by " _ 
            & "\" & strNameOfUser & "."
    End If
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Proceso \_ win32**](win32-process.md)
</dt> </dl>

 

