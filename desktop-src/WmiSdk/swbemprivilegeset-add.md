---
description: El método Add del objeto SWbemPrivilegeSet agrega un objeto SWbemPrivilege a la colección SWbemPrivilegeSet. Si ya existe un privilegio con el mismo nombre en la colección, se reemplaza.
ms.assetid: 7d44193f-60e1-4e83-8640-31d8df509d98
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 080b9d3e3ab6dbfc0ed8afc8ac0476981b7c26e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082389"
---
# <a name="swbemprivilegesetadd-method"></a><span data-ttu-id="4758f-104">SWbemPrivilegeSet. Add (método)</span><span class="sxs-lookup"><span data-stu-id="4758f-104">SWbemPrivilegeSet.Add method</span></span>

<span data-ttu-id="4758f-105">El método **Add** del objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) agrega un objeto [**SWbemPrivilege**](swbemprivilege.md) a la colección **SWbemPrivilegeSet** .</span><span class="sxs-lookup"><span data-stu-id="4758f-105">The **Add** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection.</span></span> <span data-ttu-id="4758f-106">Si ya existe un privilegio con el mismo nombre en la colección, se reemplaza.</span><span class="sxs-lookup"><span data-stu-id="4758f-106">If a privilege with the same name already exists in the collection, it is replaced.</span></span>

<span data-ttu-id="4758f-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4758f-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4758f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4758f-108">Syntax</span></span>


```VB
objPrivilege = .Add( _
  ByVal iPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4758f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4758f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4758f-110">*iPrivilege*</span><span class="sxs-lookup"><span data-stu-id="4758f-110">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="4758f-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4758f-111">Required.</span></span> <span data-ttu-id="4758f-112">Una de las constantes de WMI del grupo [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="4758f-112">One of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="4758f-113">Estas constantes son esencialmente enteros que representan privilegios específicos.</span><span class="sxs-lookup"><span data-stu-id="4758f-113">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="4758f-114">Por ejemplo, para agregar el privilegio que le permite apagar un equipo, use la constante **wbemPrivilegeShutdown** .</span><span class="sxs-lookup"><span data-stu-id="4758f-114">For example, to add the privilege that allows you to shut down a computer system, use the **wbemPrivilegeShutdown** constant.</span></span> <span data-ttu-id="4758f-115">En un script, debe usar el equivalente numérico de 23 (0x17).</span><span class="sxs-lookup"><span data-stu-id="4758f-115">In a script, you must use the numeric equivalent of 23 (0x17).</span></span> <span data-ttu-id="4758f-116">Para obtener una lista completa de estas constantes y las cadenas de privilegios asociadas, consulte [**constantes**](privilege-constants.md)de privilegios.</span><span class="sxs-lookup"><span data-stu-id="4758f-116">For a complete list of these constants and the associated privilege strings, see [**Privilege Constants**](privilege-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="4758f-117">*bIsEnabled* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="4758f-117">*bIsEnabled* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4758f-118">Valor booleano que habilita o deshabilita este privilegio.</span><span class="sxs-lookup"><span data-stu-id="4758f-118">Boolean value that enables or disables this privilege.</span></span> <span data-ttu-id="4758f-119">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="4758f-119">The default value is **TRUE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4758f-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4758f-120">Return value</span></span>

<span data-ttu-id="4758f-121">Si se realiza correctamente, el método devuelve un objeto [**SWbemPrivilege**](swbemprivilege.md) que representa el nuevo privilegio.</span><span class="sxs-lookup"><span data-stu-id="4758f-121">If successful, the method returns an [**SWbemPrivilege**](swbemprivilege.md) object that represents the new privilege.</span></span> <span data-ttu-id="4758f-122">De lo contrario, se devuelve un objeto null.</span><span class="sxs-lookup"><span data-stu-id="4758f-122">Otherwise, a null object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4758f-123">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="4758f-123">Error codes</span></span>

<span data-ttu-id="4758f-124">Una vez finalizado el método **Add** , el objeto **Err** puede contener el código de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="4758f-124">Upon the completion of the **Add** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="4758f-125">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="4758f-125">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="4758f-126">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="4758f-126">Unspecified error.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="4758f-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4758f-127">Examples</span></span>

<span data-ttu-id="4758f-128">Un ejemplo de código que usa este método se describe en el tema [**SWbemPrivilegeSet**](swbemprivilegeset.md) .</span><span class="sxs-lookup"><span data-stu-id="4758f-128">A code example using this method is described in the [**SWbemPrivilegeSet**](swbemprivilegeset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="4758f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4758f-129">Requirements</span></span>



| <span data-ttu-id="4758f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4758f-130">Requirement</span></span> | <span data-ttu-id="4758f-131">Value</span><span class="sxs-lookup"><span data-stu-id="4758f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4758f-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4758f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4758f-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4758f-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4758f-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4758f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4758f-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4758f-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4758f-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4758f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4758f-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4758f-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4758f-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4758f-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="4758f-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4758f-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4758f-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4758f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4758f-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4758f-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4758f-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="4758f-142">CLSID</span></span><br/>                    | <span data-ttu-id="4758f-143">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="4758f-143">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="4758f-144">IID</span><span class="sxs-lookup"><span data-stu-id="4758f-144">IID</span></span><br/>                      | <span data-ttu-id="4758f-145">\_ISWBEMPRIVILEGESET IID</span><span class="sxs-lookup"><span data-stu-id="4758f-145">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="4758f-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="4758f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4758f-147">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="4758f-147">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="4758f-148">Ejecutar operaciones con privilegios</span><span class="sxs-lookup"><span data-stu-id="4758f-148">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="4758f-149">Ejecutar operaciones con privilegios mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="4758f-149">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="4758f-150">**SWbemPrivilegeSet.AddAsString**</span><span class="sxs-lookup"><span data-stu-id="4758f-150">**SWbemPrivilegeSet.AddAsString**</span></span>](swbemprivilegeset-addasstring.md)
</dt> <dt>

[<span data-ttu-id="4758f-151">**SWbemPrivilegeSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="4758f-151">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> <dt>

[<span data-ttu-id="4758f-152">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="4758f-152">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="4758f-153">**Constantes de privilegio**</span><span class="sxs-lookup"><span data-stu-id="4758f-153">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 




