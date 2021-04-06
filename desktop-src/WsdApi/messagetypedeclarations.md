---
description: Genera declaraciones de constantes de C para las tablas de esquemas XML para los tipos de mensaje.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: elemento messageTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 700511d3c0a83badcb15b0e07491a14ade53f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002647"
---
# <a name="messagetypedeclarations-element"></a><span data-ttu-id="f4688-103">elemento messageTypeDeclarations</span><span class="sxs-lookup"><span data-stu-id="f4688-103">messageTypeDeclarations element</span></span>

<span data-ttu-id="f4688-104">Genera declaraciones de constantes de C para las tablas de esquemas XML para los tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4688-104">Generates C constant declarations for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="f4688-105">Uso</span><span class="sxs-lookup"><span data-stu-id="f4688-105">Usage</span></span>

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="f4688-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="f4688-106">Attributes</span></span>

<span data-ttu-id="f4688-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="f4688-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f4688-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f4688-108">Child elements</span></span>



| <span data-ttu-id="f4688-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="f4688-109">Element</span></span>                                   | <span data-ttu-id="f4688-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4688-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="f4688-111">**sesión**</span><span class="sxs-lookup"><span data-stu-id="f4688-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="f4688-112">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="f4688-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="f4688-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="f4688-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="f4688-114">Especifica el tipo de puerto para el que se generará el código.</span><span class="sxs-lookup"><span data-stu-id="f4688-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="f4688-115">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f4688-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="f4688-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="f4688-116">Parent elements</span></span>



| <span data-ttu-id="f4688-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="f4688-117">Element</span></span>                         | <span data-ttu-id="f4688-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4688-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="f4688-119">**archivo**</span><span class="sxs-lookup"><span data-stu-id="f4688-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="f4688-120">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="f4688-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f4688-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4688-121">Remarks</span></span>

<span data-ttu-id="f4688-122">Las definiciones de tipo de puerto hacen referencia a las tablas de esquema.</span><span class="sxs-lookup"><span data-stu-id="f4688-122">Schema tables are referenced by port type definitions.</span></span> <span data-ttu-id="f4688-123">Por lo tanto, este elemento se usa normalmente justo antes de los elementos [**portTypeDefinitions**](porttypedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="f4688-123">This element is therefore generally used just prior to [**portTypeDefinitions**](porttypedefinitions.md) elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="f4688-124">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="f4688-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="f4688-125">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4688-125">Minimum supported system</span></span><br/> | <span data-ttu-id="f4688-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4688-126">Windows Vista</span></span> |
| <span data-ttu-id="f4688-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f4688-127">Can be empty</span></span>                        | <span data-ttu-id="f4688-128">Sí</span><span class="sxs-lookup"><span data-stu-id="f4688-128">Yes</span></span>           |



 

 




