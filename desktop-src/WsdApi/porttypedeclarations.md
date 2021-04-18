---
description: Genera declaraciones de constantes de C para los tipos de puerto.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: elemento portTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c4e202f1451d93b519bd59ea51f591c37a92957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706139"
---
# <a name="porttypedeclarations-element"></a><span data-ttu-id="d22d6-103">elemento portTypeDeclarations</span><span class="sxs-lookup"><span data-stu-id="d22d6-103">portTypeDeclarations element</span></span>

<span data-ttu-id="d22d6-104">Genera declaraciones de constantes de C para los tipos de puerto.</span><span class="sxs-lookup"><span data-stu-id="d22d6-104">Generates C constant declarations for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="d22d6-105">Uso</span><span class="sxs-lookup"><span data-stu-id="d22d6-105">Usage</span></span>

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="d22d6-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="d22d6-106">Attributes</span></span>

<span data-ttu-id="d22d6-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="d22d6-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d22d6-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d22d6-108">Child elements</span></span>



| <span data-ttu-id="d22d6-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="d22d6-109">Element</span></span>                                   | <span data-ttu-id="d22d6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d22d6-110">Description</span></span>                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d22d6-111">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d22d6-111">**codeName**</span></span>](codename.md)<br/>   | <span data-ttu-id="d22d6-112">Especifica el nombre que se va a usar para el tipo de puerto en el código generado.</span><span class="sxs-lookup"><span data-stu-id="d22d6-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="d22d6-113">De forma predeterminada, el nombre del código se genera a partir del nombre completo del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="d22d6-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="d22d6-114">**sesión**</span><span class="sxs-lookup"><span data-stu-id="d22d6-114">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="d22d6-115">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="d22d6-115">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                          |
| [<span data-ttu-id="d22d6-116">**portType**</span><span class="sxs-lookup"><span data-stu-id="d22d6-116">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="d22d6-117">Especifica el tipo de puerto para el que se generará el código.</span><span class="sxs-lookup"><span data-stu-id="d22d6-117">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a><span data-ttu-id="d22d6-118">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d22d6-118">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="d22d6-119">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="d22d6-119">Parent elements</span></span>



| <span data-ttu-id="d22d6-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="d22d6-120">Element</span></span>                         | <span data-ttu-id="d22d6-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d22d6-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="d22d6-122">**archivo**</span><span class="sxs-lookup"><span data-stu-id="d22d6-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="d22d6-123">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="d22d6-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d22d6-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d22d6-124">Remarks</span></span>

<span data-ttu-id="d22d6-125">La aplicación hace referencia a las declaraciones de tipo de puerto y gran parte del código generado.</span><span class="sxs-lookup"><span data-stu-id="d22d6-125">Port type declarations are referenced by the application and much of the generated code.</span></span> <span data-ttu-id="d22d6-126">Este elemento se usa para generar archivos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="d22d6-126">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="d22d6-127">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d22d6-127">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="d22d6-128">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d22d6-128">Minimum supported system</span></span><br/> | <span data-ttu-id="d22d6-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d22d6-129">Windows Vista</span></span> |
| <span data-ttu-id="d22d6-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d22d6-130">Can be empty</span></span>                        | <span data-ttu-id="d22d6-131">Sí</span><span class="sxs-lookup"><span data-stu-id="d22d6-131">Yes</span></span>           |



 

 




