---
description: El método SelectParentalLevel establece el nivel parental especificado para su posterior reproducción.
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: Método SelectParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb00172b8e61f353c45981af628eb396bca7a7df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537107"
---
# <a name="selectparentallevel-method"></a><span data-ttu-id="ce143-103">Método SelectParentalLevel</span><span class="sxs-lookup"><span data-stu-id="ce143-103">SelectParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="ce143-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ce143-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ce143-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="ce143-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ce143-106">El `SelectParentalLevel` método establece el nivel parental especificado para su posterior reproducción.</span><span class="sxs-lookup"><span data-stu-id="ce143-106">The `SelectParentalLevel` method sets the specified parental level for subsequent playback.</span></span>

``` syntax
MSWebDVD.SelectParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="ce143-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce143-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce143-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span><span class="sxs-lookup"><span data-stu-id="ce143-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span></span>
</dt> <dd>

<span data-ttu-id="ce143-109">Especifica el nivel de administración parental como un entero.</span><span class="sxs-lookup"><span data-stu-id="ce143-109">Specifies the parental management level as an Integer.</span></span> <span data-ttu-id="ce143-110">Para habilitar la administración parental, el parámetro *iLevel* debe oscilar entre 1 y 8.</span><span class="sxs-lookup"><span data-stu-id="ce143-110">To enable the parental management, the *iLevel* parameter must range from 1 through 8.</span></span> <span data-ttu-id="ce143-111">Para deshabilitar la administración parental, establezca *iLevel* en-1.</span><span class="sxs-lookup"><span data-stu-id="ce143-111">To disable the parental management, set *iLevel* to -1.</span></span>

</dd> <dt>

<span data-ttu-id="ce143-112"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="ce143-112"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="ce143-113">Especifica el usuario actual como una cadena.</span><span class="sxs-lookup"><span data-stu-id="ce143-113">Specifies the current user as a String.</span></span> <span data-ttu-id="ce143-114">(Actualmente omitido).</span><span class="sxs-lookup"><span data-stu-id="ce143-114">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="ce143-115"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="ce143-115"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="ce143-116">Especifica la contraseña almacenada actualmente en el registro como una cadena.</span><span class="sxs-lookup"><span data-stu-id="ce143-116">Specifies the password currently stored in the registry as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce143-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce143-117">Return Value</span></span>

<span data-ttu-id="ce143-118">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ce143-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce143-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce143-119">Remarks</span></span>

<span data-ttu-id="ce143-120">Este método establece el nivel de acceso en el objeto MSWebDVD, que determina el contenido que el usuario puede reproducir.</span><span class="sxs-lookup"><span data-stu-id="ce143-120">This method sets the access level in the MSWebDVD object, which determines what content the user can play back.</span></span> <span data-ttu-id="ce143-121">Los niveles superiores pueden reproducir contenido de nivel inferior, pero los niveles inferiores no pueden reproducir contenido de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="ce143-121">Higher levels can play lower-level content but lower levels can't play higher-level content.</span></span> <span data-ttu-id="ce143-122">El significado exacto de los ocho niveles de administración parental varía en función del país o la región.</span><span class="sxs-lookup"><span data-stu-id="ce143-122">The exact meaning of the eight DVD parental management levels varies depending on the country/region.</span></span> <span data-ttu-id="ce143-123">En el Estados Unidos y Canadá, los niveles se asignan a las categorías de clasificación de la Asociación de imágenes de movimiento (MPAA).</span><span class="sxs-lookup"><span data-stu-id="ce143-123">In the United States and Canada, the levels are mapped to the Motion Picture Association of America (MPAA) rating categories.</span></span> <span data-ttu-id="ce143-124">La administración parental en el navegador de DVD está deshabilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ce143-124">Parental management in the DVD Navigator is disabled by default.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce143-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce143-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce143-126">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="ce143-126">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="ce143-127">**NotifyParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="ce143-127">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="ce143-128">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="ce143-128">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="ce143-129">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="ce143-129">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="ce143-130">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="ce143-130">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="ce143-131">**AcceptParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="ce143-131">**AcceptParentalLevelChange**</span></span>](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



