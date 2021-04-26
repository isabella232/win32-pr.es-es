---
description: Especifica un archivo XSD que se va a procesar para obtener información del contrato.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: elemento xsd
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851ce31230ff88ea2465040c33dc131e0902392c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994552"
---
# <a name="xsd-element"></a><span data-ttu-id="1b503-103">elemento xsd</span><span class="sxs-lookup"><span data-stu-id="1b503-103">xsd element</span></span>

<span data-ttu-id="1b503-104">Especifica un archivo XSD que se va a procesar para obtener información del contrato.</span><span class="sxs-lookup"><span data-stu-id="1b503-104">Specifies an XSD file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="1b503-105">Uso</span><span class="sxs-lookup"><span data-stu-id="1b503-105">Usage</span></span>

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a><span data-ttu-id="1b503-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="1b503-106">Attributes</span></span>



| <span data-ttu-id="1b503-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="1b503-107">Attribute</span></span>           | <span data-ttu-id="1b503-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b503-108">Type</span></span>                       | <span data-ttu-id="1b503-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1b503-109">Required</span></span>       | <span data-ttu-id="1b503-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b503-110">Description</span></span>                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="1b503-111">**path**</span><span class="sxs-lookup"><span data-stu-id="1b503-111">**path**</span></span><br/> | <span data-ttu-id="1b503-112">pathname string</span><span class="sxs-lookup"><span data-stu-id="1b503-112">pathname string</span></span><br/> | <span data-ttu-id="1b503-113">Sí</span><span class="sxs-lookup"><span data-stu-id="1b503-113">Yes</span></span><br/> | <span data-ttu-id="1b503-114">Archivo y ruta de acceso del archivo de entrada XSD.</span><span class="sxs-lookup"><span data-stu-id="1b503-114">File and path of the XSD input file.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="1b503-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1b503-115">Child elements</span></span>



| <span data-ttu-id="1b503-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="1b503-116">Element</span></span>                               | <span data-ttu-id="1b503-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b503-117">Description</span></span>                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="1b503-118">**typeUri**</span><span class="sxs-lookup"><span data-stu-id="1b503-118">**typeUri**</span></span>](typeuri.md)<br/> | <span data-ttu-id="1b503-119">Especifica un tipo que se va a incluir desde un archivo XSD.</span><span class="sxs-lookup"><span data-stu-id="1b503-119">Specifies a type to include from an XSD file.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="1b503-120">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1b503-120">Child element sequence</span></span>

``` syntax
typeUri*
```

## <a name="parent-elements"></a><span data-ttu-id="1b503-121">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="1b503-121">Parent elements</span></span>



| <span data-ttu-id="1b503-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="1b503-122">Element</span></span>                                     | <span data-ttu-id="1b503-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b503-123">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b503-124">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="1b503-124">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="1b503-125">Elemento raíz de un archivo de script XML del generador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="1b503-125">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="1b503-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1b503-126">Remarks</span></span>

<span data-ttu-id="1b503-127">La cadena de nombre de archivo también debe incluir información de ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="1b503-127">The filename string should include complete path information as well.</span></span>

## <a name="element-information"></a><span data-ttu-id="1b503-128">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1b503-128">Element information</span></span>



| <span data-ttu-id="1b503-129">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="1b503-129">Label</span></span> | <span data-ttu-id="1b503-130">Value</span><span class="sxs-lookup"><span data-stu-id="1b503-130">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="1b503-131">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b503-131">Minimum supported system</span></span><br/> | <span data-ttu-id="1b503-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b503-132">Windows Vista</span></span> |
| <span data-ttu-id="1b503-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1b503-133">Can be empty</span></span>                        | <span data-ttu-id="1b503-134">Sí</span><span class="sxs-lookup"><span data-stu-id="1b503-134">Yes</span></span>           |



 

 




