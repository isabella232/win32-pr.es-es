---
description: Obtiene acceso a los datos que se almacenan en el catálogo de COM+.
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: Clase COMAdminCatalog (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalog
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: fa6e71d13f5a3d157bd3ce1035d0616dc1e5a519
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496463"
---
# <a name="comadmincatalog-class"></a><span data-ttu-id="9448c-103">Clase COMAdminCatalog</span><span class="sxs-lookup"><span data-stu-id="9448c-103">COMAdminCatalog class</span></span>

<span data-ttu-id="9448c-104">Obtiene acceso a los datos que se almacenan en el catálogo de COM+.</span><span class="sxs-lookup"><span data-stu-id="9448c-104">Accesses the data that is stored in the COM+ catalog.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="9448c-105">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="9448c-105">When to implement</span></span>

<span data-ttu-id="9448c-106">Esta clase se implementa mediante COM+.</span><span class="sxs-lookup"><span data-stu-id="9448c-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="9448c-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="9448c-107">Requirement</span></span> | <span data-ttu-id="9448c-108">Value</span><span class="sxs-lookup"><span data-stu-id="9448c-108">Value</span></span> |
|------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9448c-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="9448c-109">CLSID</span></span>      | <span data-ttu-id="9448c-110">CLSID \_ COMAdminCatalog</span><span class="sxs-lookup"><span data-stu-id="9448c-110">CLSID\_COMAdminCatalog</span></span>                                                                                            |
| <span data-ttu-id="9448c-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="9448c-111">ProgID</span></span>     | <span data-ttu-id="9448c-112">L "COMAdmin. COMAdminCatalog"</span><span class="sxs-lookup"><span data-stu-id="9448c-112">L"COMAdmin.COMAdminCatalog"</span></span>                                                                                       |
| <span data-ttu-id="9448c-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="9448c-113">Interfaces</span></span> | [<span data-ttu-id="9448c-114">**ICOMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="9448c-114">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [<span data-ttu-id="9448c-115">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="9448c-115">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a><span data-ttu-id="9448c-116">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="9448c-116">When to use</span></span>

<span data-ttu-id="9448c-117">Los objetos creados a partir de la clase **COMAdminCatalog** se usan para comenzar el acceso mediante programación a los datos de configuración de com+ almacenados en el catálogo de com+.</span><span class="sxs-lookup"><span data-stu-id="9448c-117">You use objects created from the **COMAdminCatalog** class to begin programmatic access to COM+ configuration data stored in the COM+ catalog.</span></span> <span data-ttu-id="9448c-118">Esta información se basa en las carpetas y los elementos en el árbol de consola de la herramienta de administración de servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="9448c-118">This information underlies the folders and items in the console tree of the Component Services administration tool.</span></span> <span data-ttu-id="9448c-119">La clase **COMAdminCatalog** permite obtener acceso a las colecciones del catálogo, instalar aplicaciones y componentes com+, iniciar y detener servicios, y conectarse a los servidores remotos y administrarlos.</span><span class="sxs-lookup"><span data-stu-id="9448c-119">The **COMAdminCatalog** class enables you to access collections in the catalog, install COM+ applications and components, start and stop services, and connect to and administer remote servers.</span></span>

<span data-ttu-id="9448c-120">Las carpetas de la herramienta de administración de servicios de componentes se corresponden con las recopilaciones del catálogo, que se pueden representar mediante los objetos creados a partir de la clase [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="9448c-120">Folders in the Component Services administration tool correspond to collections in the catalog, which you can represent by using objects created from the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class.</span></span> <span data-ttu-id="9448c-121">Los elementos de las carpetas corresponden a los elementos de las colecciones, que puede representar con los objetos creados a partir de la clase [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="9448c-121">Items in the folders correspond to items in the collections, which you can represent by using objects created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="9448c-122">No todas las colecciones y elementos expuestos a través de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) y [**COMAdminCatalogObject**](comadmincatalogobject.md) están disponibles en la herramienta de administración de servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="9448c-122">Not all of the collections and items exposed through [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and [**COMAdminCatalogObject**](comadmincatalogobject.md) are available in the Component Services administration tool.</span></span>

<span data-ttu-id="9448c-123">Para obtener información sobre colecciones específicas y sus propiedades, consulte [colecciones de administración de com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="9448c-123">For information regarding specific collections and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="9448c-124">Para obtener una introducción a la administración mediante programación de COM+, vea [automatizar la administración de com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="9448c-124">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9448c-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9448c-125">Remarks</span></span>

<span data-ttu-id="9448c-126">Para crear este objeto, llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="9448c-126">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="9448c-127">Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de administración de COM+.</span><span class="sxs-lookup"><span data-stu-id="9448c-127">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="9448c-128">Un objeto COMAdminCatalog se puede declarar mediante "COMAdmin. COMAdminCatalog" como nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="9448c-128">A COMAdminCatalog object can be declared using "COMAdmin.COMAdminCatalog" as the class name.</span></span>

<span data-ttu-id="9448c-129">En COM+ 1,5, lanzado con Windows XP, la clase **COMAdminCatalog** implementa la interfaz [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) .</span><span class="sxs-lookup"><span data-stu-id="9448c-129">In COM+ 1.5, released with Windows XP, the **COMAdminCatalog** class implements the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface.</span></span> <span data-ttu-id="9448c-130">Sin embargo, en COM+ 1,0, lanzado con Windows 2000, la clase **COMAdminCatalog** solo implementa la interfaz [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) .</span><span class="sxs-lookup"><span data-stu-id="9448c-130">However, in COM+ 1.0, released with Windows 2000, the **COMAdminCatalog** class implements only the [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="9448c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9448c-131">Requirements</span></span>



| <span data-ttu-id="9448c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9448c-132">Requirement</span></span> | <span data-ttu-id="9448c-133">Value</span><span class="sxs-lookup"><span data-stu-id="9448c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9448c-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9448c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9448c-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9448c-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9448c-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9448c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9448c-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9448c-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9448c-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9448c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9448c-139"><dt>COMAdmin. h</dt></span><span class="sxs-lookup"><span data-stu-id="9448c-139"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="9448c-140">IDL</span><span class="sxs-lookup"><span data-stu-id="9448c-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9448c-141"><dt>COMAdmin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9448c-141"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9448c-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="9448c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9448c-143">**COMAdminCatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="9448c-143">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
</dt> <dt>

[<span data-ttu-id="9448c-144">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="9448c-144">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
</dt> <dt>

[<span data-ttu-id="9448c-145">**ICOMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="9448c-145">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
</dt> <dt>

[<span data-ttu-id="9448c-146">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="9448c-146">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
</dt> </dl>

 

