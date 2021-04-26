---
description: Genera declaraciones constantes de C para tipos de puerto.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: Elemento portTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19780d4a48c95cd47872b0428b368e6b7e99887
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996562"
---
# <a name="porttypedeclarations-element"></a><span data-ttu-id="71000-103">Elemento portTypeDeclarations</span><span class="sxs-lookup"><span data-stu-id="71000-103">portTypeDeclarations element</span></span>

<span data-ttu-id="71000-104">Genera declaraciones constantes de C para tipos de puerto.</span><span class="sxs-lookup"><span data-stu-id="71000-104">Generates C constant declarations for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="71000-105">Uso</span><span class="sxs-lookup"><span data-stu-id="71000-105">Usage</span></span>

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="71000-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="71000-106">Attributes</span></span>

<span data-ttu-id="71000-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="71000-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="71000-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="71000-108">Child elements</span></span>



| <span data-ttu-id="71000-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="71000-109">Element</span></span>                                   | <span data-ttu-id="71000-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="71000-110">Description</span></span>                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71000-111">**Codename**</span><span class="sxs-lookup"><span data-stu-id="71000-111">**codeName**</span></span>](codename.md)<br/>   | <span data-ttu-id="71000-112">Especifica el nombre que se usará para el tipo de puerto en el código generado.</span><span class="sxs-lookup"><span data-stu-id="71000-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="71000-113">De forma predeterminada, el nombre del código se genera a partir del nombre completo del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="71000-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="71000-114">**Operación**</span><span class="sxs-lookup"><span data-stu-id="71000-114">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="71000-115">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="71000-115">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                          |
| [<span data-ttu-id="71000-116">**portType**</span><span class="sxs-lookup"><span data-stu-id="71000-116">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="71000-117">Especifica el tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="71000-117">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a><span data-ttu-id="71000-118">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="71000-118">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="71000-119">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="71000-119">Parent elements</span></span>



| <span data-ttu-id="71000-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="71000-120">Element</span></span>                         | <span data-ttu-id="71000-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="71000-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="71000-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="71000-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="71000-123">Genera un archivo del generador de código.</span><span class="sxs-lookup"><span data-stu-id="71000-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="71000-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="71000-124">Remarks</span></span>

<span data-ttu-id="71000-125">La aplicación hace referencia a las declaraciones de tipo de puerto y gran parte del código generado.</span><span class="sxs-lookup"><span data-stu-id="71000-125">Port type declarations are referenced by the application and much of the generated code.</span></span> <span data-ttu-id="71000-126">Este elemento se usa para generar archivos de incluir.</span><span class="sxs-lookup"><span data-stu-id="71000-126">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="71000-127">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="71000-127">Element information</span></span>



| <span data-ttu-id="71000-128">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="71000-128">Label</span></span> | <span data-ttu-id="71000-129">Value</span><span class="sxs-lookup"><span data-stu-id="71000-129">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="71000-130">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71000-130">Minimum supported system</span></span><br/> | <span data-ttu-id="71000-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71000-131">Windows Vista</span></span> |
| <span data-ttu-id="71000-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="71000-132">Can be empty</span></span>                        | <span data-ttu-id="71000-133">Sí</span><span class="sxs-lookup"><span data-stu-id="71000-133">Yes</span></span>           |



 

 




