---
description: Esta propiedad se usa para indicar qué versión del conjunto de propiedades de cambio de velocidad debe usar el descodificador.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: Propiedad AM_RATE_UseRateVersion (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab609d2d38dc28257d13994e6cd464094b714be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660948"
---
# <a name="am_rate_userateversion-property"></a><span data-ttu-id="1cc4a-103">\_Propiedad UseRateVersion de tasa AM \_</span><span class="sxs-lookup"><span data-stu-id="1cc4a-103">AM\_RATE\_UseRateVersion Property</span></span>

<span data-ttu-id="1cc4a-104">Esta propiedad se usa para indicar qué versión del conjunto de propiedades de cambio de velocidad debe usar el descodificador.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-104">This property is used to signal which version of the Rate Change property set the decoder should use.</span></span> <span data-ttu-id="1cc4a-105">El valor es un tipo de **palabra** .</span><span class="sxs-lookup"><span data-stu-id="1cc4a-105">The value is a **WORD** type.</span></span> <span data-ttu-id="1cc4a-106">El byte de orden superior contiene el número de versión secundaria y el byte de orden inferior contiene el byte de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-106">The high-order byte contains the minor version number, and the low-order byte contains the low-order byte.</span></span> <span data-ttu-id="1cc4a-107">Por lo tanto, la versión 1,1 se señala con el valor 0x0101.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-107">Thus, version 1.1 is signaled with the value 0x0101.</span></span>

<span data-ttu-id="1cc4a-108">Si el descodificador no admite la versión especificada, se debería producir un error en la llamada a [**IKsPropertySet:: set**](ikspropertyset-set.md) y devolver E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-108">If the decoder does not support the specified version, it should fail the call to [**IKsPropertySet::Set**](ikspropertyset-set.md) and return E\_NOINTERFACE.</span></span> <span data-ttu-id="1cc4a-109">Si el filtro de origen no establece la versión, el descodificador debería tener como valor predeterminado la versión 1,0.</span><span class="sxs-lookup"><span data-stu-id="1cc4a-109">If the source filter does not set the version, the decoder should default to version 1.0.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="1cc4a-110">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="1cc4a-110">Property Set GUID</span></span> | <span data-ttu-id="1cc4a-111">\_TSRateChange KSPROPSETID \_ AM</span><span class="sxs-lookup"><span data-stu-id="1cc4a-111">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="1cc4a-112">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="1cc4a-112">Property ID</span></span>       | <span data-ttu-id="1cc4a-113">Tasa de AM \_ \_ UseRateVersion</span><span class="sxs-lookup"><span data-stu-id="1cc4a-113">AM\_RATE\_UseRateVersion</span></span>      |
| <span data-ttu-id="1cc4a-114">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1cc4a-114">Data Type</span></span>         | <span data-ttu-id="1cc4a-115">**WORD**</span><span class="sxs-lookup"><span data-stu-id="1cc4a-115">**WORD**</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="1cc4a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cc4a-116">Requirements</span></span>



| <span data-ttu-id="1cc4a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cc4a-117">Requirement</span></span> | <span data-ttu-id="1cc4a-118">Value</span><span class="sxs-lookup"><span data-stu-id="1cc4a-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc4a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cc4a-119">Header</span></span><br/> | <dl> <span data-ttu-id="1cc4a-120"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cc4a-120"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cc4a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cc4a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc4a-122">**Conjunto de propiedades de cambio de velocidad**</span><span class="sxs-lookup"><span data-stu-id="1cc4a-122">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




