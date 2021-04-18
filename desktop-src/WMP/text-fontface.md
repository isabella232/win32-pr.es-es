---
title: TEXT. fontFace
description: El atributo fontFace especifica o recupera el tipo de letra para el control de texto.
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- Media Player de Windows TEXT. fontFace
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 183b25547e456cb90cac4d2137354679e13d8a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718814"
---
# <a name="textfontface"></a><span data-ttu-id="94123-104">TEXT. fontFace</span><span class="sxs-lookup"><span data-stu-id="94123-104">TEXT.fontFace</span></span>

<span data-ttu-id="94123-105">El atributo **fontFace** especifica o recupera el tipo de letra para el control de texto.</span><span class="sxs-lookup"><span data-stu-id="94123-105">The **fontFace** attribute specifies or retrieves the typeface for the Text control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="94123-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="94123-106">Possible Values</span></span>

<span data-ttu-id="94123-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="94123-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="94123-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94123-108">Remarks</span></span>

<span data-ttu-id="94123-109">Este atributo puede ser el nombre de cualquier fuente válida disponible en Windows.</span><span class="sxs-lookup"><span data-stu-id="94123-109">This attribute can be the name of any valid font available on Windows.</span></span> <span data-ttu-id="94123-110">Windows Media Player no admitirá la instalación de fuentes, así que elija una fuente que sepa que se encuentra en el sistema previsto.</span><span class="sxs-lookup"><span data-stu-id="94123-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="94123-111">Si el **fontFace** especificado no está disponible en el sistema del usuario, el control de texto tiene como valor predeterminado la fuente del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="94123-111">If the **fontFace** specified is not available on the user's system, the Text control defaults to the Windows system font.</span></span>

<span data-ttu-id="94123-112">Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .</span><span class="sxs-lookup"><span data-stu-id="94123-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="94123-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94123-113">Requirements</span></span>



| <span data-ttu-id="94123-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="94123-114">Requirement</span></span> | <span data-ttu-id="94123-115">Value</span><span class="sxs-lookup"><span data-stu-id="94123-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="94123-116">Versión</span><span class="sxs-lookup"><span data-stu-id="94123-116">Version</span></span><br/> | <span data-ttu-id="94123-117">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="94123-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94123-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="94123-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94123-119">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="94123-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="94123-120">**TEXT. FontSize**</span><span class="sxs-lookup"><span data-stu-id="94123-120">**TEXT.fontSize**</span></span>](text-fontsize.md)
</dt> </dl>

 

 





