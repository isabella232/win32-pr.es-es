---
description: Obtiene el tamaño de la imagen descodificada, en píxeles.
ms.assetid: 2F0DD10F-CF7A-4A6F-91A9-E3828DF2B947
title: Propiedad AVDecVideoImageSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cbe8fc3e77de920588ca1f0ee31d86f19c7e667
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666143"
---
# <a name="avdecvideoimagesize-property"></a><span data-ttu-id="ae2ed-103">Propiedad AVDecVideoImageSize</span><span class="sxs-lookup"><span data-stu-id="ae2ed-103">AVDecVideoImageSize property</span></span>

<span data-ttu-id="ae2ed-104">Obtiene el tamaño de la imagen descodificada, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ae2ed-104">Gets the size of the decoded image, in pixels.</span></span>

<span data-ttu-id="ae2ed-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ae2ed-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="ae2ed-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ae2ed-106">Data type</span></span>

<span data-ttu-id="ae2ed-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="ae2ed-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ae2ed-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="ae2ed-108">Property GUID</span></span>

<span data-ttu-id="ae2ed-109">**CODECAPI \_ AVDecVideoImageSize**</span><span class="sxs-lookup"><span data-stu-id="ae2ed-109">**CODECAPI\_AVDecVideoImageSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="ae2ed-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ae2ed-110">Property value</span></span>

<span data-ttu-id="ae2ed-111">Los 16 bits superiores contienen el ancho y los 16 bits inferiores contienen el alto.</span><span class="sxs-lookup"><span data-stu-id="ae2ed-111">The high 16 bits contain the width, and the low 16 bits contain the height.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae2ed-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae2ed-112">Remarks</span></span>

<span data-ttu-id="ae2ed-113">El número de canales incluye el canal de efecto de baja frecuencia (LFE), si está presente.</span><span class="sxs-lookup"><span data-stu-id="ae2ed-113">The number of channels includes the low frequency effect (LFE) channel, if present.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae2ed-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae2ed-114">Requirements</span></span>



| <span data-ttu-id="ae2ed-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae2ed-115">Requirement</span></span> | <span data-ttu-id="ae2ed-116">Value</span><span class="sxs-lookup"><span data-stu-id="ae2ed-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2ed-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae2ed-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ae2ed-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="ae2ed-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ae2ed-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae2ed-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ae2ed-120">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="ae2ed-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ae2ed-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae2ed-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae2ed-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae2ed-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae2ed-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae2ed-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2ed-124">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="ae2ed-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="ae2ed-125">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="ae2ed-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




