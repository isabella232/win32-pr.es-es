---
description: Extiende el objeto IShellDispatch5.
title: Objeto IShellDispatch6 (Shldisp. h)
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
ms.openlocfilehash: 42e9690ec5b2f5995b184e4e686b27037aab891d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154933"
---
# <a name="ishelldispatch6-object"></a><span data-ttu-id="9e496-103">Objeto IShellDispatch6</span><span class="sxs-lookup"><span data-stu-id="9e496-103">IShellDispatch6 object</span></span>

<span data-ttu-id="9e496-104">Extiende el objeto [**IShellDispatch5**](ishelldispatch5.md) .</span><span class="sxs-lookup"><span data-stu-id="9e496-104">Extends the [**IShellDispatch5**](ishelldispatch5.md) object.</span></span> <span data-ttu-id="9e496-105">Además de las propiedades y los métodos admitidos por **IShellDispatch5**, **IShellDispatch6** agrega un método que muestra el panel de búsqueda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9e496-105">In addition to the properties and methods supported by **IShellDispatch5**, **IShellDispatch6** adds a method that displays the Apps Search pane.</span></span>

> [!Note]  
> <span data-ttu-id="9e496-106">**IShellDispatch6** se implementa y se obtiene acceso a él a través del objeto de [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="9e496-106">**IShellDispatch6** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="9e496-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9e496-107">Members</span></span>

<span data-ttu-id="9e496-108">El objeto **IShellDispatch6** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9e496-108">The **IShellDispatch6** object has these types of members:</span></span>

-   [<span data-ttu-id="9e496-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="9e496-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9e496-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9e496-110">Methods</span></span>

<span data-ttu-id="9e496-111">El objeto **IShellDispatch6** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9e496-111">The **IShellDispatch6** object has these methods.</span></span>



| <span data-ttu-id="9e496-112">Método</span><span class="sxs-lookup"><span data-stu-id="9e496-112">Method</span></span>                                                 | <span data-ttu-id="9e496-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e496-113">Description</span></span>                                                                                                                  |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e496-114">**SearchCommand**</span><span class="sxs-lookup"><span data-stu-id="9e496-114">**SearchCommand**</span></span>](ishelldispatch6-searchcommand.md) | <span data-ttu-id="9e496-115">Muestra el panel de búsqueda de aplicaciones, que normalmente aparece cuando empieza a escribir un término de búsqueda en la pantalla Inicio.</span><span class="sxs-lookup"><span data-stu-id="9e496-115">Displays the Apps Search pane, which normally appears when you begin to type a search term from the Start screen.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9e496-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e496-116">Requirements</span></span>



| <span data-ttu-id="9e496-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e496-117">Requirement</span></span> | <span data-ttu-id="9e496-118">Value</span><span class="sxs-lookup"><span data-stu-id="9e496-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e496-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e496-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9e496-120">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e496-120">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9e496-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e496-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9e496-122">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e496-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9e496-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e496-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e496-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e496-124"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e496-125">IDL</span><span class="sxs-lookup"><span data-stu-id="9e496-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e496-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e496-126"><dt>Shldisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="9e496-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9e496-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e496-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e496-128"><dt>Shell32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e496-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e496-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e496-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="9e496-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="9e496-131">**Objeto de Shell**</span><span class="sxs-lookup"><span data-stu-id="9e496-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="9e496-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="9e496-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="9e496-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="9e496-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="9e496-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="9e496-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="9e496-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="9e496-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> <dt>

[<span data-ttu-id="9e496-136">**IShellDispatch5**</span><span class="sxs-lookup"><span data-stu-id="9e496-136">**IShellDispatch5**</span></span>](ishelldispatch5.md)
</dt> </dl>

 

 
