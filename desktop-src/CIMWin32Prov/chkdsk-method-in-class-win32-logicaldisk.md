---
description: Invoca la operación Chkdsk en el disco.
ms.assetid: 65942702-b660-46cd-b614-e3e1ec3df7b9
ms.tgt_platform: multiple
title: Método CHKDSK de la clase Win32_LogicalDisk
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
ms.openlocfilehash: 662fc8739f90eea15295b762edc446ac16677aef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153299"
---
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a>Método CHKDSK de la \_ clase Win32 LogicalDisk

El método de instancia **CHKDSK** invoca la operación **CHKDSK** en el disco.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

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

*FixErrors* \[ de\]
</dt> <dd>

Indica qué se debe hacer con los errores encontrados en el disco. Si **es true**, se corrigen los errores. El valor predeterminado es **false**.

</dd> <dt>

*VigorousIndexCheck* \[ de\]
</dt> <dd>

Si **es true**, se debe realizar una comprobación menos exhaustiva de entradas de índice. El valor predeterminado es **false**.

</dd> <dt>

*SkipFolderCycle* \[ de\]
</dt> <dd>

Si **es true**, se debe omitir la comprobación del ciclo de la carpeta. El valor predeterminado es **true**.

</dd> <dt>

*ForceDismount* \[ de\]
</dt> <dd>

Si **es true**, se debe forzar el desmontaje de la unidad antes de la comprobación. El valor predeterminado es **false**.

</dd> <dt>

*RecoverBadSectors* \[ de\]
</dt> <dd>

Si **es true**, se deben encontrar los sectores dañados y se debe recuperar la información legible de estos sectores. El valor predeterminado es **false**.

</dd> <dt>

*OKToRunAtBootUp* \[ de\]
</dt> <dd>

Si es **true**, la operación **CHKDSK** debe realizarse en el próximo arranque, en caso de que no se pueda realizar la operación porque el disco está bloqueado en el momento en que se llama a este método. El valor predeterminado es **false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se realiza correctamente. Otros valores se muestran en la lista siguiente. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Correcto: CHKDSK completado**
</dt> <dd>

0

Correcto: [**CHKDSK**](chkdsk-method-in-class-win32-logicaldisk.md) completado

</dd> <dt>

**Correcto: bloqueado y CHKDSK programado en el reinicio**
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

## <a name="remarks"></a>Observaciones

Este método solo es aplicable a las instancias de disco lógico que representan un disco físico en el equipo. No es aplicable a las unidades lógicas asignadas.

## <a name="examples"></a>Ejemplos

El[bit de integridad de CHKDSK está establecido en un ejemplo de código de PowerShell de servidor](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) examina el sistema remoto y devuelve true o false si se ha establecido la marca chkdsk/f.

En el ejemplo de código de PowerShell de [disco remoto](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) se inicia o programa el disco de examen de forma remota.

El siguiente ejemplo de código de VBScript se ejecuta ChkDsk.exe en la unidad D de un equipo.


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
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LogicalDisk de Win32 \_**](win32-logicaldisk.md)
</dt> <dt>

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

