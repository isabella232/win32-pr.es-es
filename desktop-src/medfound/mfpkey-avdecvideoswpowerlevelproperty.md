---
description: Especifica el nivel de energía para el descodificador.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: Propiedad MFPKEY_AVDecVideoSWPowerLevel (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2180e26d3e14263c14f2f3603c8c92cf8c11daec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696596"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a><span data-ttu-id="147ca-103">\_Propiedad AVDecVideoSWPowerLevel de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="147ca-103">MFPKEY\_AVDecVideoSWPowerLevel Property</span></span>

<span data-ttu-id="147ca-104">Especifica el nivel de energía para el descodificador.</span><span class="sxs-lookup"><span data-stu-id="147ca-104">Specifies the power level for the decoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="147ca-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="147ca-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="147ca-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="147ca-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="147ca-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="147ca-107">Data Type</span></span>

<span data-ttu-id="147ca-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="147ca-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="147ca-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="147ca-109">Default Value</span></span>

<span data-ttu-id="147ca-110">**100**</span><span class="sxs-lookup"><span data-stu-id="147ca-110">**100**</span></span>

## <a name="remarks"></a><span data-ttu-id="147ca-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="147ca-111">Remarks</span></span>

<span data-ttu-id="147ca-112">Esta propiedad debe establecerse en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="147ca-112">This property must be set to one of the following values.</span></span>



| <span data-ttu-id="147ca-113">Value</span><span class="sxs-lookup"><span data-stu-id="147ca-113">Value</span></span> | <span data-ttu-id="147ca-114">Significado</span><span class="sxs-lookup"><span data-stu-id="147ca-114">Meaning</span></span>                                                             |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="147ca-115">0</span><span class="sxs-lookup"><span data-stu-id="147ca-115">0</span></span>     | <span data-ttu-id="147ca-116">El descodificador usa un nivel de energía optimizado para la duración de la batería.</span><span class="sxs-lookup"><span data-stu-id="147ca-116">The decoder uses a power level that is optimized for battery life.</span></span>  |
| <span data-ttu-id="147ca-117">50</span><span class="sxs-lookup"><span data-stu-id="147ca-117">50</span></span>    | <span data-ttu-id="147ca-118">El descodificador utiliza un nivel de energía equilibrado.</span><span class="sxs-lookup"><span data-stu-id="147ca-118">The decoder uses a balanced power level.</span></span>                            |
| <span data-ttu-id="147ca-119">100</span><span class="sxs-lookup"><span data-stu-id="147ca-119">100</span></span>   | <span data-ttu-id="147ca-120">El descodificador usa un nivel de energía optimizado para la calidad de vídeo.</span><span class="sxs-lookup"><span data-stu-id="147ca-120">The decoder uses a power level that is optimized for video quality.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="147ca-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="147ca-121">Requirements</span></span>



| <span data-ttu-id="147ca-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="147ca-122">Requirement</span></span> | <span data-ttu-id="147ca-123">Value</span><span class="sxs-lookup"><span data-stu-id="147ca-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="147ca-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="147ca-124">Minimum supported client</span></span><br/> | <span data-ttu-id="147ca-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="147ca-125">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="147ca-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="147ca-126">Minimum supported server</span></span><br/> | <span data-ttu-id="147ca-127">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="147ca-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="147ca-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="147ca-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="147ca-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="147ca-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="147ca-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="147ca-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="147ca-131">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="147ca-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
