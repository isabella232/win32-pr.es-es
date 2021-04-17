---
description: Especifica el tipo desasignador que va a usar una función de código auxiliar de operaciones.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: elemento operationDeallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c214b5dbc3245f63797c55880fe052d5c3ced15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697219"
---
# <a name="operationdeallocator-element"></a><span data-ttu-id="68f27-103">elemento operationDeallocator</span><span class="sxs-lookup"><span data-stu-id="68f27-103">operationDeallocator element</span></span>

<span data-ttu-id="68f27-104">Especifica el tipo desasignador que va a usar la función de código auxiliar de una operación.</span><span class="sxs-lookup"><span data-stu-id="68f27-104">Specifies the type deallocator to be used by an operation's stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="68f27-105">Uso</span><span class="sxs-lookup"><span data-stu-id="68f27-105">Usage</span></span>

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="68f27-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="68f27-106">Attributes</span></span>



| <span data-ttu-id="68f27-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="68f27-107">Attribute</span></span>                  | <span data-ttu-id="68f27-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="68f27-108">Type</span></span>                         | <span data-ttu-id="68f27-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="68f27-109">Required</span></span>       | <span data-ttu-id="68f27-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="68f27-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68f27-111">**desasignador**</span><span class="sxs-lookup"><span data-stu-id="68f27-111">**deallocator**</span></span><br/> | <span data-ttu-id="68f27-112">cadena de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="68f27-112">character\_string</span></span><br/> | <span data-ttu-id="68f27-113">Sí</span><span class="sxs-lookup"><span data-stu-id="68f27-113">Yes</span></span><br/> | <span data-ttu-id="68f27-114">Desasignador que se va a usar para la operación.</span><span class="sxs-lookup"><span data-stu-id="68f27-114">The deallocator to use for the operation.</span></span><br/> <br/> <span data-ttu-id="68f27-115">Las cadenas siguientes son valores válidos.</span><span class="sxs-lookup"><span data-stu-id="68f27-115">The following strings are valid values.</span></span><br/> <br/> <dl><span data-ttu-id="68f27-116"><span id="none"></span><span id="NONE"></span><dt>\* \* \* \* ninguno \* \*</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> \* \* \* \* \* \* <dt>WSDFreeLinkedMemory \* *</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> \* \* \* <dt>* \* \* \* CoTaskMemFree \* *</dt> <span id="free"></span> <span id="FREE"></span> \* \* <dt>* \* \* \* gratis \* *</dt> <span id="delete"></span> <span id="DELETE"></span> \* \* <dt>* \* \* \* eliminar \* \*</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> \* \* \* \* \* \* <dt>deleteArray \* \*</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> \* \* \* \* \* \* \* <dt>Versión \* \*</dt> \* \*</span><span class="sxs-lookup"><span data-stu-id="68f27-116"><span id="none"></span><span id="NONE"></span><dt>\*\*\*\*none\*\*\*\*</dt><span id="WSDFreeLinkedMemory"></span><span id="wsdfreelinkedmemory"></span><span id="WSDFREELINKEDMEMORY"></span><dt>\*\*\*\*WSDFreeLinkedMemory\*\*\*\*</dt><span id="CoTaskMemFree"></span><span id="cotaskmemfree"></span><span id="COTASKMEMFREE"></span><dt>\*\*\*\*CoTaskMemFree\*\*\*\*</dt><span id="free"></span><span id="FREE"></span><dt>\*\*\*\*free\*\*\*\*</dt><span id="delete"></span><span id="DELETE"></span><dt>\*\*\*\*delete\*\*\*\*</dt><span id="deleteArray"></span><span id="deletearray"></span><span id="DELETEARRAY"></span><dt>\*\*\*\*deleteArray\*\*\*\*</dt><span id="Release"></span><span id="release"></span><span id="RELEASE"></span><dt>\*\*\*\*Release\*\*\*\*</dt></span></span> </dl> |
| <span data-ttu-id="68f27-117">**operation**</span><span class="sxs-lookup"><span data-stu-id="68f27-117">**operation**</span></span><br/>   | <span data-ttu-id="68f27-118">cadena de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="68f27-118">character\_string</span></span><br/> | <span data-ttu-id="68f27-119">Sí</span><span class="sxs-lookup"><span data-stu-id="68f27-119">Yes</span></span><br/> | <span data-ttu-id="68f27-120">Nombre de la operación.</span><span class="sxs-lookup"><span data-stu-id="68f27-120">The name of the operation.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a><span data-ttu-id="68f27-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="68f27-121">Child elements</span></span>

<span data-ttu-id="68f27-122">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="68f27-122">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="68f27-123">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="68f27-123">Parent elements</span></span>



| <span data-ttu-id="68f27-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="68f27-124">Element</span></span>                                               | <span data-ttu-id="68f27-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="68f27-125">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68f27-126">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="68f27-126">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="68f27-127">Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="68f27-127">Generates implementations for stub functions for port type operations.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="68f27-128">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="68f27-128">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="68f27-129">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68f27-129">Minimum supported system</span></span><br/> | <span data-ttu-id="68f27-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68f27-130">Windows Vista</span></span> |
| <span data-ttu-id="68f27-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="68f27-131">Can be empty</span></span>                        | <span data-ttu-id="68f27-132">Sí</span><span class="sxs-lookup"><span data-stu-id="68f27-132">Yes</span></span>           |



 

 




