---
description: Especifica el desasignador de tipos que va a usar una función de código auxiliar de operaciones.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: operationDeallocator, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3ae0d9f1d37a478ceca0895806ade6a011747e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994292"
---
# <a name="operationdeallocator-element"></a><span data-ttu-id="b6cd2-103">operationDeallocator, elemento</span><span class="sxs-lookup"><span data-stu-id="b6cd2-103">operationDeallocator element</span></span>

<span data-ttu-id="b6cd2-104">Especifica el desasignador de tipos que va a usar la función de código auxiliar de una operación.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-104">Specifies the type deallocator to be used by an operation's stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="b6cd2-105">Uso</span><span class="sxs-lookup"><span data-stu-id="b6cd2-105">Usage</span></span>

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="b6cd2-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b6cd2-106">Attributes</span></span>



| <span data-ttu-id="b6cd2-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="b6cd2-107">Attribute</span></span>                  | <span data-ttu-id="b6cd2-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6cd2-108">Type</span></span>                         | <span data-ttu-id="b6cd2-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b6cd2-109">Required</span></span>       | <span data-ttu-id="b6cd2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6cd2-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6cd2-111">**desasignador**</span><span class="sxs-lookup"><span data-stu-id="b6cd2-111">**deallocator**</span></span><br/> | <span data-ttu-id="b6cd2-112">cadena \_ de caracteres</span><span class="sxs-lookup"><span data-stu-id="b6cd2-112">character\_string</span></span><br/> | <span data-ttu-id="b6cd2-113">Sí</span><span class="sxs-lookup"><span data-stu-id="b6cd2-113">Yes</span></span><br/> | <span data-ttu-id="b6cd2-114">Desasignador que se usará para la operación.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-114">The deallocator to use for the operation.</span></span><br/> <br/> <span data-ttu-id="b6cd2-115">Las cadenas siguientes son valores válidos.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-115">The following strings are valid values.</span></span><br/> <br/> <dl><span data-ttu-id="b6cd2-116"><span id="none"></span><span id="NONE"></span><dt>**none**</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> <dt>***WSDFreeLinkedMemory**</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> <dt>\*:CoTaskMemFree**</dt> <span id="free"></span> <span id="FREE"></span> <dt>**free**</dt> <span id="delete"></span> <span id="DELETE"></span> <dt>*"delete*"</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> <dt>*"deleteArray*"</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> <dt>\*\*Release***</dt></span><span class="sxs-lookup"><span data-stu-id="b6cd2-116"><span id="none"></span><span id="NONE"></span><dt>\*\*\*\*none\*\*\*\*</dt><span id="WSDFreeLinkedMemory"></span><span id="wsdfreelinkedmemory"></span><span id="WSDFREELINKEDMEMORY"></span><dt>\*\*\*\*WSDFreeLinkedMemory\*\*\*\*</dt><span id="CoTaskMemFree"></span><span id="cotaskmemfree"></span><span id="COTASKMEMFREE"></span><dt>\*\*\*\*CoTaskMemFree\*\*\*\*</dt><span id="free"></span><span id="FREE"></span><dt>\*\*\*\*free\*\*\*\*</dt><span id="delete"></span><span id="DELETE"></span><dt>\*\*\*\*delete\*\*\*\*</dt><span id="deleteArray"></span><span id="deletearray"></span><span id="DELETEARRAY"></span><dt>\*\*\*\*deleteArray\*\*\*\*</dt><span id="Release"></span><span id="release"></span><span id="RELEASE"></span><dt>\*\*\*\*Release\*\*\*\*</dt></span></span> </dl> |
| <span data-ttu-id="b6cd2-117">**operation**</span><span class="sxs-lookup"><span data-stu-id="b6cd2-117">**operation**</span></span><br/>   | <span data-ttu-id="b6cd2-118">cadena \_ de caracteres</span><span class="sxs-lookup"><span data-stu-id="b6cd2-118">character\_string</span></span><br/> | <span data-ttu-id="b6cd2-119">Sí</span><span class="sxs-lookup"><span data-stu-id="b6cd2-119">Yes</span></span><br/> | <span data-ttu-id="b6cd2-120">Nombre de la operación.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-120">The name of the operation.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a><span data-ttu-id="b6cd2-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b6cd2-121">Child elements</span></span>

<span data-ttu-id="b6cd2-122">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-122">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b6cd2-123">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b6cd2-123">Parent elements</span></span>



| <span data-ttu-id="b6cd2-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="b6cd2-124">Element</span></span>                                               | <span data-ttu-id="b6cd2-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6cd2-125">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6cd2-126">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="b6cd2-126">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="b6cd2-127">Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-127">Generates implementations for stub functions for port type operations.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="b6cd2-128">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b6cd2-128">Element information</span></span>



| <span data-ttu-id="b6cd2-129">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="b6cd2-129">Label</span></span> | <span data-ttu-id="b6cd2-130">Value</span><span class="sxs-lookup"><span data-stu-id="b6cd2-130">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="b6cd2-131">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6cd2-131">Minimum supported system</span></span><br/> | <span data-ttu-id="b6cd2-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6cd2-132">Windows Vista</span></span> |
| <span data-ttu-id="b6cd2-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b6cd2-133">Can be empty</span></span>                        | <span data-ttu-id="b6cd2-134">Sí</span><span class="sxs-lookup"><span data-stu-id="b6cd2-134">Yes</span></span>           |



 

 




