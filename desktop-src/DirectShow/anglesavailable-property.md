---
description: La propiedad AnglesAvailable recupera el número de ángulos disponibles actualmente.
ms.assetid: 1e2635d4-63f1-4c3d-a034-437489289bd7
title: Propiedad AnglesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b9d27806b314d89c68fcc4d1476a9918cd4446
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659281"
---
# <a name="anglesavailable-property"></a><span data-ttu-id="57f13-103">Propiedad AnglesAvailable</span><span class="sxs-lookup"><span data-stu-id="57f13-103">AnglesAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="57f13-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="57f13-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="57f13-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="57f13-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="57f13-106">La `AnglesAvailable` propiedad recupera el número de ángulos disponibles actualmente.</span><span class="sxs-lookup"><span data-stu-id="57f13-106">The `AnglesAvailable` property retrieves the number of angles currently available.</span></span>

``` syntax
[ iAngles = ] MSWebDVD.AnglesAvailable
```

## <a name="return-value"></a><span data-ttu-id="57f13-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57f13-107">Return Value</span></span>

<span data-ttu-id="57f13-108">Devuelve un valor entero comprendido entre 1 y 9 que representa el número de ángulos actualmente disponibles.</span><span class="sxs-lookup"><span data-stu-id="57f13-108">Returns an integer value from 1 through 9 representing the number of angles currently available.</span></span> <span data-ttu-id="57f13-109">Si</span><span class="sxs-lookup"><span data-stu-id="57f13-109">If</span></span>


```
iAngles
```



<span data-ttu-id="57f13-110">= 1, no hay ningún bloque de ángulo en la ubicación actual.</span><span class="sxs-lookup"><span data-stu-id="57f13-110">= 1, there is no angle block at the current location.</span></span>

## <a name="remarks"></a><span data-ttu-id="57f13-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57f13-111">Remarks</span></span>

<span data-ttu-id="57f13-112">Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="57f13-112">This property is read-only with no default value.</span></span> <span data-ttu-id="57f13-113">Un *bloque de ángulo* es un segmento de vídeo que se ha captado desde más de un ángulo de cámara.</span><span class="sxs-lookup"><span data-stu-id="57f13-113">An *angle block* is a video segment that was shot from more than one camera angle.</span></span> <span data-ttu-id="57f13-114">Puede haber hasta nueve ángulos en un bloque de ángulo, numerados del 1 al 9.</span><span class="sxs-lookup"><span data-stu-id="57f13-114">There can be up to nine angles in an angle block, numbered from 1 through 9.</span></span> <span data-ttu-id="57f13-115">Cuando el navegador de DVD entra por primera vez en un bloque de ángulo, envía a la aplicación una \_ \_ notificación de eventos de los ángulos de DVD de EC \_ disponibles con el número de ángulos de *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="57f13-115">When the DVD Navigator first enters an angle block, it sends your application an EC\_DVD\_ANGLES\_AVAILABLE event notification with the number of angles in *lParam1*.</span></span> <span data-ttu-id="57f13-116">Se puede crear un disco para mostrar automáticamente un menú para los ángulos disponibles cuando entra en un bloque de ángulo, pero normalmente una aplicación debe determinar el número de ángulos disponibles y ofrecer al usuario una manera de seleccionar uno.</span><span class="sxs-lookup"><span data-stu-id="57f13-116">A disc can be authored to automatically show a menu for available angles when it enters an angle block, but generally an application must determine the number of angles available and offer the user a way to select one.</span></span>

## <a name="see-also"></a><span data-ttu-id="57f13-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="57f13-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57f13-118">**CurrentAngle**</span><span class="sxs-lookup"><span data-stu-id="57f13-118">**CurrentAngle**</span></span>](currentangle-property.md)
</dt> </dl>

 

 



