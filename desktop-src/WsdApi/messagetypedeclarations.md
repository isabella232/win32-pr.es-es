---
description: Genera declaraciones constantes de C para tablas de esquema XML para tipos de mensaje.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: elemento messageTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696cd6d30e6a791f68c152e0d0c5d0b1a7300769
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998732"
---
# <a name="messagetypedeclarations-element"></a><span data-ttu-id="94e42-103">elemento messageTypeDeclarations</span><span class="sxs-lookup"><span data-stu-id="94e42-103">messageTypeDeclarations element</span></span>

<span data-ttu-id="94e42-104">Genera declaraciones constantes de C para tablas de esquema XML para tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="94e42-104">Generates C constant declarations for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="94e42-105">Uso</span><span class="sxs-lookup"><span data-stu-id="94e42-105">Usage</span></span>

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="94e42-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="94e42-106">Attributes</span></span>

<span data-ttu-id="94e42-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="94e42-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="94e42-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="94e42-108">Child elements</span></span>



| <span data-ttu-id="94e42-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="94e42-109">Element</span></span>                                   | <span data-ttu-id="94e42-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="94e42-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="94e42-111">**Operación**</span><span class="sxs-lookup"><span data-stu-id="94e42-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="94e42-112">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="94e42-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="94e42-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="94e42-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="94e42-114">Especifica el tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="94e42-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="94e42-115">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="94e42-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="94e42-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="94e42-116">Parent elements</span></span>



| <span data-ttu-id="94e42-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="94e42-117">Element</span></span>                         | <span data-ttu-id="94e42-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="94e42-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="94e42-119">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="94e42-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="94e42-120">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="94e42-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="94e42-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="94e42-121">Remarks</span></span>

<span data-ttu-id="94e42-122">Las definiciones de tipo de puerto hacen referencia a las tablas de esquema.</span><span class="sxs-lookup"><span data-stu-id="94e42-122">Schema tables are referenced by port type definitions.</span></span> <span data-ttu-id="94e42-123">Por lo tanto, este elemento se usa normalmente justo antes de los [**elementos portTypeDefinitions.**](porttypedefinitions.md)</span><span class="sxs-lookup"><span data-stu-id="94e42-123">This element is therefore generally used just prior to [**portTypeDefinitions**](porttypedefinitions.md) elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="94e42-124">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="94e42-124">Element information</span></span>



| <span data-ttu-id="94e42-125">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="94e42-125">Label</span></span> | <span data-ttu-id="94e42-126">Value</span><span class="sxs-lookup"><span data-stu-id="94e42-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="94e42-127">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94e42-127">Minimum supported system</span></span><br/> | <span data-ttu-id="94e42-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94e42-128">Windows Vista</span></span> |
| <span data-ttu-id="94e42-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="94e42-129">Can be empty</span></span>                        | <span data-ttu-id="94e42-130">Sí</span><span class="sxs-lookup"><span data-stu-id="94e42-130">Yes</span></span>           |



 

 




