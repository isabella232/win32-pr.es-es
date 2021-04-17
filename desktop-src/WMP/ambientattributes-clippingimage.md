---
title: AmbientAttributes.clippingImage
description: El atributo clippingImage especifica o recupera la región en la que se va a recortar el control.
ms.assetid: e4b51d31-f9c7-4398-983d-95867a2cab45
keywords:
- AmbientAttributes. clippingImage Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e05e05ca9c7c3efdf842ffd4297da6f9fee035d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700066"
---
# <a name="ambientattributesclippingimage"></a><span data-ttu-id="d1fbe-104">AmbientAttributes.clippingImage</span><span class="sxs-lookup"><span data-stu-id="d1fbe-104">AmbientAttributes.clippingImage</span></span>

<span data-ttu-id="d1fbe-105">El atributo **clippingImage** especifica o recupera la región en la que se va a recortar el control.</span><span class="sxs-lookup"><span data-stu-id="d1fbe-105">The **clippingImage** attribute specifies or retrieves the region to clip the control to.</span></span>

``` syntax
        elementID.clippingImage
```

## <a name="possible-values"></a><span data-ttu-id="d1fbe-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="d1fbe-106">Possible Values</span></span>

<span data-ttu-id="d1fbe-107">Este atributo es una **cadena** de lectura/escritura que indica el nombre del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="d1fbe-107">This attribute is a read/write **String** indicating the image file name.</span></span> <span data-ttu-id="d1fbe-108">No tiene valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d1fbe-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1fbe-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1fbe-109">Remarks</span></span>

<span data-ttu-id="d1fbe-110">El atributo **clippingImage** admite archivos PNG, JPG, BMP y GIF (sin incluir los GIF animados).</span><span class="sxs-lookup"><span data-stu-id="d1fbe-110">The **clippingImage** attribute supports PNG, JPG, BMP, and GIF files (not including animated GIFs).</span></span> <span data-ttu-id="d1fbe-111">Dado que los JPGs se pierden y, por lo tanto, están sujetos a cambios de color inesperados, no se recomiendan para recortar imágenes.</span><span class="sxs-lookup"><span data-stu-id="d1fbe-111">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended for clipping images.</span></span>

<span data-ttu-id="d1fbe-112">Este atributo es útil si desea mostrar solo una parte de la imagen de control y no el área rectangular completa.</span><span class="sxs-lookup"><span data-stu-id="d1fbe-112">This attribute is useful when you want to display only a part of the control image and not the entire rectangular area.</span></span> <span data-ttu-id="d1fbe-113">El atributo **clippingColor** indica las regiones de la imagen de recorte que corresponden a partes transparentes y no en las que se pueda hacer clic del control.</span><span class="sxs-lookup"><span data-stu-id="d1fbe-113">The **clippingColor** attribute indicates the regions of the clipping image that correspond to transparent, non-clickable portions of the control.</span></span> <span data-ttu-id="d1fbe-114">Por tanto, el control puede ser cualquier forma.</span><span class="sxs-lookup"><span data-stu-id="d1fbe-114">The control can therefore be of any shape.</span></span> <span data-ttu-id="d1fbe-115">Para obtener los mejores resultados, la imagen de recorte debe tener el mismo tamaño que la imagen de control.</span><span class="sxs-lookup"><span data-stu-id="d1fbe-115">For best results, the clipping image should be the same size as the control image.</span></span>

<span data-ttu-id="d1fbe-116">El atributo **clippingImage** no es compatible con los elementos de **lista de reproducción**, **vista** y **subvista** .</span><span class="sxs-lookup"><span data-stu-id="d1fbe-116">The **clippingImage** attribute is not supported by the **PLAYLIST**, **VIEW**, and **SUBVIEW** elements.</span></span> <span data-ttu-id="d1fbe-117">Una imagen de recorte no funcionará con el elemento de **vídeo** si se trata de un *vídeo*. **Windowless** está establecido en false, y en el elemento **Effects** si tiene *efectos*. **windowed** está establecido en true.</span><span class="sxs-lookup"><span data-stu-id="d1fbe-117">A clipping image will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if *EFFECTS*.**windowed** is set to true.</span></span>

<span data-ttu-id="d1fbe-118">Dado que el uso de imágenes de recorte impone una reducción del rendimiento, no se deben usar cuando la eficacia es un problema.</span><span class="sxs-lookup"><span data-stu-id="d1fbe-118">Because the use of clipping images imposes a performance penalty, they should not be used when efficiency is an issue.</span></span>

## <a name="examples"></a><span data-ttu-id="d1fbe-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d1fbe-119">Examples</span></span>

<span data-ttu-id="d1fbe-120">Vea el atributo [BUTTONELEMENT. mappingColor](buttonelement-mappingcolor.md) para obtener un ejemplo que ilustra el uso de este atributo.</span><span class="sxs-lookup"><span data-stu-id="d1fbe-120">See the [BUTTONELEMENT.mappingColor](buttonelement-mappingcolor.md) attribute for a sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1fbe-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1fbe-121">Requirements</span></span>



| <span data-ttu-id="d1fbe-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1fbe-122">Requirement</span></span> | <span data-ttu-id="d1fbe-123">Value</span><span class="sxs-lookup"><span data-stu-id="d1fbe-123">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d1fbe-124">Versión</span><span class="sxs-lookup"><span data-stu-id="d1fbe-124">Version</span></span><br/> | <span data-ttu-id="d1fbe-125">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="d1fbe-125">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1fbe-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1fbe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1fbe-127">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="d1fbe-127">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="d1fbe-128">**AmbientAttributes.clippingColor**</span><span class="sxs-lookup"><span data-stu-id="d1fbe-128">**AmbientAttributes.clippingColor**</span></span>](ambientattributes-clippingcolor.md)
</dt> </dl>

 

 





