---
title: IEnumSTATPROPSTG-Compound la implementación de archivos
description: La implementación de archivo compuesto de la interfaz IEnumSTATPROPSTG se usa para enumerar las propiedades, lo que da lugar a estructuras STATPROPSTG, que contienen datos de propiedad estadísticos.
ms.assetid: 8fa536f4-cce6-47e4-a860-2f43e48fa469
keywords:
- IEnumSTATPROPSTG Strctd STG, implementación de archivo compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbffce14016efdb4e2a77d60096b6776e6c2189
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995529"
---
# <a name="ienumstatpropstg-compound-file-implementation"></a><span data-ttu-id="59e61-104">IEnumSTATPROPSTG-Compound la implementación de archivos</span><span class="sxs-lookup"><span data-stu-id="59e61-104">IEnumSTATPROPSTG-Compound File Implementation</span></span>

<span data-ttu-id="59e61-105">La implementación de archivo compuesto de la interfaz [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) se usa para enumerar las propiedades, lo que da lugar a estructuras [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , que contienen datos de propiedad estadísticos.</span><span class="sxs-lookup"><span data-stu-id="59e61-105">The compound file implementation of the [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) interface is used to enumerate properties, resulting in [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures, which contain statistical property data.</span></span> <span data-ttu-id="59e61-106">La implementación de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) administra los datos estadísticos y está asociado a un objeto de almacenamiento de archivos compuesto actual.</span><span class="sxs-lookup"><span data-stu-id="59e61-106">The implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) manages the statistical data and is associated with a current compound file storage object.</span></span>

<span data-ttu-id="59e61-107">El constructor de la implementación COM de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) crea una clase que lee el conjunto de propiedades completo y crea una matriz estática que se puede compartir cuando se llama a **IEnumSTATPROPSTG:: Clone** .</span><span class="sxs-lookup"><span data-stu-id="59e61-107">The constructor in the COM implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) creates a class that reads the entire property set, and creates a static array which can be shared when **IEnumSTATPROPSTG::Clone** is called.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="59e61-108">Cuándo usar</span><span class="sxs-lookup"><span data-stu-id="59e61-108">When to Use</span></span>

<span data-ttu-id="59e61-109">Llame a la implementación de archivo compuesto de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) para enumerar las estructuras [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) que contienen datos sobre las propiedades del conjunto de propiedades actual.</span><span class="sxs-lookup"><span data-stu-id="59e61-109">Call the compound file implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) to enumerate the [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures that contain data about the properties within the current property set.</span></span> <span data-ttu-id="59e61-110">Al usar la implementación de archivo compuesto de las interfaces de almacenamiento de propiedades, llame a [**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) para devolver un puntero a **IEnumSTATPROPSTG** para administrar el objeto de almacenamiento de propiedades y los elementos que contiene.</span><span class="sxs-lookup"><span data-stu-id="59e61-110">When using the compound file implementation of the property storage interfaces, call [**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) to return a pointer to **IEnumSTATPROPSTG** to manage the property storage object and the elements within it.</span></span>

## <a name="remarks"></a><span data-ttu-id="59e61-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59e61-111">Remarks</span></span>

<dl> <dt>

<span data-ttu-id="59e61-112"><span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="59e61-112"><span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="59e61-113">Obtiene la siguiente estructura [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) o más (el número se especifica mediante el parámetro *Celt* ).</span><span class="sxs-lookup"><span data-stu-id="59e61-113">Gets the next one or more [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures (the number is specified by the *celt* parameter).</span></span> <span data-ttu-id="59e61-114">Devuelve S \_ correcto si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="59e61-114">Returns S\_OK if successful.</span></span>

</dd> <dt>

<span data-ttu-id="59e61-115"><span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG:: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="59e61-115"><span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG::Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="59e61-116">Omite el número de elementos especificados en *Celt*.</span><span class="sxs-lookup"><span data-stu-id="59e61-116">Skips the number of elements specified in *celt*.</span></span> <span data-ttu-id="59e61-117">El siguiente elemento que se va a enumerar a través de una llamada a Next se convierte en el elemento situado después de los elementos omitidos.</span><span class="sxs-lookup"><span data-stu-id="59e61-117">The next element to be enumerated through a call to Next then becomes the element after the skipped elements.</span></span> <span data-ttu-id="59e61-118">Devuelve S \_ OK si se omitieron los elementos *Celt* ; devuelve s \_ false si se omitieron menos de *Celt* elementos.</span><span class="sxs-lookup"><span data-stu-id="59e61-118">Returns S\_OK if *celt* elements were skipped; returns S\_FALSE if fewer than *celt* elements were skipped.</span></span>

</dd> <dt>

<span data-ttu-id="59e61-119"><span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG:: RESET**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="59e61-119"><span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG::Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="59e61-120">Establece el cursor al principio de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="59e61-120">Sets the cursor to the beginning of the enumeration.</span></span> <span data-ttu-id="59e61-121">Si se realiza correctamente, devuelve S \_ OK; de lo contrario, devuelve STG \_ E \_ INVALIDHANDLE.</span><span class="sxs-lookup"><span data-stu-id="59e61-121">If successful, returns S\_OK, otherwise, returns STG\_E\_INVALIDHANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="59e61-122"><span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="59e61-122"><span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="59e61-123">Utiliza el constructor de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) para crear una copia de la matriz.</span><span class="sxs-lookup"><span data-stu-id="59e61-123">Uses the constructor for the [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) to create a copy of the array.</span></span> <span data-ttu-id="59e61-124">Dado que la clase que construye la matriz estática contiene realmente el objeto, esta función agrega principalmente al recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="59e61-124">Because the class that constructs the static array actually contains the object, this function mainly adds to the reference count.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="59e61-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59e61-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59e61-126">**STATPROPSTG**</span><span class="sxs-lookup"><span data-stu-id="59e61-126">**STATPROPSTG**</span></span>](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dt>

[<span data-ttu-id="59e61-127">**IPropertyStorage:: enum**</span><span class="sxs-lookup"><span data-stu-id="59e61-127">**IPropertyStorage::Enum**</span></span>](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> </dl>

 

 