---
description: El método DVDAdm. GetParentalCountry recupera el país o la región parental que se guardó por última vez en el registro.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: Método GetParentalCountry (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fcee63fd3cad64498d95ca74e81a9f02804a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653837"
---
# <a name="getparentalcountry-method"></a><span data-ttu-id="4dc52-103">Método GetParentalCountry</span><span class="sxs-lookup"><span data-stu-id="4dc52-103">GetParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="4dc52-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4dc52-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4dc52-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="4dc52-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4dc52-106">El `DVDAdm.GetParentalCountry` método recupera el país o la región parental que se guardó por última vez en el registro.</span><span class="sxs-lookup"><span data-stu-id="4dc52-106">The `DVDAdm.GetParentalCountry` method retrieves the parental country/region that was last saved to the registry.</span></span>

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a><span data-ttu-id="4dc52-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4dc52-107">Return Value</span></span>

<span data-ttu-id="4dc52-108">Devuelve un entero que indica el código de país o región predeterminado almacenado en el registro.</span><span class="sxs-lookup"><span data-stu-id="4dc52-108">Returns an Integer indicating the default country/region code stored in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dc52-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4dc52-109">Remarks</span></span>

<span data-ttu-id="4dc52-110">El país o región parental que este método recupera no es necesariamente el mismo país o región almacenado actualmente en el objeto MSWebDVD.</span><span class="sxs-lookup"><span data-stu-id="4dc52-110">The parental country/region this method retrieves is not necessarily the same country/region currently stored in the MSWebDVD object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dc52-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4dc52-111">Requirements</span></span>



| <span data-ttu-id="4dc52-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dc52-112">Requirement</span></span> | <span data-ttu-id="4dc52-113">Value</span><span class="sxs-lookup"><span data-stu-id="4dc52-113">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4dc52-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4dc52-114">Header</span></span><br/> | <dl> <span data-ttu-id="4dc52-115"><dt>Segmento. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dc52-115"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dc52-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="4dc52-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dc52-117">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="4dc52-117">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




