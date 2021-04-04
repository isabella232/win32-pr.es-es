---
description: 'Evita la generación de instrucciones Import para destinos especificados con nombre en un elemento <WSDL: Import> en un archivo WSDL.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: elemento excludeImport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c08d8880029d9e03917e48b61561e3ab3eb2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908665"
---
# <a name="excludeimport-element"></a><span data-ttu-id="43edb-103">elemento excludeImport</span><span class="sxs-lookup"><span data-stu-id="43edb-103">excludeImport element</span></span>

<span data-ttu-id="43edb-104">Evita la generación de instrucciones Import para destinos especificados con nombre en un elemento <WSDL: Import> en un archivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="43edb-104">Prevents the generation of import statements for specified targets named in a <wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="43edb-105">Se puede usar para evitar que WsdCodeGen importe destinos conocidos, como las especificaciones de WS-Addressing y WS-Eventing, aunque se haga referencia a estos destinos en el WSDL.</span><span class="sxs-lookup"><span data-stu-id="43edb-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="43edb-106">El valor de este elemento debe establecerse en el espacio de nombres denominado en el elemento <WSDL: Import> que se va a excluir.</span><span class="sxs-lookup"><span data-stu-id="43edb-106">The value of this element must be set to the namespace named in the <wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="43edb-107">Uso</span><span class="sxs-lookup"><span data-stu-id="43edb-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="43edb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="43edb-108">Attributes</span></span>

<span data-ttu-id="43edb-109">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="43edb-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="43edb-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="43edb-110">Child elements</span></span>

<span data-ttu-id="43edb-111">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="43edb-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="43edb-112">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="43edb-112">Parent elements</span></span>



| <span data-ttu-id="43edb-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="43edb-113">Element</span></span>                         | <span data-ttu-id="43edb-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="43edb-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="43edb-115">**mencionados**</span><span class="sxs-lookup"><span data-stu-id="43edb-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="43edb-116">Especifica un archivo WSDL que se va a procesar para la información del contrato.</span><span class="sxs-lookup"><span data-stu-id="43edb-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="43edb-117">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="43edb-117">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="43edb-118">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43edb-118">Minimum supported system</span></span><br/> | <span data-ttu-id="43edb-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43edb-119">Windows Vista</span></span> |
| <span data-ttu-id="43edb-120">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="43edb-120">Can be empty</span></span>                        | <span data-ttu-id="43edb-121">Sí</span><span class="sxs-lookup"><span data-stu-id="43edb-121">Yes</span></span>           |



 

 




