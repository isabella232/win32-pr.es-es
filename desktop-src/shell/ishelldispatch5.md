---
description: Extiende el objeto IShellDispatch4.
title: Objeto IShellDispatch5 (Shldisp.h)
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
ms.openlocfilehash: 26c3112faa748aa443526fbe9cb493af67502cd7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843006"
---
# <a name="ishelldispatch5-object"></a><span data-ttu-id="3e49b-103">Objeto IShellDispatch5</span><span class="sxs-lookup"><span data-stu-id="3e49b-103">IShellDispatch5 object</span></span>

<span data-ttu-id="3e49b-104">Extiende el [**objeto IShellDispatch4.**](ishelldispatch4.md)</span><span class="sxs-lookup"><span data-stu-id="3e49b-104">Extends the [**IShellDispatch4**](ishelldispatch4.md) object.</span></span> <span data-ttu-id="3e49b-105">Además de las propiedades y los métodos admitidos por **IShellDispatch4,** **IShellDispatch5** agrega un método que muestra las ventanas abiertas en una pila 3D.</span><span class="sxs-lookup"><span data-stu-id="3e49b-105">In addition to the properties and methods supported by **IShellDispatch4**, **IShellDispatch5** adds a method that displays open windows in a 3D stack.</span></span>

> [!Note]  
> <span data-ttu-id="3e49b-106">**IShellDispatch5** se implementa y se accede a través del [**objeto Shell.**](shell.md)</span><span class="sxs-lookup"><span data-stu-id="3e49b-106">**IShellDispatch5** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="3e49b-107">Members</span><span class="sxs-lookup"><span data-stu-id="3e49b-107">Members</span></span>

<span data-ttu-id="3e49b-108">El **objeto IShellDispatch5** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3e49b-108">The **IShellDispatch5** object has these types of members:</span></span>

-   [<span data-ttu-id="3e49b-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="3e49b-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3e49b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="3e49b-110">Methods</span></span>

<span data-ttu-id="3e49b-111">El **objeto IShellDispatch5** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3e49b-111">The **IShellDispatch5** object has these methods.</span></span>



| <span data-ttu-id="3e49b-112">Método</span><span class="sxs-lookup"><span data-stu-id="3e49b-112">Method</span></span>                                                   | <span data-ttu-id="3e49b-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e49b-113">Description</span></span>                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="3e49b-114">**WindowSwitcher**</span><span class="sxs-lookup"><span data-stu-id="3e49b-114">**WindowSwitcher**</span></span>](ishelldispatch5-windowswitcher.md) | <span data-ttu-id="3e49b-115">Muestra las ventanas abiertas en una pila 3D por la que puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="3e49b-115">Displays your open windows in a 3D stack that you can flip through.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3e49b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e49b-116">Requirements</span></span>



| <span data-ttu-id="3e49b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e49b-117">Requirement</span></span> | <span data-ttu-id="3e49b-118">Value</span><span class="sxs-lookup"><span data-stu-id="3e49b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e49b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e49b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3e49b-120">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3e49b-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="3e49b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e49b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3e49b-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e49b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3e49b-123">Header</span><span class="sxs-lookup"><span data-stu-id="3e49b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e49b-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="3e49b-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="3e49b-125">Idl</span><span class="sxs-lookup"><span data-stu-id="3e49b-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3e49b-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="3e49b-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="3e49b-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e49b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e49b-128"><dt>Shell32.dll (versión 6.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3e49b-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e49b-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3e49b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e49b-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="3e49b-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="3e49b-131">**Objeto shell**</span><span class="sxs-lookup"><span data-stu-id="3e49b-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="3e49b-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="3e49b-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="3e49b-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="3e49b-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="3e49b-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="3e49b-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="3e49b-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="3e49b-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> </dl>

 

 
