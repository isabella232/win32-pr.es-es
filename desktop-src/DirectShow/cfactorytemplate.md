---
description: Proporciona una plantilla para crear generadores de clases.
ms.assetid: 3dbe6402-15f8-4490-9fe2-bebaa4e79170
title: Clase CFactoryTemplate (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be5ca9b8319eeddf777cbf0071c1930f21524369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660845"
---
# <a name="cfactorytemplate-class"></a><span data-ttu-id="8d4ec-103">Clase CFactoryTemplate</span><span class="sxs-lookup"><span data-stu-id="8d4ec-103">CFactoryTemplate class</span></span>

<span data-ttu-id="8d4ec-104">Proporciona una plantilla para crear generadores de clases.</span><span class="sxs-lookup"><span data-stu-id="8d4ec-104">Provides a template for creating class factories.</span></span>

<span data-ttu-id="8d4ec-105">En DirectShow, los generadores de clases se especializan mediante la clase **CFactoryTemplate** , también denominada *plantilla de fábrica*.</span><span class="sxs-lookup"><span data-stu-id="8d4ec-105">In DirectShow, class factories are specialized using the **CFactoryTemplate** class, also called the *factory template*.</span></span> <span data-ttu-id="8d4ec-106">Cada generador de clases contiene un puntero a una plantilla de fábrica.</span><span class="sxs-lookup"><span data-stu-id="8d4ec-106">Each class factory holds a pointer to a factory template.</span></span> <span data-ttu-id="8d4ec-107">La plantilla de generador contiene información sobre un objeto COM, incluido el identificador de clase (CLSID) del objeto y un puntero a una función que crea el objeto.</span><span class="sxs-lookup"><span data-stu-id="8d4ec-107">The factory template contains information about a COM object, including the object's class identifier (CLSID) and a pointer to a function that creates the object.</span></span>

<span data-ttu-id="8d4ec-108">En el archivo DLL, declare una matriz global de plantillas de fábrica denominada *g \_ templates*.</span><span class="sxs-lookup"><span data-stu-id="8d4ec-108">In your DLL, declare a global array of factory templates named *g\_Templates*.</span></span> <span data-ttu-id="8d4ec-109">Incluya una plantilla de generador para cada objeto en el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="8d4ec-109">Include one factory template for each object in the DLL.</span></span> <span data-ttu-id="8d4ec-110">Cuando la función [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) crea un nuevo generador de clases, busca en la matriz una plantilla con un CLSID coincidente.</span><span class="sxs-lookup"><span data-stu-id="8d4ec-110">When the [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) function makes a new class factory, it searches the array for a template with a matching CLSID.</span></span> <span data-ttu-id="8d4ec-111">Suponiendo que encuentra una, crea un generador de clases que contiene un puntero a la plantilla coincidente.</span><span class="sxs-lookup"><span data-stu-id="8d4ec-111">Assuming it finds one, it creates a class factory that holds a pointer to the matching template.</span></span> <span data-ttu-id="8d4ec-112">Cuando el cliente llama a **IClassFactory:: CreateInstance**, el generador de clases llama a la función de creación de instancias definida en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="8d4ec-112">When the client calls **IClassFactory::CreateInstance**, the class factory calls the instantiation function defined in the template.</span></span>

<span data-ttu-id="8d4ec-113">Para obtener más información, vea [Cómo crear un archivo dll de filtro de DirectShow](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="8d4ec-113">For more information, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>



| <span data-ttu-id="8d4ec-114">Variables de miembro público</span><span class="sxs-lookup"><span data-stu-id="8d4ec-114">Public Member Variables</span></span>                                                   | <span data-ttu-id="8d4ec-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d4ec-115">Description</span></span>                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="8d4ec-116">**\_nombre m**</span><span class="sxs-lookup"><span data-stu-id="8d4ec-116">**m\_Name**</span></span>](cfactorytemplate-m-name.md)                                | <span data-ttu-id="8d4ec-117">Nombre del filtro.</span><span class="sxs-lookup"><span data-stu-id="8d4ec-117">Name of the filter.</span></span>                                                        |
| [<span data-ttu-id="8d4ec-118">**ClsID de m \_**</span><span class="sxs-lookup"><span data-stu-id="8d4ec-118">**m\_ClsID**</span></span>](cfactorytemplate-m-clsid.md)                              | <span data-ttu-id="8d4ec-119">Puntero al CLSID del objeto.</span><span class="sxs-lookup"><span data-stu-id="8d4ec-119">Pointer to the CLSID of the object.</span></span>                                        |
| [<span data-ttu-id="8d4ec-120">**m \_ lpfnNew**</span><span class="sxs-lookup"><span data-stu-id="8d4ec-120">**m\_lpfnNew**</span></span>](cfactorytemplate-m-lpfnnew.md)                          | <span data-ttu-id="8d4ec-121">Puntero a una función que crea una instancia del objeto.</span><span class="sxs-lookup"><span data-stu-id="8d4ec-121">Pointer to a function that creates an instance of the object.</span></span>              |
| [<span data-ttu-id="8d4ec-122">**m \_ lpfnInit**</span><span class="sxs-lookup"><span data-stu-id="8d4ec-122">**m\_lpfnInit**</span></span>](cfactorytemplate-m-lpfninit.md)                        | <span data-ttu-id="8d4ec-123">Puntero a una función a la que se llama desde el punto de entrada de DLL.</span><span class="sxs-lookup"><span data-stu-id="8d4ec-123">Pointer to a function that gets called from the DLL entry point.</span></span>           |
| [<span data-ttu-id="8d4ec-124">**\_filtro m pAMovieSetup \_**</span><span class="sxs-lookup"><span data-stu-id="8d4ec-124">**m\_pAMovieSetup\_Filter**</span></span>](cfactorytemplate-m-pamoviesetup-filter.md) | <span data-ttu-id="8d4ec-125">Puntero a una estructura de [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="8d4ec-125">Pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure.</span></span> |
| <span data-ttu-id="8d4ec-126">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="8d4ec-126">Public Methods</span></span>                                                            | <span data-ttu-id="8d4ec-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d4ec-127">Description</span></span>                                                                |
| [<span data-ttu-id="8d4ec-128">**IsClassID**</span><span class="sxs-lookup"><span data-stu-id="8d4ec-128">**IsClassID**</span></span>](cfactorytemplate-isclassid.md)                           | <span data-ttu-id="8d4ec-129">Determina si un CLSID coincide con esta plantilla de clase.</span><span class="sxs-lookup"><span data-stu-id="8d4ec-129">Determines whether a CLSID matches this class template.</span></span>                    |
| [<span data-ttu-id="8d4ec-130">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="8d4ec-130">**CreateInstance**</span></span>](cfactorytemplate-createinstance.md)                 | <span data-ttu-id="8d4ec-131">Llama a la función de creación de objetos para la clase.</span><span class="sxs-lookup"><span data-stu-id="8d4ec-131">Calls the object-creation function for the class.</span></span>                          |



 

## <a name="requirements"></a><span data-ttu-id="8d4ec-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d4ec-132">Requirements</span></span>



| <span data-ttu-id="8d4ec-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d4ec-133">Requirement</span></span> | <span data-ttu-id="8d4ec-134">Value</span><span class="sxs-lookup"><span data-stu-id="8d4ec-134">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d4ec-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d4ec-135">Header</span></span><br/>  | <dl> <span data-ttu-id="8d4ec-136"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d4ec-136"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8d4ec-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d4ec-137">Library</span></span><br/> | <dl> <span data-ttu-id="8d4ec-138"><dt>Strmbase. lib; </dt> <dt>Strmbasd. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d4ec-138"><dt>Strmbase.lib; </dt> <dt>Strmbasd.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d4ec-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d4ec-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d4ec-140">Referencia de clase base</span><span class="sxs-lookup"><span data-stu-id="8d4ec-140">Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

