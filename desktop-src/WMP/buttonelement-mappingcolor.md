---
title: BUTTONELEMENT. mappingColor
description: El atributo mappingColor especifica o recupera la clave de color que identifica este BUTTONELEMENT en BUTTONGROUP.
ms.assetid: e7b1663c-3263-41d5-9a69-4cf1dcf0fc1f
keywords:
- BUTTONELEMENT. mappingColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.mappingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7318f01246578fe8ff34118427c95afb7b3bb098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698687"
---
# <a name="buttonelementmappingcolor"></a><span data-ttu-id="90d30-104">BUTTONELEMENT. mappingColor</span><span class="sxs-lookup"><span data-stu-id="90d30-104">BUTTONELEMENT.mappingColor</span></span>

<span data-ttu-id="90d30-105">El atributo **mappingColor** especifica o recupera la clave de color que identifica este **BUTTONELEMENT** en **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="90d30-105">The **mappingColor** attribute specifies or retrieves the color key that identifies this **BUTTONELEMENT** in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.mappingColor
```

## <a name="possible-values"></a><span data-ttu-id="90d30-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="90d30-106">Possible Values</span></span>

<span data-ttu-id="90d30-107">Este atributo es una **cadena** de lectura/escritura que contiene cualquier valor de color de Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="90d30-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="90d30-108">No tiene valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="90d30-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="90d30-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90d30-109">Remarks</span></span>

<span data-ttu-id="90d30-110">Este atributo especifica el color de la región en el grupo de botones **mappingImage** que corresponde a este elemento de botón.</span><span class="sxs-lookup"><span data-stu-id="90d30-110">This attribute specifies the color of the region in the button group **mappingImage** that corresponds to this button element.</span></span> <span data-ttu-id="90d30-111">Todos los clics en esta región se controlan mediante este elemento de botón.</span><span class="sxs-lookup"><span data-stu-id="90d30-111">All clicks on this region are handled by this button element.</span></span>

<span data-ttu-id="90d30-112">Si se especifica un color no válido, **BUTTONELEMENT** no se activa.</span><span class="sxs-lookup"><span data-stu-id="90d30-112">If an invalid color is specified, the **BUTTONELEMENT** is not activated.</span></span>

## <a name="examples"></a><span data-ttu-id="90d30-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="90d30-113">Examples</span></span>

<span data-ttu-id="90d30-114">El ejemplo siguiente es un archivo de definición de máscara completo que muestra cómo se usan algunos de los atributos **BUTTONELEMENT** .</span><span class="sxs-lookup"><span data-stu-id="90d30-114">The following sample is a complete skin definition file that illustrates how some of the **BUTTONELEMENT** attributes are used.</span></span> <span data-ttu-id="90d30-115">Se puede encontrar en el directorio Samples que se instaló con el SDK.</span><span class="sxs-lookup"><span data-stu-id="90d30-115">It can be found in the Samples directory that was installed with the SDK.</span></span>


```
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >
    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    />
    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "150"
    />
    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    >
      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />
      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />
    </BUTTONGROUP>
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="90d30-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90d30-116">Requirements</span></span>



| <span data-ttu-id="90d30-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="90d30-117">Requirement</span></span> | <span data-ttu-id="90d30-118">Value</span><span class="sxs-lookup"><span data-stu-id="90d30-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="90d30-119">Versión</span><span class="sxs-lookup"><span data-stu-id="90d30-119">Version</span></span><br/> | <span data-ttu-id="90d30-120">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="90d30-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="90d30-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="90d30-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90d30-122">**Referencia de color**</span><span class="sxs-lookup"><span data-stu-id="90d30-122">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="90d30-123">**BUTTONELEMENT (elemento)**</span><span class="sxs-lookup"><span data-stu-id="90d30-123">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="90d30-124">**BUTTONGROUP.mappingImage**</span><span class="sxs-lookup"><span data-stu-id="90d30-124">**BUTTONGROUP.mappingImage**</span></span>](buttongroup-mappingimage.md)
</dt> </dl>

 

 





