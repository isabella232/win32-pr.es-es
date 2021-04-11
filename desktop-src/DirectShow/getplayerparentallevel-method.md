---
description: GetPlayerParentalLevel recupera el nivel de administración parental establecido en el objeto MSWebDVD.
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: Método GetPlayerParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bac51e776a45e0d1fa748fc995240292474e902
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151995"
---
# <a name="getplayerparentallevel-method"></a><span data-ttu-id="a0062-103">Método GetPlayerParentalLevel</span><span class="sxs-lookup"><span data-stu-id="a0062-103">GetPlayerParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="a0062-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a0062-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a0062-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="a0062-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a0062-106">`GetPlayerParentalLevel`Recupera el nivel de administración parental establecido en el objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="a0062-106">The `GetPlayerParentalLevel` retrieves the parental management level set in the **MSWebDVD** object.</span></span>

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a><span data-ttu-id="a0062-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0062-107">Return Value</span></span>

<span data-ttu-id="a0062-108">Devuelve un valor entero que especifica el nivel parental actual en el navegador de DVD o-1 si la administración parental está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="a0062-108">Returns an integer value specifying the current parental level in the DVD Navigator, or -1 if parental management is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0062-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0062-109">Remarks</span></span>

<span data-ttu-id="a0062-110">Una aplicación de reproducción es responsable de aplicar controles parentales.</span><span class="sxs-lookup"><span data-stu-id="a0062-110">A player application is responsible for enforcing parental controls.</span></span> <span data-ttu-id="a0062-111">El nivel parental del reproductor es un valor establecido por una aplicación que se puede usar para indicar el nivel parental más alto que puede ver el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="a0062-111">The player parental level is a value set by an application than can be used to indicate the highest parental level the current user can view.</span></span> <span data-ttu-id="a0062-112">Cuando el navegador de DVD encuentra un nuevo nivel parental, use este método para determinar si el nuevo nivel es mayor que el nivel establecido por la aplicación a través de [**SelectParentalLevel**](selectparentallevel-method.md).</span><span class="sxs-lookup"><span data-stu-id="a0062-112">When the DVD Navigator encounters a new parental level, use this method to determine whether the new level is greater than the level that was set by the application through [**SelectParentalLevel**](selectparentallevel-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a0062-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0062-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0062-114">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="a0062-114">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="a0062-115">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="a0062-115">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="a0062-116">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="a0062-116">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="a0062-117">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="a0062-117">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> </dl>

 

 



