---
description: 'Propiedad AVEncAudioDualMono: especifica si el audio de 2 canales está codificado como estéreo o mono dual.'
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: Propiedad AVEncAudioDualMono (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58cbd901079d8f4dede1efae140791ae99c7fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096583"
---
# <a name="avencaudiodualmono-property"></a><span data-ttu-id="a7035-103">Propiedad AVEncAudioDualMono</span><span class="sxs-lookup"><span data-stu-id="a7035-103">AVEncAudioDualMono property</span></span>

<span data-ttu-id="a7035-104">Especifica si el audio de 2 canales está codificado como estéreo o mono dual.</span><span class="sxs-lookup"><span data-stu-id="a7035-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="a7035-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a7035-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a7035-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a7035-106">Data type</span></span>

<span data-ttu-id="a7035-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a7035-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a7035-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="a7035-108">Property GUID</span></span>

<span data-ttu-id="a7035-109">**CODECAPI \_ AVEncAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="a7035-109">**CODECAPI\_AVEncAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="a7035-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a7035-110">Property value</span></span>

<span data-ttu-id="a7035-111">El valor de esta propiedad es un miembro de la [**enumeración eAVEncAudioDualMono.**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono)</span><span class="sxs-lookup"><span data-stu-id="a7035-111">The value of this property is a member of the [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7035-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a7035-112">Remarks</span></span>

<span data-ttu-id="a7035-113">Esta propiedad no se aplica a los codificadores de audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="a7035-113">This property does not apply to MPEG audio encoders.</span></span> <span data-ttu-id="a7035-114">Para el audio MPEG, use [**la propiedad AVEncMPACodingMode.**](avencmpacodingmode-property.md)</span><span class="sxs-lookup"><span data-stu-id="a7035-114">For MPEG audio, use the [**AVEncMPACodingMode**](avencmpacodingmode-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7035-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7035-115">Requirements</span></span>



| <span data-ttu-id="a7035-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7035-116">Requirement</span></span> | <span data-ttu-id="a7035-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a7035-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7035-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7035-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a7035-119">Aplicaciones de escritorio de Windows 2000 Professional \[ \| para aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="a7035-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a7035-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7035-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a7035-121">Aplicaciones de escritorio de Windows 2000 Server \[ \| para aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="a7035-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a7035-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7035-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7035-123"><dt>Codecapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="a7035-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7035-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a7035-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7035-125">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="a7035-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a7035-126">**ICodecAPI (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="a7035-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

