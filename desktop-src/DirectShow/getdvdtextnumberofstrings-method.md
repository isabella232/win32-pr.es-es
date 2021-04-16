---
description: El método GetDVDTextNumberOfStrings recupera el número de cadenas de texto disponibles para el idioma especificado.
ms.assetid: 84d2b5b7-b474-48a4-9058-ea9da8109398
title: Método GetDVDTextNumberOfStrings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c9c4fadfd28d6cddc8b9013a6e426aebe9f816
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677173"
---
# <a name="getdvdtextnumberofstrings-method"></a><span data-ttu-id="181c6-103">Método GetDVDTextNumberOfStrings</span><span class="sxs-lookup"><span data-stu-id="181c6-103">GetDVDTextNumberOfStrings Method</span></span>

> [!Note]  
> <span data-ttu-id="181c6-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="181c6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="181c6-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="181c6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="181c6-106">El `GetDVDTextNumberOfStrings` método recupera el número de cadenas de texto disponibles para el idioma especificado.</span><span class="sxs-lookup"><span data-stu-id="181c6-106">The `GetDVDTextNumberOfStrings` method retrieves the number of text strings available for the specified language.</span></span>

``` syntax
[ iStrings = ] MSWebDVD.GetDVDTextNumberOfStrings(iLangIndex)
```

## <a name="parameters"></a><span data-ttu-id="181c6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="181c6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="181c6-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span><span class="sxs-lookup"><span data-stu-id="181c6-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span></span>
</dt> <dd>

<span data-ttu-id="181c6-109">Especifica el idioma como un entero.</span><span class="sxs-lookup"><span data-stu-id="181c6-109">Specifies the language as an Integer.</span></span> <span data-ttu-id="181c6-110">El valor debe estar comprendido entre cero y uno menos que el valor devuelto por [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span><span class="sxs-lookup"><span data-stu-id="181c6-110">The value must range from zero through one less than the value returned by [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="181c6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="181c6-111">Return Value</span></span>

<span data-ttu-id="181c6-112">Devuelve un valor entero que especifica el número de cadenas que contiene el disco en el idioma especificado.</span><span class="sxs-lookup"><span data-stu-id="181c6-112">Returns an integer value specifying how many strings the disc contains in the specified language.</span></span>

## <a name="see-also"></a><span data-ttu-id="181c6-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="181c6-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="181c6-114">Objeto MSWebDVD</span><span class="sxs-lookup"><span data-stu-id="181c6-114">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> </dl>

 

 



