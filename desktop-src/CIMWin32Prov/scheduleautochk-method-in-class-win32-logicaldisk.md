---
description: Programa el Autochk para que se ejecute en la unidad de disco representada por el LogicalDisk de Win32 \_ en el siguiente reinicio si se ha establecido el bit de integridad.
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: Método ScheduleAutoChk de la clase Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ScheduleAutoChk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2707810d919c119aff35f2313e9aa5218f7948f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998191"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="79fc1-103">Método ScheduleAutoChk de la \_ clase Win32 LogicalDisk</span><span class="sxs-lookup"><span data-stu-id="79fc1-103">ScheduleAutoChk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="79fc1-104">El método de clase **ScheduleAutoChk** programa el Autochk para que se ejecute en la unidad de disco representada por el [**\_ LogicalDisk de Win32**](win32-logicaldisk.md) en el siguiente reinicio si se ha establecido el bit de integridad.</span><span class="sxs-lookup"><span data-stu-id="79fc1-104">The **ScheduleAutoChk** class method schedules Autochk to be run on the disk drive represented by the [**Win32\_LogicalDisk**](win32-logicaldisk.md) at the next reboot if the dirty bit is set.</span></span>

<span data-ttu-id="79fc1-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="79fc1-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="79fc1-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="79fc1-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="79fc1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79fc1-107">Syntax</span></span>


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a><span data-ttu-id="79fc1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79fc1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79fc1-109">*LogicalDisk* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79fc1-109">*LogicalDisk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79fc1-110">Especifica la lista de unidades que se van a programar para Autochk en el siguiente reinicio.</span><span class="sxs-lookup"><span data-stu-id="79fc1-110">Specifies the list of drives to schedule for Autochk at the next reboot.</span></span> <span data-ttu-id="79fc1-111">La sintaxis de la cadena se compone de la letra de unidad seguida de dos puntos para el disco lógico, por ejemplo: "C:"</span><span class="sxs-lookup"><span data-stu-id="79fc1-111">The string syntax consists of the drive letter followed by a colon for the logical disk, for example: "C:"</span></span>

> [!Note]  
> <span data-ttu-id="79fc1-112">Compruebe siempre la validez de las letras de unidad de la matriz *LogicalDisk* cuando los datos proceden de un origen desconocido o de un origen que no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="79fc1-112">Always check the validity of the drive letters in the *LogicalDisk* array when the data comes from an unknown source, or a source that you do not trust.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79fc1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79fc1-113">Return value</span></span>

<span data-ttu-id="79fc1-114">Devuelve un valor de 0 (cero) si es correcto y otro valor si se produce algún otro error.</span><span class="sxs-lookup"><span data-stu-id="79fc1-114">Returns a value of 0 (zero) if successful, and some other value if any other error occurs.</span></span> <span data-ttu-id="79fc1-115">Los valores se muestran en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="79fc1-115">Values are listed in the following list.</span></span> <span data-ttu-id="79fc1-116">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="79fc1-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="79fc1-117">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="79fc1-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="79fc1-118">**Sin errores** (0)</span><span class="sxs-lookup"><span data-stu-id="79fc1-118">**No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79fc1-119">**Error: unidad remota** (1)</span><span class="sxs-lookup"><span data-stu-id="79fc1-119">**Error - Remote Drive** (1)</span></span>
</dt> <dt>

<span data-ttu-id="79fc1-120">**Error: unidad extraíble** (2)</span><span class="sxs-lookup"><span data-stu-id="79fc1-120">**Error - Removable Drive** (2)</span></span>
</dt> <dt>

<span data-ttu-id="79fc1-121">**Error: la unidad no es el directorio raíz** (3)</span><span class="sxs-lookup"><span data-stu-id="79fc1-121">**Error - Drive Not Root Directory** (3)</span></span>
</dt> <dt>

<span data-ttu-id="79fc1-122">**Error: unidad desconocida** (4)</span><span class="sxs-lookup"><span data-stu-id="79fc1-122">**Error - Unknown Drive** (4)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="79fc1-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79fc1-123">Remarks</span></span>

<span data-ttu-id="79fc1-124">Este método solo es aplicable a las instancias de disco lógico que representan un disco físico en el equipo.</span><span class="sxs-lookup"><span data-stu-id="79fc1-124">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="79fc1-125">Este método no es aplicable a las unidades lógicas asignadas.</span><span class="sxs-lookup"><span data-stu-id="79fc1-125">This method is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="79fc1-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="79fc1-126">Examples</span></span>

<span data-ttu-id="79fc1-127">Los siguientes ejemplos de VBScript y PowerShell programan Autochk.exe ejecutarse en la unidad C la próxima vez que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="79fc1-127">The following VBScript and PowerShell samples schedule Autochk.exe to run against drive C the next time the computer reboots.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ScheduleAutoChk(Array("C:")) 
```


```PowerShell

Invoke-WmiMethod -path win32_logicaldisk -Name ScheduleAutoChk -ArgumentList @(&quot;C:&quot;)
```





## <a name="requirements"></a><span data-ttu-id="79fc1-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79fc1-128">Requirements</span></span>



| <span data-ttu-id="79fc1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="79fc1-129">Requirement</span></span> | <span data-ttu-id="79fc1-130">Value</span><span class="sxs-lookup"><span data-stu-id="79fc1-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79fc1-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79fc1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="79fc1-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79fc1-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="79fc1-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79fc1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="79fc1-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79fc1-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79fc1-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="79fc1-135">Namespace</span></span><br/>                | <span data-ttu-id="79fc1-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="79fc1-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="79fc1-137">MOF</span><span class="sxs-lookup"><span data-stu-id="79fc1-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79fc1-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79fc1-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="79fc1-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79fc1-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79fc1-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79fc1-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79fc1-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="79fc1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79fc1-142">**LogicalDisk de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="79fc1-142">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> </dl>

 

