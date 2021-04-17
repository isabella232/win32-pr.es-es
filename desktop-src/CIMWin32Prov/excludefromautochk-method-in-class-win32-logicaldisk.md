---
description: Excluye los discos de la operación de AUTOCHK que se ejecutarán en el siguiente reinicio.
ms.assetid: 5df2bc3b-e149-4853-aa02-af4cb8af6da0
ms.tgt_platform: multiple
title: Método ExcludeFromAutochk de la clase Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ExcludeFromAutochk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c41d93111742e975490d97169c7e9147ba5fb1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659485"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="f6d75-103">Método ExcludeFromAutochk de la \_ clase Win32 LogicalDisk</span><span class="sxs-lookup"><span data-stu-id="f6d75-103">ExcludeFromAutochk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="f6d75-104">El método **ExcludeFromAutochk** excluye los discos de la operación **Autochk** que se va a ejecutar en el siguiente reinicio.</span><span class="sxs-lookup"><span data-stu-id="f6d75-104">The **ExcludeFromAutochk** method excludes disks from the **autochk** operation to be run at the next reboot.</span></span>

<span data-ttu-id="f6d75-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f6d75-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f6d75-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f6d75-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f6d75-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6d75-107">Syntax</span></span>


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a><span data-ttu-id="f6d75-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6d75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6d75-109">*LogicalDisk* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6d75-109">*LogicalDisk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6d75-110">Lista de unidades que deben excluirse de **Autochk** en el siguiente reinicio.</span><span class="sxs-lookup"><span data-stu-id="f6d75-110">List of drives that should be excluded from **autochk** at the next reboot.</span></span> <span data-ttu-id="f6d75-111">La sintaxis de la cadena se compone de la letra de unidad seguida de dos puntos para el disco lógico.</span><span class="sxs-lookup"><span data-stu-id="f6d75-111">The string syntax consists of the drive letter followed by a colon for the logical disk.</span></span>

<span data-ttu-id="f6d75-112">Ejemplo: "C:"</span><span class="sxs-lookup"><span data-stu-id="f6d75-112">Example: "C:"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6d75-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6d75-113">Return value</span></span>

<span data-ttu-id="f6d75-114">Devuelve un valor de 0 (cero) si no se produce ningún error.</span><span class="sxs-lookup"><span data-stu-id="f6d75-114">Returns a value of 0 (zero) when no error occurs.</span></span> <span data-ttu-id="f6d75-115">Los valores se muestran en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="f6d75-115">Values are listed in the following list.</span></span> <span data-ttu-id="f6d75-116">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f6d75-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f6d75-117">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f6d75-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f6d75-118">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="f6d75-118">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f6d75-119">**Error: unidad remota** (1)</span><span class="sxs-lookup"><span data-stu-id="f6d75-119">**Error - Remote Drive** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f6d75-120">**Error: unidad extraíble** (2)</span><span class="sxs-lookup"><span data-stu-id="f6d75-120">**Error - Removable Drive** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f6d75-121">**Error: la unidad no es el directorio raíz** (3)</span><span class="sxs-lookup"><span data-stu-id="f6d75-121">**Error - Drive Not Root Directory** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f6d75-122">**Error: unidad desconocida** (4)</span><span class="sxs-lookup"><span data-stu-id="f6d75-122">**Error - Unknown Drive** (4)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f6d75-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6d75-123">Remarks</span></span>

<span data-ttu-id="f6d75-124">Si no se excluye, **Autochk** se realiza en el disco cuando se establece el bit de integridad del disco.</span><span class="sxs-lookup"><span data-stu-id="f6d75-124">If not excluded, **autochk** is performed on the disk when the dirty bit is set for the disk.</span></span> <span data-ttu-id="f6d75-125">Tenga en cuenta que las llamadas para excluir discos no son acumulativas.</span><span class="sxs-lookup"><span data-stu-id="f6d75-125">Note that the calls to exclude disks are not cumulative.</span></span> <span data-ttu-id="f6d75-126">Si se realiza una llamada para excluir algunos discos, la nueva lista no se agrega a la lista de discos que ya están marcados para su exclusión.</span><span class="sxs-lookup"><span data-stu-id="f6d75-126">If a call is made to exclude some disks, then the new list is not added to the list of disks that are already marked for exclusion.</span></span> <span data-ttu-id="f6d75-127">La nueva lista de discos sobrescribe la lista anterior.</span><span class="sxs-lookup"><span data-stu-id="f6d75-127">The new list of disks overwrites the previous list.</span></span> <span data-ttu-id="f6d75-128">Este método solo es aplicable a las instancias de disco lógico que representan un disco físico en el equipo.</span><span class="sxs-lookup"><span data-stu-id="f6d75-128">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="f6d75-129">No es aplicable a las unidades lógicas asignadas.</span><span class="sxs-lookup"><span data-stu-id="f6d75-129">It is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="f6d75-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f6d75-130">Examples</span></span>

<span data-ttu-id="f6d75-131">El siguiente ejemplo de código de VBScript garantiza que Autochk.exe no se ejecutarán en la unidad C la próxima vez que se reinicie el equipo, incluso si se ha establecido el "bit de integridad" en la unidad C.</span><span class="sxs-lookup"><span data-stu-id="f6d75-131">The following VBScript code sample ensures that Autochk.exe will not run against drive C the next time the computer reboots, even if the "dirty bit" has been set on drive C.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ExcludeFromAutoChk(Array("C:")) 
```



## <a name="requirements"></a><span data-ttu-id="f6d75-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6d75-132">Requirements</span></span>



| <span data-ttu-id="f6d75-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6d75-133">Requirement</span></span> | <span data-ttu-id="f6d75-134">Value</span><span class="sxs-lookup"><span data-stu-id="f6d75-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6d75-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6d75-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f6d75-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6d75-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f6d75-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6d75-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f6d75-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6d75-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f6d75-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f6d75-139">Namespace</span></span><br/>                | <span data-ttu-id="f6d75-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f6d75-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f6d75-141">MOF</span><span class="sxs-lookup"><span data-stu-id="f6d75-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6d75-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6d75-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6d75-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6d75-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6d75-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6d75-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6d75-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6d75-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6d75-146">**LogicalDisk de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="f6d75-146">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="f6d75-147">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="f6d75-147">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

