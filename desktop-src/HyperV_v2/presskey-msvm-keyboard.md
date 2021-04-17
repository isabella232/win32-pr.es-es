---
description: Simula una pulsación de tecla.
ms.assetid: 42C11F92-6143-40D7-9C07-56A6514EB4D1
title: Método PressKey de la clase Msvm_Keyboard
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
ms.openlocfilehash: 5e9f196c5af3f8946460564e56bb425ffc24b51c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669940"
---
# <a name="presskey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="3e2dc-103">Método PressKey de la \_ clase de teclado MSVM</span><span class="sxs-lookup"><span data-stu-id="3e2dc-103">PressKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="3e2dc-104">Simula una pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="3e2dc-104">Simulates a key press.</span></span> <span data-ttu-id="3e2dc-105">Cuando se realice correctamente, la clave estará en estado inactivo.</span><span class="sxs-lookup"><span data-stu-id="3e2dc-105">When successful the key will be in the down state.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e2dc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e2dc-106">Syntax</span></span>


```mof
uint32 PressKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="3e2dc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e2dc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e2dc-108">*KeyCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e2dc-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e2dc-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3e2dc-109">Type: **uint32**</span></span>

<span data-ttu-id="3e2dc-110">Código de tecla virtual de la tecla que se va a presionar.</span><span class="sxs-lookup"><span data-stu-id="3e2dc-110">The virtual-key code of the key to press.</span></span> <span data-ttu-id="3e2dc-111">Para obtener la lista de códigos de tecla virtual, consulte [**códigos de tecla virtual**](../inputdev/virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3e2dc-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e2dc-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e2dc-112">Return value</span></span>

<span data-ttu-id="3e2dc-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3e2dc-113">Type: **uint32**</span></span>

<span data-ttu-id="3e2dc-114">Un valor devuelto de cero indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3e2dc-114">A return value of zero indicates success.</span></span> <span data-ttu-id="3e2dc-115">Un valor distinto de cero indica un error al modificar el estado de la clave.</span><span class="sxs-lookup"><span data-stu-id="3e2dc-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="3e2dc-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="3e2dc-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="3e2dc-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="3e2dc-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="3e2dc-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="3e2dc-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-121">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="3e2dc-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-122">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="3e2dc-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-123">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="3e2dc-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-124">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="3e2dc-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="3e2dc-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="3e2dc-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-127">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="3e2dc-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3e2dc-128">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="3e2dc-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="3e2dc-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e2dc-129">Remarks</span></span>

<span data-ttu-id="3e2dc-130">El método **PressKey** asigna referencias a los **\_ menús VK** (18), **VK \_ (** 17) y **VK \_ Shift** (16) a **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) y **VK \_ LSHIFT** (160), respectivamente, ya que el **\_ menú VK**, el **\_ control VK** y los códigos de tecla virtual **\_ Shift de VK** no representan claves reales en un teclado.</span><span class="sxs-lookup"><span data-stu-id="3e2dc-130">The **PressKey** method maps references to the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, because the **VK\_MENU**, **VK\_CONTROL**, and **VK\_SHIFT** virtual key codes do not represent real keys on a keyboard.</span></span>

<span data-ttu-id="3e2dc-131">El acceso a la clase de [**\_ teclado MSVM**](msvm-keyboard.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="3e2dc-131">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3e2dc-132">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3e2dc-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="3e2dc-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3e2dc-133">Examples</span></span>

<span data-ttu-id="3e2dc-134">En el siguiente ejemplo de C# se simula una pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="3e2dc-134">The following C# sample simulates a key press.</span></span> <span data-ttu-id="3e2dc-135">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="3e2dc-135">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


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



<span data-ttu-id="3e2dc-136">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se simula una pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="3e2dc-136">The following Visual Basic Scripting Edition (VBScript) sample simulates a key press.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3e2dc-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e2dc-137">Requirements</span></span>



| <span data-ttu-id="3e2dc-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e2dc-138">Requirement</span></span> | <span data-ttu-id="3e2dc-139">Value</span><span class="sxs-lookup"><span data-stu-id="3e2dc-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e2dc-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e2dc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="3e2dc-141">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e2dc-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3e2dc-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e2dc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="3e2dc-143">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e2dc-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e2dc-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3e2dc-144">Namespace</span></span><br/>                | <span data-ttu-id="3e2dc-145">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3e2dc-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3e2dc-146">MOF</span><span class="sxs-lookup"><span data-stu-id="3e2dc-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e2dc-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e2dc-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e2dc-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e2dc-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e2dc-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3e2dc-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3e2dc-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e2dc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e2dc-151">**\_Teclado MSVM**</span><span class="sxs-lookup"><span data-stu-id="3e2dc-151">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="3e2dc-152">**Códigos de tecla virtual**</span><span class="sxs-lookup"><span data-stu-id="3e2dc-152">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

