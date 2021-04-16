---
title: LISTBOX. fontFace
description: El atributo fontFace especifica o recupera la fuente para el control de cuadro de lista.
ms.assetid: 15e3180a-6e1e-4654-a0bb-164d66a86a26
keywords:
- LISTBOX. fontFace Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c03c367001b307dd8bd5059ec7e3f4a0b364e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699637"
---
# <a name="listboxfontface"></a><span data-ttu-id="262ca-104">LISTBOX. fontFace</span><span class="sxs-lookup"><span data-stu-id="262ca-104">LISTBOX.fontFace</span></span>

<span data-ttu-id="262ca-105">El atributo **fontFace** especifica o recupera la fuente para el control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="262ca-105">The **fontFace** attribute specifies or retrieves the font for the list box control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="262ca-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="262ca-106">Possible Values</span></span>

<span data-ttu-id="262ca-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="262ca-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="262ca-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="262ca-108">Remarks</span></span>

<span data-ttu-id="262ca-109">Este atributo puede ser el nombre de cualquier fuente válida disponible en Windows.</span><span class="sxs-lookup"><span data-stu-id="262ca-109">This attribute can be the name of any valid font available in Windows.</span></span> <span data-ttu-id="262ca-110">Windows Media Player no admitirá la instalación de fuentes, así que elija una fuente que sepa que se encuentra en el sistema previsto.</span><span class="sxs-lookup"><span data-stu-id="262ca-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="262ca-111">Si el **fontFace** especificado no está disponible en el sistema del usuario, el control de cuadro de lista tiene como valor predeterminado la fuente del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="262ca-111">If the **fontFace** specified is not available on the user's system, the list box control defaults to the Windows system font.</span></span> <span data-ttu-id="262ca-112">El valor predeterminado para los sistemas en inglés es "Tahoma".</span><span class="sxs-lookup"><span data-stu-id="262ca-112">The default value for English-language systems is "Tahoma".</span></span> <span data-ttu-id="262ca-113">En el caso de los sistemas internacionales, el valor predeterminado se carga desde un archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="262ca-113">For international systems, the default is loaded from a resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="262ca-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="262ca-114">Requirements</span></span>



| <span data-ttu-id="262ca-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="262ca-115">Requirement</span></span> | <span data-ttu-id="262ca-116">Value</span><span class="sxs-lookup"><span data-stu-id="262ca-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="262ca-117">Versión</span><span class="sxs-lookup"><span data-stu-id="262ca-117">Version</span></span><br/> | <span data-ttu-id="262ca-118">Windows Media Player para Windows XP o posterior</span><span class="sxs-lookup"><span data-stu-id="262ca-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="262ca-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="262ca-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="262ca-120">**Elemento LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="262ca-120">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="262ca-121">**LISTBOX. FontSize**</span><span class="sxs-lookup"><span data-stu-id="262ca-121">**LISTBOX.fontSize**</span></span>](listbox-fontsize.md)
</dt> <dt>

[<span data-ttu-id="262ca-122">**LISTBOX. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="262ca-122">**LISTBOX.fontStyle**</span></span>](listbox-fontstyle.md)
</dt> </dl>

 

 





