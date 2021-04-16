---
description: Función de devolución de llamada que se usa para notificar al host cuando se ha completado una carga de textura.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureFromFileComplete\_UINT\_PixEngineTextureDescriptor\_UINT\_PixEngineTextureSliceIndex\_arr\_PixEngineTextureSliceDescriptor\_arr\_UINT\_int\_arr\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5Callbacks:: LoadTextureFromFileComplete (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7fb4c38b733a7e85a237260404b5b253e3eb88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696082"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptrspanipixengine5callbacksloadtexturefromfilecomplete-method"></a><span data-ttu-id="3406c-103"><span id="vspixengine.ipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptr"></span>IPixEngine5Callbacks:: LoadTextureFromFileComplete (método)</span><span class="sxs-lookup"><span data-stu-id="3406c-103"><span id="vspixengine.ipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadTextureFromFileComplete method</span></span>

<span data-ttu-id="3406c-104">Función de devolución de llamada que se usa para notificar al host cuando se ha completado una carga de textura.</span><span class="sxs-lookup"><span data-stu-id="3406c-104">A callback function used to notify the host when a texture load has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3406c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3406c-105">Syntax</span></span>


```C++
HRESULT LoadTextureFromFileComplete(
   UINT                               textureId,
   PixEngineTextureDescriptor         textureDesc,
   UINT                               numSlices,
   PixEngineTextureSliceIndex []      count2_sliceIndicies,
   PixEngineTextureSliceDescriptor [] count2_sliceDescriptors,
   UINT                               numFormatOverrides,
   int []                             count5_formatOverrides,
   PixEngineHistogram*                histogram
);
```

## <a name="parameters"></a><span data-ttu-id="3406c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3406c-106">Parameters</span></span>

<span data-ttu-id="3406c-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="3406c-107">*textureId* </span></span>  
<span data-ttu-id="3406c-108">IDENTIFICADOR de la textura cargada.</span><span class="sxs-lookup"><span data-stu-id="3406c-108">The ID of the loaded texture.</span></span>

<span data-ttu-id="3406c-109">*textureDesc* </span><span class="sxs-lookup"><span data-stu-id="3406c-109">*textureDesc* </span></span>  
<span data-ttu-id="3406c-110">Descriptor de textura de la textura cargada.</span><span class="sxs-lookup"><span data-stu-id="3406c-110">The texture descriptor of the loaded texture.</span></span>

<span data-ttu-id="3406c-111">*numSlices* </span><span class="sxs-lookup"><span data-stu-id="3406c-111">*numSlices* </span></span>  
<span data-ttu-id="3406c-112">Número de segmentos que tiene la textura.</span><span class="sxs-lookup"><span data-stu-id="3406c-112">The number of slices the texture has.</span></span>

<span data-ttu-id="3406c-113">*count2 \_ sliceIndicies* </span><span class="sxs-lookup"><span data-stu-id="3406c-113">*count2\_sliceIndicies* </span></span>  
<span data-ttu-id="3406c-114">Segmentar las lenguas indias asociadas a la textura.</span><span class="sxs-lookup"><span data-stu-id="3406c-114">Slice indicies associated with the texture.</span></span>

<span data-ttu-id="3406c-115">*count2 \_ sliceDescriptors* </span><span class="sxs-lookup"><span data-stu-id="3406c-115">*count2\_sliceDescriptors* </span></span>  
<span data-ttu-id="3406c-116">Descriptores de cada segmento.</span><span class="sxs-lookup"><span data-stu-id="3406c-116">Descriptors for each slice.</span></span>

<span data-ttu-id="3406c-117">*numFormatOverrides* </span><span class="sxs-lookup"><span data-stu-id="3406c-117">*numFormatOverrides* </span></span>  
<span data-ttu-id="3406c-118">Número de invalidaciones de formato.</span><span class="sxs-lookup"><span data-stu-id="3406c-118">The number of format overrides.</span></span>

<span data-ttu-id="3406c-119">*count5 \_ formatOverrides* </span><span class="sxs-lookup"><span data-stu-id="3406c-119">*count5\_formatOverrides* </span></span>  
<span data-ttu-id="3406c-120">El formato invalida.</span><span class="sxs-lookup"><span data-stu-id="3406c-120">The format overrides.</span></span>

<span data-ttu-id="3406c-121">*cargas* </span><span class="sxs-lookup"><span data-stu-id="3406c-121">*histogram* </span></span>  
<span data-ttu-id="3406c-122">Dirección de los datos del histograma para la textura cargada.</span><span class="sxs-lookup"><span data-stu-id="3406c-122">The address of histogram data for the loaded texture.</span></span>

## <a name="return-value"></a><span data-ttu-id="3406c-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3406c-123">Return value</span></span>

<span data-ttu-id="3406c-124">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3406c-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3406c-125">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3406c-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3406c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3406c-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3406c-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3406c-127">Header</span></span></p></td><td><span data-ttu-id="3406c-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3406c-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3406c-129"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="3406c-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3406c-130">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="3406c-130">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
