---
title: ClosedCaption.SAMIStyle
description: La propiedad SAMIStyle especifica o recupera el estilo de subtítulos (CC).
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- ClosedCaption. SAMIStyle Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyle
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe81c2c2c4f4504d6167abe538c52ab769550a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699535"
---
# <a name="closedcaptionsamistyle"></a><span data-ttu-id="f10e7-104">ClosedCaption.SAMIStyle</span><span class="sxs-lookup"><span data-stu-id="f10e7-104">ClosedCaption.SAMIStyle</span></span>

<span data-ttu-id="f10e7-105">La propiedad **SAMIStyle** especifica o recupera el estilo de subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="f10e7-105">The **SAMIStyle** property specifies or retrieves the closed captioning style.</span></span>

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a><span data-ttu-id="f10e7-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="f10e7-106">Possible Values</span></span>

<span data-ttu-id="f10e7-107">Esta propiedad es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="f10e7-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f10e7-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f10e7-108">Remarks</span></span>

<span data-ttu-id="f10e7-109">Un archivo SAMI puede contener varias definiciones de estilo de formato.</span><span class="sxs-lookup"><span data-stu-id="f10e7-109">A SAMI file can contain several format style definitions.</span></span> <span data-ttu-id="f10e7-110">Los estilos SAMI se definen entre las etiquetas <STYLE> y </STYLE> del archivo Sami.</span><span class="sxs-lookup"><span data-stu-id="f10e7-110">SAMI styles are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="f10e7-111">Un estilo se define con una cadena de texto precedida por un \# carácter.</span><span class="sxs-lookup"><span data-stu-id="f10e7-111">A style is defined with a text string preceded by a \# character.</span></span> <span data-ttu-id="f10e7-112">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f10e7-112">For example:</span></span>


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



<span data-ttu-id="f10e7-113">Especifica un estilo que genera una fuente determinada.</span><span class="sxs-lookup"><span data-stu-id="f10e7-113">This specifies a style that produces a particular font.</span></span>

<span data-ttu-id="f10e7-114">Si no se especifica ningún estilo SAMI, se usa de forma predeterminada el primer estilo definido en el archivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="f10e7-114">If no SAMI style is specified, the first style defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="f10e7-115">**Windows Media Player 10 Mobile:** Esta propiedad es de solo lectura y siempre devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="f10e7-115">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="f10e7-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f10e7-116">Examples</span></span>

<span data-ttu-id="f10e7-117">En el siguiente ejemplo de JScript se crea un elemento SELECT de HTML que usa *closedCaption*. **SAMIStyle** para cambiar la apariencia del texto de la leyenda cerrada.</span><span class="sxs-lookup"><span data-stu-id="f10e7-117">The following JScript example creates an HTML SELECT element that uses *closedCaption*.**SAMIStyle** to change the appearance of the closed caption text.</span></span> <span data-ttu-id="f10e7-118">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f10e7-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCMode  NAME = "CCMode"  LANGUAGE = "JScript"

       /* Change the text style when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMIStyle = CCMode.value;
        ">

       /* Fill the SELECT list with options, set the default to Strong. */
        <OPTION VALUE = "Normal">Normal
        <OPTION VALUE = "Small">Small 
        <OPTION VALUE = "Big Bold Italic" SELECTED>Strong
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="f10e7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f10e7-119">Requirements</span></span>



| <span data-ttu-id="f10e7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f10e7-120">Requirement</span></span> | <span data-ttu-id="f10e7-121">Value</span><span class="sxs-lookup"><span data-stu-id="f10e7-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f10e7-122">Versión</span><span class="sxs-lookup"><span data-stu-id="f10e7-122">Version</span></span><br/> | <span data-ttu-id="f10e7-123">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f10e7-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f10e7-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f10e7-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="f10e7-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f10e7-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f10e7-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f10e7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f10e7-127">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="f10e7-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="f10e7-128">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="f10e7-128">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





