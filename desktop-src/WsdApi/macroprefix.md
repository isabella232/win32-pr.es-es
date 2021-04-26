---
description: Define el prefijo que se usará en el código generado para los nombres de macros en el espacio de nombres .
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: macroPrefix, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9590092d78ea4700715a868bb7e50f15833011
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998752"
---
# <a name="macroprefix-element"></a><span data-ttu-id="8f61b-103">macroPrefix, elemento</span><span class="sxs-lookup"><span data-stu-id="8f61b-103">macroPrefix element</span></span>

<span data-ttu-id="8f61b-104">Define el prefijo que se usará en el código generado para los nombres de macros en el espacio de nombres .</span><span class="sxs-lookup"><span data-stu-id="8f61b-104">Defines the prefix to be used in the generated code for names of macros in the namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="8f61b-105">Uso</span><span class="sxs-lookup"><span data-stu-id="8f61b-105">Usage</span></span>

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="8f61b-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="8f61b-106">Attributes</span></span>

<span data-ttu-id="8f61b-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="8f61b-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8f61b-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8f61b-108">Child elements</span></span>

<span data-ttu-id="8f61b-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="8f61b-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="8f61b-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="8f61b-110">Parent elements</span></span>



| <span data-ttu-id="8f61b-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="8f61b-111">Element</span></span>                                   | <span data-ttu-id="8f61b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f61b-112">Description</span></span>                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="8f61b-113">**Nombres**</span><span class="sxs-lookup"><span data-stu-id="8f61b-113">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="8f61b-114">Espacio de nombres que se va a usar para la generación de código.</span><span class="sxs-lookup"><span data-stu-id="8f61b-114">A namespace to be used for code generation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8f61b-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8f61b-115">Remarks</span></span>

<span data-ttu-id="8f61b-116">Este elemento invalida el prefijo URI predeterminado que se usa para las macros generadas.</span><span class="sxs-lookup"><span data-stu-id="8f61b-116">This element overrides the default URI prefix used for generated macros.</span></span> <span data-ttu-id="8f61b-117">Por ejemplo, si el prefijo de macro es "AV" y el nombre es "Tuner", la macro generada para el nombre completo \_ será "AV \_ Tuner".</span><span class="sxs-lookup"><span data-stu-id="8f61b-117">For example, if the macro prefix is "AV\_" and the name is "Tuner", the macro generated for the qualified name will be "AV\_Tuner".</span></span>

<span data-ttu-id="8f61b-118">De forma predeterminada, el código generado crea un prefijo de macro preferido a partir del URI.</span><span class="sxs-lookup"><span data-stu-id="8f61b-118">By default, the code generated creates a preferred macro prefix from the URI.</span></span>

## <a name="element-information"></a><span data-ttu-id="8f61b-119">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8f61b-119">Element information</span></span>



| <span data-ttu-id="8f61b-120">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="8f61b-120">Label</span></span> | <span data-ttu-id="8f61b-121">Value</span><span class="sxs-lookup"><span data-stu-id="8f61b-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="8f61b-122">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f61b-122">Minimum supported system</span></span><br/> | <span data-ttu-id="8f61b-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f61b-123">Windows Vista</span></span> |
| <span data-ttu-id="8f61b-124">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8f61b-124">Can be empty</span></span>                        | <span data-ttu-id="8f61b-125">Sí</span><span class="sxs-lookup"><span data-stu-id="8f61b-125">Yes</span></span>           |



 

 




