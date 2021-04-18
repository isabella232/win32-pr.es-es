---
description: Puede usar el método AddAsString del objeto SWbemPrivilegeSet para agregar un privilegio a una colección SWbemPrivilegeSet mediante una cadena de privilegios.
ms.assetid: 729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet. AddAsString (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b3a740141b14766080a09d01b36b5c0202351eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707262"
---
# <a name="swbemprivilegesetaddasstring-method"></a><span data-ttu-id="88734-103">SWbemPrivilegeSet. AddAsString, método</span><span class="sxs-lookup"><span data-stu-id="88734-103">SWbemPrivilegeSet.AddAsString method</span></span>

<span data-ttu-id="88734-104">Puede usar el método **AddAsString** del objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) para agregar un privilegio a una colección **SWbemPrivilegeSet** mediante una cadena de privilegios.</span><span class="sxs-lookup"><span data-stu-id="88734-104">You can use the **AddAsString** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object to add a privilege to an **SWbemPrivilegeSet** collection using a privilege string.</span></span> <span data-ttu-id="88734-105">Use este método para agregar un privilegio o para habilitar un privilegio para objetos [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="88734-105">Use this method to add a privilege or to enable a privilege for [**SWbemSecurity**](swbemsecurity.md) objects.</span></span> <span data-ttu-id="88734-106">Vea [ejecutar operaciones con privilegios mediante VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="88734-106">See [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="88734-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="88734-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="88734-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88734-108">Syntax</span></span>


```VB
objPrivilege = .AddAsString( _
  ByVal strPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a><span data-ttu-id="88734-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88734-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88734-110">*strPrivilege*</span><span class="sxs-lookup"><span data-stu-id="88734-110">*strPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="88734-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="88734-111">Required.</span></span> <span data-ttu-id="88734-112">Una de las cadenas de privilegios.</span><span class="sxs-lookup"><span data-stu-id="88734-112">One of the privilege strings.</span></span> <span data-ttu-id="88734-113">Para obtener una lista completa de estas cadenas y las constantes de WMI asociadas, consulte [**constantes de privilegios**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="88734-113">For a complete list of these strings and the associated WMI constants, see [**Privilege Constants**](privilege-constants.md).</span></span> <span data-ttu-id="88734-114">Cada cadena de privilegios representa un privilegio específico.</span><span class="sxs-lookup"><span data-stu-id="88734-114">Every privilege string represents a specific privilege.</span></span> <span data-ttu-id="88734-115">Por ejemplo, para agregar el privilegio que usa para apagar un equipo, use la cadena **SeShutdownPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="88734-115">For example, to add the privilege that use to shut down a computer system, use the **SeShutdownPrivilege** string.</span></span>

</dd> <dt>

<span data-ttu-id="88734-116">*bIsEnabled* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="88734-116">*bIsEnabled* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="88734-117">Valor booleano que habilita o deshabilita este privilegio.</span><span class="sxs-lookup"><span data-stu-id="88734-117">Boolean value that enables or disables this privilege.</span></span> <span data-ttu-id="88734-118">El valor predeterminado es **True**.</span><span class="sxs-lookup"><span data-stu-id="88734-118">The default value is **True**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88734-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88734-119">Return value</span></span>

<span data-ttu-id="88734-120">Si es correcto, este método devuelve un objeto [**SWbemPrivilege**](swbemprivilege.md) que representa el nuevo privilegio.</span><span class="sxs-lookup"><span data-stu-id="88734-120">If successful, this method returns an [**SWbemPrivilege**](swbemprivilege.md) object that represents the new privilege.</span></span> <span data-ttu-id="88734-121">De lo contrario, se devuelve un objeto null.</span><span class="sxs-lookup"><span data-stu-id="88734-121">Otherwise, a null object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="88734-122">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="88734-122">Error codes</span></span>

<span data-ttu-id="88734-123">Una vez finalizado el método **AddAsString** , el objeto **Err** puede contener el código de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="88734-123">Upon the completion of the **AddAsString** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="88734-124">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="88734-124">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="88734-125">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="88734-125">Unspecified error.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="88734-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="88734-126">Examples</span></span>

<span data-ttu-id="88734-127">En el siguiente ejemplo de código de VBScript se crea un nuevo puerto para un servidor de impresión mediante [**Win32 \_ TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport).</span><span class="sxs-lookup"><span data-stu-id="88734-127">The following VBScript code example creates a new port for a print server using [**Win32\_TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport).</span></span> <span data-ttu-id="88734-128">La **SeLoadDriverPrivilege** es necesaria para esta operación.</span><span class="sxs-lookup"><span data-stu-id="88734-128">The **SeLoadDriverPrivilege** is required for this operation.</span></span> <span data-ttu-id="88734-129">Vea [ejecutar operaciones con privilegios](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="88734-129">See [Executing Privileged Operations](executing-privileged-operations.md).</span></span>


```VB
Set objWMIService = GetObject("Winmgmts:")
objWMIService.Security_.Privileges. _
    AddAsString "SeLoadDriverPrivilege", True
Set objNewPort = objWMIService.Get _
    ("Win32_TCPIPPrinterPort").SpawnInstance_
objNewPort.Name = "IP_111.222.111.11"
objNewPort.Protocol = 1
objNewPort.HostAddress = "111.222.111.11"
objNewPort.PortNumber = "9999"
objNewPort.SNMPEnabled = False
objNewPort.Put_
```



<span data-ttu-id="88734-130">Un ejemplo de código que usa este método también se describe en el tema [**SWbemPrivilegeSet**](swbemprivilegeset.md) .</span><span class="sxs-lookup"><span data-stu-id="88734-130">A code example using this method is also described in the [**SWbemPrivilegeSet**](swbemprivilegeset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="88734-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88734-131">Requirements</span></span>



| <span data-ttu-id="88734-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="88734-132">Requirement</span></span> | <span data-ttu-id="88734-133">Value</span><span class="sxs-lookup"><span data-stu-id="88734-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88734-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88734-134">Minimum supported client</span></span><br/> | <span data-ttu-id="88734-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88734-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88734-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88734-136">Minimum supported server</span></span><br/> | <span data-ttu-id="88734-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88734-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88734-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88734-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="88734-139"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="88734-139"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="88734-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="88734-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="88734-141"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="88734-141"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="88734-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88734-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88734-143"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88734-143"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="88734-144">CLSID</span><span class="sxs-lookup"><span data-stu-id="88734-144">CLSID</span></span><br/>                    | <span data-ttu-id="88734-145">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="88734-145">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="88734-146">IID</span><span class="sxs-lookup"><span data-stu-id="88734-146">IID</span></span><br/>                      | <span data-ttu-id="88734-147">\_ISWBEMPRIVILEGESET IID</span><span class="sxs-lookup"><span data-stu-id="88734-147">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="88734-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="88734-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88734-149">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="88734-149">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="88734-150">**SWbemPrivilegeSet. Add**</span><span class="sxs-lookup"><span data-stu-id="88734-150">**SWbemPrivilegeSet.Add**</span></span>](swbemprivilegeset-add.md)
</dt> <dt>

[<span data-ttu-id="88734-151">**SWbemPrivilegeSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="88734-151">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> <dt>

[<span data-ttu-id="88734-152">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="88734-152">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="88734-153">**Constantes de privilegio**</span><span class="sxs-lookup"><span data-stu-id="88734-153">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> <dt>

[<span data-ttu-id="88734-154">Ejecutar operaciones con privilegios</span><span class="sxs-lookup"><span data-stu-id="88734-154">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="88734-155">Ejecutar operaciones con privilegios mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="88734-155">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

