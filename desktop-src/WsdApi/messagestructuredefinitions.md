---
description: Genera definiciones de estructura de C para los tipos de mensaje.
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: elemento messageStructureDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8840e4493cb97d33cb0dac8ce1ace97cc1789e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696908"
---
# <a name="messagestructuredefinitions-element"></a><span data-ttu-id="b1ffb-103">elemento messageStructureDefinitions</span><span class="sxs-lookup"><span data-stu-id="b1ffb-103">messageStructureDefinitions element</span></span>

<span data-ttu-id="b1ffb-104">Genera definiciones de estructura de C para los tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-104">Generates C structure definitions for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="b1ffb-105">Uso</span><span class="sxs-lookup"><span data-stu-id="b1ffb-105">Usage</span></span>

``` syntax
<messageStructureDefinitions>
  child elements
</messageStructureDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="b1ffb-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b1ffb-106">Attributes</span></span>

<span data-ttu-id="b1ffb-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b1ffb-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b1ffb-108">Child elements</span></span>



| <span data-ttu-id="b1ffb-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="b1ffb-109">Element</span></span>                                   | <span data-ttu-id="b1ffb-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1ffb-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="b1ffb-111">**sesión**</span><span class="sxs-lookup"><span data-stu-id="b1ffb-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="b1ffb-112">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="b1ffb-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="b1ffb-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="b1ffb-114">Especifica el tipo de puerto para el que se generará el código.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="b1ffb-115">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b1ffb-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="b1ffb-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b1ffb-116">Parent elements</span></span>



| <span data-ttu-id="b1ffb-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="b1ffb-117">Element</span></span>                         | <span data-ttu-id="b1ffb-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1ffb-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="b1ffb-119">**archivo**</span><span class="sxs-lookup"><span data-stu-id="b1ffb-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="b1ffb-120">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b1ffb-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1ffb-121">Remarks</span></span>

<span data-ttu-id="b1ffb-122">El código auxiliar y el proxy generado hacen referencia a las estructuras de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-122">Message structures are referenced by generated proxy and stub code.</span></span> <span data-ttu-id="b1ffb-123">Este elemento se usa para generar archivos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-123">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="b1ffb-124">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b1ffb-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b1ffb-125">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1ffb-125">Minimum supported system</span></span><br/> | <span data-ttu-id="b1ffb-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1ffb-126">Windows Vista</span></span> |
| <span data-ttu-id="b1ffb-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b1ffb-127">Can be empty</span></span>                        | <span data-ttu-id="b1ffb-128">Sí</span><span class="sxs-lookup"><span data-stu-id="b1ffb-128">Yes</span></span>           |



 

 




