---
description: Define el prefijo que se usará en el código generado para garantizar la unidad de los símbolos generados.
ms.assetid: 50cb443a-15ae-4f8f-b5f7-b8708810a6c3
title: elemento layerPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98970013c72600affd7d4d9e7a71781f477cd87d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994702"
---
# <a name="layerprefix-element"></a><span data-ttu-id="73902-103">elemento layerPrefix</span><span class="sxs-lookup"><span data-stu-id="73902-103">layerPrefix element</span></span>

<span data-ttu-id="73902-104">Define el prefijo que se usará en el código generado para garantizar la unidad de los símbolos generados.</span><span class="sxs-lookup"><span data-stu-id="73902-104">Defines the prefix to use in the generated code to assure uniqueness of generated symbols.</span></span>

## <a name="usage"></a><span data-ttu-id="73902-105">Uso</span><span class="sxs-lookup"><span data-stu-id="73902-105">Usage</span></span>

``` syntax
<layerPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="73902-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="73902-106">Attributes</span></span>

<span data-ttu-id="73902-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="73902-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="73902-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="73902-108">Child elements</span></span>

<span data-ttu-id="73902-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="73902-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="73902-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="73902-110">Parent elements</span></span>



| <span data-ttu-id="73902-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="73902-111">Element</span></span>                                     | <span data-ttu-id="73902-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="73902-112">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="73902-113">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="73902-113">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="73902-114">Elemento raíz de un archivo de script XML del generador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="73902-114">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="73902-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="73902-115">Remarks</span></span>

<span data-ttu-id="73902-116">Cada script generador de código debe definir una cadena de prefijo única para los módulos creados.</span><span class="sxs-lookup"><span data-stu-id="73902-116">Each code generator script should define a unique prefix string for the modules created.</span></span> <span data-ttu-id="73902-117">Por ejemplo, los scripts de fotogramas de imagen usan un prefijo de "PFDEMO".</span><span class="sxs-lookup"><span data-stu-id="73902-117">For example, the Picture Frame scripts use a prefix of "PFDEMO".</span></span>

<span data-ttu-id="73902-118">WSDAPI usa el prefijo "WSD".</span><span class="sxs-lookup"><span data-stu-id="73902-118">WSDAPI uses the prefix "WSD".</span></span>

## <a name="element-information"></a><span data-ttu-id="73902-119">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="73902-119">Element information</span></span>



| <span data-ttu-id="73902-120">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="73902-120">Label</span></span> | <span data-ttu-id="73902-121">Value</span><span class="sxs-lookup"><span data-stu-id="73902-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="73902-122">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73902-122">Minimum supported system</span></span><br/> | <span data-ttu-id="73902-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73902-123">Windows Vista</span></span> |
| <span data-ttu-id="73902-124">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="73902-124">Can be empty</span></span>                        | <span data-ttu-id="73902-125">Sí</span><span class="sxs-lookup"><span data-stu-id="73902-125">Yes</span></span>           |



 

 




