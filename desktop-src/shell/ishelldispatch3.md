---
description: Extiende el objeto IShellDispatch2.
ms.assetid: 89d0aa4d-844d-497d-82bb-bcc2bcf9c78b
title: Objeto IShellDispatch3 (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch3
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 501b1396bd08ad8fd06f25da9b7030d4ce28d1e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984663"
---
# <a name="ishelldispatch3-object"></a><span data-ttu-id="021c4-103">Objeto IShellDispatch3</span><span class="sxs-lookup"><span data-stu-id="021c4-103">IShellDispatch3 object</span></span>

<span data-ttu-id="021c4-104">Extiende el objeto [**IShellDispatch2**](ishelldispatch2-object.md) .</span><span class="sxs-lookup"><span data-stu-id="021c4-104">Extends the [**IShellDispatch2**](ishelldispatch2-object.md) object.</span></span> <span data-ttu-id="021c4-105">**IShellDispatch3** admite un nuevo método además de las propiedades y los métodos admitidos por **IShellDispatch2**.</span><span class="sxs-lookup"><span data-stu-id="021c4-105">**IShellDispatch3** supports one new method in addition to the properties and methods supported by **IShellDispatch2**.</span></span>

> [!Note]  
> <span data-ttu-id="021c4-106">**IShellDispatch3** se implementa y se obtiene acceso a él a través del objeto de [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="021c4-106">**IShellDispatch3** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="021c4-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="021c4-107">Members</span></span>

<span data-ttu-id="021c4-108">El objeto **IShellDispatch3** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="021c4-108">The **IShellDispatch3** object has these types of members:</span></span>

-   [<span data-ttu-id="021c4-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="021c4-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="021c4-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="021c4-110">Methods</span></span>

<span data-ttu-id="021c4-111">El objeto **IShellDispatch3** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="021c4-111">The **IShellDispatch3** object has these methods.</span></span>



| <span data-ttu-id="021c4-112">Método</span><span class="sxs-lookup"><span data-stu-id="021c4-112">Method</span></span>                                             | <span data-ttu-id="021c4-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="021c4-113">Description</span></span>                                                  |
|:---------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="021c4-114">**AddToRecent**</span><span class="sxs-lookup"><span data-stu-id="021c4-114">**AddToRecent**</span></span>](ishelldispatch3-addtorecent.md) | <span data-ttu-id="021c4-115">Agrega un archivo a la lista de elementos usados más recientemente (MRU).</span><span class="sxs-lookup"><span data-stu-id="021c4-115">Adds a file to the most recently used (MRU) list.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="021c4-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="021c4-116">Remarks</span></span>

<span data-ttu-id="021c4-117">Para obtener una explicación de los servicios de Windows, consulte la documentación de los [servicios](../services/services.md) .</span><span class="sxs-lookup"><span data-stu-id="021c4-117">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="021c4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="021c4-118">Requirements</span></span>



| <span data-ttu-id="021c4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="021c4-119">Requirement</span></span> | <span data-ttu-id="021c4-120">Value</span><span class="sxs-lookup"><span data-stu-id="021c4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="021c4-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="021c4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="021c4-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="021c4-122">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="021c4-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="021c4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="021c4-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="021c4-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="021c4-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="021c4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="021c4-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="021c4-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="021c4-127">IDL</span><span class="sxs-lookup"><span data-stu-id="021c4-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="021c4-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="021c4-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="021c4-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="021c4-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="021c4-130"><dt>Shell32.dll (versión 6,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="021c4-130"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="021c4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="021c4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="021c4-132">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="021c4-132">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="021c4-133">**Objeto de Shell**</span><span class="sxs-lookup"><span data-stu-id="021c4-133">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="021c4-134">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="021c4-134">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="021c4-135">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="021c4-135">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> </dl>

 

 
