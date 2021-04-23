---
description: Se aplica a Windows Vista y versiones posteriores.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: AM_RATE_ReverseMaxFullDataRate propiedad (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31e376c6e95160c6a6c3c6637a765d868e282d33
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910243"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a><span data-ttu-id="b2ec9-103">Propiedad AM \_ RATE \_ ReverseMaxFullDataRate</span><span class="sxs-lookup"><span data-stu-id="b2ec9-103">AM\_RATE\_ReverseMaxFullDataRate Property</span></span>

<span data-ttu-id="b2ec9-104">Se aplica a Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b2ec9-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="b2ec9-105">Devuelve la velocidad máxima de reproducción inversa del descodificador.</span><span class="sxs-lookup"><span data-stu-id="b2ec9-105">Returns the decoder's maximum reverse playback rate.</span></span> <span data-ttu-id="b2ec9-106">El valor de la propiedad es el valor absoluto de la velocidad inversa máxima x 10000.</span><span class="sxs-lookup"><span data-stu-id="b2ec9-106">The value of the property is the absolute value of the maximum reverse speed x 10000.</span></span> <span data-ttu-id="b2ec9-107">Por ejemplo, si la velocidad inversa máxima es -2,0, el valor de esta propiedad es 20000.</span><span class="sxs-lookup"><span data-stu-id="b2ec9-107">For example, if the maximum reverse speed is -2.0, the value of this property is 20000.</span></span>

<span data-ttu-id="b2ec9-108">El tipo de datos de esta propiedad **es AM \_ MaxFullDataRate,** que es para `typedef` **LONG.**</span><span class="sxs-lookup"><span data-stu-id="b2ec9-108">The data type for this property is **AM\_MaxFullDataRate**, which is a `typedef` for **LONG**.</span></span>

<span data-ttu-id="b2ec9-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b2ec9-109">This property is read-only.</span></span>



| <span data-ttu-id="b2ec9-110">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="b2ec9-110">Label</span></span> | <span data-ttu-id="b2ec9-111">Value</span><span class="sxs-lookup"><span data-stu-id="b2ec9-111">Value</span></span> |
|-------------------|----------------------------------|
| <span data-ttu-id="b2ec9-112">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="b2ec9-112">Property Set GUID</span></span> | <span data-ttu-id="b2ec9-113">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="b2ec9-113">AM\_KSPROPSETID\_TSRateChange</span></span>    |
| <span data-ttu-id="b2ec9-114">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="b2ec9-114">Property ID</span></span>       | <span data-ttu-id="b2ec9-115">AM \_ RATE \_ ReverseMaxFullDataRate</span><span class="sxs-lookup"><span data-stu-id="b2ec9-115">AM\_RATE\_ReverseMaxFullDataRate</span></span> |
| <span data-ttu-id="b2ec9-116">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b2ec9-116">Data Type</span></span>         | <span data-ttu-id="b2ec9-117">**AM \_ MaxFullDataRate**</span><span class="sxs-lookup"><span data-stu-id="b2ec9-117">**AM\_MaxFullDataRate**</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="b2ec9-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b2ec9-118">Remarks</span></span>

<span data-ttu-id="b2ec9-119">Los descodificadores que admiten la reproducción inversa sin problemas deben exponer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b2ec9-119">Decoders that support smooth reverse playback should expose this property.</span></span> <span data-ttu-id="b2ec9-120">Para obtener más información, vea [Dvd Playback Enhancements in Windows Vista (Mejoras](dvd-playback-enhancements-in-windows-vista.md)de reproducción de DVD en Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="b2ec9-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2ec9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2ec9-121">Requirements</span></span>



| <span data-ttu-id="b2ec9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2ec9-122">Requirement</span></span> | <span data-ttu-id="b2ec9-123">Value</span><span class="sxs-lookup"><span data-stu-id="b2ec9-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2ec9-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2ec9-124">Header</span></span><br/> | <dl> <span data-ttu-id="b2ec9-125"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="b2ec9-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2ec9-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b2ec9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2ec9-127">**Conjunto de propiedades de cambio de frecuencia**</span><span class="sxs-lookup"><span data-stu-id="b2ec9-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




