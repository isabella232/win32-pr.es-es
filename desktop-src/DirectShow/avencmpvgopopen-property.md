---
description: Especifica si el codificador genera grupos abiertos de imágenes (GOP) o GOP cerrados. Esta propiedad se aplica a los codificadores de vídeo MPEG.
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: Propiedad AVEncMPVGOPOpen (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd971a6cc9926245b97794868f58758af814803
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806344"
---
# <a name="avencmpvgopopen-property"></a><span data-ttu-id="2dbe9-104">Propiedad AVEncMPVGOPOpen</span><span class="sxs-lookup"><span data-stu-id="2dbe9-104">AVEncMPVGOPOpen property</span></span>

<span data-ttu-id="2dbe9-105">Especifica si el codificador genera grupos abiertos de imágenes (GOP) o GOP cerrados.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-105">Specifies whether the encoder produces open groups of pictures (GOPs) or closed GOPs.</span></span> <span data-ttu-id="2dbe9-106">Esta propiedad se aplica a los codificadores de vídeo MPEG.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="2dbe9-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="2dbe9-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2dbe9-108">Data type</span></span>

<span data-ttu-id="2dbe9-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="2dbe9-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="2dbe9-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="2dbe9-110">Property GUID</span></span>

<span data-ttu-id="2dbe9-111">**CODECAPI \_ AVEncMPVGOPOpen**</span><span class="sxs-lookup"><span data-stu-id="2dbe9-111">**CODECAPI\_AVEncMPVGOPOpen**</span></span>

## <a name="property-value"></a><span data-ttu-id="2dbe9-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2dbe9-112">Property value</span></span>



| <span data-ttu-id="2dbe9-113">Value</span><span class="sxs-lookup"><span data-stu-id="2dbe9-113">Value</span></span>          | <span data-ttu-id="2dbe9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2dbe9-114">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="2dbe9-115">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="2dbe9-115">VARIANT\_FALSE</span></span> | <span data-ttu-id="2dbe9-116">GOP cerrado</span><span class="sxs-lookup"><span data-stu-id="2dbe9-116">Closed GOPs</span></span> |
| <span data-ttu-id="2dbe9-117">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="2dbe9-117">VARIANT\_TRUE</span></span>  | <span data-ttu-id="2dbe9-118">Abrir GOP</span><span class="sxs-lookup"><span data-stu-id="2dbe9-118">Open GOPs</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="2dbe9-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2dbe9-119">Remarks</span></span>

<span data-ttu-id="2dbe9-120">Un GOP abierto contiene fotogramas Delta que hacen referencia a fotogramas del GOP anterior.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-120">An open GOP contains delta frames that reference frames from the previous GOP.</span></span> <span data-ttu-id="2dbe9-121">Un GOP cerrado no contiene ningún fotograma Delta que haga referencia al GOP anterior.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-121">A closed GOP does not contain any delta frames that reference the previous GOP.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dbe9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dbe9-122">Requirements</span></span>



| <span data-ttu-id="2dbe9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dbe9-123">Requirement</span></span> | <span data-ttu-id="2dbe9-124">Value</span><span class="sxs-lookup"><span data-stu-id="2dbe9-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2dbe9-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dbe9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2dbe9-126">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="2dbe9-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="2dbe9-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dbe9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2dbe9-128">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="2dbe9-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2dbe9-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2dbe9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dbe9-130"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dbe9-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dbe9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="2dbe9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dbe9-132">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="2dbe9-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="2dbe9-133">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="2dbe9-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




