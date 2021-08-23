---
description: Invoca la operación chkdsk en el disco.
ms.assetid: 65942702-b660-46cd-b614-e3e1ec3df7b9
ms.tgt_platform: multiple
title: Método Chkdsk de la Win32_LogicalDisk clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.Chkdsk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 24d7052cd7d36da8a9464cbbef142904a70f83767872dadf25fda2033fa66fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959114"
---
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a>Método Chkdsk de la clase \_ LogicalDisk win32

El método de instancia de **Chkdsk** invoca la **operación chkdsk** en el disco.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Chkdsk(
  [in] boolean FixErrors = ,
  [in] boolean VigorousIndexCheck = ,
  [in] boolean SkipFolderCycle = ,
  [in] boolean ForceDismount = ,
  [in] boolean RecoverBadSectors = ,
  [in] boolean OKToRunAtBootUp = 
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FixErrors* \[ En\]
</dt> <dd>

Indica lo que se debe hacer a los errores encontrados en el disco. Si **es true**, se corregirán los errores. El valor predeterminado es **false**.

</dd> <dt>

*DesindexCheck Desacombado* \[ En\]
</dt> <dd>

Si **es true,** se debe realizar una comprobación menos productiva de las entradas de índice. El valor predeterminado es **false**.

</dd> <dt>

*SkipFolderCycle* \[ En\]
</dt> <dd>

Si **es true,** se debe omitir la comprobación del ciclo de carpeta. El valor predeterminado es **true**.

</dd> <dt>

*ForceDismount* \[ En\]
</dt> <dd>

Si **es true,** se debe forzar el desmontaje de la unidad antes de la comprobación. El valor predeterminado es **false**.

</dd> <dt>

*RecoverBadSectors* \[ En\]
</dt> <dd>

Si **es true,** se deben encontrar los sectores no válidos y se debe recuperar la información legible de estos sectores. El valor predeterminado es **false**.

</dd> <dt>

*OKToRunAtBootUp* \[ En\]
</dt> <dd>

Si **es true**, la operación **chkdsk** debe realizarse en el siguiente tiempo de arranque, en caso de que no se pueda realizar la operación porque el disco está bloqueado en el momento en que se llama a este método. El valor predeterminado es **false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se realiza correctamente. En la lista siguiente se enumeran otros valores. Para obtener códigos de error adicionales, [**vea Constantes de error WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Correcto: Chkdsk completado**
</dt> <dd>

0

Correcto: [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) completado

</dd> <dt>

**Correcto: bloqueados y chkdsk programados al reiniciar**
</dt> <dd>

1

</dd> <dt>

**Error: sistema de archivos desconocido**
</dt> <dd>

2

</dd> <dt>

**Error: error desconocido**
</dt> <dd>

3

</dd> <dt>

**Error: sistema de archivos no admitido**
</dt> <dd>

4

</dd> </dl>

## <a name="remarks"></a>Comentarios

Este método solo es aplicable a las instancias de disco lógico que representan un disco físico en la máquina. No es aplicable a las unidades lógicas asignadas.

## <a name="examples"></a>Ejemplos

El ejemplo de código de PowerShell[Is CHKDSK Dirty Bit Set](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) on a server examina el sistema remoto y devuelve un valor true o false si se estableció la marca chkdsk /f.

El [ejemplo de código de](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) PowerShell Detección remota de disco se inicia o programa Detección de disco de forma remota.

El siguiente ejemplo de código VBScript ejecuta ChkDsk.exe en la unidad D de un equipo.


```VB
Const FIX_ERRORS = True 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk.DeviceID='D:'") 
 
errReturn = objDisk.ChkDsk(FIX_ERRORS) 
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

[**Disco lógico \_ win32**](win32-logicaldisk.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

