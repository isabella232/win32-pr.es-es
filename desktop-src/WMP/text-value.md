---
title: TEXT. Value
description: El atributo value especifica o recupera el texto que se muestra en el control de texto.
ms.assetid: dbc50be2-ee18-4661-a343-9e906879aba0
keywords:
- Windows Media Player TEXT. Value
topic_type:
- apiref
api_name:
- TEXT.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d87f688f7afffeb588a37ac13ebff4cdc7cc105
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649765"
---
# <a name="textvalue"></a><span data-ttu-id="a6c53-104">TEXT. Value</span><span class="sxs-lookup"><span data-stu-id="a6c53-104">TEXT.value</span></span>

<span data-ttu-id="a6c53-105">El atributo **Value** especifica o recupera el texto que se muestra en el control de texto.</span><span class="sxs-lookup"><span data-stu-id="a6c53-105">The **value** attribute specifies or retrieves the text that is displayed in the Text control.</span></span>

``` syntax
        elementID.value
```

## <a name="possible-values"></a><span data-ttu-id="a6c53-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="a6c53-106">Possible Values</span></span>

<span data-ttu-id="a6c53-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="a6c53-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6c53-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6c53-108">Remarks</span></span>

<span data-ttu-id="a6c53-109">Si el ancho del control de texto no es suficiente para contener el texto proporcionado, se recorta el texto y se muestra un botón de puntos suspensivos para ilustrar el hecho.</span><span class="sxs-lookup"><span data-stu-id="a6c53-109">If the width of the Text control is insufficient to contain the text provided, the text is cropped, and an ellipsis is shown to illustrate the fact.</span></span> <span data-ttu-id="a6c53-110">Si no se ha establecido el atributo **ToolTip** , el texto completo aparecerá como información sobre herramientas cuando el cursor se mantenga sobre el control.</span><span class="sxs-lookup"><span data-stu-id="a6c53-110">If the **toolTip** attribute has not been set, the complete text will then appear as a ToolTip when the cursor hovers over the control.</span></span>

<span data-ttu-id="a6c53-111">Si no se especifica un ancho, el ancho predeterminado del control es el ancho de la cadena.</span><span class="sxs-lookup"><span data-stu-id="a6c53-111">If a width is not specified, the default width for the control is the width of the string.</span></span>

<span data-ttu-id="a6c53-112">Si no se especifica el alto del control, el alto predeterminado es una línea.</span><span class="sxs-lookup"><span data-stu-id="a6c53-112">If the height of the control is not specified, the default height is one line.</span></span>

<span data-ttu-id="a6c53-113">Si el atributo **WordWrap** está establecido en true y el alto del control es suficiente para alojar otra línea de texto, el texto se ajusta a una línea posterior.</span><span class="sxs-lookup"><span data-stu-id="a6c53-113">If the **wordWrap** attribute is set to true and the height of the control is enough to accommodate another line of text, the text wraps to a subsequent line.</span></span> <span data-ttu-id="a6c53-114">El ajuste solo se produce entre palabras.</span><span class="sxs-lookup"><span data-stu-id="a6c53-114">Wrapping only occurs between words.</span></span> <span data-ttu-id="a6c53-115">También se pueden forzar saltos de línea, como se explica en **WordWrap**.</span><span class="sxs-lookup"><span data-stu-id="a6c53-115">Line breaks may also be forced, as explained under **wordWrap**.</span></span>

## <a name="examples"></a><span data-ttu-id="a6c53-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a6c53-116">Examples</span></span>

<span data-ttu-id="a6c53-117">El ejemplo siguiente es un archivo de definición de máscara completo que muestra cómo se utilizan los atributos del elemento de **texto** .</span><span class="sxs-lookup"><span data-stu-id="a6c53-117">The following sample is a complete skin definition file that illustrates how the attributes of the **TEXT** element are used.</span></span> <span data-ttu-id="a6c53-118">Se puede encontrar en el directorio Samples que se instaló con el SDK.</span><span class="sxs-lookup"><span data-stu-id="a6c53-118">It can be found in the Samples directory that was installed with the SDK.</span></span>


```C++
<THEME>
  <VIEW
    height = "175"
  >
    <TEXT 
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Play"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.play"
      onClick = "JScript: player.URL='https://proseware.com/laure.wma';"
    />
    <TEXT
      top = "50"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Stop"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.stop"
      onClick = "JScript: player.controls.stop();"
    />
    <TEXT
      top = "100"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "Close"
      cursor = "hand"
      onClick = "JScript: view.close();"
    />
    <TEXT
      top = "30"
      left = "120"
      width = "200"
      fontSize = "20"
      fontStyle = "Underline"
      justification = "Center"
      value = "Volume"
    />
    <TEXT
      top = "60"
      left = "120"
      width = "200"
      fontSize = "40"
      justification = "Center"
      value = "wmpprop:player.settings.volume"
    />
    <TEXT
      top = "65"
      left = "142"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "-"
      cursor = "hand"
      toolTip = "decrease volume"
      onClick = "player.settings.volume = player.settings.volume - 5"
    />
    <TEXT
      top = "65"
      left = "260"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "+"
      cursor = "hand"
      toolTip = "increase volume"
      onClick = "player.settings.volume = player.settings.volume + 5"
    />
    <TEXT
      top = "155"
      width = "300"
      height = "30"
      fontFace = "System"
      backgroundColor = "blue"
      foregroundColor = "white"
      justification = "Center"
      scrolling = "true"
      scrollingAmount = "1"
      scrollingDelay = "50"
      value = "wmpprop:player.status"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="a6c53-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6c53-119">Requirements</span></span>



| <span data-ttu-id="a6c53-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6c53-120">Requirement</span></span> | <span data-ttu-id="a6c53-121">Value</span><span class="sxs-lookup"><span data-stu-id="a6c53-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a6c53-122">Versión</span><span class="sxs-lookup"><span data-stu-id="a6c53-122">Version</span></span><br/> | <span data-ttu-id="a6c53-123">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a6c53-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a6c53-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6c53-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6c53-125">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="a6c53-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="a6c53-126">**TEXTO. toolTip**</span><span class="sxs-lookup"><span data-stu-id="a6c53-126">**TEXT.toolTip**</span></span>](text-tooltip.md)
</dt> <dt>

[<span data-ttu-id="a6c53-127">**TEXT. wordWrap**</span><span class="sxs-lookup"><span data-stu-id="a6c53-127">**TEXT.wordWrap**</span></span>](text-wordwrap.md)
</dt> </dl>

 

 





