---
description: El método DeleteAll del objeto SWbemPrivilegeSet quita todos los privilegios de la colección, con lo que se vacía.
ms.assetid: 368caa14-1c53-4090-8569-97ea743905de
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet. DeleteAll (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 382382b0c22c029f41c9ab33fb959287e5222d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697594"
---
# <a name="swbemprivilegesetdeleteall-method"></a><span data-ttu-id="e30a6-103">SWbemPrivilegeSet. DeleteAll, método</span><span class="sxs-lookup"><span data-stu-id="e30a6-103">SWbemPrivilegeSet.DeleteAll method</span></span>

<span data-ttu-id="e30a6-104">El método **DeleteAll** del objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) quita todos los privilegios de la colección, con lo que se vacía.</span><span class="sxs-lookup"><span data-stu-id="e30a6-104">The **DeleteAll** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object removes all privileges from the collection, thus emptying it.</span></span>

## <a name="syntax"></a><span data-ttu-id="e30a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e30a6-105">Syntax</span></span>


```VB
SWbemPrivilegeSet.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="e30a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e30a6-106">Parameters</span></span>

<span data-ttu-id="e30a6-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e30a6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e30a6-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e30a6-108">Return value</span></span>

<span data-ttu-id="e30a6-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e30a6-109">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e30a6-110">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e30a6-110">Error codes</span></span>

<span data-ttu-id="e30a6-111">Tras completar el método **DeleteAll** , el objeto **Err** puede contener el código de error siguiente.</span><span class="sxs-lookup"><span data-stu-id="e30a6-111">Upon the completion of the **DeleteAll** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="e30a6-112">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="e30a6-112">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="e30a6-113">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="e30a6-113">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e30a6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e30a6-114">Requirements</span></span>



| <span data-ttu-id="e30a6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e30a6-115">Requirement</span></span> | <span data-ttu-id="e30a6-116">Value</span><span class="sxs-lookup"><span data-stu-id="e30a6-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e30a6-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e30a6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e30a6-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e30a6-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e30a6-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e30a6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e30a6-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e30a6-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e30a6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e30a6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e30a6-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e30a6-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e30a6-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e30a6-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="e30a6-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e30a6-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e30a6-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e30a6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e30a6-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e30a6-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e30a6-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="e30a6-127">CLSID</span></span><br/>                    | <span data-ttu-id="e30a6-128">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="e30a6-128">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="e30a6-129">IID</span><span class="sxs-lookup"><span data-stu-id="e30a6-129">IID</span></span><br/>                      | <span data-ttu-id="e30a6-130">\_ISWBEMPRIVILEGESET IID</span><span class="sxs-lookup"><span data-stu-id="e30a6-130">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="e30a6-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e30a6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e30a6-132">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="e30a6-132">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="e30a6-133">Ejecutar operaciones con privilegios</span><span class="sxs-lookup"><span data-stu-id="e30a6-133">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="e30a6-134">**SWbemPrivilegeSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="e30a6-134">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> </dl>

 

 




