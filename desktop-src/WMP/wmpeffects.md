---
title: WMPEFFECTS
description: Se trata de efectos predefinidos con los siguientes valores predeterminados.
ms.assetid: ebee17e3-96b0-4748-b69f-4ff41d0bc386
keywords:
- WMPEFFECTS Windows Media Player
topic_type:
- apiref
api_name:
- WMPEFFECTS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: db3e35143242c5ca7888ffc50feb006f586e68d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718848"
---
# <a name="wmpeffects"></a><span data-ttu-id="3a632-104">WMPEFFECTS</span><span class="sxs-lookup"><span data-stu-id="3a632-104">WMPEFFECTS</span></span>

<span data-ttu-id="3a632-105">Se trata de **efectos** predefinidos con los siguientes valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="3a632-105">This is a predefined **EFFECTS** with the following default values.</span></span>

``` syntax
horizontalAlignment="stretch"
verticalAlignment="stretch"
height="200"
width="250"
tabStop="false"
onclick="next();"
```

## <a name="remarks"></a><span data-ttu-id="3a632-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a632-106">Remarks</span></span>

<span data-ttu-id="3a632-107">Se creará un elemento **Effects** que recorrerá los valores preestablecidos de visualización cuando el usuario haga clic en el control.</span><span class="sxs-lookup"><span data-stu-id="3a632-107">This will create an **EFFECTS** element that will step through the visualization presets when the user clicks the control.</span></span> <span data-ttu-id="3a632-108">También se extienden las visualizaciones cuando se cambia el tamaño del reproductor.</span><span class="sxs-lookup"><span data-stu-id="3a632-108">It will also stretch the visualizations when the player is resized.</span></span>

<span data-ttu-id="3a632-109">El valor preestablecido de visualización inicial mostrado es el seleccionado en el menú **Ver** en **visualizaciones**.</span><span class="sxs-lookup"><span data-stu-id="3a632-109">The initial visualization preset shown is the one selected on the **View** menu under **Visualizations**.</span></span> <span data-ttu-id="3a632-110">Al cambiar la selección en este menú, se cambia automáticamente el valor preestablecido que muestra este elemento cuando el reproductor está en modo de máscara.</span><span class="sxs-lookup"><span data-stu-id="3a632-110">Changing the selection on this menu will automatically change the preset displayed by this element when the Player is in skin mode.</span></span> <span data-ttu-id="3a632-111">El menú **Ver** se muestra en el modo completo del reproductor o cuando el atributo **View. TitleBar** está establecido en true en una máscara.</span><span class="sxs-lookup"><span data-stu-id="3a632-111">The **View** menu is displayed in the full mode of the Player or when the **VIEW.titleBar** attribute is set to true in a skin.</span></span>

<span data-ttu-id="3a632-112">Todas las propiedades de este elemento **Effects** se pueden invalidar si se especifican de forma explícita.</span><span class="sxs-lookup"><span data-stu-id="3a632-112">All properties of this **EFFECTS** element can be overridden by explicitly specifying them.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a632-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a632-113">Requirements</span></span>



| <span data-ttu-id="3a632-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a632-114">Requirement</span></span> | <span data-ttu-id="3a632-115">Value</span><span class="sxs-lookup"><span data-stu-id="3a632-115">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="3a632-116">Versión</span><span class="sxs-lookup"><span data-stu-id="3a632-116">Version</span></span><br/> | <span data-ttu-id="3a632-117">Windows Media Player 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3a632-117">Windows Media Player 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a632-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a632-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a632-119">**EFFECTs, elemento**</span><span class="sxs-lookup"><span data-stu-id="3a632-119">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





