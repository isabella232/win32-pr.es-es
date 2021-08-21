---
description: Simula una pulsación de tecla.
ms.assetid: 42C11F92-6143-40D7-9C07-56A6514EB4D1
title: Método PressKey de la Msvm_Keyboard clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.PressKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93dfa4ca5ad1233f1d36323e5d59c31e194398df2b0b941036c8fc0ff182d505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146164"
---
# <a name="presskey-method-of-the-msvm_keyboard-class"></a>Método PressKey de la clase Msvm \_ Keyboard

Simula una pulsación de tecla. Cuando se realiza correctamente, la clave estará en estado de baja.

## <a name="syntax"></a>Sintaxis


```mof
uint32 PressKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*keyCode* \[ En\]
</dt> <dd>

Tipo: **uint32**

Código de clave virtual de la tecla que se debe presionar. Para obtener la lista de códigos de clave virtual, vea [**Códigos de clave virtual**](../inputdev/virtual-key-codes.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Un valor devuelto de cero indica que se ha correcto. Un valor distinto de cero indica un error al modificar el estado de la clave.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**Sistema en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

## <a name="remarks"></a>Comentarios

El método **PressKey** asigna referencias al menú de **VK \_** (18), **\_ VK CONTROL** (17) y **VK \_ SHIFT** (16) a **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) y **VK \_ LSHIFT** (160), respectivamente, porque los códigos de clave virtual **VK \_ MENU,** **VK \_ CONTROL** y **VK \_ MAYÚS** no representan claves reales en un teclado.

El acceso a [**la clase Msvm \_ Keyboard**](msvm-keyboard.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de C# simula una pulsación de tecla. Las utilidades a las que se hace referencia se pueden encontrar [en Utilidades comunes para los ejemplos de virtualización (V2).](common-utilities-for-the-virtualization-samples-v2.md)


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class PressKeyClass
    {
        static ManagementObject GetComputerKeyboard(ManagementObject vm)
        {
            ManagementObjectCollection keyboardCollection = vm.GetRelated
            (
                "Msvm_Keyboard",
                "Msvm_SystemDevice",
                null,
                null,
                "PartComponent",
                "GroupComponent",
                false,
                null
            );

            ManagementObject keyboard = null;

            foreach (ManagementObject instance in keyboardCollection)
            {
                keyboard = instance;
                break;
            }

            return keyboard;
        }

        static void PressKey(string vmName, int keyCode)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject keyboard = GetComputerKeyboard(vm);

            ManagementBaseObject inParams = keyboard.GetMethodParameters("PressKey");

            inParams["keyCode"] = keyCode;

            ManagementBaseObject outParams = keyboard.InvokeMethod("PressKey", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Key {0} was pressed on {1}", keyCode, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to press key {0}' on {1}", keyCode, vm["ElementName"]);
            }

            inParams.Dispose();
            outParams.Dispose();
            keyboard.Dispose();
            vm.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: PressKey vmName keyCode");
                return;
            }
            string vmName = args[0];
            int keyCode = int.Parse(args[1]);
            PressKey(args[0], keyCode);
        }

    }
}

```



El ejemplo Visual Basic Scripting Edition (VBScript) siguiente simula una pulsación de tecla.


```VB
option explicit 

dim objWMIService
dim fileSystem
const wmiSuccessful = 0

Main()

'-----------------------------------------------------------------
' Main routine
'-----------------------------------------------------------------
Sub Main()
    
    dim computer, objArgs, vmName, computerSystem, keycode, keyboard
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       keycode = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript PressKey.vbs vmName keycode"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set keyboard = GetComputerKeyboard(computerSystem)

    if PressKey(keyboard, keycode) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "PressKey failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
' 
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    dim query
    On Error Resume Next
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Retrieve Msvm_Keyboard from given computer system
' 
'-----------------------------------------------------------------
Function GetComputerKeyboard(computerSystem)
    dim query
    On Error Resume Next
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_Keyboard", computerSystem.Path_.Path)
    set GetComputerKeyboard = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function

'-----------------------------------------------------------------
' Press the key with the given key code on the given keyboard
'-----------------------------------------------------------------
Function PressKey(keyboard, keyCode)
    WriteLog Format2("PressKey({0}, {1})", keyboard.ElementName, keyCode)
    
    dim objInParam, objOutParams
    
    PressKey = false
    set objInParam = keyboard.Methods_("PressKey").InParameters.SpawnInstance_()
    objInParam.keyCode = keyCode

    set objOutParams = keyboard.ExecMethod_("PressKey", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("The key with code '{0}' is typed on {1}.", keyCode, keyboard.ElementName)
        PressKey = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\PressKey.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub


'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Teclado de \_ Msvm**](msvm-keyboard.md)
</dt> <dt>

[**Códigos de clave virtual**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

