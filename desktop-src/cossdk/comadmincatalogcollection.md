---
description: Representa cualquier colección en el catálogo de COM+. Úselo para enumerar, agregar, quitar y recuperar elementos de una colección y para obtener acceso a colecciones relacionadas.
ms.assetid: 2530e44f-c428-4baa-88e1-8d01eaf234cc
title: Clase COMAdminCatalogCollection (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogCollection
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 985a6b947708542ec3ce1dc6ecc835c94259b315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807646"
---
# <a name="comadmincatalogcollection-class"></a><span data-ttu-id="a1116-104">Clase COMAdminCatalogCollection</span><span class="sxs-lookup"><span data-stu-id="a1116-104">COMAdminCatalogCollection class</span></span>

<span data-ttu-id="a1116-105">Representa cualquier colección en el catálogo de COM+.</span><span class="sxs-lookup"><span data-stu-id="a1116-105">Represents any collection in the COM+ catalog.</span></span> <span data-ttu-id="a1116-106">Úselo para enumerar, agregar, quitar y recuperar elementos de una colección y para obtener acceso a colecciones relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a1116-106">Use it to enumerate, add, remove, and retrieve items in a collection and to access related collections.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="a1116-107">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="a1116-107">When to implement</span></span>

<span data-ttu-id="a1116-108">Esta clase se implementa mediante COM+.</span><span class="sxs-lookup"><span data-stu-id="a1116-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="a1116-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1116-109">Requirement</span></span> | <span data-ttu-id="a1116-110">Value</span><span class="sxs-lookup"><span data-stu-id="a1116-110">Value</span></span> |
|------------|--------------------------------------------------|
| <span data-ttu-id="a1116-111">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a1116-111">Interfaces</span></span> | [<span data-ttu-id="a1116-112">**ICatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="a1116-112">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a><span data-ttu-id="a1116-113">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="a1116-113">When to use</span></span>

<span data-ttu-id="a1116-114">Utilice los objetos creados a partir de la clase **COMAdminCatalogCollection** cuando desee manipular mediante programación una colección en el catálogo de com+.</span><span class="sxs-lookup"><span data-stu-id="a1116-114">Use objects created from the **COMAdminCatalogCollection** class when you want to programmatically manipulate a collection in the COM+ catalog.</span></span> <span data-ttu-id="a1116-115">Estas colecciones corresponden a las carpetas de la herramienta de administración de servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="a1116-115">These collections correspond to folders in the Component Services administration tool.</span></span> <span data-ttu-id="a1116-116">Los elementos de las carpetas se corresponden con los elementos de las colecciones, que puede representar con los objetos creados a partir de la clase [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="a1116-116">Items inside the folders correspond to items in collections, which you can represent by using objects created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="a1116-117">Para obtener información sobre las colecciones en el catálogo y sus propiedades, consulte [colecciones de administración de com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="a1116-117">For information regarding the collections on the catalog and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="a1116-118">Para obtener una introducción a la administración mediante programación de COM+, vea [automatizar la administración de com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="a1116-118">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a1116-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1116-119">Remarks</span></span>

<span data-ttu-id="a1116-120">No se puede crear directamente un objeto **COMAdminCatalogCollection** .</span><span class="sxs-lookup"><span data-stu-id="a1116-120">You cannot directly create a **COMAdminCatalogCollection** object.</span></span> <span data-ttu-id="a1116-121">Para usar los métodos de este objeto, debe crear un objeto [**COMAdminCatalog**](comadmincatalog.md) , obtener una referencia a [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)y, a continuación, usar [**ICOMAdminCatalog:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) para obtener una referencia a una interfaz [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) que representa una colección de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="a1116-121">To use the methods this object, you must create a [**COMAdminCatalog**](comadmincatalog.md) object, obtain a reference to [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), and then use [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) to get a reference to an [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface that represents a top-level collection.</span></span> <span data-ttu-id="a1116-122">Esto se muestra en el ejemplo siguiente, donde "cocollection" se debe reemplazar por el nombre de una de las colecciones de administración de COM+ de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="a1116-122">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections.</span></span>


```C++
    HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
      (void**)&pCatalog); 
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pCatalog->GetCollection(L"TopCollection", 
      (IDispatch**)&pTopColl);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
```



<span data-ttu-id="a1116-123">Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de administración de COM+.</span><span class="sxs-lookup"><span data-stu-id="a1116-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="a1116-124">Se puede crear un objeto COMAdminCatalogCollection llamando a [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) en un objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="a1116-124">A COMAdminCatalogCollection object can be created by calling [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) on a [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="a1116-125">Esto se muestra en el ejemplo siguiente, donde "cocollection" se debe reemplazar por el nombre de una de las colecciones de administración de COM+ de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="a1116-125">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections.</span></span>


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")

```



## <a name="requirements"></a><span data-ttu-id="a1116-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1116-126">Requirements</span></span>



| <span data-ttu-id="a1116-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1116-127">Requirement</span></span> | <span data-ttu-id="a1116-128">Value</span><span class="sxs-lookup"><span data-stu-id="a1116-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1116-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1116-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a1116-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a1116-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a1116-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1116-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a1116-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a1116-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a1116-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1116-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1116-134"><dt>COMAdmin. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1116-134"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1116-135">IDL</span><span class="sxs-lookup"><span data-stu-id="a1116-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a1116-136"><dt>COMAdmin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a1116-136"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1116-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1116-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1116-138">**COMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="a1116-138">**COMAdminCatalog**</span></span>](comadmincatalog.md)
</dt> <dt>

[<span data-ttu-id="a1116-139">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="a1116-139">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
</dt> <dt>

[<span data-ttu-id="a1116-140">**ICatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="a1116-140">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




