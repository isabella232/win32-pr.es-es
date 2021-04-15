---
title: Atributo WM/GenreID
description: El atributo WM/GenreID es un identificador de género compatible con la etiqueta TCON en ID3v2.
ms.assetid: 9b68f9be-1f02-4b14-b052-90657b8800e3
keywords:
- Media Player de Windows de atributos de WM/GenreID
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d31e54805f778a51f345c84654056391ec4052e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708719"
---
# <a name="wmgenreid-attribute"></a><span data-ttu-id="57916-104">Atributo WM/GenreID</span><span class="sxs-lookup"><span data-stu-id="57916-104">WM/GenreID Attribute</span></span>

<span data-ttu-id="57916-105">El atributo **WM/GenreID** es un identificador de género compatible con la etiqueta TCON en ID3v2.</span><span class="sxs-lookup"><span data-stu-id="57916-105">The **WM/GenreID** attribute is a genre identifier compliant with the TCON tag in ID3v2.</span></span>

## <a name="applies-to"></a><span data-ttu-id="57916-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="57916-106">Applies To</span></span>

-   [<span data-ttu-id="57916-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="57916-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="57916-108">Atributos de archivo de Windows Media de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="57916-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="57916-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57916-109">Remarks</span></span>

<span data-ttu-id="57916-110">Este atributo solo se almacena en el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="57916-110">This attribute is stored only in the digital media file.</span></span>

<span data-ttu-id="57916-111">ID3 versión 2 es una Convención de etiquetado que se diseñó originalmente para MP3.</span><span class="sxs-lookup"><span data-stu-id="57916-111">ID3 version 2 is a tagging convention that was originally designed for MP3.</span></span> <span data-ttu-id="57916-112">Para obtener más información, consulte el [sitio web de la organización ID3](https://id3.org/).</span><span class="sxs-lookup"><span data-stu-id="57916-112">For more information, see the [ID3 organization's website](https://id3.org/).</span></span>

<span data-ttu-id="57916-113">La constante del SDK de Windows Media Format para este atributo es g \_ wszGenreID.</span><span class="sxs-lookup"><span data-stu-id="57916-113">The Windows Media Format SDK constant for this attribute is g\_wszGenreID.</span></span>

<span data-ttu-id="57916-114">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="57916-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="57916-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57916-115">Requirements</span></span>



| <span data-ttu-id="57916-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="57916-116">Requirement</span></span> | <span data-ttu-id="57916-117">Value</span><span class="sxs-lookup"><span data-stu-id="57916-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57916-118">Versión</span><span class="sxs-lookup"><span data-stu-id="57916-118">Version</span></span><br/> | <span data-ttu-id="57916-119">Windows Media Player 9 series Windows Media Player 10 o posterior no admite este atributo</span><span class="sxs-lookup"><span data-stu-id="57916-119">Windows Media Player 9 Series Windows Media Player 10 or later does not support this attribute</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="57916-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="57916-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57916-121">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="57916-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





