---
description: Esta propiedad se usa para indicar qué versión del conjunto de propiedades De cambio de frecuencia debe usar el descodificador.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: AM_RATE_UseRateVersion propiedad (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd33ef96c50ecc3da0711f08f0c7ffbf0a20825
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910223"
---
# <a name="am_rate_userateversion-property"></a><span data-ttu-id="1dd7a-103">Propiedad \_ \_ UseRateVersion de AM RATE</span><span class="sxs-lookup"><span data-stu-id="1dd7a-103">AM\_RATE\_UseRateVersion Property</span></span>

<span data-ttu-id="1dd7a-104">Esta propiedad se usa para indicar qué versión del conjunto de propiedades De cambio de frecuencia debe usar el descodificador.</span><span class="sxs-lookup"><span data-stu-id="1dd7a-104">This property is used to signal which version of the Rate Change property set the decoder should use.</span></span> <span data-ttu-id="1dd7a-105">El valor es un **tipo WORD.**</span><span class="sxs-lookup"><span data-stu-id="1dd7a-105">The value is a **WORD** type.</span></span> <span data-ttu-id="1dd7a-106">El byte de orden superior contiene el número de versión secundaria y el byte de orden bajo contiene el byte de orden bajo.</span><span class="sxs-lookup"><span data-stu-id="1dd7a-106">The high-order byte contains the minor version number, and the low-order byte contains the low-order byte.</span></span> <span data-ttu-id="1dd7a-107">Por lo tanto, la versión 1.1 se señala con el valor 0x0101.</span><span class="sxs-lookup"><span data-stu-id="1dd7a-107">Thus, version 1.1 is signaled with the value 0x0101.</span></span>

<span data-ttu-id="1dd7a-108">Si el descodificador no admite la versión especificada, debe producir un error en la llamada a [**IKsPropertySet::Set**](ikspropertyset-set.md) y devolver E \_ NOINTERFACE.</span><span class="sxs-lookup"><span data-stu-id="1dd7a-108">If the decoder does not support the specified version, it should fail the call to [**IKsPropertySet::Set**](ikspropertyset-set.md) and return E\_NOINTERFACE.</span></span> <span data-ttu-id="1dd7a-109">Si el filtro de origen no establece la versión, el descodificador debe tener como valor predeterminado la versión 1.0.</span><span class="sxs-lookup"><span data-stu-id="1dd7a-109">If the source filter does not set the version, the decoder should default to version 1.0.</span></span>



| <span data-ttu-id="1dd7a-110">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="1dd7a-110">Label</span></span> | <span data-ttu-id="1dd7a-111">Value</span><span class="sxs-lookup"><span data-stu-id="1dd7a-111">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="1dd7a-112">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="1dd7a-112">Property Set GUID</span></span> | <span data-ttu-id="1dd7a-113">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="1dd7a-113">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="1dd7a-114">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="1dd7a-114">Property ID</span></span>       | <span data-ttu-id="1dd7a-115">AM \_ RATE \_ UseRateVersion</span><span class="sxs-lookup"><span data-stu-id="1dd7a-115">AM\_RATE\_UseRateVersion</span></span>      |
| <span data-ttu-id="1dd7a-116">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1dd7a-116">Data Type</span></span>         | <span data-ttu-id="1dd7a-117">**WORD**</span><span class="sxs-lookup"><span data-stu-id="1dd7a-117">**WORD**</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="1dd7a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dd7a-118">Requirements</span></span>



| <span data-ttu-id="1dd7a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dd7a-119">Requirement</span></span> | <span data-ttu-id="1dd7a-120">Value</span><span class="sxs-lookup"><span data-stu-id="1dd7a-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd7a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1dd7a-121">Header</span></span><br/> | <dl> <span data-ttu-id="1dd7a-122"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="1dd7a-122"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dd7a-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1dd7a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dd7a-124">**Conjunto de propiedades de cambio de frecuencia**</span><span class="sxs-lookup"><span data-stu-id="1dd7a-124">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




