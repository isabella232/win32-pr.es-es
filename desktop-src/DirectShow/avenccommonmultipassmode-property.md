---
description: Especifica el número de pasos de codificación que admite el codificador.
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: Propiedad AVEncCommonMultipassMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4302cf0a9524f16dee8e7b84060065a4c750e4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906792"
---
# <a name="avenccommonmultipassmode-property"></a><span data-ttu-id="1fd64-103">Propiedad AVEncCommonMultipassMode</span><span class="sxs-lookup"><span data-stu-id="1fd64-103">AVEncCommonMultipassMode property</span></span>

<span data-ttu-id="1fd64-104">Especifica el número de pasos de codificación que admite el codificador.</span><span class="sxs-lookup"><span data-stu-id="1fd64-104">Specifies the number of encoding passes that the encoder supports.</span></span>

<span data-ttu-id="1fd64-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1fd64-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="1fd64-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1fd64-106">Data type</span></span>

<span data-ttu-id="1fd64-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="1fd64-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="1fd64-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="1fd64-108">Property GUID</span></span>

<span data-ttu-id="1fd64-109">**CODECAPI \_ AVEncCommonMultipassMode**</span><span class="sxs-lookup"><span data-stu-id="1fd64-109">**CODECAPI\_AVEncCommonMultipassMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="1fd64-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1fd64-110">Property value</span></span>

<span data-ttu-id="1fd64-111">Esta propiedad se devuelve como un intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="1fd64-111">This property is returned as a range of values.</span></span> <span data-ttu-id="1fd64-112">Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="1fd64-112">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="1fd64-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1fd64-113">Remarks</span></span>

<span data-ttu-id="1fd64-114">La latencia de descodificación se define como la cantidad de datos que el descodificador debe almacenar en búfer.</span><span class="sxs-lookup"><span data-stu-id="1fd64-114">Decoding latency is defined as the amount of data the decoder must buffer.</span></span> <span data-ttu-id="1fd64-115">Por ejemplo, si se establece esta propiedad en **Variant \_ true** en un codificador de vídeo MPEG, se limitan los tipos de estructuras GOP que el codificador puede utilizar.</span><span class="sxs-lookup"><span data-stu-id="1fd64-115">For example, setting this property to **VARIANT\_TRUE** on an MPEG video encoder limits the types of GOP structures the encoder can use.</span></span>

<span data-ttu-id="1fd64-116">Para establecer la fase de codificación actual, establezca la propiedad [**AVEncCommonPassStart**](avenccommonpassstart-property.md) .</span><span class="sxs-lookup"><span data-stu-id="1fd64-116">To set the current encoding pass, set the [**AVEncCommonPassStart**](avenccommonpassstart-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fd64-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fd64-117">Requirements</span></span>



| <span data-ttu-id="1fd64-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fd64-118">Requirement</span></span> | <span data-ttu-id="1fd64-119">Value</span><span class="sxs-lookup"><span data-stu-id="1fd64-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fd64-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fd64-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1fd64-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="1fd64-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="1fd64-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fd64-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1fd64-123">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="1fd64-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="1fd64-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fd64-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fd64-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fd64-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fd64-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fd64-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fd64-127">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="1fd64-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="1fd64-128">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="1fd64-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




