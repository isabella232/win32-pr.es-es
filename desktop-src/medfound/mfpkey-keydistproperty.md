---
description: Especifica el tiempo máximo, en milisegundos, entre los fotogramas clave de la salida del códec.
ms.assetid: 2a52e6a5-10a0-46dd-aa31-cb55094903b5
title: Propiedad MFPKEY_KEYDIST (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55925811db71f24cf360113aa6d03a325bcdc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908770"
---
# <a name="mfpkey_keydist-property"></a><span data-ttu-id="72110-103">\_Propiedad KEYDIST de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="72110-103">MFPKEY\_KEYDIST Property</span></span>

<span data-ttu-id="72110-104">Especifica el tiempo máximo, en milisegundos, entre los fotogramas clave de la salida del códec.</span><span class="sxs-lookup"><span data-stu-id="72110-104">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="72110-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="72110-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="72110-106">g \_ wszWMVCKeyframeDistance</span><span class="sxs-lookup"><span data-stu-id="72110-106">g\_wszWMVCKeyframeDistance</span></span>

## <a name="data-type"></a><span data-ttu-id="72110-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="72110-107">Data Type</span></span>

<span data-ttu-id="72110-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="72110-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="72110-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="72110-109">Default Value</span></span>

<span data-ttu-id="72110-110">El valor predeterminado depende de la versión de Windows que se esté ejecutando, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="72110-110">The default value depends on which version of Windows is running, as shown in the following table.</span></span>



| <span data-ttu-id="72110-111">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="72110-111">Operating system</span></span> | <span data-ttu-id="72110-112">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="72110-112">Default value</span></span> |
|------------------|---------------|
| <span data-ttu-id="72110-113">Windows XP</span><span class="sxs-lookup"><span data-stu-id="72110-113">Windows XP</span></span>       | <span data-ttu-id="72110-114">8000</span><span class="sxs-lookup"><span data-stu-id="72110-114">8000</span></span>          |
| <span data-ttu-id="72110-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72110-115">Windows Vista</span></span>    | <span data-ttu-id="72110-116">8000</span><span class="sxs-lookup"><span data-stu-id="72110-116">8000</span></span>          |
| <span data-ttu-id="72110-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="72110-117">Windows 7</span></span>        | <span data-ttu-id="72110-118">2000</span><span class="sxs-lookup"><span data-stu-id="72110-118">2000</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="72110-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72110-119">Remarks</span></span>

<span data-ttu-id="72110-120">La lógica interna del códec determina la ubicación real de cada fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="72110-120">The internal logic of the codec determines the actual location of each key frame.</span></span> <span data-ttu-id="72110-121">La distancia entre dos fotogramas clave puede ser menor que el valor de esta propiedad; sin embargo, nunca será mayor.</span><span class="sxs-lookup"><span data-stu-id="72110-121">The distance between any two key frames may be less than the value of this property, however, it will never be greater.</span></span>

## <a name="requirements"></a><span data-ttu-id="72110-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72110-122">Requirements</span></span>



| <span data-ttu-id="72110-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="72110-123">Requirement</span></span> | <span data-ttu-id="72110-124">Value</span><span class="sxs-lookup"><span data-stu-id="72110-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72110-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72110-125">Minimum supported client</span></span><br/> | <span data-ttu-id="72110-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="72110-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="72110-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72110-127">Minimum supported server</span></span><br/> | <span data-ttu-id="72110-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="72110-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="72110-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72110-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="72110-130"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="72110-130"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72110-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="72110-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72110-132">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="72110-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




