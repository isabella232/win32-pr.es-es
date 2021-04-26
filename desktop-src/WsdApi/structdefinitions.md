---
description: Genera definiciones de estructura de C para tipos conocidos.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: Elemento structDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f680db18b06253362f932cc7d34d5b85f7c1b5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996462"
---
# <a name="structdefinitions-element"></a><span data-ttu-id="fc183-103">Elemento structDefinitions</span><span class="sxs-lookup"><span data-stu-id="fc183-103">structDefinitions element</span></span>

<span data-ttu-id="fc183-104">Genera definiciones de estructura de C para tipos conocidos.</span><span class="sxs-lookup"><span data-stu-id="fc183-104">Generates C structure definitions for known types.</span></span>

## <a name="usage"></a><span data-ttu-id="fc183-105">Uso</span><span class="sxs-lookup"><span data-stu-id="fc183-105">Usage</span></span>

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a><span data-ttu-id="fc183-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="fc183-106">Attributes</span></span>

<span data-ttu-id="fc183-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="fc183-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fc183-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fc183-108">Child elements</span></span>

<span data-ttu-id="fc183-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="fc183-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="fc183-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="fc183-110">Parent elements</span></span>



| <span data-ttu-id="fc183-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="fc183-111">Element</span></span>                         | <span data-ttu-id="fc183-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc183-112">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="fc183-113">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="fc183-113">**file**</span></span>](file.md)<br/> | <span data-ttu-id="fc183-114">Genera un archivo del generador de código.</span><span class="sxs-lookup"><span data-stu-id="fc183-114">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="fc183-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fc183-115">Remarks</span></span>

<span data-ttu-id="fc183-116">Gran parte del código generado y el código de aplicación hacen referencia a las estructuras para los tipos conocidos.</span><span class="sxs-lookup"><span data-stu-id="fc183-116">Structures for known types are referenced by much of the generated code and by application code.</span></span> <span data-ttu-id="fc183-117">Este elemento se usa para generar archivos de incluir.</span><span class="sxs-lookup"><span data-stu-id="fc183-117">This element is used to generate include files.</span></span> <span data-ttu-id="fc183-118">Este elemento debe producirse después de [**un elemento structDeclarations**](structdeclarations.md) para que las referencias entre estructuras se controlen correctamente.</span><span class="sxs-lookup"><span data-stu-id="fc183-118">This element should occur after a [**structDeclarations**](structdeclarations.md) element so that references between structures are handled properly.</span></span>

## <a name="element-information"></a><span data-ttu-id="fc183-119">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="fc183-119">Element information</span></span>



| <span data-ttu-id="fc183-120">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="fc183-120">Label</span></span> | <span data-ttu-id="fc183-121">Value</span><span class="sxs-lookup"><span data-stu-id="fc183-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="fc183-122">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc183-122">Minimum supported system</span></span><br/> | <span data-ttu-id="fc183-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc183-123">Windows Vista</span></span> |
| <span data-ttu-id="fc183-124">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fc183-124">Can be empty</span></span>                        | <span data-ttu-id="fc183-125">Sí</span><span class="sxs-lookup"><span data-stu-id="fc183-125">Yes</span></span>           |



 

 




