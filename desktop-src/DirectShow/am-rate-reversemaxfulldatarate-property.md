---
description: 'AM_RATE_ReverseMaxFullDataRate propiedad: se aplica a Windows Vista y versiones posteriores.'
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: AM_RATE_ReverseMaxFullDataRate propiedad (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e70a330433c8ea6e8116db944d8fb3d2ffff4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099973"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a><span data-ttu-id="e4ed0-103">Propiedad \_ \_ ReverseMaxFullDataRate de AM RATE</span><span class="sxs-lookup"><span data-stu-id="e4ed0-103">AM\_RATE\_ReverseMaxFullDataRate Property</span></span>

<span data-ttu-id="e4ed0-104">Se aplica a Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e4ed0-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="e4ed0-105">Devuelve la velocidad máxima de reproducción inversa del descodificador.</span><span class="sxs-lookup"><span data-stu-id="e4ed0-105">Returns the decoder's maximum reverse playback rate.</span></span> <span data-ttu-id="e4ed0-106">El valor de la propiedad es el valor absoluto de la velocidad inversa máxima x 10000.</span><span class="sxs-lookup"><span data-stu-id="e4ed0-106">The value of the property is the absolute value of the maximum reverse speed x 10000.</span></span> <span data-ttu-id="e4ed0-107">Por ejemplo, si la velocidad inversa máxima es -2,0, el valor de esta propiedad es 20000.</span><span class="sxs-lookup"><span data-stu-id="e4ed0-107">For example, if the maximum reverse speed is -2.0, the value of this property is 20000.</span></span>

<span data-ttu-id="e4ed0-108">El tipo de datos de esta propiedad **es AM \_ MaxFullDataRate**, que es para `typedef` **LONG.**</span><span class="sxs-lookup"><span data-stu-id="e4ed0-108">The data type for this property is **AM\_MaxFullDataRate**, which is a `typedef` for **LONG**.</span></span>

<span data-ttu-id="e4ed0-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e4ed0-109">This property is read-only.</span></span>



| <span data-ttu-id="e4ed0-110">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="e4ed0-110">Label</span></span> | <span data-ttu-id="e4ed0-111">Valor</span><span class="sxs-lookup"><span data-stu-id="e4ed0-111">Value</span></span> |
|-------------------|----------------------------------|
| <span data-ttu-id="e4ed0-112">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="e4ed0-112">Property Set GUID</span></span> | <span data-ttu-id="e4ed0-113">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="e4ed0-113">AM\_KSPROPSETID\_TSRateChange</span></span>    |
| <span data-ttu-id="e4ed0-114">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="e4ed0-114">Property ID</span></span>       | <span data-ttu-id="e4ed0-115">AM \_ RATE \_ ReverseMaxFullDataRate</span><span class="sxs-lookup"><span data-stu-id="e4ed0-115">AM\_RATE\_ReverseMaxFullDataRate</span></span> |
| <span data-ttu-id="e4ed0-116">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e4ed0-116">Data Type</span></span>         | <span data-ttu-id="e4ed0-117">**AM \_ MaxFullDataRate**</span><span class="sxs-lookup"><span data-stu-id="e4ed0-117">**AM\_MaxFullDataRate**</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="e4ed0-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e4ed0-118">Remarks</span></span>

<span data-ttu-id="e4ed0-119">Los descodificadores que admiten la reproducción inversa sin problemas deben exponer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e4ed0-119">Decoders that support smooth reverse playback should expose this property.</span></span> <span data-ttu-id="e4ed0-120">Para obtener más información, vea [Mejoras de reproducción de DVD en Windows Vista.](dvd-playback-enhancements-in-windows-vista.md)</span><span class="sxs-lookup"><span data-stu-id="e4ed0-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4ed0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4ed0-121">Requirements</span></span>



| <span data-ttu-id="e4ed0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4ed0-122">Requirement</span></span> | <span data-ttu-id="e4ed0-123">Value</span><span class="sxs-lookup"><span data-stu-id="e4ed0-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ed0-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4ed0-124">Header</span></span><br/> | <dl> <span data-ttu-id="e4ed0-125"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="e4ed0-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4ed0-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e4ed0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4ed0-127">**Conjunto de propiedades de cambio de velocidad**</span><span class="sxs-lookup"><span data-stu-id="e4ed0-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




