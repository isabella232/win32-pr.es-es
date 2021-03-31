---
description: Define el número de la capa de código que se va a generar.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: elemento layerNumber
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c22a20db7817e449b05c943c9016b6002f35b54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277117"
---
# <a name="layernumber-element"></a><span data-ttu-id="ba9aa-103">elemento layerNumber</span><span class="sxs-lookup"><span data-stu-id="ba9aa-103">layerNumber element</span></span>

<span data-ttu-id="ba9aa-104">Define el número de la capa de código que se va a generar.</span><span class="sxs-lookup"><span data-stu-id="ba9aa-104">Defines the number of the code layer to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="ba9aa-105">Uso</span><span class="sxs-lookup"><span data-stu-id="ba9aa-105">Usage</span></span>

``` syntax
<layerNumber/>
```

## <a name="attributes"></a><span data-ttu-id="ba9aa-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="ba9aa-106">Attributes</span></span>

<span data-ttu-id="ba9aa-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="ba9aa-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ba9aa-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ba9aa-108">Child elements</span></span>

<span data-ttu-id="ba9aa-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="ba9aa-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="ba9aa-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="ba9aa-110">Parent elements</span></span>



| <span data-ttu-id="ba9aa-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="ba9aa-111">Element</span></span>                                     | <span data-ttu-id="ba9aa-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba9aa-112">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba9aa-113">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="ba9aa-113">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="ba9aa-114">Elemento raíz de un archivo de script XML del generador de código de WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="ba9aa-114">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ba9aa-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba9aa-115">Remarks</span></span>

<span data-ttu-id="ba9aa-116">Los números de capa se utilizan en tablas en tiempo de ejecución para distinguir un nivel de código para otro.</span><span class="sxs-lookup"><span data-stu-id="ba9aa-116">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="ba9aa-117">WSDAPI utiliza código generado que tiene un número de capa de 0.</span><span class="sxs-lookup"><span data-stu-id="ba9aa-117">WSDAPI itself uses generated code that has a layer number of 0.</span></span>

<span data-ttu-id="ba9aa-118">Normalmente, este valor será 1, lo que indica que el código generado está en capas en la parte superior de WSDAPI y no en otra capa.</span><span class="sxs-lookup"><span data-stu-id="ba9aa-118">Typically, this value will be 1, indicating that the generated code is layered on top of WSDAPI and no other layer.</span></span> <span data-ttu-id="ba9aa-119">En algunos casos, se pueden usar números más altos.</span><span class="sxs-lookup"><span data-stu-id="ba9aa-119">In some cases, higher numbers may be used.</span></span> <span data-ttu-id="ba9aa-120">Por ejemplo, si una empresa produce código para una clase de dispositivo (capa numerada 1), es posible que un fabricante de hardware determinado desee agregar una capa 2 con número de capa adicional.</span><span class="sxs-lookup"><span data-stu-id="ba9aa-120">For example, if one company produces code for a device class (numbered layer 1), a particular hardware vendor may want to add an additional layer numbered layer 2.</span></span>

<span data-ttu-id="ba9aa-121">Los valores válidos, excepto en el caso del propio WSDAPI, son mayores que 0 y menores que 16.</span><span class="sxs-lookup"><span data-stu-id="ba9aa-121">Legal values, except in the case of WSDAPI itself are greater than 0 and less than 16.</span></span>

## <a name="element-information"></a><span data-ttu-id="ba9aa-122">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ba9aa-122">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="ba9aa-123">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba9aa-123">Minimum supported system</span></span><br/> | <span data-ttu-id="ba9aa-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba9aa-124">Windows Vista</span></span> |
| <span data-ttu-id="ba9aa-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ba9aa-125">Can be empty</span></span>                        | <span data-ttu-id="ba9aa-126">Sí</span><span class="sxs-lookup"><span data-stu-id="ba9aa-126">Yes</span></span>           |



 

 




