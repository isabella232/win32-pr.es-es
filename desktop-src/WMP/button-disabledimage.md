---
title: BUTTON. disabledImage
description: El atributo disabledImage especifica o recupera la imagen que se muestra cuando el botón está deshabilitado.
ms.assetid: b5654323-589a-45da-9534-6fa67c3a4c4b
keywords:
- BUTTON. disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eac407f6e7fbdd155f4bcabe98cecc0546f7d97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698616"
---
# <a name="buttondisabledimage"></a><span data-ttu-id="fcee1-104">BUTTON. disabledImage</span><span class="sxs-lookup"><span data-stu-id="fcee1-104">BUTTON.disabledImage</span></span>

<span data-ttu-id="fcee1-105">El atributo **disabledImage** especifica o recupera la imagen que se muestra cuando el **botón** está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="fcee1-105">The **disabledImage** attribute specifies or retrieves the image that displays when the **BUTTON** is disabled.</span></span>

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a><span data-ttu-id="fcee1-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="fcee1-106">Possible Values</span></span>

<span data-ttu-id="fcee1-107">Este atributo es una **cadena** de lectura/escritura que contiene el nombre del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="fcee1-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcee1-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcee1-108">Remarks</span></span>

<span data-ttu-id="fcee1-109">Los formatos de imagen admitidos son BMP, JPG, PNG y GIF.</span><span class="sxs-lookup"><span data-stu-id="fcee1-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="fcee1-110">Esta imagen se mostrará siempre que el atributo **deshabilitado** del control esté establecido en true.</span><span class="sxs-lookup"><span data-stu-id="fcee1-110">This image will be displayed whenever the **disabled** attribute of the control is set to true.</span></span> <span data-ttu-id="fcee1-111">Si la imagen deshabilitada es mayor que la región definida, se recortará la imagen deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="fcee1-111">If the disabled image is larger than the defined region, the disabled image will be cropped.</span></span>

<span data-ttu-id="fcee1-112">Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).</span><span class="sxs-lookup"><span data-stu-id="fcee1-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcee1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcee1-113">Requirements</span></span>



| <span data-ttu-id="fcee1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcee1-114">Requirement</span></span> | <span data-ttu-id="fcee1-115">Value</span><span class="sxs-lookup"><span data-stu-id="fcee1-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="fcee1-116">Versión</span><span class="sxs-lookup"><span data-stu-id="fcee1-116">Version</span></span><br/> | <span data-ttu-id="fcee1-117">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="fcee1-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fcee1-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcee1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcee1-119">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="fcee1-119">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





