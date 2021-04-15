---
description: El método SelectParentalCountry establece el país o la región infantil especificados para la posterior reproducción.
ms.assetid: 70368351-c7b9-4640-a4f7-7d972b8e4628
title: Método SelectParentalCountry
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2216d2b2ed72436aca003b42cbf811c8a01bd8fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537786"
---
# <a name="selectparentalcountry-method"></a><span data-ttu-id="2c10f-103">Método SelectParentalCountry</span><span class="sxs-lookup"><span data-stu-id="2c10f-103">SelectParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="2c10f-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2c10f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2c10f-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="2c10f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2c10f-106">El `SelectParentalCountry` método establece el país o la región infantil especificados para la posterior reproducción.</span><span class="sxs-lookup"><span data-stu-id="2c10f-106">The `SelectParentalCountry` method sets the specified parental country/region for subsequent playback.</span></span>

``` syntax
MSWebDVD.SelectParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="2c10f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c10f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c10f-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span><span class="sxs-lookup"><span data-stu-id="2c10f-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span></span>
</dt> <dd>

<span data-ttu-id="2c10f-109">Especifica el país o región como un entero.</span><span class="sxs-lookup"><span data-stu-id="2c10f-109">Specifies the country/region as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="2c10f-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="2c10f-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="2c10f-111">Especifica el usuario que ha iniciado sesión como una cadena.</span><span class="sxs-lookup"><span data-stu-id="2c10f-111">Specifies the current logged-on user as a String.</span></span> <span data-ttu-id="2c10f-112">(Actualmente omitido).</span><span class="sxs-lookup"><span data-stu-id="2c10f-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="2c10f-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="2c10f-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="2c10f-114">Especifica la cadena de contraseña de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2c10f-114">Specifies the application password String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c10f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c10f-115">Return Value</span></span>

<span data-ttu-id="2c10f-116">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2c10f-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c10f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c10f-117">Remarks</span></span>

<span data-ttu-id="2c10f-118">El país o la región parental determina cómo se interpretan los niveles parentales.</span><span class="sxs-lookup"><span data-stu-id="2c10f-118">The parental country/region determines how the parental levels are interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c10f-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c10f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c10f-120">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="2c10f-120">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="2c10f-121">**NotifyParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="2c10f-121">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="2c10f-122">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="2c10f-122">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="2c10f-123">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="2c10f-123">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="2c10f-124">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="2c10f-124">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="2c10f-125">**AcceptParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="2c10f-125">**AcceptParentalLevelChange**</span></span>](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



