---
description: Especifica el número predeterminado de fotogramas B consecutivos entre los fotogramas I y P.
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: Propiedad AVEncMPVDefaultBPictureCount (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2026ddcb6a2b4ce813bd8ba2f6144f0c4a32344
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080033"
---
# <a name="avencmpvdefaultbpicturecount-property"></a><span data-ttu-id="693fd-103">Propiedad AVEncMPVDefaultBPictureCount</span><span class="sxs-lookup"><span data-stu-id="693fd-103">AVEncMPVDefaultBPictureCount property</span></span>

<span data-ttu-id="693fd-104">Especifica el número predeterminado de fotogramas B consecutivos entre los fotogramas I y P.</span><span class="sxs-lookup"><span data-stu-id="693fd-104">Specifies the default number of consecutive B frames between I and P frames.</span></span>

<span data-ttu-id="693fd-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="693fd-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="693fd-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="693fd-106">Data type</span></span>

<span data-ttu-id="693fd-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="693fd-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="693fd-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="693fd-108">Property GUID</span></span>

<span data-ttu-id="693fd-109">**CODECAPI \_ AVEncMPVDefaultBPictureCount**</span><span class="sxs-lookup"><span data-stu-id="693fd-109">**CODECAPI\_AVEncMPVDefaultBPictureCount**</span></span>

## <a name="property-value"></a><span data-ttu-id="693fd-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="693fd-110">Property value</span></span>

<span data-ttu-id="693fd-111">Esta propiedad tiene un intervalo de valores lineal.</span><span class="sxs-lookup"><span data-stu-id="693fd-111">This property has a linear range of values.</span></span> <span data-ttu-id="693fd-112">Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="693fd-112">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="693fd-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="693fd-113">Remarks</span></span>

<span data-ttu-id="693fd-114">Antes de Windows 8, esta propiedad se aplica a los codificadores de vídeo MPEG.</span><span class="sxs-lookup"><span data-stu-id="693fd-114">Prior to Windows 8, this property applies to MPEG video encoders.</span></span> <span data-ttu-id="693fd-115">A partir de Windows 8, esta propiedad la usan los codificadores de vídeo MPEG, WMV y H. 264.</span><span class="sxs-lookup"><span data-stu-id="693fd-115">Starting with Windows 8, this property is used by MPEG, WMV, and H.264 video encoders.</span></span>

<span data-ttu-id="693fd-116">Si el codificador admite esta propiedad, se puede usar para controlar la estructura del grupo de imágenes (GOP).</span><span class="sxs-lookup"><span data-stu-id="693fd-116">If the encoder supports this property, it can be used to control the group of pictures (GOP) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="693fd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="693fd-117">Requirements</span></span>



| <span data-ttu-id="693fd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="693fd-118">Requirement</span></span> | <span data-ttu-id="693fd-119">Value</span><span class="sxs-lookup"><span data-stu-id="693fd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="693fd-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="693fd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="693fd-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="693fd-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="693fd-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="693fd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="693fd-123">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="693fd-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="693fd-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="693fd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="693fd-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="693fd-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="693fd-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="693fd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="693fd-127">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="693fd-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="693fd-128">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="693fd-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




