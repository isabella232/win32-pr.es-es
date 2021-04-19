---
description: Genera implementaciones para las funciones QueryInterface, AddRef y Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Elemento IUnknownDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ca92338e3dc97a12e04228510fc17eb2ef2483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715802"
---
# <a name="iunknowndefinitions-element"></a><span data-ttu-id="c2fa1-103">Elemento IUnknownDefinitions</span><span class="sxs-lookup"><span data-stu-id="c2fa1-103">IUnknownDefinitions element</span></span>

<span data-ttu-id="c2fa1-104">Genera implementaciones para las funciones QueryInterface, AddRef y Release.</span><span class="sxs-lookup"><span data-stu-id="c2fa1-104">Generates implementations for the QueryInterface, AddRef and Release functions.</span></span>

## <a name="usage"></a><span data-ttu-id="c2fa1-105">Uso</span><span class="sxs-lookup"><span data-stu-id="c2fa1-105">Usage</span></span>

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="c2fa1-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="c2fa1-106">Attributes</span></span>



| <span data-ttu-id="c2fa1-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="c2fa1-107">Attribute</span></span>                  | <span data-ttu-id="c2fa1-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2fa1-108">Type</span></span>                         | <span data-ttu-id="c2fa1-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c2fa1-109">Required</span></span>       | <span data-ttu-id="c2fa1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2fa1-110">Description</span></span>                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| <span data-ttu-id="c2fa1-111">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="c2fa1-111">**proxyClass**</span></span><br/>  | <span data-ttu-id="c2fa1-112">cadena de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="c2fa1-112">character\_string</span></span><br/> | <span data-ttu-id="c2fa1-113">Sí</span><span class="sxs-lookup"><span data-stu-id="c2fa1-113">Yes</span></span><br/> | <span data-ttu-id="c2fa1-114">Nombre de la clase de implementación.</span><span class="sxs-lookup"><span data-stu-id="c2fa1-114">The name of the implementing class.</span></span><br/> <br/> |
| <span data-ttu-id="c2fa1-115">**refCountVar**</span><span class="sxs-lookup"><span data-stu-id="c2fa1-115">**refCountVar**</span></span><br/> | <span data-ttu-id="c2fa1-116">cadena de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="c2fa1-116">character\_string</span></span><br/> | <span data-ttu-id="c2fa1-117">Sí</span><span class="sxs-lookup"><span data-stu-id="c2fa1-117">Yes</span></span><br/> | <span data-ttu-id="c2fa1-118">Nombre de la variable de recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="c2fa1-118">The reference count variable name.</span></span><br/> <br/>  |



## <a name="child-elements"></a><span data-ttu-id="c2fa1-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c2fa1-119">Child elements</span></span>



| <span data-ttu-id="c2fa1-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="c2fa1-120">Element</span></span>                                   | <span data-ttu-id="c2fa1-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2fa1-121">Description</span></span>                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2fa1-122">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="c2fa1-122">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="c2fa1-123">Nombre de la interfaz que se va a devolver mediante QueryInterface.</span><span class="sxs-lookup"><span data-stu-id="c2fa1-123">The name of the interface to be returned by QueryInterface.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="c2fa1-124">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c2fa1-124">Child element sequence</span></span>

``` syntax
interface
```

## <a name="parent-elements"></a><span data-ttu-id="c2fa1-125">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="c2fa1-125">Parent elements</span></span>



| <span data-ttu-id="c2fa1-126">Elemento</span><span class="sxs-lookup"><span data-stu-id="c2fa1-126">Element</span></span>                         | <span data-ttu-id="c2fa1-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2fa1-127">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="c2fa1-128">**archivo**</span><span class="sxs-lookup"><span data-stu-id="c2fa1-128">**file**</span></span>](file.md)<br/> | <span data-ttu-id="c2fa1-129">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="c2fa1-129">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="c2fa1-130">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="c2fa1-130">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="c2fa1-131">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2fa1-131">Minimum supported system</span></span><br/> | <span data-ttu-id="c2fa1-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2fa1-132">Windows Vista</span></span> |
| <span data-ttu-id="c2fa1-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c2fa1-133">Can be empty</span></span>                        | <span data-ttu-id="c2fa1-134">No</span><span class="sxs-lookup"><span data-stu-id="c2fa1-134">No</span></span>            |



 

 




