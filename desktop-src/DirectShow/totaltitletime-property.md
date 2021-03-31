---
description: La propiedad TotalTitleTime recupera el tiempo total de reproducción del título actual.
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: Propiedad TotalTitleTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a300a2da8de2698a74e0d72362818bd8a2a5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910406"
---
# <a name="totaltitletime-property"></a><span data-ttu-id="81b46-103">Propiedad TotalTitleTime</span><span class="sxs-lookup"><span data-stu-id="81b46-103">TotalTitleTime Property</span></span>

> [!Note]  
> <span data-ttu-id="81b46-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="81b46-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="81b46-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="81b46-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="81b46-106">La `TotalTitleTime` propiedad recupera el tiempo total de reproducción del título actual.</span><span class="sxs-lookup"><span data-stu-id="81b46-106">The `TotalTitleTime` property retrieves the total playback time for the current title.</span></span>

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a><span data-ttu-id="81b46-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81b46-107">Return Value</span></span>

<span data-ttu-id="81b46-108">Devuelve el tiempo total de reproducción del título actual como una cadena con el formato "HH: mm: SS: FF".</span><span class="sxs-lookup"><span data-stu-id="81b46-108">Returns the total playing time of the current title as a String in the format "hh:mm:ss:ff".</span></span>

## <a name="remarks"></a><span data-ttu-id="81b46-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81b46-109">Remarks</span></span>

<span data-ttu-id="81b46-110">Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="81b46-110">This property is read-only with no default value.</span></span> <span data-ttu-id="81b46-111">La cadena devuelta tendrá 11 caracteres de longitud en el formato "HH: mm: SS: FF" (horas, minutos, segundos, fotogramas).</span><span class="sxs-lookup"><span data-stu-id="81b46-111">The returned string will be 11 characters long in the format "hh:mm:ss:ff" (hours, minutes, seconds, frames).</span></span>

## <a name="see-also"></a><span data-ttu-id="81b46-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="81b46-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81b46-113">**PlayAtTime**</span><span class="sxs-lookup"><span data-stu-id="81b46-113">**PlayAtTime**</span></span>](playattime-method.md)
</dt> <dt>

[<span data-ttu-id="81b46-114">**PlayAtTimeInTitle**</span><span class="sxs-lookup"><span data-stu-id="81b46-114">**PlayAtTimeInTitle**</span></span>](playattimeintitle-method.md)
</dt> </dl>

 

 



