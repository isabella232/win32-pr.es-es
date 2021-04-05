---
description: El método Remove del objeto SWbemPrivilegeSet elimina un privilegio de la colección.
ms.assetid: 4c0b6d49-262c-4840-955b-35b16b68f29f
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f277e291a4296253d7c0b1b11c694952ddc17ddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910277"
---
# <a name="swbemprivilegesetremove-method"></a><span data-ttu-id="3c90d-103">SWbemPrivilegeSet. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="3c90d-103">SWbemPrivilegeSet.Remove method</span></span>

<span data-ttu-id="3c90d-104">El método **Remove** del objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) elimina un privilegio de la colección.</span><span class="sxs-lookup"><span data-stu-id="3c90d-104">The **Remove** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object deletes a privilege from the collection.</span></span>

<span data-ttu-id="3c90d-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3c90d-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3c90d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c90d-106">Syntax</span></span>


```VB
SWbemPrivilegeSet.Remove( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a><span data-ttu-id="3c90d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c90d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c90d-108">*iPrivilege*</span><span class="sxs-lookup"><span data-stu-id="3c90d-108">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="3c90d-109">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3c90d-109">Required.</span></span> <span data-ttu-id="3c90d-110">Esta es una de las constantes de WMI del grupo [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="3c90d-110">This is one of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="3c90d-111">Estas constantes son esencialmente enteros que representan privilegios específicos.</span><span class="sxs-lookup"><span data-stu-id="3c90d-111">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="3c90d-112">Por ejemplo, para quitar el privilegio que le permite apagar un sistema de Windows, use la constante **wbemPrivilegeShutdown** o el equivalente numérico de 0x17.</span><span class="sxs-lookup"><span data-stu-id="3c90d-112">For example, to remove the privilege that allows you to shut down a Windows system, use the **wbemPrivilegeShutdown** constant or the numeric equivalent of 0x17.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c90d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c90d-113">Return value</span></span>

<span data-ttu-id="3c90d-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3c90d-114">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3c90d-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="3c90d-115">Error codes</span></span>

<span data-ttu-id="3c90d-116">Al completarse el método **Remove** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="3c90d-116">Upon completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="3c90d-117">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="3c90d-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="3c90d-118">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="3c90d-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="3c90d-119">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="3c90d-119">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="3c90d-120">El privilegio especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="3c90d-120">Specified privilege does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c90d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c90d-121">Requirements</span></span>



| <span data-ttu-id="3c90d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c90d-122">Requirement</span></span> | <span data-ttu-id="3c90d-123">Value</span><span class="sxs-lookup"><span data-stu-id="3c90d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c90d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c90d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3c90d-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c90d-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3c90d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c90d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3c90d-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c90d-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c90d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c90d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c90d-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c90d-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c90d-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3c90d-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="3c90d-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3c90d-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3c90d-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c90d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c90d-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c90d-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3c90d-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="3c90d-134">CLSID</span></span><br/>                    | <span data-ttu-id="3c90d-135">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="3c90d-135">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="3c90d-136">IID</span><span class="sxs-lookup"><span data-stu-id="3c90d-136">IID</span></span><br/>                      | <span data-ttu-id="3c90d-137">\_ISWBEMPRIVILEGESET IID</span><span class="sxs-lookup"><span data-stu-id="3c90d-137">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="3c90d-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c90d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c90d-139">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="3c90d-139">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="3c90d-140">**SWbemPrivilegeSet. Add**</span><span class="sxs-lookup"><span data-stu-id="3c90d-140">**SWbemPrivilegeSet.Add**</span></span>](swbemprivilegeset-add.md)
</dt> </dl>

 

 




