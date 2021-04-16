---
title: CCLSOBJ. CPP
description: En el componente de proveedor de ejemplo, las funciones del objeto de clase de esquema se encuentran en cclsobj. cpp.
ms.assetid: e8cdef8e-c031-49e0-9496-871064aec8bd
ms.tgt_platform: multiple
keywords:
- CSampleDSClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23c198413819627ce1fcb5a605bd8e45faae0ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656193"
---
# <a name="cclsobjcpp"></a><span data-ttu-id="f568b-104">CCLSOBJ. CPP</span><span class="sxs-lookup"><span data-stu-id="f568b-104">CCLSOBJ.CPP</span></span>

<span data-ttu-id="f568b-105">En el componente de proveedor de ejemplo, las funciones del objeto de clase de esquema se encuentran en cclsobj. cpp.</span><span class="sxs-lookup"><span data-stu-id="f568b-105">In the example provider component, the functions for the schema class object are contained in cclsobj.cpp.</span></span>

<span data-ttu-id="f568b-106">La clase **CSampleDSClass** se define en este archivo.</span><span class="sxs-lookup"><span data-stu-id="f568b-106">The **CSampleDSClass** class is defined in this file.</span></span> <span data-ttu-id="f568b-107">**CSampleDSClass** se define con métodos y propiedades que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f568b-107">**CSampleDSClass** is defined with methods and properties listed in the following table.</span></span>



| <span data-ttu-id="f568b-108">Método</span><span class="sxs-lookup"><span data-stu-id="f568b-108">Method</span></span>                      | <span data-ttu-id="f568b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f568b-109">Description</span></span>                                                                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f568b-110">**CSampleDSClass**</span><span class="sxs-lookup"><span data-stu-id="f568b-110">**CSampleDSClass**</span></span>          | <span data-ttu-id="f568b-111">Constructor estándar.</span><span class="sxs-lookup"><span data-stu-id="f568b-111">Standard constructor.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="f568b-112">**~ CSampleDSClass**</span><span class="sxs-lookup"><span data-stu-id="f568b-112">**~CSampleDSClass**</span></span>         | <span data-ttu-id="f568b-113">Destructor estándar.</span><span class="sxs-lookup"><span data-stu-id="f568b-113">Standard destructor.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="f568b-114">**CreateClass**</span><span class="sxs-lookup"><span data-stu-id="f568b-114">**CreateClass**</span></span>             | <span data-ttu-id="f568b-115">Cree un objeto de clase de esquema ADs.</span><span class="sxs-lookup"><span data-stu-id="f568b-115">Create an ADs schema class object.</span></span> <span data-ttu-id="f568b-116">Definiciones de atributos de búsqueda mediante una llamada a **SampleDSGetClassDefinition**.</span><span class="sxs-lookup"><span data-stu-id="f568b-116">Lookup attribute definitions by calling **SampleDSGetClassDefinition**.</span></span>                                                                                                 |
| <span data-ttu-id="f568b-117">**CreateClass**</span><span class="sxs-lookup"><span data-stu-id="f568b-117">**CreateClass**</span></span>             | <span data-ttu-id="f568b-118">Cree un objeto de clase de esquema, según las definiciones de atributo, estableciendo los atributos conocidos, como los enumerados en [**IADsClass:: MandatoryAttributes**](iadsclass-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f568b-118">Create a schema class object, given the attribute definitions, setting known attributes, such as those listed in [**IADsClass::MandatoryAttributes**](iadsclass-property-methods.md).</span></span>                     |
| <span data-ttu-id="f568b-119">**AllocateClassObject**</span><span class="sxs-lookup"><span data-stu-id="f568b-119">**AllocateClassObject**</span></span>     | <span data-ttu-id="f568b-120">Cree un objeto de clase de esquema y cargue sus datos de tipo.</span><span class="sxs-lookup"><span data-stu-id="f568b-120">Create a schema class object and load its type data.</span></span>                                                                                                                                                       |
| <span data-ttu-id="f568b-121">**QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="f568b-121">**QueryInterface**</span></span>          | <span data-ttu-id="f568b-122">Devuelve el puntero de interfaz solicitado, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="f568b-122">Return the requested interface pointer, if available.</span></span>                                                                                                                                                      |
| <span data-ttu-id="f568b-123">Métodos IADs estándar.</span><span class="sxs-lookup"><span data-stu-id="f568b-123">Standard IADs methods.</span></span>      | <span data-ttu-id="f568b-124">Métodos de interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) estándar incluidos en este archivo.</span><span class="sxs-lookup"><span data-stu-id="f568b-124">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface methods included in this file.</span></span>                                                                                                                                     |
| <span data-ttu-id="f568b-125">Métodos estándar de IADsClass.</span><span class="sxs-lookup"><span data-stu-id="f568b-125">Standard IADsClass methods.</span></span> | <span data-ttu-id="f568b-126">Métodos de interfaz [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) estándar incluidos en este archivo.</span><span class="sxs-lookup"><span data-stu-id="f568b-126">Standard [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface methods included in this file.</span></span>                                                                                                                           |
| <span data-ttu-id="f568b-127">**CreatePropertyList**</span><span class="sxs-lookup"><span data-stu-id="f568b-127">**CreatePropertyList**</span></span>      | <span data-ttu-id="f568b-128">Cree una lista de propiedades asociadas a esta clase de esquema mediante una llamada a **CreatePropertyEntry**.</span><span class="sxs-lookup"><span data-stu-id="f568b-128">Create a list of properties associated with this schema class by calling **CreatePropertyEntry**.</span></span>                                                                                                          |
| <span data-ttu-id="f568b-129">**CreatePropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="f568b-129">**CreatePropertyEntry**</span></span>     | <span data-ttu-id="f568b-130">Cree un objeto de propiedad en esta clase de esquema.</span><span class="sxs-lookup"><span data-stu-id="f568b-130">Create one property object in this schema class.</span></span>                                                                                                                                                           |
| <span data-ttu-id="f568b-131">**FreePropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="f568b-131">**FreePropertyEntry**</span></span>       | <span data-ttu-id="f568b-132">Libere la entrada realizada en **CreatePropertyEntry**.</span><span class="sxs-lookup"><span data-stu-id="f568b-132">Free the entry made in **CreatePropertyEntry**.</span></span>                                                                                                                                                            |
| <span data-ttu-id="f568b-133">**MakeVariantFromPropList**</span><span class="sxs-lookup"><span data-stu-id="f568b-133">**MakeVariantFromPropList**</span></span> | <span data-ttu-id="f568b-134">Cree una matriz de variantes a partir de la lista de propiedades creada por **CreatePropertyList**.</span><span class="sxs-lookup"><span data-stu-id="f568b-134">Create an array of VARIANTS from the property list created by **CreatePropertyList**.</span></span> <span data-ttu-id="f568b-135">Se puede usar en la implementación de [**IADsClass:: MandatoryAttributes**](iadsclass-property-methods.md) y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="f568b-135">Can be used in the implementation of [**IADsClass::MandatoryAttributes**](iadsclass-property-methods.md) and so on.</span></span> |



 

 

 




