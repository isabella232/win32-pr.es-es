---
description: 'Especifica la ubicación de descarga de una directiva <WSDL: Import> que no especifica explícitamente una ubicación.'
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: elemento importHint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce8da0a7fa45ed00489d405aaba8f1f6d7ab8fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706146"
---
# <a name="importhint-element"></a><span data-ttu-id="41cde-103">elemento importHint</span><span class="sxs-lookup"><span data-stu-id="41cde-103">importHint element</span></span>

<span data-ttu-id="41cde-104">Especifica la ubicación de descarga de una directiva <WSDL: Import> que no especifica explícitamente una ubicación.</span><span class="sxs-lookup"><span data-stu-id="41cde-104">Specifies the download location for a <wsdl:import> directive that does not explicitly specify a location.</span></span>

## <a name="usage"></a><span data-ttu-id="41cde-105">Uso</span><span class="sxs-lookup"><span data-stu-id="41cde-105">Usage</span></span>

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a><span data-ttu-id="41cde-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="41cde-106">Attributes</span></span>

<span data-ttu-id="41cde-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="41cde-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="41cde-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="41cde-108">Child elements</span></span>



| <span data-ttu-id="41cde-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="41cde-109">Element</span></span>                                   | <span data-ttu-id="41cde-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="41cde-110">Description</span></span>                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41cde-111">**Cód**</span><span class="sxs-lookup"><span data-stu-id="41cde-111">**location**</span></span>](location.md)<br/>   | <span data-ttu-id="41cde-112">Ubicación del archivo que se va a importar.</span><span class="sxs-lookup"><span data-stu-id="41cde-112">The location of the file to import.</span></span> <span data-ttu-id="41cde-113">La ubicación puede ser una ruta de acceso relativa, una ruta de acceso absoluta o una dirección URL HTTP.</span><span class="sxs-lookup"><span data-stu-id="41cde-113">The location may be a relative path, an absolute path, or an HTTP URL.</span></span><br/> <br/> |
| [<span data-ttu-id="41cde-114">**System.IO**</span><span class="sxs-lookup"><span data-stu-id="41cde-114">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="41cde-115">Espacio de nombres que se va a importar.</span><span class="sxs-lookup"><span data-stu-id="41cde-115">The namespace to import.</span></span> <span data-ttu-id="41cde-116">Debe coincidir con el espacio de nombres especificado en el elemento <WSDL: Import>.</span><span class="sxs-lookup"><span data-stu-id="41cde-116">This should match the namespace specified in the <wsdl:import> element.</span></span><br/> <br/>     |



### <a name="child-element-sequence"></a><span data-ttu-id="41cde-117">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="41cde-117">Child element sequence</span></span>

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a><span data-ttu-id="41cde-118">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="41cde-118">Parent elements</span></span>



| <span data-ttu-id="41cde-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="41cde-119">Element</span></span>                         | <span data-ttu-id="41cde-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="41cde-120">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="41cde-121">**mencionados**</span><span class="sxs-lookup"><span data-stu-id="41cde-121">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="41cde-122">Especifica un archivo WSDL que se va a procesar para la información del contrato.</span><span class="sxs-lookup"><span data-stu-id="41cde-122">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="41cde-123">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="41cde-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="41cde-124">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41cde-124">Minimum supported system</span></span><br/> | <span data-ttu-id="41cde-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41cde-125">Windows Vista</span></span> |
| <span data-ttu-id="41cde-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="41cde-126">Can be empty</span></span>                        | <span data-ttu-id="41cde-127">No</span><span class="sxs-lookup"><span data-stu-id="41cde-127">No</span></span>            |



 

 




