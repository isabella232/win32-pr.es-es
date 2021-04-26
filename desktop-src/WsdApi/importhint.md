---
description: Especifica la ubicación de descarga de una directiva wsdl:import que no especifica explícitamente una ubicación.
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: elemento importHint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c874879ee0a608c100f32a0520a85efe76080cc2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998762"
---
# <a name="importhint-element"></a><span data-ttu-id="8010c-103">elemento importHint</span><span class="sxs-lookup"><span data-stu-id="8010c-103">importHint element</span></span>

<span data-ttu-id="8010c-104">Especifica la ubicación de descarga de una \<wsdl:import> directiva que no especifica explícitamente una ubicación.</span><span class="sxs-lookup"><span data-stu-id="8010c-104">Specifies the download location for a \<wsdl:import> directive that does not explicitly specify a location.</span></span>

## <a name="usage"></a><span data-ttu-id="8010c-105">Uso</span><span class="sxs-lookup"><span data-stu-id="8010c-105">Usage</span></span>

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a><span data-ttu-id="8010c-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="8010c-106">Attributes</span></span>

<span data-ttu-id="8010c-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="8010c-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8010c-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8010c-108">Child elements</span></span>



| <span data-ttu-id="8010c-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="8010c-109">Element</span></span>                                   | <span data-ttu-id="8010c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8010c-110">Description</span></span>                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8010c-111">**ubicación**</span><span class="sxs-lookup"><span data-stu-id="8010c-111">**location**</span></span>](location.md)<br/>   | <span data-ttu-id="8010c-112">Ubicación del archivo que se importará.</span><span class="sxs-lookup"><span data-stu-id="8010c-112">The location of the file to import.</span></span> <span data-ttu-id="8010c-113">La ubicación puede ser una ruta de acceso relativa, una ruta de acceso absoluta o una dirección URL HTTP.</span><span class="sxs-lookup"><span data-stu-id="8010c-113">The location may be a relative path, an absolute path, or an HTTP URL.</span></span><br/> <br/> |
| [<span data-ttu-id="8010c-114">**Nombres**</span><span class="sxs-lookup"><span data-stu-id="8010c-114">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="8010c-115">Espacio de nombres que se va a importar.</span><span class="sxs-lookup"><span data-stu-id="8010c-115">The namespace to import.</span></span> <span data-ttu-id="8010c-116">Debe coincidir con el espacio de nombres especificado en el \<wsdl:import> elemento .</span><span class="sxs-lookup"><span data-stu-id="8010c-116">This should match the namespace specified in the \<wsdl:import> element.</span></span><br/> <br/>     |



### <a name="child-element-sequence"></a><span data-ttu-id="8010c-117">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8010c-117">Child element sequence</span></span>

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a><span data-ttu-id="8010c-118">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="8010c-118">Parent elements</span></span>



| <span data-ttu-id="8010c-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="8010c-119">Element</span></span>                         | <span data-ttu-id="8010c-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="8010c-120">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="8010c-121">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="8010c-121">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="8010c-122">Especifica un archivo WSDL para procesar la información del contrato.</span><span class="sxs-lookup"><span data-stu-id="8010c-122">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="8010c-123">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8010c-123">Element information</span></span>



| <span data-ttu-id="8010c-124">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="8010c-124">Label</span></span> | <span data-ttu-id="8010c-125">Value</span><span class="sxs-lookup"><span data-stu-id="8010c-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="8010c-126">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8010c-126">Minimum supported system</span></span><br/> | <span data-ttu-id="8010c-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8010c-127">Windows Vista</span></span> |
| <span data-ttu-id="8010c-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8010c-128">Can be empty</span></span>                        | <span data-ttu-id="8010c-129">No</span><span class="sxs-lookup"><span data-stu-id="8010c-129">No</span></span>            |



 

 




