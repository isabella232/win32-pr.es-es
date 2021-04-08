---
description: El método Item del objeto SWbemPrivilegeSet devuelve un objeto SWbemPrivilege de la colección. El método Item es el método predeterminado de un objeto SWbemPrivilegeSet.
ms.assetid: 93a35e65-99ee-40da-9415-4151ac635091
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7ea37ae758ec599198fc35a1fd2a4b89ff25a087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908549"
---
# <a name="swbemprivilegesetitem-method"></a><span data-ttu-id="cb81c-104">SWbemPrivilegeSet. Item (método)</span><span class="sxs-lookup"><span data-stu-id="cb81c-104">SWbemPrivilegeSet.Item method</span></span>

<span data-ttu-id="cb81c-105">El método **Item** del objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) devuelve un objeto [**SWbemPrivilege**](swbemprivilege.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="cb81c-105">The **Item** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object returns an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span> <span data-ttu-id="cb81c-106">El método **Item** es el método predeterminado de un objeto **SWbemPrivilegeSet** .</span><span class="sxs-lookup"><span data-stu-id="cb81c-106">The **Item** method is the default method of an **SWbemPrivilegeSet** object.</span></span>

<span data-ttu-id="cb81c-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="cb81c-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cb81c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb81c-108">Syntax</span></span>


```VB
objPrivilege = .Item( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a><span data-ttu-id="cb81c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb81c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb81c-110">*iPrivilege*</span><span class="sxs-lookup"><span data-stu-id="cb81c-110">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="cb81c-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cb81c-111">Required.</span></span> <span data-ttu-id="cb81c-112">Una de las constantes de WMI del grupo [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="cb81c-112">One of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="cb81c-113">Estas constantes son esencialmente enteros que representan privilegios específicos.</span><span class="sxs-lookup"><span data-stu-id="cb81c-113">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="cb81c-114">Por ejemplo, para obtener el privilegio que le permite apagar un sistema de Windows, use la constante **wbemPrivilegeShutdown** o el equivalente numérico de 23 (0x17).</span><span class="sxs-lookup"><span data-stu-id="cb81c-114">For example, to get the privilege that allows you to shut down a Windows system, use the **wbemPrivilegeShutdown** constant or the numeric equivalent of 23 (0x17).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb81c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb81c-115">Return value</span></span>

<span data-ttu-id="cb81c-116">Si se realiza correctamente, se devuelve el objeto [**SWbemPrivilege**](swbemprivilege.md) solicitado.</span><span class="sxs-lookup"><span data-stu-id="cb81c-116">If successful, the requested [**SWbemPrivilege**](swbemprivilege.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cb81c-117">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="cb81c-117">Error codes</span></span>

<span data-ttu-id="cb81c-118">Una vez finalizado el método **Item** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="cb81c-118">Upon the completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="cb81c-119">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="cb81c-119">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="cb81c-120">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="cb81c-120">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="cb81c-121">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="cb81c-121">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="cb81c-122">El privilegio especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="cb81c-122">Specified privilege does not exist.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="cb81c-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cb81c-123">Examples</span></span>

<span data-ttu-id="cb81c-124">En el siguiente ejemplo de código de VBScript se usa el método **Item**</span><span class="sxs-lookup"><span data-stu-id="cb81c-124">The following VBScript code example uses the **Item** method</span></span>


```VB
strComputer ="."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")
Set colServices = objWMIService.ExecQuery( _
    "Select * from Win32_Service")
For Each objService In colServices
    WScript.Echo objService.Properties_.Item("Caption")
Next
```



## <a name="requirements"></a><span data-ttu-id="cb81c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb81c-125">Requirements</span></span>



| <span data-ttu-id="cb81c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb81c-126">Requirement</span></span> | <span data-ttu-id="cb81c-127">Value</span><span class="sxs-lookup"><span data-stu-id="cb81c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb81c-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb81c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cb81c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb81c-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cb81c-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb81c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cb81c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb81c-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cb81c-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb81c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb81c-133"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb81c-133"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb81c-134">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="cb81c-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="cb81c-135"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cb81c-135"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cb81c-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb81c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb81c-137"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb81c-137"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cb81c-138">CLSID</span><span class="sxs-lookup"><span data-stu-id="cb81c-138">CLSID</span></span><br/>                    | <span data-ttu-id="cb81c-139">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="cb81c-139">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="cb81c-140">IID</span><span class="sxs-lookup"><span data-stu-id="cb81c-140">IID</span></span><br/>                      | <span data-ttu-id="cb81c-141">\_ISWBEMPRIVILEGESET IID</span><span class="sxs-lookup"><span data-stu-id="cb81c-141">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="cb81c-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb81c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb81c-143">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="cb81c-143">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="cb81c-144">Ejecutar operaciones con privilegios</span><span class="sxs-lookup"><span data-stu-id="cb81c-144">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="cb81c-145">**SWbemPrivilege**</span><span class="sxs-lookup"><span data-stu-id="cb81c-145">**SWbemPrivilege**</span></span>](swbemprivilege.md)
</dt> </dl>

 

 




