---
description: Especifica si se debe agregar una comprobación de redundancia cíclica (CRC) al encabezado del marco. Esta propiedad se aplica a los codificadores de audio MPEG.
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: Propiedad AVEncMPAEnableRedundancyProtection (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2028b5adaad55d46cc53c61f9d65a73819cc899
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659279"
---
# <a name="avencmpaenableredundancyprotection-property"></a><span data-ttu-id="04875-104">Propiedad AVEncMPAEnableRedundancyProtection</span><span class="sxs-lookup"><span data-stu-id="04875-104">AVEncMPAEnableRedundancyProtection property</span></span>

<span data-ttu-id="04875-105">Especifica si se debe agregar una comprobación de redundancia cíclica (CRC) al encabezado del marco.</span><span class="sxs-lookup"><span data-stu-id="04875-105">Specifies whether to add a cyclic redundancy check (CRC) to the frame header.</span></span> <span data-ttu-id="04875-106">Esta propiedad se aplica a los codificadores de audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="04875-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="04875-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="04875-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="04875-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="04875-108">Data type</span></span>

<span data-ttu-id="04875-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="04875-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="04875-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="04875-110">Property GUID</span></span>

<span data-ttu-id="04875-111">**CODECAPI \_ AVEncMPAEnableRedundancyProtection**</span><span class="sxs-lookup"><span data-stu-id="04875-111">**CODECAPI\_AVEncMPAEnableRedundancyProtection**</span></span>

## <a name="property-value"></a><span data-ttu-id="04875-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="04875-112">Property value</span></span>

<span data-ttu-id="04875-113">Esta propiedad puede tener los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="04875-113">This property can have the following values.</span></span>



| <span data-ttu-id="04875-114">Value</span><span class="sxs-lookup"><span data-stu-id="04875-114">Value</span></span>          | <span data-ttu-id="04875-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="04875-115">Description</span></span>                |
|----------------|----------------------------|
| <span data-ttu-id="04875-116">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="04875-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="04875-117">No agregue una suma de comprobación CRC.</span><span class="sxs-lookup"><span data-stu-id="04875-117">Do not add a CRC checksum.</span></span> |
| <span data-ttu-id="04875-118">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="04875-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="04875-119">Agregue una suma de comprobación CRC.</span><span class="sxs-lookup"><span data-stu-id="04875-119">Add a CRC checksum.</span></span>        |



 

## <a name="requirements"></a><span data-ttu-id="04875-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04875-120">Requirements</span></span>



| <span data-ttu-id="04875-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="04875-121">Requirement</span></span> | <span data-ttu-id="04875-122">Value</span><span class="sxs-lookup"><span data-stu-id="04875-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04875-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04875-123">Minimum supported client</span></span><br/> | <span data-ttu-id="04875-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="04875-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="04875-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04875-125">Minimum supported server</span></span><br/> | <span data-ttu-id="04875-126">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="04875-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="04875-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04875-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="04875-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="04875-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04875-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="04875-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04875-130">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="04875-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="04875-131">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="04875-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




