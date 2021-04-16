---
title: TEXT. wordWrap
description: El atributo wordWrap especifica o recupera un valor que indica si el ajuste de palabras está habilitado o deshabilitado.
ms.assetid: 3bb127d8-42f1-4167-986a-d41690cb5647
keywords:
- TEXT. wordWrap Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.wordWrap
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2b4d030a7e9efdda1bc7503ae3bf8eb5985401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650088"
---
# <a name="textwordwrap"></a><span data-ttu-id="8d9bf-104">TEXT. wordWrap</span><span class="sxs-lookup"><span data-stu-id="8d9bf-104">TEXT.wordWrap</span></span>

<span data-ttu-id="8d9bf-105">El atributo **WordWrap** especifica o recupera un valor que indica si el ajuste de palabras está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8d9bf-105">The **wordWrap** attribute specifies or retrieves a value indicating whether word wrap is enabled or disabled.</span></span>

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a><span data-ttu-id="8d9bf-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="8d9bf-106">Possible Values</span></span>

<span data-ttu-id="8d9bf-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="8d9bf-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="8d9bf-108">Value</span><span class="sxs-lookup"><span data-stu-id="8d9bf-108">Value</span></span> | <span data-ttu-id="8d9bf-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d9bf-109">Description</span></span>                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d9bf-110">true</span><span class="sxs-lookup"><span data-stu-id="8d9bf-110">true</span></span>  | <span data-ttu-id="8d9bf-111">El ajuste de palabra está habilitado.</span><span class="sxs-lookup"><span data-stu-id="8d9bf-111">Word wrap is enabled.</span></span>                                                                             |
| <span data-ttu-id="8d9bf-112">false</span><span class="sxs-lookup"><span data-stu-id="8d9bf-112">false</span></span> | <span data-ttu-id="8d9bf-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8d9bf-113">Default.</span></span> <span data-ttu-id="8d9bf-114">El ajuste de palabra está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8d9bf-114">Word wrap is disabled.</span></span> <span data-ttu-id="8d9bf-115">Si el texto no cabe en el control, el texto se recorta.</span><span class="sxs-lookup"><span data-stu-id="8d9bf-115">If the text does not fit within the control, the text is cropped.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8d9bf-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d9bf-116">Remarks</span></span>

<span data-ttu-id="8d9bf-117">El control de texto no separa palabras.</span><span class="sxs-lookup"><span data-stu-id="8d9bf-117">The Text control does not split words apart.</span></span> <span data-ttu-id="8d9bf-118">Si una palabra se extiende más allá del ancho del control, se emplea el ajuste automático de línea para colocar la palabra en la línea siguiente.</span><span class="sxs-lookup"><span data-stu-id="8d9bf-118">If a word extends beyond the width of the control, word wrap is employed to move the word to the next line.</span></span> <span data-ttu-id="8d9bf-119">Si una sola palabra es más larga que el ancho del control, esa palabra se recorta y ocupa una sola línea.</span><span class="sxs-lookup"><span data-stu-id="8d9bf-119">If a single word is longer than the control width, that word is clipped and occupies a single line.</span></span>

<span data-ttu-id="8d9bf-120">Si no se especifica el atributo **width** , se omite **WordWrap** y se cambia el tamaño del control de texto en lugar de ajustar el texto.</span><span class="sxs-lookup"><span data-stu-id="8d9bf-120">If the **width** attribute is not specified, **wordWrap** is ignored and the Text control will resize rather than wrapping the text.</span></span>

<span data-ttu-id="8d9bf-121">Si se desean saltos de línea en ubicaciones concretas, se deben especificar explícitamente en el **valor** mediante "&\# 13;" o " \\ r".</span><span class="sxs-lookup"><span data-stu-id="8d9bf-121">If line breaks are desired in particular locations, they must be explicitly specified in **value** using "&\#13;" or "\\r".</span></span> <span data-ttu-id="8d9bf-122">Si se usa el último formulario al especificar el valor directamente, la cadena debe ir precedida de "JScript:" y el valor real debe estar rodeado por comillas simples, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="8d9bf-122">If the latter form is used when specifying the value directly, the string must be prefixed with "JScript:" and the actual value must be surrounded by single quotes, as shown below.</span></span> <span data-ttu-id="8d9bf-123">Esto no es necesario si el valor se establece dinámicamente desde un controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="8d9bf-123">This is not necessary if the value is set dynamically from within an event handler.</span></span>

<span data-ttu-id="8d9bf-124">Si **WordWrap** está establecido en true y no se especifica la **información sobre herramientas** , la información sobre herramientas mostrará el texto completo del atributo **Value** .</span><span class="sxs-lookup"><span data-stu-id="8d9bf-124">If **wordWrap** is set to true and **toolTip** is not specified, the ToolTip will display the full text of the **value** attribute.</span></span> <span data-ttu-id="8d9bf-125">Si no se desea información sobre herramientas, establezca la **información sobre herramientas** en "" (cadena vacía).</span><span class="sxs-lookup"><span data-stu-id="8d9bf-125">If no ToolTip is desired, set **toolTip** to "" (empty string).</span></span>

## <a name="examples"></a><span data-ttu-id="8d9bf-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8d9bf-126">Examples</span></span>


```C++
<THEME>
  <VIEW>
    <TEXT
      width = "50"
      height = "200"
      wordWrap = "true"
      backgroundColor = "blue"
      foregroundColor = "white"
      value = "This is a test.&#13;&#13;It is only a test."
    />
    <TEXT
      width = "50"
      height = "200"
      left = "100"
      wordWrap = "true"
      backgroundColor = "green"
      foregroundColor = "white"
      value = "JScript:'This is a test.\r\rIt is only a test.'"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="8d9bf-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d9bf-127">Requirements</span></span>



| <span data-ttu-id="8d9bf-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d9bf-128">Requirement</span></span> | <span data-ttu-id="8d9bf-129">Value</span><span class="sxs-lookup"><span data-stu-id="8d9bf-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8d9bf-130">Versión</span><span class="sxs-lookup"><span data-stu-id="8d9bf-130">Version</span></span><br/> | <span data-ttu-id="8d9bf-131">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8d9bf-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8d9bf-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d9bf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d9bf-133">**AmbientAttributes. width**</span><span class="sxs-lookup"><span data-stu-id="8d9bf-133">**AmbientAttributes.width**</span></span>](ambientattributes-width.md)
</dt> <dt>

[<span data-ttu-id="8d9bf-134">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="8d9bf-134">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="8d9bf-135">**TEXTO. toolTip**</span><span class="sxs-lookup"><span data-stu-id="8d9bf-135">**TEXT.toolTip**</span></span>](text-tooltip.md)
</dt> <dt>

[<span data-ttu-id="8d9bf-136">**TEXT. Value**</span><span class="sxs-lookup"><span data-stu-id="8d9bf-136">**TEXT.value**</span></span>](text-value.md)
</dt> </dl>

 

 





