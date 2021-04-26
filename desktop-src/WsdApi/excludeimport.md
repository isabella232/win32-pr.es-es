---
description: Impide la generación de instrucciones de importación para destinos especificados denominados en un elemento wsdl:import de un archivo WSDL.
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: excludeImport, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e14d79576151fbb3dc266621c3fa34816cea55e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995882"
---
# <a name="excludeimport-element"></a><span data-ttu-id="8d86c-103">excludeImport, elemento</span><span class="sxs-lookup"><span data-stu-id="8d86c-103">excludeImport element</span></span>

<span data-ttu-id="8d86c-104">Impide la generación de instrucciones de importación para destinos especificados denominados en \<wsdl:import> un elemento de un archivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="8d86c-104">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="8d86c-105">Esto se puede usar para evitar que WsdCodeGen importe destinos conocidos, como las especificaciones WS-Addressing y WS-Eventing, aunque se haga referencia a estos destinos en WSDL.</span><span class="sxs-lookup"><span data-stu-id="8d86c-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="8d86c-106">El valor de este elemento debe establecerse en el espacio de nombres denominado en el \<wsdl:import> elemento que se va a excluir.</span><span class="sxs-lookup"><span data-stu-id="8d86c-106">The value of this element must be set to the namespace named in the \<wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="8d86c-107">Uso</span><span class="sxs-lookup"><span data-stu-id="8d86c-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="8d86c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8d86c-108">Attributes</span></span>

<span data-ttu-id="8d86c-109">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="8d86c-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8d86c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8d86c-110">Child elements</span></span>

<span data-ttu-id="8d86c-111">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="8d86c-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="8d86c-112">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="8d86c-112">Parent elements</span></span>



| <span data-ttu-id="8d86c-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="8d86c-113">Element</span></span>                         | <span data-ttu-id="8d86c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d86c-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="8d86c-115">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="8d86c-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="8d86c-116">Especifica un archivo WSDL que se procesará para obtener información del contrato.</span><span class="sxs-lookup"><span data-stu-id="8d86c-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="8d86c-117">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8d86c-117">Element information</span></span>



| <span data-ttu-id="8d86c-118">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="8d86c-118">Label</span></span> | <span data-ttu-id="8d86c-119">Value</span><span class="sxs-lookup"><span data-stu-id="8d86c-119">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="8d86c-120">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d86c-120">Minimum supported system</span></span><br/> | <span data-ttu-id="8d86c-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d86c-121">Windows Vista</span></span> |
| <span data-ttu-id="8d86c-122">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8d86c-122">Can be empty</span></span>                        | <span data-ttu-id="8d86c-123">Sí</span><span class="sxs-lookup"><span data-stu-id="8d86c-123">Yes</span></span>           |



 

 




