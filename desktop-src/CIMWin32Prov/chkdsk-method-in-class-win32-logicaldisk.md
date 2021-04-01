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
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="2eb20-103">Método CHKDSK de la \_ clase Win32 LogicalDisk</span><span class="sxs-lookup"><span data-stu-id="2eb20-103">Chkdsk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="2eb20-104">El método de instancia **CHKDSK** invoca la operación **CHKDSK** en el disco.</span><span class="sxs-lookup"><span data-stu-id="2eb20-104">The **Chkdsk** instance method invokes the **chkdsk** operation on the disk.</span></span>

<span data-ttu-id="2eb20-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="2eb20-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2eb20-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2eb20-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2eb20-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2eb20-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="2eb20-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2eb20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eb20-109">*FixErrors* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2eb20-109">*FixErrors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb20-110">Indica qué se debe hacer con los errores encontrados en el disco.</span><span class="sxs-lookup"><span data-stu-id="2eb20-110">Indicates what should be done to errors found on the disk.</span></span> <span data-ttu-id="2eb20-111">Si **es true**, se corrigen los errores.</span><span class="sxs-lookup"><span data-stu-id="2eb20-111">If **true**, then errors are fixed.</span></span> <span data-ttu-id="2eb20-112">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="2eb20-112">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="2eb20-113">*VigorousIndexCheck* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2eb20-113">*VigorousIndexCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb20-114">Si **es true**, se debe realizar una comprobación menos exhaustiva de entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="2eb20-114">If **true**, a less vigorous check of index entries should be performed.</span></span> <span data-ttu-id="2eb20-115">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="2eb20-115">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="2eb20-116">*SkipFolderCycle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2eb20-116">*SkipFolderCycle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb20-117">Si **es true**, se debe omitir la comprobación del ciclo de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="2eb20-117">If **true**, the folder cycle checking should be skipped.</span></span> <span data-ttu-id="2eb20-118">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="2eb20-118">The default is **true**.</span></span>

</dd> <dt>

<span data-ttu-id="2eb20-119">*ForceDismount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2eb20-119">*ForceDismount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb20-120">Si **es true**, se debe forzar el desmontaje de la unidad antes de la comprobación.</span><span class="sxs-lookup"><span data-stu-id="2eb20-120">If **true**, the drive should be forced to dismount before checking.</span></span> <span data-ttu-id="2eb20-121">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="2eb20-121">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="2eb20-122">*RecoverBadSectors* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2eb20-122">*RecoverBadSectors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb20-123">Si **es true**, se deben encontrar los sectores dañados y se debe recuperar la información legible de estos sectores.</span><span class="sxs-lookup"><span data-stu-id="2eb20-123">If **true**, the bad sectors should be located and the readable information should be recovered from these sectors.</span></span> <span data-ttu-id="2eb20-124">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="2eb20-124">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="2eb20-125">*OKToRunAtBootUp* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2eb20-125">*OKToRunAtBootUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb20-126">Si es **true**, la operación **CHKDSK** debe realizarse en el próximo arranque, en caso de que no se pueda realizar la operación porque el disco está bloqueado en el momento en que se llama a este método.</span><span class="sxs-lookup"><span data-stu-id="2eb20-126">If **true**, the **chkdsk** operation should be performed at next boot up time, in case the operation could not be performed because the disk is locked at time this method is called.</span></span> <span data-ttu-id="2eb20-127">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="2eb20-127">The default is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eb20-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2eb20-128">Return value</span></span>

<span data-ttu-id="2eb20-129">Devuelve un valor de 0 (cero) si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="2eb20-129">Returns a value of 0 (zero) if successful.</span></span> <span data-ttu-id="2eb20-130">Otros valores se muestran en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="2eb20-130">Other values are listed in the following list.</span></span> <span data-ttu-id="2eb20-131">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2eb20-131">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2eb20-132">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2eb20-132">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2eb20-133">**Correcto: CHKDSK completado**</span><span class="sxs-lookup"><span data-stu-id="2eb20-133">**Success - Chkdsk completed**</span></span>
</dt> <dd>

<span data-ttu-id="2eb20-134">0</span><span class="sxs-lookup"><span data-stu-id="2eb20-134">0</span></span>

<span data-ttu-id="2eb20-135">Correcto: [**CHKDSK**](chkdsk-method-in-class-win32-logicaldisk.md) completado</span><span class="sxs-lookup"><span data-stu-id="2eb20-135">Success - [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) Completed</span></span>

</dd> <dt>

<span data-ttu-id="2eb20-136">**Correcto: bloqueado y CHKDSK programado en el reinicio**</span><span class="sxs-lookup"><span data-stu-id="2eb20-136">**Success - Locked and chkdsk scheduled on reboot**</span></span>
</dt> <dd>

<span data-ttu-id="2eb20-137">1</span><span class="sxs-lookup"><span data-stu-id="2eb20-137">1</span></span>

</dd> <dt>

<span data-ttu-id="2eb20-138">**Error: sistema de archivos desconocido**</span><span class="sxs-lookup"><span data-stu-id="2eb20-138">**Failure - Unknown file system**</span></span>
</dt> <dd>

<span data-ttu-id="2eb20-139">2</span><span class="sxs-lookup"><span data-stu-id="2eb20-139">2</span></span>

</dd> <dt>

<span data-ttu-id="2eb20-140">**Error: error desconocido**</span><span class="sxs-lookup"><span data-stu-id="2eb20-140">**Failure - Unknown error**</span></span>
</dt> <dd>

<span data-ttu-id="2eb20-141">3</span><span class="sxs-lookup"><span data-stu-id="2eb20-141">3</span></span>

</dd> <dt>

<span data-ttu-id="2eb20-142">**Error: sistema de archivos no admitido**</span><span class="sxs-lookup"><span data-stu-id="2eb20-142">**Failure - Unsupported File System**</span></span>
</dt> <dd>

<span data-ttu-id="2eb20-143">4</span><span class="sxs-lookup"><span data-stu-id="2eb20-143">4</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2eb20-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2eb20-144">Remarks</span></span>

<span data-ttu-id="2eb20-145">Este método solo es aplicable a las instancias de disco lógico que representan un disco físico en el equipo.</span><span class="sxs-lookup"><span data-stu-id="2eb20-145">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="2eb20-146">No es aplicable a las unidades lógicas asignadas.</span><span class="sxs-lookup"><span data-stu-id="2eb20-146">It is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="2eb20-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2eb20-147">Examples</span></span>

<span data-ttu-id="2eb20-148">El[bit de integridad de CHKDSK está establecido en un ejemplo de código de PowerShell de servidor](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) examina el sistema remoto y devuelve true o false si se ha establecido la marca chkdsk/f.</span><span class="sxs-lookup"><span data-stu-id="2eb20-148">The[Is CHKDSK Dirty Bit Set on a server](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) PowerShell code sample examines the remote system and returns a true or false if the chkdsk /f flag was set.</span></span>

<span data-ttu-id="2eb20-149">En el ejemplo de código de PowerShell de [disco remoto](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) se inicia o programa el disco de examen de forma remota.</span><span class="sxs-lookup"><span data-stu-id="2eb20-149">The [Remotely scan disk](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) PowerShell code sample remotely starts or schedules Scan Disk.</span></span>

<span data-ttu-id="2eb20-150">El siguiente ejemplo de código de VBScript se ejecuta ChkDsk.exe en la unidad D de un equipo.</span><span class="sxs-lookup"><span data-stu-id="2eb20-150">The following VBScript code sample Runs ChkDsk.exe against drive D on a computer.</span></span>


```VB
Const FIX_ERRORS = True 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk.DeviceID='D:'") 
 
errReturn = objDisk.ChkDsk(FIX_ERRORS) 
```



## <a name="requirements"></a><span data-ttu-id="2eb20-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2eb20-151">Requirements</span></span>



| <span data-ttu-id="2eb20-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eb20-152">Requirement</span></span> | <span data-ttu-id="2eb20-153">Value</span><span class="sxs-lookup"><span data-stu-id="2eb20-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb20-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2eb20-154">Minimum supported client</span></span><br/> | <span data-ttu-id="2eb20-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2eb20-155">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2eb20-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2eb20-156">Minimum supported server</span></span><br/> | <span data-ttu-id="2eb20-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2eb20-157">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2eb20-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2eb20-158">Namespace</span></span><br/>                | <span data-ttu-id="2eb20-159">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2eb20-159">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2eb20-160">MOF</span><span class="sxs-lookup"><span data-stu-id="2eb20-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2eb20-161"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2eb20-161"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2eb20-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2eb20-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2eb20-163"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2eb20-163"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eb20-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="2eb20-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb20-165">**LogicalDisk de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="2eb20-165">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="2eb20-166">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="2eb20-166">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

