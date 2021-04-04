---
description: La \_ \_ \_ enumeración de enumeraciones de página S0 de MXDC se usa para especificar los tipos de recursos que se pueden asociar a las páginas de los documentos XPS y que se pueden procesar, o pasar sin procesar, el convertidor de documentos XPS de Microsoft (MXDC) a su salida.
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: Enumeración MXDC_S0_PAGE_ENUMS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0_PAGE_ENUMS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1b4331210027f7fc23f36fb6b9d13a2c232ccbf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909577"
---
# <a name="mxdc_s0_page_enums-enumeration"></a><span data-ttu-id="f619c-103">Enumeración de enumeraciones de \_ Página S0 de MXDC \_ \_</span><span class="sxs-lookup"><span data-stu-id="f619c-103">MXDC\_S0\_PAGE\_ENUMS enumeration</span></span>

<span data-ttu-id="f619c-104">La enumeración de **\_ \_ \_ enumeraciones de página S0 de MXDC** se usa para especificar los tipos de recursos que se pueden asociar a las páginas de los documentos XPS y que se pueden procesar, o pasar sin procesar, el convertidor de documentos XPS de Microsoft (MXDC) a su salida.</span><span class="sxs-lookup"><span data-stu-id="f619c-104">The **MXDC\_S0\_PAGE\_ENUMS** enumeration is used to specify types of resources that can be associated with pages in XPS documents and that can be processed, or passed unprocessed, by Microsoft XPS Document Converter (MXDC) to its output.</span></span>

## <a name="syntax"></a><span data-ttu-id="f619c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f619c-105">Syntax</span></span>


```C++
typedef enum tagMxdcS0PageEnums { 
  MXDC_RESOURCE_TTF,
  MXDC_RESOURCE_JPEG,
  MXDC_RESOURCE_PNG,
  MXDC_RESOURCE_TIFF,
  MXDC_RESOURCE_WDP,
  MXDC_RESOURCE_DICTIONARY,
  MXDC_RESOURCE_ICC_PROFILE,
  MXDC_RESOURCE_JPEG_THUMBNAIL,
  MXDC_RESOURCE_PNG_THUMBNAIL,
  MXDC_RESOURCE_MAX
} MXDC_S0_PAGE_ENUMS;
```



## <a name="constants"></a><span data-ttu-id="f619c-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="f619c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f619c-107"><span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**\_recurso MXDC \_ ttf**</span><span class="sxs-lookup"><span data-stu-id="f619c-107"><span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**MXDC\_RESOURCE\_TTF**</span></span>
</dt> <dd>

<span data-ttu-id="f619c-108">Fuente TrueType o OpenType.</span><span class="sxs-lookup"><span data-stu-id="f619c-108">TrueType or OpenType font.</span></span>

</dd> <dt>

<span data-ttu-id="f619c-109"><span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC \_ recurso \_ JPEG**</span><span class="sxs-lookup"><span data-stu-id="f619c-109"><span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC\_RESOURCE\_JPEG**</span></span>
</dt> <dd>

<span data-ttu-id="f619c-110">Imagen JPEG</span><span class="sxs-lookup"><span data-stu-id="f619c-110">JPEG image</span></span>

</dd> <dt>

<span data-ttu-id="f619c-111"><span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC de \_ recursos \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="f619c-111"><span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC\_RESOURCE\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="f619c-112">Imagen PNG.</span><span class="sxs-lookup"><span data-stu-id="f619c-112">PNG image.</span></span>

</dd> <dt>

<span data-ttu-id="f619c-113"><span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**MXDC de \_ recursos \_ TIFF**</span><span class="sxs-lookup"><span data-stu-id="f619c-113"><span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**MXDC\_RESOURCE\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="f619c-114">Imagen TIFF.</span><span class="sxs-lookup"><span data-stu-id="f619c-114">TIFF image.</span></span>

</dd> <dt>

<span data-ttu-id="f619c-115"><span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**MXDC \_ Resource \_ WDP**</span><span class="sxs-lookup"><span data-stu-id="f619c-115"><span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**MXDC\_RESOURCE\_WDP**</span></span>
</dt> <dd>

<span data-ttu-id="f619c-116">Imagen de Windows Media Photo.</span><span class="sxs-lookup"><span data-stu-id="f619c-116">Windows Media Photo image.</span></span>

</dd> <dt>

<span data-ttu-id="f619c-117"><span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**\_Diccionario de recursos MXDC \_**</span><span class="sxs-lookup"><span data-stu-id="f619c-117"><span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**MXDC\_RESOURCE\_DICTIONARY**</span></span>
</dt> <dd>

<span data-ttu-id="f619c-118">Diccionario de recursos remotos que debe pasarse a la salida de MXDC sin procesar.</span><span class="sxs-lookup"><span data-stu-id="f619c-118">Remote resource dictionary that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="f619c-119"><span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**\_ \_ perfil ICC de recurso MXDC \_**</span><span class="sxs-lookup"><span data-stu-id="f619c-119"><span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**MXDC\_RESOURCE\_ICC\_PROFILE**</span></span>
</dt> <dd>

<span data-ttu-id="f619c-120">Perfil ICC que debe pasarse a la salida de MXDC sin procesar.</span><span class="sxs-lookup"><span data-stu-id="f619c-120">ICC profile that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="f619c-121"><span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**MXDC \_ miniatura de recurso \_ JPEG \_**</span><span class="sxs-lookup"><span data-stu-id="f619c-121"><span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**MXDC\_RESOURCE\_JPEG\_THUMBNAIL**</span></span>
</dt> <dd>

<span data-ttu-id="f619c-122">Miniatura JPEG que se debe pasar a la salida de MXDC sin procesar.</span><span class="sxs-lookup"><span data-stu-id="f619c-122">JPEG thumbnail that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="f619c-123"><span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**MXDC \_ miniatura de recurso \_ PNG \_**</span><span class="sxs-lookup"><span data-stu-id="f619c-123"><span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**MXDC\_RESOURCE\_PNG\_THUMBNAIL**</span></span>
</dt> <dd>

<span data-ttu-id="f619c-124">Miniatura PNG que debe pasarse a la salida de MXDC sin procesar.</span><span class="sxs-lookup"><span data-stu-id="f619c-124">PNG thumbnail that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="f619c-125"><span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**\_recurso MXDC \_ máximo**</span><span class="sxs-lookup"><span data-stu-id="f619c-125"><span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC\_RESOURCE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="f619c-126">Recuento máximo de recursos para la validación.</span><span class="sxs-lookup"><span data-stu-id="f619c-126">The maximum resource count for validation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f619c-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f619c-127">Remarks</span></span>

<span data-ttu-id="f619c-128">Esta enumeración se utiliza principalmente como el miembro **dwResourceType** de la estructura de [**\_ \_ \_ recursos \_ T S0PAGE de MXDC XPS**](mxdcxpss0pageresource.md) .</span><span class="sxs-lookup"><span data-stu-id="f619c-128">This enumeration is primarily used as the **dwResourceType** member of the [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f619c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f619c-129">Requirements</span></span>



| <span data-ttu-id="f619c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f619c-130">Requirement</span></span> | <span data-ttu-id="f619c-131">Value</span><span class="sxs-lookup"><span data-stu-id="f619c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f619c-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f619c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f619c-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f619c-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f619c-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f619c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f619c-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f619c-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f619c-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f619c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f619c-137"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f619c-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




