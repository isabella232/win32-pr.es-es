---
description: Genera constantes de C para los tipos de puerto.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: elemento portTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60f55408df938ed95af14c69b2676473ac1bda71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276969"
---
# <a name="porttypedefinitions-element"></a><span data-ttu-id="61a9e-103">elemento portTypeDefinitions</span><span class="sxs-lookup"><span data-stu-id="61a9e-103">portTypeDefinitions element</span></span>

<span data-ttu-id="61a9e-104">Genera constantes de C para los tipos de puerto.</span><span class="sxs-lookup"><span data-stu-id="61a9e-104">Generates C constants for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="61a9e-105">Uso</span><span class="sxs-lookup"><span data-stu-id="61a9e-105">Usage</span></span>

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="61a9e-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="61a9e-106">Attributes</span></span>

<span data-ttu-id="61a9e-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="61a9e-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="61a9e-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="61a9e-108">Child elements</span></span>



| <span data-ttu-id="61a9e-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="61a9e-109">Element</span></span>                                                   | <span data-ttu-id="61a9e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="61a9e-110">Description</span></span>                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61a9e-111">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="61a9e-111">**codeName**</span></span>](codename.md)<br/>                   | <span data-ttu-id="61a9e-112">Especifica el nombre que se va a usar para el tipo de puerto en el código generado.</span><span class="sxs-lookup"><span data-stu-id="61a9e-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="61a9e-113">De forma predeterminada, el nombre del código se genera a partir del nombre completo del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="61a9e-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/>         |
| [<span data-ttu-id="61a9e-114">**eventStubFunction**</span><span class="sxs-lookup"><span data-stu-id="61a9e-114">**eventStubFunction**</span></span>](eventstubfunction.md)<br/> | <span data-ttu-id="61a9e-115">Especifica si las referencias de funciones de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones de notificación.</span><span class="sxs-lookup"><span data-stu-id="61a9e-115">Specifies whether stub function references should be included in the operation structures in the port type definitions for notification operations.</span></span><br/> <br/>        |
| [<span data-ttu-id="61a9e-116">**sesión**</span><span class="sxs-lookup"><span data-stu-id="61a9e-116">**operation**</span></span>](operation.md)<br/>                 | <span data-ttu-id="61a9e-117">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="61a9e-117">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                                  |
| [<span data-ttu-id="61a9e-118">**portType**</span><span class="sxs-lookup"><span data-stu-id="61a9e-118">**portType**</span></span>](porttype.md)<br/>                   | <span data-ttu-id="61a9e-119">Especifica el tipo de puerto para el que se generará el código.</span><span class="sxs-lookup"><span data-stu-id="61a9e-119">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                                 |
| [<span data-ttu-id="61a9e-120">**stubFunction**</span><span class="sxs-lookup"><span data-stu-id="61a9e-120">**stubFunction**</span></span>](stubfunction.md)<br/>           | <span data-ttu-id="61a9e-121">Especifica si las referencias de funciones de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones unidireccionales y bidireccionales.</span><span class="sxs-lookup"><span data-stu-id="61a9e-121">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="61a9e-122">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="61a9e-122">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="61a9e-123">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="61a9e-123">Parent elements</span></span>



| <span data-ttu-id="61a9e-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="61a9e-124">Element</span></span>                         | <span data-ttu-id="61a9e-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="61a9e-125">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="61a9e-126">**archivo**</span><span class="sxs-lookup"><span data-stu-id="61a9e-126">**file**</span></span>](file.md)<br/> | <span data-ttu-id="61a9e-127">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="61a9e-127">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="61a9e-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61a9e-128">Remarks</span></span>

<span data-ttu-id="61a9e-129">Este elemento se utiliza generalmente en archivos de código fuente de C para proporcionar las constantes de tipo de Puerto declaradas por [**portTypeDeclarations**](porttypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="61a9e-129">This element is generally used in C source files to provide the port type constants declared by [**portTypeDeclarations**](porttypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="61a9e-130">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="61a9e-130">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="61a9e-131">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61a9e-131">Minimum supported system</span></span><br/> | <span data-ttu-id="61a9e-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61a9e-132">Windows Vista</span></span> |
| <span data-ttu-id="61a9e-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="61a9e-133">Can be empty</span></span>                        | <span data-ttu-id="61a9e-134">Sí</span><span class="sxs-lookup"><span data-stu-id="61a9e-134">Yes</span></span>           |



 

 




