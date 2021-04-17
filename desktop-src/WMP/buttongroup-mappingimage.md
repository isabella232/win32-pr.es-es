---
title: BUTTONGROUP.mappingImage
description: El atributo mappingImage especifica o recupera el nombre de la imagen que representa el mapa de botones de BUTTONGROUP.
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- BUTTONGROUP. mappingImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4afc44a00d5ce9b15ee01d4a0dc1aff52c555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699947"
---
# <a name="buttongroupmappingimage"></a><span data-ttu-id="3b851-104">BUTTONGROUP.mappingImage</span><span class="sxs-lookup"><span data-stu-id="3b851-104">BUTTONGROUP.mappingImage</span></span>

<span data-ttu-id="3b851-105">El atributo **mappingImage** especifica o recupera el nombre de la imagen que representa el mapa de botones de **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="3b851-105">The **mappingImage** attribute specifies or retrieves the name of the image representing the button map of the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a><span data-ttu-id="3b851-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="3b851-106">Possible Values</span></span>

<span data-ttu-id="3b851-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="3b851-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b851-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b851-108">Remarks</span></span>

<span data-ttu-id="3b851-109">Se trata de un atributo obligatorio que debe especificarse.</span><span class="sxs-lookup"><span data-stu-id="3b851-109">This is a mandatory attribute that must be specified.</span></span>

<span data-ttu-id="3b851-110">La imagen de asignación debe ser las mismas dimensiones que la **imagen** principal.</span><span class="sxs-lookup"><span data-stu-id="3b851-110">The mapping image should be the same dimensions as the main **image**.</span></span> <span data-ttu-id="3b851-111">Se trata de un mapa de las áreas en las que se hace clic de la imagen principal.</span><span class="sxs-lookup"><span data-stu-id="3b851-111">It is a map of the clickable areas of the main image.</span></span> <span data-ttu-id="3b851-112">Construya el mapa rellenando cada área seleccionable con un color diferente.</span><span class="sxs-lookup"><span data-stu-id="3b851-112">Construct the map by filling each clickable area with a different color.</span></span>

<span data-ttu-id="3b851-113">Al definir cada **BUTTONELEMENT**, designe su color a partir del mapa mediante el atributo **mappingColor** .</span><span class="sxs-lookup"><span data-stu-id="3b851-113">When defining each **BUTTONELEMENT**, designate its color from the map using the **mappingColor** attribute.</span></span> <span data-ttu-id="3b851-114">Por ejemplo, si tiene un gráfico de botón de signo de cierre en la imagen principal, puede crear un mapa con el área del signo de color rojo.</span><span class="sxs-lookup"><span data-stu-id="3b851-114">For example, if you have a stop-sign-shaped button graphic in the main image, you can create a map with the area of the sign colored red.</span></span> <span data-ttu-id="3b851-115">El atributo **BUTTONELEMENT** debe especificarse en rojo para que se pueda hacer clic en la imagen de detención de firma.</span><span class="sxs-lookup"><span data-stu-id="3b851-115">The **BUTTONELEMENT** attribute must then be specified as red to make the stop-sign image clickable.</span></span>

<span data-ttu-id="3b851-116">Los formatos de imagen admitidos son BMP, JPG, PNG y GIF (sin incluir los GIF animados).</span><span class="sxs-lookup"><span data-stu-id="3b851-116">The supported image formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span> <span data-ttu-id="3b851-117">Debido a que las JPGs son perdidas y, por tanto, están sujetas a cambios de color inesperados, no se recomiendan para asignar imágenes.</span><span class="sxs-lookup"><span data-stu-id="3b851-117">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended for mapping images.</span></span>

## <a name="examples"></a><span data-ttu-id="3b851-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3b851-118">Examples</span></span>

<span data-ttu-id="3b851-119">La siguiente ilustración es un ejemplo de **mappingImage** y la imagen visible a la que corresponde.</span><span class="sxs-lookup"><span data-stu-id="3b851-119">The following illustration is an example of a **mappingImage** and the visible image it corresponds to.</span></span> <span data-ttu-id="3b851-120">Estas imágenes forman parte de la máscara en la pequeña carpeta incluida con el SDK.</span><span class="sxs-lookup"><span data-stu-id="3b851-120">These images are part of the skin in the Tiny folder included with the SDK.</span></span>

![imagen de asignación de ejemplo](images/absam01m.png)![imagen de fondo de ejemplo](images/absam01f.png)

<span data-ttu-id="3b851-123">Vea *BUTTONELEMENT*. atributo [mappingColor](buttonelement-mappingcolor.md) para un ejemplo de código que ilustra el uso de este atributo.</span><span class="sxs-lookup"><span data-stu-id="3b851-123">See the *BUTTONELEMENT*.[mappingColor](buttonelement-mappingcolor.md) attribute for a code sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b851-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b851-124">Requirements</span></span>



| <span data-ttu-id="3b851-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b851-125">Requirement</span></span> | <span data-ttu-id="3b851-126">Value</span><span class="sxs-lookup"><span data-stu-id="3b851-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3b851-127">Versión</span><span class="sxs-lookup"><span data-stu-id="3b851-127">Version</span></span><br/> | <span data-ttu-id="3b851-128">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3b851-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b851-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b851-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b851-130">**BUTTONELEMENT. mappingColor**</span><span class="sxs-lookup"><span data-stu-id="3b851-130">**BUTTONELEMENT.mappingColor**</span></span>](buttonelement-mappingcolor.md)
</dt> <dt>

[<span data-ttu-id="3b851-131">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="3b851-131">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="3b851-132">**BUTTONGROUP. Image**</span><span class="sxs-lookup"><span data-stu-id="3b851-132">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="3b851-133">**BUTTONGROUP. transparencyColor**</span><span class="sxs-lookup"><span data-stu-id="3b851-133">**BUTTONGROUP.transparencyColor**</span></span>](buttongroup-transparencycolor.md)
</dt> </dl>

 

 





