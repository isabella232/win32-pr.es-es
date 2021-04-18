---
title: BOTÓN. imagen
description: El atributo Image especifica o recupera la imagen predeterminada del botón.
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- BOTÓN. Image Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d27363383d72110ebe7b3e94187013ab701a6a3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700134"
---
# <a name="buttonimage"></a><span data-ttu-id="471a1-104">BOTÓN. imagen</span><span class="sxs-lookup"><span data-stu-id="471a1-104">BUTTON.image</span></span>

<span data-ttu-id="471a1-105">El atributo **Image** especifica o recupera la imagen predeterminada del **botón**.</span><span class="sxs-lookup"><span data-stu-id="471a1-105">The **image** attribute specifies or retrieves the default image of the **BUTTON**.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="471a1-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="471a1-106">Possible Values</span></span>

<span data-ttu-id="471a1-107">Este atributo es una **cadena** de lectura/escritura que contiene el nombre del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="471a1-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="471a1-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="471a1-108">Remarks</span></span>

<span data-ttu-id="471a1-109">Los formatos de imagen admitidos son BMP, JPG, PNG y GIF (incluidos los GIF animados).</span><span class="sxs-lookup"><span data-stu-id="471a1-109">The supported image formats are BMP, JPG, PNG, and GIF (including animated GIFs).</span></span>

<span data-ttu-id="471a1-110">Si la imagen del **botón** es mayor que la región definida por los atributos de **ancho** y **alto** , se recortará la imagen.</span><span class="sxs-lookup"><span data-stu-id="471a1-110">If the **BUTTON** image is larger than the region defined by the **width** and **height** attributes, the image will be cropped.</span></span>

<span data-ttu-id="471a1-111">Si no se especifica la imagen pero el **alto** y el **ancho** son, se muestra la imagen que se encuentra directamente detrás de este control.</span><span class="sxs-lookup"><span data-stu-id="471a1-111">If the image is not specified but the **height** and **width** are, then the image directly behind this control is displayed.</span></span> <span data-ttu-id="471a1-112">Esto puede facilitar el dibujo de la imagen en la propia **vista** , lo que reduce el número de archivos de imagen independientes necesarios.</span><span class="sxs-lookup"><span data-stu-id="471a1-112">This can facilitate drawing the image on the **VIEW** itself, reducing the number of separate image files needed.</span></span>

<span data-ttu-id="471a1-113">Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).</span><span class="sxs-lookup"><span data-stu-id="471a1-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="471a1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="471a1-114">Requirements</span></span>



| <span data-ttu-id="471a1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="471a1-115">Requirement</span></span> | <span data-ttu-id="471a1-116">Value</span><span class="sxs-lookup"><span data-stu-id="471a1-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="471a1-117">Versión</span><span class="sxs-lookup"><span data-stu-id="471a1-117">Version</span></span><br/> | <span data-ttu-id="471a1-118">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="471a1-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="471a1-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="471a1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="471a1-120">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="471a1-120">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





