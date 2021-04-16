---
title: AmbientAttributes.nineGridMargins
description: El atributo nineGridMargins especifica el ancho del margen para el escalado no uniforme del elemento de máscara.
ms.assetid: b8a7efd0-6c12-4436-9d53-0dcfa1600aa5
keywords:
- AmbientAttributes. nineGridMargins Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.nineGridMargins
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cf77c1fcfdb64fb9e4b0dde8753572255c17eda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699431"
---
# <a name="ambientattributesninegridmargins"></a><span data-ttu-id="a3da0-104">AmbientAttributes.nineGridMargins</span><span class="sxs-lookup"><span data-stu-id="a3da0-104">AmbientAttributes.nineGridMargins</span></span>

<span data-ttu-id="a3da0-105">El atributo **nineGridMargins** especifica el ancho del margen para el escalado no uniforme del elemento de máscara.</span><span class="sxs-lookup"><span data-stu-id="a3da0-105">The **nineGridMargins** attribute specifies margin widths for non-uniform scaling of the skin element.</span></span>

``` syntax
        elementID.nineGridMargins
```

## <a name="possible-values"></a><span data-ttu-id="a3da0-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="a3da0-106">Possible Values</span></span>

<span data-ttu-id="a3da0-107">Este atributo es una **cadena** de lectura/escritura que contiene el ancho de los márgenes en el formato "*widthLeft*,*widthTop*,*widthRight*,*widthBottom*".</span><span class="sxs-lookup"><span data-stu-id="a3da0-107">This attribute is a read/write **String** that contains the widths of the margins in the form "*widthLeft*,*widthTop*,*widthRight*,*widthBottom*".</span></span> <span data-ttu-id="a3da0-108">Cada valor de ancho es un número que representa el ancho, en píxeles, de un margen para la cuadrícula nueve.</span><span class="sxs-lookup"><span data-stu-id="a3da0-108">Each width value is a number representing the width, in pixels, of a margin for the nine grid.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3da0-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3da0-109">Remarks</span></span>

<span data-ttu-id="a3da0-110">Una *cuadrícula de nueve* es una técnica que se usa para dividir los elementos de la interfaz de usuario en nueve regiones rectangulares organizadas en una matriz de 3 por 3.</span><span class="sxs-lookup"><span data-stu-id="a3da0-110">A *nine grid* is a technique used to divide user interface elements into nine rectangular regions arranged in a 3 by 3 matrix.</span></span> <span data-ttu-id="a3da0-111">Cuando se cambia el tamaño de un elemento, las nueve regiones de la cuadrícula pueden escalarse por un factor diferente.</span><span class="sxs-lookup"><span data-stu-id="a3da0-111">When an element is resized, the nine grid regions can each scale by a different factor.</span></span>

<span data-ttu-id="a3da0-112">Cada uno de los cuatro valores de ancho que especifique representa el ancho de una fila o columna de tres regiones adyacentes.</span><span class="sxs-lookup"><span data-stu-id="a3da0-112">Each of the four width values you specify represents the width of a row or column of three adjacent regions.</span></span> <span data-ttu-id="a3da0-113">Cada fila o columna forma el lado izquierdo, la parte superior, el lado derecho o la parte inferior de la cuadrícula nueve.</span><span class="sxs-lookup"><span data-stu-id="a3da0-113">Each row or column forms the left side, top, right side, or bottom of the nine grid.</span></span>

<span data-ttu-id="a3da0-114">[AmbientAttributes. resizeImages](ambientattributes-resizeimages.md) debe establecerse en true para que este atributo funcione.</span><span class="sxs-lookup"><span data-stu-id="a3da0-114">[AmbientAttributes.resizeImages](ambientattributes-resizeimages.md) must be set to true for this attribute to work.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3da0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3da0-115">Requirements</span></span>



| <span data-ttu-id="a3da0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3da0-116">Requirement</span></span> | <span data-ttu-id="a3da0-117">Value</span><span class="sxs-lookup"><span data-stu-id="a3da0-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="a3da0-118">Versión</span><span class="sxs-lookup"><span data-stu-id="a3da0-118">Version</span></span><br/> | <span data-ttu-id="a3da0-119">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="a3da0-119">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a3da0-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3da0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3da0-121">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="a3da0-121">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





