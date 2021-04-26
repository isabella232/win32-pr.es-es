---
description: Genera constantes de C para los tipos de puerto.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: elemento portTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff073eb7b0f9cbc4b0b6df87c8f9fc84d4f62882
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996552"
---
# <a name="porttypedefinitions-element"></a><span data-ttu-id="6c94b-103">elemento portTypeDefinitions</span><span class="sxs-lookup"><span data-stu-id="6c94b-103">portTypeDefinitions element</span></span>

<span data-ttu-id="6c94b-104">Genera constantes de C para los tipos de puerto.</span><span class="sxs-lookup"><span data-stu-id="6c94b-104">Generates C constants for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="6c94b-105">Uso</span><span class="sxs-lookup"><span data-stu-id="6c94b-105">Usage</span></span>

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="6c94b-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="6c94b-106">Attributes</span></span>

<span data-ttu-id="6c94b-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="6c94b-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6c94b-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6c94b-108">Child elements</span></span>



| <span data-ttu-id="6c94b-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="6c94b-109">Element</span></span>                                                   | <span data-ttu-id="6c94b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c94b-110">Description</span></span>                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c94b-111">**Codename**</span><span class="sxs-lookup"><span data-stu-id="6c94b-111">**codeName**</span></span>](codename.md)<br/>                   | <span data-ttu-id="6c94b-112">Especifica el nombre que se usará para el tipo de puerto en el código generado.</span><span class="sxs-lookup"><span data-stu-id="6c94b-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="6c94b-113">De forma predeterminada, el nombre del código se genera a partir del nombre completo del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="6c94b-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/>         |
| [<span data-ttu-id="6c94b-114">**eventStubFunction**</span><span class="sxs-lookup"><span data-stu-id="6c94b-114">**eventStubFunction**</span></span>](eventstubfunction.md)<br/> | <span data-ttu-id="6c94b-115">Especifica si las referencias de función de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones de notificación.</span><span class="sxs-lookup"><span data-stu-id="6c94b-115">Specifies whether stub function references should be included in the operation structures in the port type definitions for notification operations.</span></span><br/> <br/>        |
| [<span data-ttu-id="6c94b-116">**Operación**</span><span class="sxs-lookup"><span data-stu-id="6c94b-116">**operation**</span></span>](operation.md)<br/>                 | <span data-ttu-id="6c94b-117">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="6c94b-117">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                                  |
| [<span data-ttu-id="6c94b-118">**portType**</span><span class="sxs-lookup"><span data-stu-id="6c94b-118">**portType**</span></span>](porttype.md)<br/>                   | <span data-ttu-id="6c94b-119">Especifica el tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="6c94b-119">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                                 |
| [<span data-ttu-id="6c94b-120">**stubFunction**</span><span class="sxs-lookup"><span data-stu-id="6c94b-120">**stubFunction**</span></span>](stubfunction.md)<br/>           | <span data-ttu-id="6c94b-121">Especifica si las referencias de función de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones un sentido y dos.</span><span class="sxs-lookup"><span data-stu-id="6c94b-121">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="6c94b-122">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6c94b-122">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="6c94b-123">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="6c94b-123">Parent elements</span></span>



| <span data-ttu-id="6c94b-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="6c94b-124">Element</span></span>                         | <span data-ttu-id="6c94b-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c94b-125">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="6c94b-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="6c94b-126">**file**</span></span>](file.md)<br/> | <span data-ttu-id="6c94b-127">Genera un archivo del generador de código.</span><span class="sxs-lookup"><span data-stu-id="6c94b-127">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6c94b-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6c94b-128">Remarks</span></span>

<span data-ttu-id="6c94b-129">Este elemento se usa generalmente en los archivos de código fuente de C para proporcionar las constantes de tipo de puerto declaradas por [**portTypeDeclarations**](porttypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="6c94b-129">This element is generally used in C source files to provide the port type constants declared by [**portTypeDeclarations**](porttypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="6c94b-130">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6c94b-130">Element information</span></span>



| <span data-ttu-id="6c94b-131">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="6c94b-131">Label</span></span> | <span data-ttu-id="6c94b-132">Value</span><span class="sxs-lookup"><span data-stu-id="6c94b-132">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="6c94b-133">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c94b-133">Minimum supported system</span></span><br/> | <span data-ttu-id="6c94b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c94b-134">Windows Vista</span></span> |
| <span data-ttu-id="6c94b-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6c94b-135">Can be empty</span></span>                        | <span data-ttu-id="6c94b-136">Sí</span><span class="sxs-lookup"><span data-stu-id="6c94b-136">Yes</span></span>           |



 

 




