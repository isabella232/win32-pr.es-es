---
title: VIEW. backgroundImage
description: El atributo backgroundImage especifica o recupera la imagen de fondo de la vista o la subvista.
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- VIEW. backgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96f4a93882e02589d7f15b74ba5cb225f506d69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649620"
---
# <a name="viewbackgroundimage"></a><span data-ttu-id="1493a-104">VIEW. backgroundImage</span><span class="sxs-lookup"><span data-stu-id="1493a-104">VIEW.backgroundImage</span></span>

<span data-ttu-id="1493a-105">El atributo **BackgroundImage** especifica o recupera la imagen de fondo de la **vista** o la **subvista**.</span><span class="sxs-lookup"><span data-stu-id="1493a-105">The **backgroundImage** attribute specifies or retrieves the background image of the **VIEW** or **SUBVIEW**.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="1493a-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="1493a-106">Possible Values</span></span>

<span data-ttu-id="1493a-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="1493a-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1493a-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1493a-108">Remarks</span></span>

<span data-ttu-id="1493a-109">Los formatos admitidos son BMP, JPG, GIF y PNG.</span><span class="sxs-lookup"><span data-stu-id="1493a-109">The supported formats are BMP, JPG, GIF, and PNG.</span></span> <span data-ttu-id="1493a-110">Si la imagen es un archivo BMP de 8 bits, sus valores de matiz y saturación se pueden cambiar dinámicamente con los atributos **backgroundImageHueShift** y **backgroundImageSaturation** .</span><span class="sxs-lookup"><span data-stu-id="1493a-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **backgroundImageHueShift** and **backgroundImageSaturation** attributes.</span></span>

<span data-ttu-id="1493a-111">En un paquete de descarga de Windows Media, si especifica el atributo **BackgroundImage** para un elemento de **vista** , también debe especificar el atributo **BackgroundColor** para ese elemento.</span><span class="sxs-lookup"><span data-stu-id="1493a-111">In a Windows Media Download package, if you specify the **backgroundImage** attribute for a **VIEW** element, then you must also specify the **backgroundColor** attribute for that element.</span></span>

## <a name="requirements"></a><span data-ttu-id="1493a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1493a-112">Requirements</span></span>



| <span data-ttu-id="1493a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1493a-113">Requirement</span></span> | <span data-ttu-id="1493a-114">Value</span><span class="sxs-lookup"><span data-stu-id="1493a-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1493a-115">Versión</span><span class="sxs-lookup"><span data-stu-id="1493a-115">Version</span></span><br/> | <span data-ttu-id="1493a-116">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="1493a-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1493a-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="1493a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1493a-118">**Elemento de vista**</span><span class="sxs-lookup"><span data-stu-id="1493a-118">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="1493a-119">**VER. backgroundImageHueShift**</span><span class="sxs-lookup"><span data-stu-id="1493a-119">**VIEW.backgroundImageHueShift**</span></span>](view-backgroundimagehueshift.md)
</dt> <dt>

[<span data-ttu-id="1493a-120">**VER. backgroundImageSaturation**</span><span class="sxs-lookup"><span data-stu-id="1493a-120">**VIEW.backgroundImageSaturation**</span></span>](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





