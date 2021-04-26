---
description: Genera definiciones de estructura de C para tipos de mensaje.
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: elemento messageStructureDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a116658fc7ce7f985b7b717c7a7b4ce38be4637
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993672"
---
# <a name="messagestructuredefinitions-element"></a><span data-ttu-id="6a1e2-103">elemento messageStructureDefinitions</span><span class="sxs-lookup"><span data-stu-id="6a1e2-103">messageStructureDefinitions element</span></span>

<span data-ttu-id="6a1e2-104">Genera definiciones de estructura de C para tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-104">Generates C structure definitions for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="6a1e2-105">Uso</span><span class="sxs-lookup"><span data-stu-id="6a1e2-105">Usage</span></span>

``` syntax
<messageStructureDefinitions>
  child elements
</messageStructureDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="6a1e2-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="6a1e2-106">Attributes</span></span>

<span data-ttu-id="6a1e2-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6a1e2-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6a1e2-108">Child elements</span></span>



| <span data-ttu-id="6a1e2-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="6a1e2-109">Element</span></span>                                   | <span data-ttu-id="6a1e2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a1e2-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="6a1e2-111">**Operación**</span><span class="sxs-lookup"><span data-stu-id="6a1e2-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="6a1e2-112">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="6a1e2-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="6a1e2-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="6a1e2-114">Especifica el tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="6a1e2-115">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6a1e2-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="6a1e2-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="6a1e2-116">Parent elements</span></span>



| <span data-ttu-id="6a1e2-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="6a1e2-117">Element</span></span>                         | <span data-ttu-id="6a1e2-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a1e2-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="6a1e2-119">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="6a1e2-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="6a1e2-120">Genera un archivo del generador de código.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6a1e2-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6a1e2-121">Remarks</span></span>

<span data-ttu-id="6a1e2-122">El proxy y el código auxiliar generados hacen referencia a las estructuras de mensaje.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-122">Message structures are referenced by generated proxy and stub code.</span></span> <span data-ttu-id="6a1e2-123">Este elemento se usa para generar archivos de incluir.</span><span class="sxs-lookup"><span data-stu-id="6a1e2-123">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="6a1e2-124">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6a1e2-124">Element information</span></span>



| <span data-ttu-id="6a1e2-125">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="6a1e2-125">Label</span></span> | <span data-ttu-id="6a1e2-126">Value</span><span class="sxs-lookup"><span data-stu-id="6a1e2-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="6a1e2-127">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a1e2-127">Minimum supported system</span></span><br/> | <span data-ttu-id="6a1e2-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a1e2-128">Windows Vista</span></span> |
| <span data-ttu-id="6a1e2-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6a1e2-129">Can be empty</span></span>                        | <span data-ttu-id="6a1e2-130">Sí</span><span class="sxs-lookup"><span data-stu-id="6a1e2-130">Yes</span></span>           |



 

 




