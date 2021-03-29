---
description: Elimina un nombre de recurso compartido de la lista de recursos compartidos de un servidor y desconecta las conexiones al recurso compartido.
ms.assetid: 175f9c0e-0017-4a86-8e05-ad78e2c93c11
ms.tgt_platform: multiple
title: Método Delete de la clase Win32_Share
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
ms.openlocfilehash: 2048ba9dac91b139888f27c037d64849de8a4ee8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153148"
---
# <a name="delete-method-of-the-win32_share-class"></a><span data-ttu-id="1b50e-103">Método Delete de la \_ clase de recurso compartido Win32</span><span class="sxs-lookup"><span data-stu-id="1b50e-103">Delete method of the Win32\_Share class</span></span>

<span data-ttu-id="1b50e-104">El método **Delete** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) elimina un nombre de recurso compartido de la lista de recursos compartidos de un servidor y desconecta las conexiones al recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="1b50e-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes a share name from a server's list of shared resources, disconnecting connections to the shared resource.</span></span>

<span data-ttu-id="1b50e-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="1b50e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1b50e-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1b50e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b50e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b50e-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="1b50e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b50e-108">Parameters</span></span>

<span data-ttu-id="1b50e-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1b50e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1b50e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b50e-110">Return value</span></span>

<span data-ttu-id="1b50e-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="1b50e-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="1b50e-112">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1b50e-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1b50e-113">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1b50e-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1b50e-114">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="1b50e-114">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1b50e-115">**Acceso denegado** (2)</span><span class="sxs-lookup"><span data-stu-id="1b50e-115">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1b50e-116">**Error desconocido** (8)</span><span class="sxs-lookup"><span data-stu-id="1b50e-116">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1b50e-117">**Nombre no válido** (9)</span><span class="sxs-lookup"><span data-stu-id="1b50e-117">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1b50e-118">**Nivel no válido** (10)</span><span class="sxs-lookup"><span data-stu-id="1b50e-118">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1b50e-119">**Parámetro no válido** (21)</span><span class="sxs-lookup"><span data-stu-id="1b50e-119">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="1b50e-120">**Recurso compartido duplicado** (22)</span><span class="sxs-lookup"><span data-stu-id="1b50e-120">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="1b50e-121">**Ruta de acceso redirigida** (23)</span><span class="sxs-lookup"><span data-stu-id="1b50e-121">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="1b50e-122">**Dispositivo o directorio desconocido** (24)</span><span class="sxs-lookup"><span data-stu-id="1b50e-122">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="1b50e-123">**No se encontró el nombre de red** (25)</span><span class="sxs-lookup"><span data-stu-id="1b50e-123">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="1b50e-124">**Otro** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="1b50e-124">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="1b50e-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b50e-125">Remarks</span></span>

<span data-ttu-id="1b50e-126">El método **Delete** es un método de objeto y se usa en una instancia de una clase.</span><span class="sxs-lookup"><span data-stu-id="1b50e-126">The **Delete** method is an object method and is used on an instance of a class.</span></span>

<span data-ttu-id="1b50e-127">Solo los miembros del grupo local Administradores o operadores de cuenta, o los que tengan la pertenencia a un grupo de operador de servidor o de comunicación pueden ejecutar correctamente el método.</span><span class="sxs-lookup"><span data-stu-id="1b50e-127">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute the method.</span></span> <span data-ttu-id="1b50e-128">El operador Print solo puede eliminar colas de impresión.</span><span class="sxs-lookup"><span data-stu-id="1b50e-128">The Print operator can delete only printer queues.</span></span> <span data-ttu-id="1b50e-129">El operador de comunicación solo puede eliminar colas de dispositivos de comunicación.</span><span class="sxs-lookup"><span data-stu-id="1b50e-129">The Communication operator can delete only communication-device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="1b50e-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1b50e-130">Examples</span></span>

<span data-ttu-id="1b50e-131">En el siguiente ejemplo de código de VBScript se elimina el recurso compartido especificado.</span><span class="sxs-lookup"><span data-stu-id="1b50e-131">The following VBScript code sample deletes the specified share.</span></span>


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



<span data-ttu-id="1b50e-132">En el siguiente ejemplo de código de PowerShell se eliminan los recursos compartidos en blanco.</span><span class="sxs-lookup"><span data-stu-id="1b50e-132">The following PowerShell code sample deletes blank shares.</span></span>


```PowerShell
$Shares = Get-WMIObject Win32_Share | Where {$_.Name -eq ""}

Foreach ($Share in $Shares) {
   $Share.Delete()
}
"{0} blank shares found and removed" -f $shares.count
```



## <a name="requirements"></a><span data-ttu-id="1b50e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b50e-133">Requirements</span></span>



| <span data-ttu-id="1b50e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b50e-134">Requirement</span></span> | <span data-ttu-id="1b50e-135">Value</span><span class="sxs-lookup"><span data-stu-id="1b50e-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b50e-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b50e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1b50e-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b50e-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b50e-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b50e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1b50e-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b50e-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b50e-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1b50e-140">Namespace</span></span><br/>                | <span data-ttu-id="1b50e-141">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1b50e-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1b50e-142">MOF</span><span class="sxs-lookup"><span data-stu-id="1b50e-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b50e-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b50e-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b50e-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1b50e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b50e-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b50e-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b50e-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b50e-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="1b50e-147">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1b50e-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1b50e-148">**\_Recurso compartido de Win32**</span><span class="sxs-lookup"><span data-stu-id="1b50e-148">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

