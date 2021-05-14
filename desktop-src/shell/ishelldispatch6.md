---
description: Extiende el objeto IShellDispatch5.
title: Objeto IShellDispatch6 (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch6
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 540A5CFD-1520-4B61-B461-E893EFA27115
ms.openlocfilehash: de27322324dc8a25bdc679374e625f94a1d1a2ae
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843036"
---
# <a name="ishelldispatch6-object"></a><span data-ttu-id="98f24-103">Objeto IShellDispatch6</span><span class="sxs-lookup"><span data-stu-id="98f24-103">IShellDispatch6 object</span></span>

<span data-ttu-id="98f24-104">Extiende el [**objeto IShellDispatch5.**](ishelldispatch5.md)</span><span class="sxs-lookup"><span data-stu-id="98f24-104">Extends the [**IShellDispatch5**](ishelldispatch5.md) object.</span></span> <span data-ttu-id="98f24-105">Además de las propiedades y los métodos admitidos por **IShellDispatch5,** **IShellDispatch6** agrega un método que muestra el panel Búsqueda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="98f24-105">In addition to the properties and methods supported by **IShellDispatch5**, **IShellDispatch6** adds a method that displays the Apps Search pane.</span></span>

> [!Note]  
> <span data-ttu-id="98f24-106">**IShellDispatch6** se implementa y se accede a través del [**objeto Shell.**](shell.md)</span><span class="sxs-lookup"><span data-stu-id="98f24-106">**IShellDispatch6** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="98f24-107">Members</span><span class="sxs-lookup"><span data-stu-id="98f24-107">Members</span></span>

<span data-ttu-id="98f24-108">El **objeto IShellDispatch6** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="98f24-108">The **IShellDispatch6** object has these types of members:</span></span>

-   [<span data-ttu-id="98f24-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="98f24-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="98f24-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="98f24-110">Methods</span></span>

<span data-ttu-id="98f24-111">El **objeto IShellDispatch6** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="98f24-111">The **IShellDispatch6** object has these methods.</span></span>



| <span data-ttu-id="98f24-112">Método</span><span class="sxs-lookup"><span data-stu-id="98f24-112">Method</span></span>                                                 | <span data-ttu-id="98f24-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="98f24-113">Description</span></span>                                                                                                                  |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98f24-114">**SearchCommand**</span><span class="sxs-lookup"><span data-stu-id="98f24-114">**SearchCommand**</span></span>](ishelldispatch6-searchcommand.md) | <span data-ttu-id="98f24-115">Muestra el panel Búsqueda de aplicaciones, que normalmente aparece cuando se empieza a escribir un término de búsqueda desde el pantalla Inicio.</span><span class="sxs-lookup"><span data-stu-id="98f24-115">Displays the Apps Search pane, which normally appears when you begin to type a search term from the Start screen.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="98f24-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98f24-116">Requirements</span></span>



| <span data-ttu-id="98f24-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="98f24-117">Requirement</span></span> | <span data-ttu-id="98f24-118">Value</span><span class="sxs-lookup"><span data-stu-id="98f24-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98f24-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98f24-119">Minimum supported client</span></span><br/> | <span data-ttu-id="98f24-120">Windows 8 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="98f24-120">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="98f24-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98f24-121">Minimum supported server</span></span><br/> | <span data-ttu-id="98f24-122">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="98f24-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="98f24-123">Header</span><span class="sxs-lookup"><span data-stu-id="98f24-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="98f24-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="98f24-124"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="98f24-125">Idl</span><span class="sxs-lookup"><span data-stu-id="98f24-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="98f24-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="98f24-126"><dt>Shldisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="98f24-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="98f24-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98f24-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98f24-128"><dt>Shell32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98f24-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="98f24-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98f24-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="98f24-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="98f24-131">**Objeto Shell**</span><span class="sxs-lookup"><span data-stu-id="98f24-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="98f24-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="98f24-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="98f24-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="98f24-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="98f24-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="98f24-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="98f24-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="98f24-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> <dt>

[<span data-ttu-id="98f24-136">**IShellDispatch5**</span><span class="sxs-lookup"><span data-stu-id="98f24-136">**IShellDispatch5**</span></span>](ishelldispatch5.md)
</dt> </dl>

 

 
