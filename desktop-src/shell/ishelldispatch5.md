---
description: Extiende el objeto IShellDispatch4.
title: Objeto IShellDispatch5 (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch5
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9170340a-0f11-4ec9-877d-fb7fef9888b2
ms.openlocfilehash: cbf3e960d7bfb9cd15411142cc036a21a9995ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984643"
---
# <a name="ishelldispatch5-object"></a><span data-ttu-id="5f2ab-103">Objeto IShellDispatch5</span><span class="sxs-lookup"><span data-stu-id="5f2ab-103">IShellDispatch5 object</span></span>

<span data-ttu-id="5f2ab-104">Extiende el objeto [**IShellDispatch4**](ishelldispatch4.md) .</span><span class="sxs-lookup"><span data-stu-id="5f2ab-104">Extends the [**IShellDispatch4**](ishelldispatch4.md) object.</span></span> <span data-ttu-id="5f2ab-105">Además de las propiedades y los métodos admitidos por **IShellDispatch4**, **IShellDispatch5** agrega un método que muestra ventanas abiertas en una pila 3D.</span><span class="sxs-lookup"><span data-stu-id="5f2ab-105">In addition to the properties and methods supported by **IShellDispatch4**, **IShellDispatch5** adds a method that displays open windows in a 3D stack.</span></span>

> [!Note]  
> <span data-ttu-id="5f2ab-106">**IShellDispatch5** se implementa y se obtiene acceso a él a través del objeto de [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="5f2ab-106">**IShellDispatch5** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="5f2ab-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5f2ab-107">Members</span></span>

<span data-ttu-id="5f2ab-108">El objeto **IShellDispatch5** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5f2ab-108">The **IShellDispatch5** object has these types of members:</span></span>

-   [<span data-ttu-id="5f2ab-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5f2ab-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5f2ab-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="5f2ab-110">Methods</span></span>

<span data-ttu-id="5f2ab-111">El objeto **IShellDispatch5** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5f2ab-111">The **IShellDispatch5** object has these methods.</span></span>



| <span data-ttu-id="5f2ab-112">Método</span><span class="sxs-lookup"><span data-stu-id="5f2ab-112">Method</span></span>                                                   | <span data-ttu-id="5f2ab-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f2ab-113">Description</span></span>                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="5f2ab-114">**WindowSwitcher**</span><span class="sxs-lookup"><span data-stu-id="5f2ab-114">**WindowSwitcher**</span></span>](ishelldispatch5-windowswitcher.md) | <span data-ttu-id="5f2ab-115">Muestra las ventanas abiertas en una pila 3D que se puede desplazar.</span><span class="sxs-lookup"><span data-stu-id="5f2ab-115">Displays your open windows in a 3D stack that you can flip through.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5f2ab-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f2ab-116">Requirements</span></span>



| <span data-ttu-id="5f2ab-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f2ab-117">Requirement</span></span> | <span data-ttu-id="5f2ab-118">Value</span><span class="sxs-lookup"><span data-stu-id="5f2ab-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f2ab-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f2ab-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5f2ab-120">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5f2ab-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="5f2ab-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f2ab-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5f2ab-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f2ab-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5f2ab-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f2ab-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f2ab-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f2ab-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="5f2ab-125">IDL</span><span class="sxs-lookup"><span data-stu-id="5f2ab-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5f2ab-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5f2ab-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="5f2ab-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5f2ab-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f2ab-128"><dt>Shell32.dll (versión 6,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5f2ab-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f2ab-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f2ab-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f2ab-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="5f2ab-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="5f2ab-131">**Objeto de Shell**</span><span class="sxs-lookup"><span data-stu-id="5f2ab-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="5f2ab-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="5f2ab-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="5f2ab-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="5f2ab-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="5f2ab-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="5f2ab-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="5f2ab-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="5f2ab-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> </dl>

 

 
