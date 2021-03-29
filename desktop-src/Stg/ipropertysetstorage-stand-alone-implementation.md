---
title: 'IPropertySetStorage: implementación independiente'
description: La implementación independiente proporcionada por el sistema de IPropertySetStorage incluye una implementación de IPropertyStorage y IPropertySetStorage.
ms.assetid: 0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2
keywords:
- IPropertySetStorage Strctd STG, implementaciones
- IPropertySetStorage Strctd STG, implementaciones, independiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9fd0afe31775b06b3a5f61f4c79939be976e98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077859"
---
# <a name="ipropertysetstorage-stand-alone-implementation"></a><span data-ttu-id="94f3c-105">IPropertySetStorage: implementación independiente</span><span class="sxs-lookup"><span data-stu-id="94f3c-105">IPropertySetStorage-Stand-alone Implementation</span></span>

<span data-ttu-id="94f3c-106">La implementación independiente proporcionada por el sistema de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) incluye una implementación de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) y **IPropertySetStorage**. [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) es la interfaz que lee y escribe propiedades en un almacenamiento de conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="94f3c-106">The system-provided, stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) includes an implementation of both [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) and **IPropertySetStorage**.[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) is the interface that reads and writes properties in a property set storage.</span></span> <span data-ttu-id="94f3c-107">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) es la interfaz que crea y abre conjuntos de propiedades en un almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="94f3c-107">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) is the interface that creates and opens property sets in a storage.</span></span> <span data-ttu-id="94f3c-108">Las interfaces [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) y [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) también se proporcionan en la implementación independiente.</span><span class="sxs-lookup"><span data-stu-id="94f3c-108">The [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) and [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) interfaces are also provided in the stand-alone implementation.</span></span>

<span data-ttu-id="94f3c-109">Para usar la implementación independiente de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), obtenga primero un puntero a la implementación independiente proporcionada por el sistema y asocie la implementación proporcionada por el sistema con el objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="94f3c-109">To use the stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), first obtain a pointer to the system-provided, stand-alone implementation and associate the system-provided implementation with your storage object.</span></span> <span data-ttu-id="94f3c-110">Para obtener un puntero a la implementación independiente de **IPropertySetStorage**, llame a la función [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) y proporcione el parámetro *pStorage* que especifica el objeto de almacenamiento que contendrá el conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="94f3c-110">To get a pointer to the stand-alone implementation of **IPropertySetStorage**, call the [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) function and provide the *pStorage* parameter specifying the storage object that will contain the property set.</span></span> <span data-ttu-id="94f3c-111">Esta función proporciona un puntero a la nueva interfaz **IPropertySetStorage** para el objeto de almacenamiento especificado.</span><span class="sxs-lookup"><span data-stu-id="94f3c-111">This function provides a pointer to the new **IPropertySetStorage** interface for the specified storage object.</span></span>

<span data-ttu-id="94f3c-112">La implementación independiente de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) crea conjuntos de propiedades en cualquier objeto de almacenamiento, no solo en almacenamientos de archivos compuestos.</span><span class="sxs-lookup"><span data-stu-id="94f3c-112">The stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) creates property sets on any storage object, not just on compound file storages.</span></span> <span data-ttu-id="94f3c-113">La implementación independiente no depende de archivos compuestos y se puede usar con cualquier implementación de almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="94f3c-113">The stand-alone implementation does not depend on compound files and can be used with any implementation of structured storages.</span></span> <span data-ttu-id="94f3c-114">Las restricciones en los almacenamientos estructurados proporcionados por el llamador se aplican a esta implementación de conjuntos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="94f3c-114">Any restrictions on the caller-provided structured storages apply to this implementation of property sets.</span></span> <span data-ttu-id="94f3c-115">Por ejemplo, si proporciona un almacenamiento de modo simple a [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), el [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)proporcionado restringirá el **IPropertySetStorage** resultante.</span><span class="sxs-lookup"><span data-stu-id="94f3c-115">For example, if you provide a simple-mode storage to [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), the resulting **IPropertySetStorage** will be restricted by the supplied [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage).</span></span>

<span data-ttu-id="94f3c-116">Para obtener más información sobre la implementación de archivos compuestos de esta interfaz, vea la sección [implementación de archivos compuestos IPropertySetStorage](ipropertysetstorage-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="94f3c-116">For more information about the compound file implementation of this interface, see the section [IPropertySetStorage-Compound File Implementation](ipropertysetstorage-compound-file-implementation.md).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="94f3c-117">Cuándo usar</span><span class="sxs-lookup"><span data-stu-id="94f3c-117">When to Use</span></span>

<span data-ttu-id="94f3c-118">Llame a los métodos de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para crear, abrir y eliminar conjuntos de propiedades en cualquier almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="94f3c-118">Call the methods of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) to create, open, and delete property sets in any structured storage.</span></span> <span data-ttu-id="94f3c-119">También hay un método que proporciona un puntero al enumerador [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) que se puede usar para enumerar los conjuntos de propiedades en el almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="94f3c-119">There is also a method that supplies a pointer to the [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) enumerator that can be used to enumerate the property sets in the storage.</span></span>

<span data-ttu-id="94f3c-120">La implementación independiente también proporciona las funciones auxiliares [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) y [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) , además de los métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) y [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , para crear y abrir conjuntos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="94f3c-120">The stand-alone implementation also provides the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) and [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) helper functions, in addition to the [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) methods, to create and open property sets.</span></span> <span data-ttu-id="94f3c-121">Estas dos funciones agregan compatibilidad para el \_ valor no almacenado en búfer de PROPSETFLAG, por lo que puede escribir cambios directamente en el conjunto de propiedades en lugar de almacenarlos en búfer en una memoria caché.</span><span class="sxs-lookup"><span data-stu-id="94f3c-121">These two functions add support for the PROPSETFLAG\_UNBUFFERED value so you can write changes directly to the property set instead of buffering them in a cache.</span></span> <span data-ttu-id="94f3c-122">Para obtener más información, vea [**constantes PROPSETFLAG**](propsetflag-constants.md).</span><span class="sxs-lookup"><span data-stu-id="94f3c-122">For more information, see [**PROPSETFLAG Constants**](propsetflag-constants.md).</span></span>

## <a name="methods"></a><span data-ttu-id="94f3c-123">Métodos</span><span class="sxs-lookup"><span data-stu-id="94f3c-123">Methods</span></span>

<span data-ttu-id="94f3c-124">La implementación independiente de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) admite los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="94f3c-124">The stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) supports the following methods.</span></span>

<dl> <dt>

<span data-ttu-id="94f3c-125"><span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)</span><span class="sxs-lookup"><span data-stu-id="94f3c-125"><span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)</span></span>
</dt> <dd>

<span data-ttu-id="94f3c-126">Crea un nuevo conjunto de propiedades en el almacenamiento y devuelve un puntero a la interfaz [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) en el conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="94f3c-126">Creates a new property set in the storage and returns a pointer to the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

<span data-ttu-id="94f3c-127">Si tiene previsto usar el valor de PROPSETFLAG no \_ almacenado en búfer, utilice en su lugar la función [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) para crear y abrir el nuevo conjunto de propiedades y para obtener un puntero a la implementación independiente de la interfaz [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) en el conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="94f3c-127">If you plan to use the PROPSETFLAG\_UNBUFFERED value, use the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) function instead to create and open the new property set and to obtain a pointer to the stand-alone implementation for the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

</dd> <dt>

<span data-ttu-id="94f3c-128"><span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)</span><span class="sxs-lookup"><span data-stu-id="94f3c-128"><span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)</span></span>
</dt> <dd>

<span data-ttu-id="94f3c-129">Abre un conjunto de propiedades existente en el almacenamiento y devuelve un puntero a la interfaz [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) en el conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="94f3c-129">Opens an existing property set in the storage and returns a pointer to the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

<span data-ttu-id="94f3c-130">Si tiene previsto usar el valor de PROPSETFLAG no \_ almacenado en búfer, utilice en su lugar la función [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) para obtener un puntero a la implementación independiente de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) en el conjunto de propiedades especificado.</span><span class="sxs-lookup"><span data-stu-id="94f3c-130">If you plan to use the PROPSETFLAG\_UNBUFFERED value, use the [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) function instead to obtain a pointer to the stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) on the specified property set.</span></span>

</dd> <dt>

<span data-ttu-id="94f3c-131"><span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D iminar**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)</span><span class="sxs-lookup"><span data-stu-id="94f3c-131"><span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::Delete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)</span></span>
</dt> <dd>

<span data-ttu-id="94f3c-132">Elimina un conjunto de propiedades en este almacenamiento de conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="94f3c-132">Deletes a property set in this property set storage.</span></span>

</dd> <dt>

<span data-ttu-id="94f3c-133"><span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)</span><span class="sxs-lookup"><span data-stu-id="94f3c-133"><span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)</span></span>
</dt> <dd>

<span data-ttu-id="94f3c-134">Crea un objeto que se puede utilizar para enumerar las estructuras [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) .</span><span class="sxs-lookup"><span data-stu-id="94f3c-134">Creates an object that can be used to enumerate [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structures.</span></span> <span data-ttu-id="94f3c-135">Cada estructura **STATPROPSETSTG** proporciona datos sobre un conjunto de propiedades único.</span><span class="sxs-lookup"><span data-stu-id="94f3c-135">Each **STATPROPSETSTG** structure provides data about a single property set.</span></span>

> [!Note]  
> <span data-ttu-id="94f3c-136">El conjunto de propiedades DocumentSummaryInformation y UserDefined es único en el sentido de que puede tener dos secciones set de propiedad en una única secuencia subyacente.</span><span class="sxs-lookup"><span data-stu-id="94f3c-136">The DocumentSummaryInformation and UserDefined property set is unique in that it may have two property set sections in a single underlying stream.</span></span> <span data-ttu-id="94f3c-137">Para obtener más información, vea [los conjuntos de propiedades DocumentSummaryInformation y UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="94f3c-137">For more information, see [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md) .</span></span>

 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="94f3c-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="94f3c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94f3c-139">IPropertyStorage: implementación independiente</span><span class="sxs-lookup"><span data-stu-id="94f3c-139">IPropertyStorage-Stand-alone Implementation</span></span>](ipropertystorage-stand-alone-implementation.md)
</dt> <dt>

[<span data-ttu-id="94f3c-140">**IPropertySetStorage**</span><span class="sxs-lookup"><span data-stu-id="94f3c-140">**IPropertySetStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[<span data-ttu-id="94f3c-141">**IPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="94f3c-141">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[<span data-ttu-id="94f3c-142">**IStorage:: EnumElements**</span><span class="sxs-lookup"><span data-stu-id="94f3c-142">**IStorage::EnumElements**</span></span>](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[<span data-ttu-id="94f3c-143">**Constantes de PROPSETFLAG**</span><span class="sxs-lookup"><span data-stu-id="94f3c-143">**PROPSETFLAG Constants**</span></span>](propsetflag-constants.md)
</dt> <dt>

[<span data-ttu-id="94f3c-144">**STATPROPSETSTG**</span><span class="sxs-lookup"><span data-stu-id="94f3c-144">**STATPROPSETSTG**</span></span>](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dt>

[<span data-ttu-id="94f3c-145">**StgCreatePropSetStg**</span><span class="sxs-lookup"><span data-stu-id="94f3c-145">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> <dt>

[<span data-ttu-id="94f3c-146">**StgCreatePropStg**</span><span class="sxs-lookup"><span data-stu-id="94f3c-146">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[<span data-ttu-id="94f3c-147">**StgOpenPropStg**</span><span class="sxs-lookup"><span data-stu-id="94f3c-147">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[<span data-ttu-id="94f3c-148">**Constantes de STGM**</span><span class="sxs-lookup"><span data-stu-id="94f3c-148">**STGM Constants**</span></span>](stgm-constants.md)
</dt> </dl>

 

 