---
description: Genera implementaciones para las funciones QueryInterface, AddRef y Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Elemento IUnknownDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb3a4f76145e585411e64c10ea7af922db931846
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995152"
---
# <a name="iunknowndefinitions-element"></a><span data-ttu-id="45306-103">Elemento IUnknownDefinitions</span><span class="sxs-lookup"><span data-stu-id="45306-103">IUnknownDefinitions element</span></span>

<span data-ttu-id="45306-104">Genera implementaciones para las funciones QueryInterface, AddRef y Release.</span><span class="sxs-lookup"><span data-stu-id="45306-104">Generates implementations for the QueryInterface, AddRef and Release functions.</span></span>

## <a name="usage"></a><span data-ttu-id="45306-105">Uso</span><span class="sxs-lookup"><span data-stu-id="45306-105">Usage</span></span>

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="45306-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="45306-106">Attributes</span></span>



| <span data-ttu-id="45306-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="45306-107">Attribute</span></span>                  | <span data-ttu-id="45306-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="45306-108">Type</span></span>                         | <span data-ttu-id="45306-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="45306-109">Required</span></span>       | <span data-ttu-id="45306-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="45306-110">Description</span></span>                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| <span data-ttu-id="45306-111">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="45306-111">**proxyClass**</span></span><br/>  | <span data-ttu-id="45306-112">cadena \_ de caracteres</span><span class="sxs-lookup"><span data-stu-id="45306-112">character\_string</span></span><br/> | <span data-ttu-id="45306-113">Sí</span><span class="sxs-lookup"><span data-stu-id="45306-113">Yes</span></span><br/> | <span data-ttu-id="45306-114">Nombre de la clase de implementación.</span><span class="sxs-lookup"><span data-stu-id="45306-114">The name of the implementing class.</span></span><br/> <br/> |
| <span data-ttu-id="45306-115">**refCountVar**</span><span class="sxs-lookup"><span data-stu-id="45306-115">**refCountVar**</span></span><br/> | <span data-ttu-id="45306-116">cadena \_ de caracteres</span><span class="sxs-lookup"><span data-stu-id="45306-116">character\_string</span></span><br/> | <span data-ttu-id="45306-117">Sí</span><span class="sxs-lookup"><span data-stu-id="45306-117">Yes</span></span><br/> | <span data-ttu-id="45306-118">Nombre de la variable de recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="45306-118">The reference count variable name.</span></span><br/> <br/>  |



## <a name="child-elements"></a><span data-ttu-id="45306-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="45306-119">Child elements</span></span>



| <span data-ttu-id="45306-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="45306-120">Element</span></span>                                   | <span data-ttu-id="45306-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="45306-121">Description</span></span>                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="45306-122">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="45306-122">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="45306-123">Nombre de la interfaz que va a devolver QueryInterface.</span><span class="sxs-lookup"><span data-stu-id="45306-123">The name of the interface to be returned by QueryInterface.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="45306-124">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="45306-124">Child element sequence</span></span>

``` syntax
interface
```

## <a name="parent-elements"></a><span data-ttu-id="45306-125">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="45306-125">Parent elements</span></span>



| <span data-ttu-id="45306-126">Elemento</span><span class="sxs-lookup"><span data-stu-id="45306-126">Element</span></span>                         | <span data-ttu-id="45306-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="45306-127">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="45306-128">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="45306-128">**file**</span></span>](file.md)<br/> | <span data-ttu-id="45306-129">Genera un archivo del generador de código.</span><span class="sxs-lookup"><span data-stu-id="45306-129">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="45306-130">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="45306-130">Element information</span></span>



| <span data-ttu-id="45306-131">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="45306-131">Label</span></span> | <span data-ttu-id="45306-132">Value</span><span class="sxs-lookup"><span data-stu-id="45306-132">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="45306-133">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45306-133">Minimum supported system</span></span><br/> | <span data-ttu-id="45306-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45306-134">Windows Vista</span></span> |
| <span data-ttu-id="45306-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="45306-135">Can be empty</span></span>                        | <span data-ttu-id="45306-136">No</span><span class="sxs-lookup"><span data-stu-id="45306-136">No</span></span>            |



 

 




