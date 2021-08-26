---
description: Elimina un nombre de recurso compartido de la lista de recursos compartidos de un servidor y desconecta las conexiones al recurso compartido.
ms.assetid: 175f9c0e-0017-4a86-8e05-ad78e2c93c11
ms.tgt_platform: multiple
title: Método Delete de la Win32_Share clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c1331ce9dfa3309c1cfbd0ba0ddc3b4a0c96d431d524d8f0e74f7937c8cdb332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918475"
---
# <a name="delete-method-of-the-win32_share-class"></a>Método Delete de la clase Win32 \_ Share

El **método de** clase WMI [Delete](/windows/desktop/WmiSdk/retrieving-a-class) elimina un nombre de recurso compartido de la lista de recursos compartidos de un servidor y desconecta las conexiones al recurso compartido.

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Acceso denegado** (2)
</dt> <dt>

**Error desconocido** (8)
</dt> <dt>

**Nombre no válido** (9)
</dt> <dt>

**Nivel no válido** (10)
</dt> <dt>

**Parámetro no válido** (21)
</dt> <dt>

**Recurso compartido duplicado** (22)
</dt> <dt>

**Ruta de acceso redirigida** (23)
</dt> <dt>

**Dispositivo o directorio desconocidos** (24)
</dt> <dt>

**Nombre de red no encontrado** (25)
</dt> <dt>

**Otros** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentarios

El **método Delete** es un método de objeto y se usa en una instancia de una clase .

Solo los miembros del grupo local Administradores u Operadores de cuenta o aquellos con pertenencia a grupos de operadores de comunicación, impresión o servidor pueden ejecutar correctamente el método . El operador Print solo puede eliminar colas de impresora. El operador Communication solo puede eliminar colas de dispositivos de comunicación.

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de código VBScript elimina el recurso compartido especificado.


```VB
On Error Resume Next

ComputerName = InputBox("Enter the computer name:", "Delete Share", "localhost")

SName = InputBox("Enter the name of the share:", "Delete Share")



Set Shares = GetObject("winmgmts:\\" & ComputerName & _
 "\root\cimv2").ExecQuery("SELECT * FROM Win32_Share WHERE name = '" & SName & "'")



For Each Share in Shares
 Share.Delete()
Next
```



El siguiente ejemplo de código de PowerShell elimina recursos compartidos en blanco.


```PowerShell
$Shares = Get-WMIObject Win32_Share | Where {$_.Name -eq ""}

Foreach ($Share in $Shares) {
   $Share.Delete()
}
"{0} blank shares found and removed" -f $shares.count
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**Recurso compartido de \_ Win32**](win32-share.md)
</dt> </dl>

 

