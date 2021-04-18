---
title: EDITBOX. fontFace
description: El atributo fontFace especifica o recupera la fuente para el texto en el control de cuadro de edición.
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- FontFace Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c5794da93821db840a48facbba45540da9249a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700109"
---
# <a name="editboxfontface"></a><span data-ttu-id="7efc5-104">EDITBOX. fontFace</span><span class="sxs-lookup"><span data-stu-id="7efc5-104">EDITBOX.fontFace</span></span>

<span data-ttu-id="7efc5-105">El atributo **fontFace** especifica o recupera la fuente para el texto en el control de cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="7efc5-105">The **fontFace** attribute specifies or retrieves the font for text in the edit box control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="7efc5-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="7efc5-106">Possible Values</span></span>

<span data-ttu-id="7efc5-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="7efc5-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7efc5-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7efc5-108">Remarks</span></span>

<span data-ttu-id="7efc5-109">Este atributo puede ser el nombre de cualquier fuente válida disponible en Windows.</span><span class="sxs-lookup"><span data-stu-id="7efc5-109">This attribute can be the name of any valid font available in Windows.</span></span> <span data-ttu-id="7efc5-110">Windows Media Player no admitirá la instalación de fuentes, así que elija una fuente que sepa que se encuentra en el sistema previsto.</span><span class="sxs-lookup"><span data-stu-id="7efc5-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="7efc5-111">Si el **fontFace** especificado no está disponible en el sistema del usuario, el control del cuadro de edición tiene como valor predeterminado la fuente del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="7efc5-111">If the **fontFace** specified is not available on the user's system, the edit box control defaults to the Windows system font.</span></span> <span data-ttu-id="7efc5-112">El valor predeterminado para los sistemas en inglés es "Tahoma".</span><span class="sxs-lookup"><span data-stu-id="7efc5-112">The default value for English-language systems is "Tahoma".</span></span> <span data-ttu-id="7efc5-113">En el caso de los sistemas internacionales, el valor predeterminado se carga desde un archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7efc5-113">For international systems, the default is loaded from a resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="7efc5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7efc5-114">Requirements</span></span>



| <span data-ttu-id="7efc5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7efc5-115">Requirement</span></span> | <span data-ttu-id="7efc5-116">Value</span><span class="sxs-lookup"><span data-stu-id="7efc5-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="7efc5-117">Versión</span><span class="sxs-lookup"><span data-stu-id="7efc5-117">Version</span></span><br/> | <span data-ttu-id="7efc5-118">Windows Media Player para Windows XP o posterior</span><span class="sxs-lookup"><span data-stu-id="7efc5-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7efc5-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="7efc5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7efc5-120">**Elemento EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="7efc5-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="7efc5-121">**EDITBOX. FontSize**</span><span class="sxs-lookup"><span data-stu-id="7efc5-121">**EDITBOX.fontSize**</span></span>](editbox-fontsize.md)
</dt> <dt>

[<span data-ttu-id="7efc5-122">**EDITBOX. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="7efc5-122">**EDITBOX.fontStyle**</span></span>](editbox-fontstyle.md)
</dt> </dl>

 

 





