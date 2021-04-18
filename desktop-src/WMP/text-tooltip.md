---
title: TEXTO. toolTip
description: El atributo toolTip especifica o recupera el texto de información sobre herramientas para el control de texto.
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- TEXT. toolTip Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b064f2abefd07ec65a82069196b1012561699b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679505"
---
# <a name="texttooltip"></a><span data-ttu-id="bfca9-104">TEXTO. toolTip</span><span class="sxs-lookup"><span data-stu-id="bfca9-104">TEXT.toolTip</span></span>

<span data-ttu-id="bfca9-105">El atributo **ToolTip** especifica o recupera el texto de información sobre herramientas para el control de texto.</span><span class="sxs-lookup"><span data-stu-id="bfca9-105">The **toolTip** attribute specifies or retrieves the ToolTip text for the text control.</span></span>

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a><span data-ttu-id="bfca9-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="bfca9-106">Possible Values</span></span>

<span data-ttu-id="bfca9-107">Este atributo es una **cadena** de lectura/escritura con una longitud máxima de 1024 caracteres.</span><span class="sxs-lookup"><span data-stu-id="bfca9-107">This attribute is a read/write **String** with a maximum length of 1024 characters.</span></span> <span data-ttu-id="bfca9-108">No tiene valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bfca9-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfca9-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfca9-109">Remarks</span></span>

<span data-ttu-id="bfca9-110">Si no se especifica este atributo y el texto del atributo de **valor** se trunca en el control de texto, o el valor de **WordWrap** se establece en true, la información sobre herramientas mostrará el texto completo del atributo **Value** .</span><span class="sxs-lookup"><span data-stu-id="bfca9-110">If this attribute is not specified, and the text in the **value** attribute is truncated in the Text control, or **wordWrap** is set to true, the ToolTip will display the full text of the **value** attribute.</span></span>

<span data-ttu-id="bfca9-111">Cuando este atributo se establece en "" (cadena vacía), no se muestra ninguna información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="bfca9-111">When this attribute is set to "" (empty string), no ToolTip is displayed.</span></span>

<span data-ttu-id="bfca9-112">Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .</span><span class="sxs-lookup"><span data-stu-id="bfca9-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfca9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfca9-113">Requirements</span></span>



| <span data-ttu-id="bfca9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfca9-114">Requirement</span></span> | <span data-ttu-id="bfca9-115">Value</span><span class="sxs-lookup"><span data-stu-id="bfca9-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="bfca9-116">Versión</span><span class="sxs-lookup"><span data-stu-id="bfca9-116">Version</span></span><br/> | <span data-ttu-id="bfca9-117">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="bfca9-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bfca9-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfca9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfca9-119">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="bfca9-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="bfca9-120">**TEXT. Value**</span><span class="sxs-lookup"><span data-stu-id="bfca9-120">**TEXT.value**</span></span>](text-value.md)
</dt> <dt>

[<span data-ttu-id="bfca9-121">**TEXT. wordWrap**</span><span class="sxs-lookup"><span data-stu-id="bfca9-121">**TEXT.wordWrap**</span></span>](text-wordwrap.md)
</dt> </dl>

 

 





