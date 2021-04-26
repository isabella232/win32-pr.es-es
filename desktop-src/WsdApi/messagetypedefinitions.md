---
description: Genera constantes de C para tablas de esquema XML para tipos de mensaje.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: elemento messageTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f1b6563254a93122960b4a990fe0bd18ab1453
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998712"
---
# <a name="messagetypedefinitions-element"></a><span data-ttu-id="2e1ba-103">elemento messageTypeDefinitions</span><span class="sxs-lookup"><span data-stu-id="2e1ba-103">messageTypeDefinitions element</span></span>

<span data-ttu-id="2e1ba-104">Genera constantes de C para tablas de esquema XML para tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="2e1ba-104">Generates C constants for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="2e1ba-105">Uso</span><span class="sxs-lookup"><span data-stu-id="2e1ba-105">Usage</span></span>

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="2e1ba-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="2e1ba-106">Attributes</span></span>

<span data-ttu-id="2e1ba-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="2e1ba-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2e1ba-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2e1ba-108">Child elements</span></span>



| <span data-ttu-id="2e1ba-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="2e1ba-109">Element</span></span>                                   | <span data-ttu-id="2e1ba-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e1ba-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="2e1ba-111">**Operación**</span><span class="sxs-lookup"><span data-stu-id="2e1ba-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="2e1ba-112">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="2e1ba-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="2e1ba-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="2e1ba-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="2e1ba-114">Especifica el tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="2e1ba-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="2e1ba-115">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2e1ba-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="2e1ba-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="2e1ba-116">Parent elements</span></span>



| <span data-ttu-id="2e1ba-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="2e1ba-117">Element</span></span>                         | <span data-ttu-id="2e1ba-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e1ba-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="2e1ba-119">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="2e1ba-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="2e1ba-120">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="2e1ba-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="2e1ba-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e1ba-121">Remarks</span></span>

<span data-ttu-id="2e1ba-122">Este elemento se usa generalmente en los archivos de código fuente de C para proporcionar las tablas de esquema declaradas por [**messageTypeDeclarations**](messagetypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="2e1ba-122">This element is generally used in C source files to provide the schema tables declared by [**messageTypeDeclarations**](messagetypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="2e1ba-123">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2e1ba-123">Element information</span></span>



| <span data-ttu-id="2e1ba-124">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2e1ba-124">Label</span></span> | <span data-ttu-id="2e1ba-125">Value</span><span class="sxs-lookup"><span data-stu-id="2e1ba-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="2e1ba-126">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e1ba-126">Minimum supported system</span></span><br/> | <span data-ttu-id="2e1ba-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e1ba-127">Windows Vista</span></span> |
| <span data-ttu-id="2e1ba-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2e1ba-128">Can be empty</span></span>                        | <span data-ttu-id="2e1ba-129">Sí</span><span class="sxs-lookup"><span data-stu-id="2e1ba-129">Yes</span></span>           |



 

 




