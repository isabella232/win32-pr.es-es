---
title: CENUMOBJ. CPP
description: En el componente de proveedor de ejemplo, la enumeración de un objeto contenedor usa las rutinas, desde cenumobj. cpp, que se enumeran en la tabla siguiente.
ms.assetid: 7166230d-0bf8-4f7d-9781-72f125a3dd21
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b7859571c7136cf1f8a2895b69fe7cdcdf07604
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793797"
---
# <a name="cenumobjcpp"></a><span data-ttu-id="19914-103">CENUMOBJ. CPP</span><span class="sxs-lookup"><span data-stu-id="19914-103">CENUMOBJ.CPP</span></span>

<span data-ttu-id="19914-104">En el componente de proveedor de ejemplo, la enumeración de un objeto contenedor usa las rutinas, desde cenumobj. cpp, que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="19914-104">In the example provider component, the enumeration of a container object uses the routines, from cenumobj.cpp, listed in the following table.</span></span>



| <span data-ttu-id="19914-105">Método</span><span class="sxs-lookup"><span data-stu-id="19914-105">Method</span></span>                                                 | <span data-ttu-id="19914-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="19914-106">Description</span></span>                                                                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19914-107">**CSampleDSGenObjectEnum:: Create**</span><span class="sxs-lookup"><span data-stu-id="19914-107">**CSampleDSGenObjectEnum::Create**</span></span>                     | <span data-ttu-id="19914-108">Cree un objeto para habilitar la enumeración de objetos de Active Directory genéricos.</span><span class="sxs-lookup"><span data-stu-id="19914-108">Create an object to enable enumeration of generic Active Directory objects.</span></span>                                                                                           |
| <span data-ttu-id="19914-109">**CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**</span><span class="sxs-lookup"><span data-stu-id="19914-109">**CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**</span></span>     | <span data-ttu-id="19914-110">Inicialización.</span><span class="sxs-lookup"><span data-stu-id="19914-110">Initialization.</span></span>                                                                                                                                                       |
| <span data-ttu-id="19914-111">**CSampleDSGenObjectEnum::EnumGenericObjects**</span><span class="sxs-lookup"><span data-stu-id="19914-111">**CSampleDSGenObjectEnum::EnumGenericObjects**</span></span>         | <span data-ttu-id="19914-112">Administrar la recuperación de objetos.</span><span class="sxs-lookup"><span data-stu-id="19914-112">Manage retrieval of objects.</span></span>                                                                                                                                          |
| <span data-ttu-id="19914-113">**CSampleDSGenObjectEnum::FetchObjects**</span><span class="sxs-lookup"><span data-stu-id="19914-113">**CSampleDSGenObjectEnum::FetchObjects**</span></span>               | <span data-ttu-id="19914-114">Recupera el conjunto de punteros [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que coinciden con el filtro.</span><span class="sxs-lookup"><span data-stu-id="19914-114">Retrieve the set of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointers that match the filter.</span></span>                                                             |
| <span data-ttu-id="19914-115">**CSampleDSGenObjectEnum::FetchNextObject**</span><span class="sxs-lookup"><span data-stu-id="19914-115">**CSampleDSGenObjectEnum::FetchNextObject**</span></span>            | <span data-ttu-id="19914-116">Recupera un objeto y coincide con el filtro.</span><span class="sxs-lookup"><span data-stu-id="19914-116">Retrieve an object and match against the filter.</span></span> <span data-ttu-id="19914-117">Si coincide, inclúyalo en el objeto genérico y devuelva un puntero [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="19914-117">If it matches, wrap it in generic object and return a [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer.</span></span> |
| <span data-ttu-id="19914-118">**CSampleDSGenObjectEnum::EnumGenericObjects**</span><span class="sxs-lookup"><span data-stu-id="19914-118">**CSampleDSGenObjectEnum::EnumGenericObjects**</span></span>         | <span data-ttu-id="19914-119">Administrar la recuperación de los objetos.</span><span class="sxs-lookup"><span data-stu-id="19914-119">Manage retrieving the objects.</span></span>                                                                                                                                        |
| <span data-ttu-id="19914-120">**CSampleDSGenObjectEnum:: Next**</span><span class="sxs-lookup"><span data-stu-id="19914-120">**CSampleDSGenObjectEnum::Next**</span></span>                       | <span data-ttu-id="19914-121">Recupera el número especificado de elementos del objeto de enumeración indicado.</span><span class="sxs-lookup"><span data-stu-id="19914-121">Retrieve the specified number of elements from the enumeration object indicated.</span></span>                                                                                      |
| <span data-ttu-id="19914-122">**CSampleDSGenObjectEnum::IsValidDSFilter**</span><span class="sxs-lookup"><span data-stu-id="19914-122">**CSampleDSGenObjectEnum::IsValidDSFilter**</span></span>            | <span data-ttu-id="19914-123">Compruebe que la clase de objeto coincide con una de la lista de filtros.</span><span class="sxs-lookup"><span data-stu-id="19914-123">Verify that object class matches one in the filter list.</span></span>                                                                                                              |
| <span data-ttu-id="19914-124">**CSampleDSGenObjectEnum::BuildDSFilterArray**</span><span class="sxs-lookup"><span data-stu-id="19914-124">**CSampleDSGenObjectEnum::BuildDSFilterArray**</span></span>         | <span data-ttu-id="19914-125">Administrar la matriz de filtros.</span><span class="sxs-lookup"><span data-stu-id="19914-125">Manage the filter array.</span></span>                                                                                                                                              |
| <span data-ttu-id="19914-126">**CSampleDSGenObjectEnum::CreateAndAppendFilterEntry**</span><span class="sxs-lookup"><span data-stu-id="19914-126">**CSampleDSGenObjectEnum::CreateAndAppendFilterEntry**</span></span> | <span data-ttu-id="19914-127">Agregue una nueva clase de objeto al filtro y establezca el filtro como contiguo.</span><span class="sxs-lookup"><span data-stu-id="19914-127">Add a new object class to the filter and set the filter as contiguous.</span></span>                                                                                                |
| <span data-ttu-id="19914-128">**FreeFilterList**</span><span class="sxs-lookup"><span data-stu-id="19914-128">**FreeFilterList**</span></span>                                     | <span data-ttu-id="19914-129">Libere el filtro.</span><span class="sxs-lookup"><span data-stu-id="19914-129">Free the filter.</span></span>                                                                                                                                                      |



 

 

 