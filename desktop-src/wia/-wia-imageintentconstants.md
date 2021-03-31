---
description: Las constantes de intención de imagen especifican qué tipo de datos pretende representar la imagen.
ms.assetid: 171228d9-a619-49aa-964e-f72a7f294a9d
title: Constantes de intención de imagen (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_INTENT_IMAGE_TYPE_COLOR
- WIA_INTENT_IMAGE_TYPE_GRAYSCALE
- WIA_INTENT_IMAGE_TYPE_TEXT
- WIA_INTENT_MINIMIZE_SIZE
- WIA_INTENT_MAXIMIZE_QUALITY
- WIA_INTENT_BEST_PREVIEW
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f35c1f7436c8cc5110215a6ccf0383960ec3fb87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001305"
---
# <a name="image-intent-constants"></a><span data-ttu-id="73f10-103">Constantes de intención de imagen</span><span class="sxs-lookup"><span data-stu-id="73f10-103">Image Intent Constants</span></span>

<span data-ttu-id="73f10-104">Las constantes de intención de imagen especifican qué tipo de datos pretende representar la imagen.</span><span class="sxs-lookup"><span data-stu-id="73f10-104">Image intent constants specify what type of data the image is meant to represent.</span></span> <span data-ttu-id="73f10-105">La propiedad del escáner de [**\_ \_ \_ intento de IPS de WIA IP**](-wia-wiaitempropscanneritem.md) utiliza estas marcas.</span><span class="sxs-lookup"><span data-stu-id="73f10-105">The [**WIA\_IPS\_CUR\_INTENT**](-wia-wiaitempropscanneritem.md) scanner property uses these flags.</span></span> <span data-ttu-id="73f10-106">Para proporcionar una intención, combine una marca de tipo de imagen deseada con una marca de tamaño/calidad deseada mediante el operador o.</span><span class="sxs-lookup"><span data-stu-id="73f10-106">To provide an intent, combine an intended image type flag with an intended size/quality flag by using the OR operator.</span></span> <span data-ttu-id="73f10-107">La \_ intención \_ de WIA ninguno no debe combinarse con otras marcas.</span><span class="sxs-lookup"><span data-stu-id="73f10-107">WIA\_INTENT\_NONE should not be combined with any other flags.</span></span> <span data-ttu-id="73f10-108">Tenga en cuenta que una imagen no puede ser de escala de grises y de color.</span><span class="sxs-lookup"><span data-stu-id="73f10-108">Note that an image cannot be both grayscale and color.</span></span>

<span data-ttu-id="73f10-109">Las siguientes son constantes de intención de imagen válidas:</span><span class="sxs-lookup"><span data-stu-id="73f10-109">The following are valid image intent constants:</span></span>



| <span data-ttu-id="73f10-110">Marcas de tipo de imagen previsto</span><span class="sxs-lookup"><span data-stu-id="73f10-110">Intended image type flags</span></span>           | <span data-ttu-id="73f10-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="73f10-111">Description</span></span>                                  |
|-------------------------------------|----------------------------------------------|
| <span data-ttu-id="73f10-112">intento de WIA \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="73f10-112">WIA\_INTENT\_NONE</span></span>                   | <span data-ttu-id="73f10-113">Valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="73f10-113">Default value.</span></span> <span data-ttu-id="73f10-114">No configure ninguna propiedad.</span><span class="sxs-lookup"><span data-stu-id="73f10-114">Do not preset any properties.</span></span> |
| <span data-ttu-id="73f10-115">\_color del \_ tipo de imagen de intención de WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="73f10-115">WIA\_INTENT\_IMAGE\_TYPE\_COLOR</span></span>     | <span data-ttu-id="73f10-116">Propiedades preestablecidas para el contenido de color.</span><span class="sxs-lookup"><span data-stu-id="73f10-116">Preset properties for color content.</span></span>         |
| <span data-ttu-id="73f10-117">tipo de imagen de intención de WIA en \_ \_ escala de \_ \_ grises</span><span class="sxs-lookup"><span data-stu-id="73f10-117">WIA\_INTENT\_IMAGE\_TYPE\_GRAYSCALE</span></span> | <span data-ttu-id="73f10-118">Propiedades preestablecidas para el contenido de escala de grises.</span><span class="sxs-lookup"><span data-stu-id="73f10-118">Preset properties for grayscale content.</span></span>     |
| <span data-ttu-id="73f10-119">\_texto de \_ tipo de imagen de intención de WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="73f10-119">WIA\_INTENT\_IMAGE\_TYPE\_TEXT</span></span>      | <span data-ttu-id="73f10-120">Propiedades preestablecidas para el contenido de texto.</span><span class="sxs-lookup"><span data-stu-id="73f10-120">Preset properties for text content.</span></span>          |
| <span data-ttu-id="73f10-121">\_máscara de \_ tipo de imagen de intención de WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="73f10-121">WIA\_INTENT\_IMAGE\_TYPE\_MASK</span></span>      | <span data-ttu-id="73f10-122">Máscara para todas las marcas de tipo de imagen.</span><span class="sxs-lookup"><span data-stu-id="73f10-122">Mask for all of the image type flags.</span></span>        |



 



| <span data-ttu-id="73f10-123">Marcas de calidad y tamaño de imagen previsto</span><span class="sxs-lookup"><span data-stu-id="73f10-123">Intended image size/quality flags</span></span> | <span data-ttu-id="73f10-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="73f10-124">Description</span></span>                                  |
|-----------------------------------|----------------------------------------------|
| <span data-ttu-id="73f10-125">tamaño de la intención de WIA \_ \_ minimizar \_</span><span class="sxs-lookup"><span data-stu-id="73f10-125">WIA\_INTENT\_MINIMIZE\_SIZE</span></span>       | <span data-ttu-id="73f10-126">Propiedades preestablecidas para minimizar el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="73f10-126">Preset properties to minimize image size.</span></span>    |
| <span data-ttu-id="73f10-127">calidad de la \_ maximización del intento de WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="73f10-127">WIA\_INTENT\_MAXIMIZE\_QUALITY</span></span>    | <span data-ttu-id="73f10-128">Propiedades preestablecidas para maximizar la calidad de la imagen.</span><span class="sxs-lookup"><span data-stu-id="73f10-128">Preset properties to maximize image quality.</span></span> |
| <span data-ttu-id="73f10-129">\_máscara de \_ tamaño de intención de WIA \_</span><span class="sxs-lookup"><span data-stu-id="73f10-129">WIA\_INTENT\_SIZE\_MASK</span></span>           | <span data-ttu-id="73f10-130">Máscara para todas las marcas de tamaño/calidad.</span><span class="sxs-lookup"><span data-stu-id="73f10-130">Mask for all of the size/quality flags.</span></span>      |
| <span data-ttu-id="73f10-131">\_ \_ mejor \_ vista previa de la intención de WIA</span><span class="sxs-lookup"><span data-stu-id="73f10-131">WIA\_INTENT\_BEST\_PREVIEW</span></span>        | <span data-ttu-id="73f10-132">Especifica la mejor vista previa de calidad.</span><span class="sxs-lookup"><span data-stu-id="73f10-132">Specifies the best quality preview.</span></span>          |



 

<span data-ttu-id="73f10-133">La lista siguiente muestra el nombre de la constante de C/C++ seguido del nombre correspondiente entre paréntesis que se usa en el scripting.</span><span class="sxs-lookup"><span data-stu-id="73f10-133">The following list shows the C/C++ constant name followed by the corresponding name in parentheses that is used in scripting.</span></span> <span data-ttu-id="73f10-134">Los nombres de script son del tipo enumerado WiaIntent.</span><span class="sxs-lookup"><span data-stu-id="73f10-134">The script names are from the WiaIntent enumerated type.</span></span> <span data-ttu-id="73f10-135">Tenga en cuenta que no todas las constantes están disponibles a través del script.</span><span class="sxs-lookup"><span data-stu-id="73f10-135">Note that not all constants are available through script.</span></span>



| <span data-ttu-id="73f10-136">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="73f10-136">Constant/value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="73f10-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="73f10-137">Description</span></span>                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| <span id="WIA_INTENT_IMAGE_TYPE_COLOR"></span><span id="wia_intent_image_type_color"></span><dl> <span data-ttu-id="73f10-138"><dt>**WIA \_ \_Color del \_ tipo \_ de imagen de intención**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="73f10-138"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_COLOR**</dt> <dt>0x00000001</dt></span></span> </dl>             | <span data-ttu-id="73f10-139">Propiedades preestablecidas para el contenido de color.</span><span class="sxs-lookup"><span data-stu-id="73f10-139">Preset properties for color content.</span></span><br/>         |
| <span id="WIA_INTENT_IMAGE_TYPE_GRAYSCALE"></span><span id="wia_intent_image_type_grayscale"></span><dl> <span data-ttu-id="73f10-140"><dt>**WIA \_ Tipo de imagen de intención de \_ \_ escala de \_ grises**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="73f10-140"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_GRAYSCALE**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="73f10-141">Propiedades preestablecidas para el contenido de escala de grises.</span><span class="sxs-lookup"><span data-stu-id="73f10-141">Preset properties for grayscale content.</span></span><br/>     |
| <span id="WIA_INTENT_IMAGE_TYPE_TEXT"></span><span id="wia_intent_image_type_text"></span><dl> <span data-ttu-id="73f10-142"><dt>**WIA \_ Tipo de imagen de intención \_ \_ \_ texto**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="73f10-142"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_TEXT**</dt> <dt>0x00000004</dt></span></span> </dl>                | <span data-ttu-id="73f10-143">Propiedades preestablecidas para el contenido de texto.</span><span class="sxs-lookup"><span data-stu-id="73f10-143">Preset properties for text content.</span></span><br/>          |
| <span id="WIA_INTENT_MINIMIZE_SIZE"></span><span id="wia_intent_minimize_size"></span><dl> <span data-ttu-id="73f10-144"><dt>**WIA \_ INTENCIÓN de \_ minimizar \_ el tamaño**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="73f10-144"><dt>**WIA\_INTENT\_MINIMIZE\_SIZE**</dt> <dt>0x00010000</dt></span></span> </dl>                       | <span data-ttu-id="73f10-145">Propiedades preestablecidas para minimizar el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="73f10-145">Preset properties to minimize image size.</span></span><br/>    |
| <span id="WIA_INTENT_MAXIMIZE_QUALITY"></span><span id="wia_intent_maximize_quality"></span><dl> <span data-ttu-id="73f10-146"><dt>**WIA \_ INTENCIÓN de \_ maximizar la \_ calidad**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="73f10-146"><dt>**WIA\_INTENT\_MAXIMIZE\_QUALITY**</dt> <dt>0x00020000</dt></span></span> </dl>              | <span data-ttu-id="73f10-147">Propiedades preestablecidas para maximizar la calidad de la imagen.</span><span class="sxs-lookup"><span data-stu-id="73f10-147">Preset properties to maximize image quality.</span></span><br/> |
| <span id="WIA_INTENT_BEST_PREVIEW"></span><span id="wia_intent_best_preview"></span><dl> <span data-ttu-id="73f10-148"><dt>**WIA \_ INTENCIÓN \_ Best \_ Preview**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="73f10-148"><dt>**WIA\_INTENT\_BEST\_PREVIEW**</dt> <dt>0x00040000</dt></span></span> </dl>                          | <span data-ttu-id="73f10-149">Especifica la mejor vista previa de calidad.</span><span class="sxs-lookup"><span data-stu-id="73f10-149">Specifies the best quality preview.</span></span><br/>          |



## <a name="requirements"></a><span data-ttu-id="73f10-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73f10-150">Requirements</span></span>



| <span data-ttu-id="73f10-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="73f10-151">Requirement</span></span> | <span data-ttu-id="73f10-152">Value</span><span class="sxs-lookup"><span data-stu-id="73f10-152">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="73f10-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73f10-153">Minimum supported client</span></span><br/> | <span data-ttu-id="73f10-154">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="73f10-154">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="73f10-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73f10-155">Minimum supported server</span></span><br/> | <span data-ttu-id="73f10-156">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="73f10-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="73f10-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73f10-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="73f10-158"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="73f10-158"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




