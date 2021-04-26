---
description: Define el número de la capa de código que se va a generar.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: elemento layerNumber
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c33ee4468ab81f030bfd8b49dfe104bbe76248
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995492"
---
# <a name="layernumber-element"></a><span data-ttu-id="8d1be-103">elemento layerNumber</span><span class="sxs-lookup"><span data-stu-id="8d1be-103">layerNumber element</span></span>

<span data-ttu-id="8d1be-104">Define el número de la capa de código que se va a generar.</span><span class="sxs-lookup"><span data-stu-id="8d1be-104">Defines the number of the code layer to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="8d1be-105">Uso</span><span class="sxs-lookup"><span data-stu-id="8d1be-105">Usage</span></span>

``` syntax
<layerNumber/>
```

## <a name="attributes"></a><span data-ttu-id="8d1be-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="8d1be-106">Attributes</span></span>

<span data-ttu-id="8d1be-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="8d1be-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8d1be-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8d1be-108">Child elements</span></span>

<span data-ttu-id="8d1be-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="8d1be-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="8d1be-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="8d1be-110">Parent elements</span></span>



| <span data-ttu-id="8d1be-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="8d1be-111">Element</span></span>                                     | <span data-ttu-id="8d1be-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d1be-112">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d1be-113">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="8d1be-113">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="8d1be-114">Elemento raíz de un archivo de script XML del generador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="8d1be-114">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8d1be-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8d1be-115">Remarks</span></span>

<span data-ttu-id="8d1be-116">Los números de capa se usan en tablas en tiempo de ejecución para distinguir una capa de código para otra.</span><span class="sxs-lookup"><span data-stu-id="8d1be-116">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="8d1be-117">El propio WSDAPI usa código generado que tiene un número de capa de 0.</span><span class="sxs-lookup"><span data-stu-id="8d1be-117">WSDAPI itself uses generated code that has a layer number of 0.</span></span>

<span data-ttu-id="8d1be-118">Normalmente, este valor será 1, lo que indica que el código generado está en capas sobre WSDAPI y ninguna otra capa.</span><span class="sxs-lookup"><span data-stu-id="8d1be-118">Typically, this value will be 1, indicating that the generated code is layered on top of WSDAPI and no other layer.</span></span> <span data-ttu-id="8d1be-119">En algunos casos, se pueden usar números más altos.</span><span class="sxs-lookup"><span data-stu-id="8d1be-119">In some cases, higher numbers may be used.</span></span> <span data-ttu-id="8d1be-120">Por ejemplo, si una empresa genera código para una clase de dispositivo (nivel numerado 1), es posible que un proveedor de hardware determinado quiera agregar una capa adicional numerada de capa 2.</span><span class="sxs-lookup"><span data-stu-id="8d1be-120">For example, if one company produces code for a device class (numbered layer 1), a particular hardware vendor may want to add an additional layer numbered layer 2.</span></span>

<span data-ttu-id="8d1be-121">Los valores legales, excepto en el caso del propio WSDAPI, son mayores que 0 y menores que 16.</span><span class="sxs-lookup"><span data-stu-id="8d1be-121">Legal values, except in the case of WSDAPI itself are greater than 0 and less than 16.</span></span>

## <a name="element-information"></a><span data-ttu-id="8d1be-122">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8d1be-122">Element information</span></span>



| <span data-ttu-id="8d1be-123">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="8d1be-123">Label</span></span> | <span data-ttu-id="8d1be-124">Value</span><span class="sxs-lookup"><span data-stu-id="8d1be-124">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="8d1be-125">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d1be-125">Minimum supported system</span></span><br/> | <span data-ttu-id="8d1be-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d1be-126">Windows Vista</span></span> |
| <span data-ttu-id="8d1be-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8d1be-127">Can be empty</span></span>                        | <span data-ttu-id="8d1be-128">Sí</span><span class="sxs-lookup"><span data-stu-id="8d1be-128">Yes</span></span>           |



 

 




