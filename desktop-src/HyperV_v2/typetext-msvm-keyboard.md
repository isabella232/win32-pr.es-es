---
description: Simula una serie de caracteres con tipo.
ms.assetid: 5D4C9F27-84AA-4131-A9A3-2C72DB2E8909
title: Método TypeText de la clase Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeText
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 37e8227a545975a6193be63a8bd363e10e9805f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688355"
---
# <a name="typetext-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="e297b-103">Método TypeText de la \_ clase de teclado MSVM</span><span class="sxs-lookup"><span data-stu-id="e297b-103">TypeText method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="e297b-104">Simula una serie de caracteres con tipo.</span><span class="sxs-lookup"><span data-stu-id="e297b-104">Simulates a series of typed characters.</span></span> <span data-ttu-id="e297b-105">Esto es equivalente a llamar a [**PressKey**](presskey-msvm-keyboard.md) seguido de [**ReleaseKey**](releasekey-msvm-keyboard.md) para cada carácter de la cadena.</span><span class="sxs-lookup"><span data-stu-id="e297b-105">This is equivalent to calling [**PressKey**](presskey-msvm-keyboard.md) followed by [**ReleaseKey**](releasekey-msvm-keyboard.md) for each character in the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e297b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e297b-106">Syntax</span></span>


```mof
uint32 TypeText(
  [in] string asciiText
);
```



## <a name="parameters"></a><span data-ttu-id="e297b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e297b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e297b-108">*asciiText* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e297b-108">*asciiText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e297b-109">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="e297b-109">Type: **string**</span></span>

<span data-ttu-id="e297b-110">La serie de caracteres ASCII o Unicode que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="e297b-110">The series of ASCII or Unicode characters to type.</span></span> <span data-ttu-id="e297b-111">La longitud máxima de esta cadena depende del tipo de caracteres de la cadena.</span><span class="sxs-lookup"><span data-stu-id="e297b-111">The maximum length of this string depends on the type of characters in the string.</span></span>



| <span data-ttu-id="e297b-112">Tipo de cadena</span><span class="sxs-lookup"><span data-stu-id="e297b-112">String type</span></span>        | <span data-ttu-id="e297b-113">Número máximo de caracteres</span><span class="sxs-lookup"><span data-stu-id="e297b-113">Maximum characters</span></span>                                                               |
|--------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e297b-114">ASCII</span><span class="sxs-lookup"><span data-stu-id="e297b-114">ASCII</span></span><br/>   | <span data-ttu-id="e297b-115">512</span><span class="sxs-lookup"><span data-stu-id="e297b-115">512</span></span><br/>                                                                   |
| <span data-ttu-id="e297b-116">Unicode</span><span class="sxs-lookup"><span data-stu-id="e297b-116">Unicode</span></span><br/> | <span data-ttu-id="e297b-117">de 256 a 512, dependiendo del número de pares suplentes de la cadena.</span><span class="sxs-lookup"><span data-stu-id="e297b-117">256 to 512, depending on the number of surrogate pairs in the string.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e297b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e297b-118">Return value</span></span>

<span data-ttu-id="e297b-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e297b-119">Type: **uint32**</span></span>

<span data-ttu-id="e297b-120">Un valor devuelto de cero indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e297b-120">A return value of zero indicates success.</span></span> <span data-ttu-id="e297b-121">Un valor devuelto de uno indica un error causado por caracteres no traducibles en la cadena de entrada.</span><span class="sxs-lookup"><span data-stu-id="e297b-121">A return value of one indicates a failure caused by nontranslatable characters in the input string.</span></span> <span data-ttu-id="e297b-122">Los demás valores distintos de cero indican un error al modificar el estado de la clave.</span><span class="sxs-lookup"><span data-stu-id="e297b-122">All other nonzero values indicate a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="e297b-123">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="e297b-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e297b-124">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="e297b-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e297b-125">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="e297b-125">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e297b-126">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e297b-126">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e297b-127">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="e297b-127">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e297b-128">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e297b-128">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e297b-129">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="e297b-129">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e297b-130">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e297b-130">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e297b-131">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e297b-131">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e297b-132">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="e297b-132">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e297b-133">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e297b-133">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e297b-134">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="e297b-134">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e297b-135">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e297b-135">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e297b-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e297b-136">Remarks</span></span>

<span data-ttu-id="e297b-137">El acceso a la clase de [**\_ teclado MSVM**](msvm-keyboard.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="e297b-137">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e297b-138">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e297b-138">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="e297b-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e297b-139">Examples</span></span>

<span data-ttu-id="e297b-140">En el siguiente ejemplo de C# se simula el texto escrito.</span><span class="sxs-lookup"><span data-stu-id="e297b-140">The following C# sample simulates typing text.</span></span> <span data-ttu-id="e297b-141">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="e297b-141">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class TypeTextClass
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

        static void TypeText(string vmName, string text)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject keyboard = GetComputerKeyboard(vm);

            ManagementBaseObject inParams = keyboard.GetMethodParameters("TypeText");

            inParams["asciiText"] = text;

            ManagementBaseObject outParams = keyboard.InvokeMethod("TypeText", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Text {0} was typed on {1}", text, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to type '{0}' on {1}", text, vm["ElementName"]);
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
                Console.WriteLine("Usage: TypeText vmName Text");
                return;
            }
            TypeText(args[0], args[1]);
        }
    }
}

```



<span data-ttu-id="e297b-142">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se simula el texto escrito.</span><span class="sxs-lookup"><span data-stu-id="e297b-142">The following Visual Basic Scripting Edition (VBScript) sample simulates typing text.</span></span>


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
    dim computer, objArgs, vmName, computerSystem, text, keyboard
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       text = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript TypeText.vbs vmName text"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set keyboard = GetComputerKeyboard(computerSystem)

    if TypeText(keyboard, text) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "TypeText operation failed"
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
' Type the given text to the given keyboard
'-----------------------------------------------------------------
Function TypeText(keyboard, text)
    WriteLog Format2("TypeText({0}, {1})", keyboard.ElementName, text)
    
    dim objInParam, objOutParams

    TypeText = false
    set objInParam = keyboard.Methods_("TypeText").InParameters.SpawnInstance_()
    objInParam.asciiText = text

    set objOutParams = keyboard.ExecMethod_("TypeText", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("'{0}' was typed on {1}", text, keyboard.ElementName)
        TypeText = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\Typetext.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="e297b-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e297b-143">Requirements</span></span>



| <span data-ttu-id="e297b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="e297b-144">Requirement</span></span> | <span data-ttu-id="e297b-145">Value</span><span class="sxs-lookup"><span data-stu-id="e297b-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e297b-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e297b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e297b-147">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e297b-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e297b-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e297b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e297b-149">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e297b-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e297b-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e297b-150">Namespace</span></span><br/>                | <span data-ttu-id="e297b-151">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e297b-151">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e297b-152">MOF</span><span class="sxs-lookup"><span data-stu-id="e297b-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e297b-153"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e297b-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e297b-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e297b-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e297b-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e297b-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e297b-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="e297b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e297b-157">**\_Teclado MSVM**</span><span class="sxs-lookup"><span data-stu-id="e297b-157">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

