---
title: Constantes de Direct2D
description: Direct2D define la siguiente lista de constantes.
ms.assetid: 98a443af-4bb7-486d-bc87-ff34c3671bdd
topic_type:
- apiref
api_name:
- D2D1_APPEND_ALIGNED_ELEMENT
- D2D1_DEFAULT_FLATTENING_TOLERANCE
- D2D1_INVALID_PROPERTY_INDEX
- D2D1_INVALID_TAG
- D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL
api_location:
- d2d1.h
- d2d1effects_2.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 09/19/2019
ms.openlocfilehash: bc25bf1055b923a383fc580a622e96d787ed13e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658269"
---
# <a name="direct2d-constants"></a><span data-ttu-id="64721-103">Constantes de Direct2D</span><span class="sxs-lookup"><span data-stu-id="64721-103">Direct2D constants</span></span>

<span data-ttu-id="64721-104">Las constantes siguientes se declaran en `d2d1effectauthor.h` los `d2d1.h` archivos de encabezado,, `d2d1_1.h` y `d2d1effects_2.h` .</span><span class="sxs-lookup"><span data-stu-id="64721-104">The following constants are declared in the `d2d1effectauthor.h`, `d2d1.h`, `d2d1_1.h`, and `d2d1effects_2.h` header files.</span></span>

## <a name="d2d1_append_aligned_element--1"></a><span data-ttu-id="64721-105">D2D1_APPEND_ALIGNED_ELEMENT (-1)</span><span class="sxs-lookup"><span data-stu-id="64721-105">D2D1_APPEND_ALIGNED_ELEMENT (-1)</span></span>
<span data-ttu-id="64721-106">Se usa al empaquetar elementos de diseño de entrada.</span><span class="sxs-lookup"><span data-stu-id="64721-106">Used when packing input layout elements.</span></span> <span data-ttu-id="64721-107">Indica que los elementos deben empaquetarse de forma contigua.</span><span class="sxs-lookup"><span data-stu-id="64721-107">It indicates that the elements must be packed contiguously.</span></span>

## <a name="d2d1_default_flattening_tolerance-025f"></a><span data-ttu-id="64721-108">D2D1_DEFAULT_FLATTENING_TOLERANCE (0,25 f)</span><span class="sxs-lookup"><span data-stu-id="64721-108">D2D1_DEFAULT_FLATTENING_TOLERANCE (0.25f)</span></span>
<span data-ttu-id="64721-109">La tolerancia predeterminada para las operaciones de simplificación geométrica.</span><span class="sxs-lookup"><span data-stu-id="64721-109">The default tolerance for geometric flattening operations.</span></span>

## <a name="d2d1_invalid_property_index-uint_max"></a><span data-ttu-id="64721-110">D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)</span><span class="sxs-lookup"><span data-stu-id="64721-110">D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)</span></span>
<span data-ttu-id="64721-111">Define un índice de propiedad no válido.</span><span class="sxs-lookup"><span data-stu-id="64721-111">Defines an invalid property index.</span></span>

<span data-ttu-id="64721-112">Esta constante se devuelve desde [**ID2D1Properties:: GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) para indicar que la propiedad con nombre que proporcionó no tiene un índice en la interfaz de propiedad.</span><span class="sxs-lookup"><span data-stu-id="64721-112">This constant is returned from [**ID2D1Properties::GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) to indicate that the named property that you provided doesn't have an index in the property interface.</span></span>

<span data-ttu-id="64721-113">Si pasa esta constante a [**ID2D1Properties:: GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) o [**ID2D1Properties:: GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), se produce un error en la llamada y el búfer de salida se rellena con ceros.</span><span class="sxs-lookup"><span data-stu-id="64721-113">If you pass this constant to [**ID2D1Properties::GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) or [**ID2D1Properties::GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), then the call fails, and the output buffer is zero-filled.</span></span>

## <a name="d2d1_invalid_tag-ulonglong_max"></a><span data-ttu-id="64721-114">D2D1_INVALID_TAG (ULONGLONG_MAX)</span><span class="sxs-lookup"><span data-stu-id="64721-114">D2D1_INVALID_TAG (ULONGLONG_MAX)</span></span>
<span data-ttu-id="64721-115">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="64721-115">Reserved; don't use.</span></span>

## <a name="d2d1_scene_referred_sdr_white_level-800f"></a><span data-ttu-id="64721-116">D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80,0 f)</span><span class="sxs-lookup"><span data-stu-id="64721-116">D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80.0f)</span></span>
<span data-ttu-id="64721-117">Número de Nits que utiliza el espacio de colores sRGB o scRGB para el blanco de SDR o valores de punto flotante de 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="64721-117">The number of nits that sRGB or scRGB color space uses for SDR white, or floating point values of 1.0f.</span></span> <span data-ttu-id="64721-118">Este valor es constante solo cuando el espacio de colores utiliza la luminancia a la que se refiere la escena, lo que es cierto para el contenido de intervalo dinámico alto (HDR).</span><span class="sxs-lookup"><span data-stu-id="64721-118">This value is constant only when the color space uses scene-referred luminance, which is true for high dynamic range (HDR) content.</span></span> <span data-ttu-id="64721-119">Si en su lugar el espacio de colores utiliza la luminancia a la que se hace referencia, el nivel blanco de SDR debe consultarse desde la pantalla.</span><span class="sxs-lookup"><span data-stu-id="64721-119">If the color space uses display-referred luminance instead, then the SDR white level should be queried from the display.</span></span>

## <a name="requirements"></a><span data-ttu-id="64721-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64721-120">Requirements</span></span>

| <span data-ttu-id="64721-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="64721-121">Requirement</span></span> | <span data-ttu-id="64721-122">Value</span><span class="sxs-lookup"><span data-stu-id="64721-122">Value</span></span> |
|-|-|
| <span data-ttu-id="64721-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64721-123">Minimum supported client</span></span> | <span data-ttu-id="64721-124">Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="64721-124">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span> |
| <span data-ttu-id="64721-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64721-125">Minimum supported server</span></span> | <span data-ttu-id="64721-126">Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="64721-126">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span> |
| <span data-ttu-id="64721-127">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64721-127">Minimum supported phone</span></span> | <span data-ttu-id="64721-128">Windows Phone 8,1 \[ Windows Phone Windows Runtime aplicaciones de silverlight 8,1 y \] , Windows Phone 8,1 \[ Windows Phone aplicaciones de silverlight 8,1 y Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="64721-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\], Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span> |
| <span data-ttu-id="64721-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64721-129">Header</span></span> | <span data-ttu-id="64721-130">d2d1effectauthor. h, d2d1. h, d2d1_1. h, d2d1effects_2. h</span><span class="sxs-lookup"><span data-stu-id="64721-130">d2d1effectauthor.h, d2d1.h, d2d1_1.h, d2d1effects_2.h</span></span> |
