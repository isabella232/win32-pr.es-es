---
description: Especifica la configuración predeterminada para el bit de copyright en la secuencia de audio MPEG-1. Esta propiedad se aplica a los codificadores de audio MPEG.
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: Propiedad AVEncMPACopyright (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4449c41448d59ce673e667be7400d4a713236dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423027"
---
# <a name="avencmpacopyright-property"></a><span data-ttu-id="5bb33-104">Propiedad AVEncMPACopyright</span><span class="sxs-lookup"><span data-stu-id="5bb33-104">AVEncMPACopyright property</span></span>

<span data-ttu-id="5bb33-105">Especifica la configuración predeterminada para el bit de copyright en la secuencia de audio MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="5bb33-105">Specifies the default setting for the copyright bit in the MPEG-1 audio stream.</span></span> <span data-ttu-id="5bb33-106">Esta propiedad se aplica a los codificadores de audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="5bb33-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="5bb33-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5bb33-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="5bb33-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5bb33-108">Data type</span></span>

<span data-ttu-id="5bb33-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="5bb33-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5bb33-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="5bb33-110">Property GUID</span></span>

<span data-ttu-id="5bb33-111">**CODECAPI \_ AVEncMPACopyright**</span><span class="sxs-lookup"><span data-stu-id="5bb33-111">**CODECAPI\_AVEncMPACopyright**</span></span>

## <a name="property-value"></a><span data-ttu-id="5bb33-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5bb33-112">Property value</span></span>

<span data-ttu-id="5bb33-113">Esta propiedad puede tener los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5bb33-113">This property can have the following values.</span></span>



| <span data-ttu-id="5bb33-114">Value</span><span class="sxs-lookup"><span data-stu-id="5bb33-114">Value</span></span>          | <span data-ttu-id="5bb33-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5bb33-115">Description</span></span>           |
|----------------|-----------------------|
| <span data-ttu-id="5bb33-116">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="5bb33-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="5bb33-117">El bit de copyright está desactivado.</span><span class="sxs-lookup"><span data-stu-id="5bb33-117">Copyright bit is off.</span></span> |
| <span data-ttu-id="5bb33-118">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="5bb33-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="5bb33-119">El bit de copyright está activado.</span><span class="sxs-lookup"><span data-stu-id="5bb33-119">Copyright bit is on.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="5bb33-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bb33-120">Remarks</span></span>

<span data-ttu-id="5bb33-121">El codificador podría invalidar esta configuración, en función del contenido del flujo de entrada.</span><span class="sxs-lookup"><span data-stu-id="5bb33-121">The encoder might override this setting, based on the contents of the input stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bb33-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bb33-122">Requirements</span></span>



| <span data-ttu-id="5bb33-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bb33-123">Requirement</span></span> | <span data-ttu-id="5bb33-124">Value</span><span class="sxs-lookup"><span data-stu-id="5bb33-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5bb33-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bb33-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5bb33-126">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="5bb33-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="5bb33-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bb33-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5bb33-128">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="5bb33-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5bb33-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5bb33-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bb33-130"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bb33-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bb33-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bb33-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bb33-132">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="5bb33-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="5bb33-133">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="5bb33-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




