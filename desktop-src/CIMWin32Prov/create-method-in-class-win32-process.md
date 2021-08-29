---
description: La&\# 8194; El método de clase WMI crea un nuevo proceso.
ms.assetid: be80abec-fab4-4403-bc29-d0d4a38e3c87
ms.tgt_platform: multiple
title: Método Create de la Win32_Process clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15fef5786487a0e5dad6aa96f4061a2e7414773e2f269ea9834cc3dd17211e3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003855"
---
# <a name="create-method-of-the-win32_process-class"></a>Método Create de la clase Process de Win32 \_

El **método de** clase Create [WMI](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuevo proceso.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Create(
  [in]  string               CommandLine,
  [in]  string               CurrentDirectory,
  [in]  Win32_ProcessStartup ProcessStartupInformation,
  [out] uint32               ProcessId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CommandLine* \[ En\]
</dt> <dd>

Línea de comandos que se ejecutará. El sistema agrega un carácter nulo a la línea de comandos, recortando la cadena si es necesario, para indicar qué archivo se usó realmente.

</dd> <dt>

*CurrentDirectory* \[ En\]
</dt> <dd>

Unidad y directorio actuales del proceso secundario. La cadena requiere que el directorio actual se resuelva en una ruta de acceso conocida. Un usuario puede especificar una ruta de acceso absoluta o una ruta de acceso relativa al directorio de trabajo actual. Si este parámetro es **NULL,** el nuevo proceso tendrá la misma ruta de acceso que el proceso de llamada. Esta opción se proporciona principalmente para los shells que deben iniciar una aplicación y especificar la unidad inicial de la aplicación y el directorio de trabajo.

</dd> <dt>

*ProcessStartupInformation* \[ En\]
</dt> <dd>

Configuración de inicio de un Windows de inicio. Para obtener más información, [**vea Win32 \_ ProcessStartup**](win32-processstartup.md).

</dd> <dt>

*ProcessId* \[ out\]
</dt> <dd>

Identificador de proceso global que se puede usar para identificar un proceso. El valor es válido desde el momento en que se crea el proceso hasta el momento en que finaliza el proceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el proceso se creó correctamente y cualquier otro número para indicar un error. Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

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

## <a name="remarks"></a>Comentarios

Puede crear una instancia de la clase [**\_ ProcessStartup de Win32**](win32-processstartup.md) para configurar el proceso antes de llamar a este método.

Se debe especificar una ruta de acceso completa en los casos en los que el programa que se va a iniciar no se encuentra en la ruta de acceso de búsqueda Winmgmt.exe. Si el proceso recién creado intenta interactuar con objetos en el sistema de destino sin los privilegios de acceso adecuados, se termina sin notificación a este método.

Por motivos de seguridad, **el método \_ Process.Create de Win32** no se puede usar para iniciar un proceso interactivo de forma remota.

Los procesos creados con **el método \_ Process.Create de Win32** están limitados por el objeto de trabajo a menos que se especifique la marca CREATE **\_ BREAKAWAY FROM \_ \_ JOB.** Para obtener más información, [**vea Win32 \_ ProcessStartup**](win32-processstartup.md) y [**\_ \_ ProviderHostQuotaConfiguration.**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration)

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de VBScript se muestra cómo invocar un método CIM como si fuera un método de automatización de SWbemObject.


```VB
on error resume next

set process = GetObject("winmgmts:Win32_Process")

result = process.Create ("notepad.exe",null,null,processid)

WScript.Echo "Method returned result = " & result
WScript.Echo "Id of new process is " & processid

if err <>0 then
 WScript.Echo Err.Description, "0x" & Hex(Err.Number)
end if
```



En el siguiente ejemplo de Perl se muestra cómo invocar un método CIM como si fuera un método de automatización de SWbemObject.


```VB
use strict;
use Win32::OLE;

my ($process, $outParam, $processid, $inParam, $objMethod);

eval { $process = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_Process"); };

if (!$@ && defined $process)
{
 $objMethod = $process->Methods_("Create");

 #Spawn an instance of inParameters and assign the values.
 $inParam = $objMethod->inParameters->SpawnInstance_ if (defined $objMethod);
 $inParam->{CommandLine} = "notepad.exe";
 $inParam->{CurrentDirectory} = undef;
 $inParam->{ProcessStartupInformation} = undef;

 $outParam = $process->ExecMethod_("Create", $inParam) if (defined $inParam);
 if ($outParam->{ReturnValue})
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
 else
 {
  print "Method returned result = $outParam->{ReturnValue}\n";
  print "Id of new process is $outParam->{ProcessId}\n"
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



En el siguiente ejemplo de código vbscript se crea Bloc de notas proceso en el equipo local. [**Win32 \_ ProcessStartup**](win32-processstartup.md) se usa para configurar los valores del proceso.


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Process ID: " & intProcessID
End If
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

[**Proceso \_ win32**](win32-process.md)
</dt> <dt>

[Tareas wmi: procesos](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

