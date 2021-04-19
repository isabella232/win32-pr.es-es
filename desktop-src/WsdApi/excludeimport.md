---
description: 'Evita la generación de instrucciones Import para los destinos especificados denominados en un elemento wsdl: Import en un archivo WSDL.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: elemento excludeImport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf511a24ad4007deb886900843991364fcf03a5a
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380779"
---
# <a name="excludeimport-element"></a><span data-ttu-id="43cf2-103">elemento excludeImport</span><span class="sxs-lookup"><span data-stu-id="43cf2-103">excludeImport element</span></span>

<span data-ttu-id="43cf2-104">Evita la generación de instrucciones Import para los destinos especificados denominados en un \<wsdl:import> elemento de un archivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="43cf2-104">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="43cf2-105">Se puede usar para evitar que WsdCodeGen importe destinos conocidos, como las especificaciones de WS-Addressing y WS-Eventing, aunque se haga referencia a estos destinos en el WSDL.</span><span class="sxs-lookup"><span data-stu-id="43cf2-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="43cf2-106">El valor de este elemento debe establecerse en el espacio de nombres denominado en el \<wsdl:import> elemento que se va a excluir.</span><span class="sxs-lookup"><span data-stu-id="43cf2-106">The value of this element must be set to the namespace named in the \<wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="43cf2-107">Uso</span><span class="sxs-lookup"><span data-stu-id="43cf2-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="43cf2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="43cf2-108">Attributes</span></span>

<span data-ttu-id="43cf2-109">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="43cf2-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="43cf2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="43cf2-110">Child elements</span></span>

<span data-ttu-id="43cf2-111">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="43cf2-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="43cf2-112">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="43cf2-112">Parent elements</span></span>



| <span data-ttu-id="43cf2-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="43cf2-113">Element</span></span>                         | <span data-ttu-id="43cf2-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="43cf2-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="43cf2-115">**mencionados**</span><span class="sxs-lookup"><span data-stu-id="43cf2-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="43cf2-116">Especifica un archivo WSDL que se va a procesar para la información del contrato.</span><span class="sxs-lookup"><span data-stu-id="43cf2-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="43cf2-117">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="43cf2-117">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="43cf2-118">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43cf2-118">Minimum supported system</span></span><br/> | <span data-ttu-id="43cf2-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43cf2-119">Windows Vista</span></span> |
| <span data-ttu-id="43cf2-120">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="43cf2-120">Can be empty</span></span>                        | <span data-ttu-id="43cf2-121">Sí</span><span class="sxs-lookup"><span data-stu-id="43cf2-121">Yes</span></span>           |



 

 




