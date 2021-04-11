---
description: Genera constantes de C para las tablas de esquemas XML para los tipos de mensaje.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: elemento messageTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f86043cc28b527778c91772ad731d3a271921f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276233"
---
# <a name="messagetypedefinitions-element"></a><span data-ttu-id="18037-103">elemento messageTypeDefinitions</span><span class="sxs-lookup"><span data-stu-id="18037-103">messageTypeDefinitions element</span></span>

<span data-ttu-id="18037-104">Genera constantes de C para las tablas de esquemas XML para los tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="18037-104">Generates C constants for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="18037-105">Uso</span><span class="sxs-lookup"><span data-stu-id="18037-105">Usage</span></span>

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="18037-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="18037-106">Attributes</span></span>

<span data-ttu-id="18037-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="18037-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="18037-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="18037-108">Child elements</span></span>



| <span data-ttu-id="18037-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="18037-109">Element</span></span>                                   | <span data-ttu-id="18037-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="18037-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="18037-111">**sesión**</span><span class="sxs-lookup"><span data-stu-id="18037-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="18037-112">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="18037-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="18037-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="18037-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="18037-114">Especifica el tipo de puerto para el que se generará el código.</span><span class="sxs-lookup"><span data-stu-id="18037-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="18037-115">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="18037-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="18037-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="18037-116">Parent elements</span></span>



| <span data-ttu-id="18037-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="18037-117">Element</span></span>                         | <span data-ttu-id="18037-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="18037-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="18037-119">**archivo**</span><span class="sxs-lookup"><span data-stu-id="18037-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="18037-120">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="18037-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="18037-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18037-121">Remarks</span></span>

<span data-ttu-id="18037-122">Este elemento se utiliza generalmente en archivos de código fuente de C para proporcionar las tablas de esquema declaradas por [**messageTypeDeclarations**](messagetypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="18037-122">This element is generally used in C source files to provide the schema tables declared by [**messageTypeDeclarations**](messagetypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="18037-123">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="18037-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="18037-124">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18037-124">Minimum supported system</span></span><br/> | <span data-ttu-id="18037-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18037-125">Windows Vista</span></span> |
| <span data-ttu-id="18037-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="18037-126">Can be empty</span></span>                        | <span data-ttu-id="18037-127">Sí</span><span class="sxs-lookup"><span data-stu-id="18037-127">Yes</span></span>           |



 

 




