---
description: Especifica un archivo XSD para procesar la información de contrato.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: elemento XSD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9628a078129446f51729c92c447f8da5736dab88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103909954"
---
# <a name="xsd-element"></a><span data-ttu-id="332ca-103">elemento XSD</span><span class="sxs-lookup"><span data-stu-id="332ca-103">xsd element</span></span>

<span data-ttu-id="332ca-104">Especifica un archivo XSD para procesar la información de contrato.</span><span class="sxs-lookup"><span data-stu-id="332ca-104">Specifies an XSD file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="332ca-105">Uso</span><span class="sxs-lookup"><span data-stu-id="332ca-105">Usage</span></span>

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a><span data-ttu-id="332ca-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="332ca-106">Attributes</span></span>



| <span data-ttu-id="332ca-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="332ca-107">Attribute</span></span>           | <span data-ttu-id="332ca-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="332ca-108">Type</span></span>                       | <span data-ttu-id="332ca-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="332ca-109">Required</span></span>       | <span data-ttu-id="332ca-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="332ca-110">Description</span></span>                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="332ca-111">**path**</span><span class="sxs-lookup"><span data-stu-id="332ca-111">**path**</span></span><br/> | <span data-ttu-id="332ca-112">cadena pathname</span><span class="sxs-lookup"><span data-stu-id="332ca-112">pathname string</span></span><br/> | <span data-ttu-id="332ca-113">Sí</span><span class="sxs-lookup"><span data-stu-id="332ca-113">Yes</span></span><br/> | <span data-ttu-id="332ca-114">Archivo y ruta de acceso del archivo de entrada XSD.</span><span class="sxs-lookup"><span data-stu-id="332ca-114">File and path of the XSD input file.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="332ca-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="332ca-115">Child elements</span></span>



| <span data-ttu-id="332ca-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="332ca-116">Element</span></span>                               | <span data-ttu-id="332ca-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="332ca-117">Description</span></span>                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="332ca-118">**typeUri**</span><span class="sxs-lookup"><span data-stu-id="332ca-118">**typeUri**</span></span>](typeuri.md)<br/> | <span data-ttu-id="332ca-119">Especifica un tipo que se va a incluir de un archivo XSD.</span><span class="sxs-lookup"><span data-stu-id="332ca-119">Specifies a type to include from an XSD file.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="332ca-120">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="332ca-120">Child element sequence</span></span>

``` syntax
typeUri*
```

## <a name="parent-elements"></a><span data-ttu-id="332ca-121">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="332ca-121">Parent elements</span></span>



| <span data-ttu-id="332ca-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="332ca-122">Element</span></span>                                     | <span data-ttu-id="332ca-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="332ca-123">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="332ca-124">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="332ca-124">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="332ca-125">Elemento raíz de un archivo de script XML del generador de código de WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="332ca-125">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="332ca-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="332ca-126">Remarks</span></span>

<span data-ttu-id="332ca-127">La cadena de nombre de archivo debe incluir también la información de ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="332ca-127">The filename string should include complete path information as well.</span></span>

## <a name="element-information"></a><span data-ttu-id="332ca-128">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="332ca-128">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="332ca-129">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="332ca-129">Minimum supported system</span></span><br/> | <span data-ttu-id="332ca-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="332ca-130">Windows Vista</span></span> |
| <span data-ttu-id="332ca-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="332ca-131">Can be empty</span></span>                        | <span data-ttu-id="332ca-132">Sí</span><span class="sxs-lookup"><span data-stu-id="332ca-132">Yes</span></span>           |



 

 




