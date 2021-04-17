---
description: Se aplica a Windows Vista y versiones posteriores.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: Propiedad AM_RATE_ReverseMaxFullDataRate (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679e83038a74e64d7a39e8757a9ffaf61fc88c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660951"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a><span data-ttu-id="31fb7-103">\_Propiedad ReverseMaxFullDataRate de tasa AM \_</span><span class="sxs-lookup"><span data-stu-id="31fb7-103">AM\_RATE\_ReverseMaxFullDataRate Property</span></span>

<span data-ttu-id="31fb7-104">Se aplica a Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="31fb7-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="31fb7-105">Devuelve la velocidad máxima de reproducción inversa del descodificador.</span><span class="sxs-lookup"><span data-stu-id="31fb7-105">Returns the decoder's maximum reverse playback rate.</span></span> <span data-ttu-id="31fb7-106">El valor de la propiedad es el valor absoluto de la velocidad máxima inversa x 10000.</span><span class="sxs-lookup"><span data-stu-id="31fb7-106">The value of the property is the absolute value of the maximum reverse speed x 10000.</span></span> <span data-ttu-id="31fb7-107">Por ejemplo, si la velocidad máxima inversa es-2,0, el valor de esta propiedad es 20000.</span><span class="sxs-lookup"><span data-stu-id="31fb7-107">For example, if the maximum reverse speed is -2.0, the value of this property is 20000.</span></span>

<span data-ttu-id="31fb7-108">El tipo de datos de esta propiedad es **AM \_ MaxFullDataRate**, que es un `typedef` para **Long**.</span><span class="sxs-lookup"><span data-stu-id="31fb7-108">The data type for this property is **AM\_MaxFullDataRate**, which is a `typedef` for **LONG**.</span></span>

<span data-ttu-id="31fb7-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="31fb7-109">This property is read-only.</span></span>



|                   |                                  |
|-------------------|----------------------------------|
| <span data-ttu-id="31fb7-110">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="31fb7-110">Property Set GUID</span></span> | <span data-ttu-id="31fb7-111">\_TSRateChange KSPROPSETID \_ AM</span><span class="sxs-lookup"><span data-stu-id="31fb7-111">AM\_KSPROPSETID\_TSRateChange</span></span>    |
| <span data-ttu-id="31fb7-112">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="31fb7-112">Property ID</span></span>       | <span data-ttu-id="31fb7-113">Tasa de AM \_ \_ ReverseMaxFullDataRate</span><span class="sxs-lookup"><span data-stu-id="31fb7-113">AM\_RATE\_ReverseMaxFullDataRate</span></span> |
| <span data-ttu-id="31fb7-114">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="31fb7-114">Data Type</span></span>         | <span data-ttu-id="31fb7-115">**\_MAXFULLDATARATE AM**</span><span class="sxs-lookup"><span data-stu-id="31fb7-115">**AM\_MaxFullDataRate**</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="31fb7-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31fb7-116">Remarks</span></span>

<span data-ttu-id="31fb7-117">Los descodificadores que admiten la reproducción fluida inversa deben exponer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="31fb7-117">Decoders that support smooth reverse playback should expose this property.</span></span> <span data-ttu-id="31fb7-118">Para obtener más información, consulte [mejoras en la reproducción de DVD en Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="31fb7-118">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31fb7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31fb7-119">Requirements</span></span>



| <span data-ttu-id="31fb7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="31fb7-120">Requirement</span></span> | <span data-ttu-id="31fb7-121">Value</span><span class="sxs-lookup"><span data-stu-id="31fb7-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31fb7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31fb7-122">Header</span></span><br/> | <dl> <span data-ttu-id="31fb7-123"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="31fb7-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31fb7-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="31fb7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31fb7-125">**Conjunto de propiedades de cambio de velocidad**</span><span class="sxs-lookup"><span data-stu-id="31fb7-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




