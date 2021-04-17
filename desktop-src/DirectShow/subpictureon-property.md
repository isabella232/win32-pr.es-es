---
description: La propiedad subpictureon establece o recupera el estado actual de la subimagen (activada o desactivada).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: Subimagenon (propiedad)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83376793f20468bda88edd8897e8c956094c1a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688489"
---
# <a name="subpictureon-property"></a><span data-ttu-id="61168-103">Subimagenon (propiedad)</span><span class="sxs-lookup"><span data-stu-id="61168-103">SubpictureOn Property</span></span>

> [!Note]  
> <span data-ttu-id="61168-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="61168-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="61168-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="61168-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="61168-106">La `SubpictureOn` propiedad establece o recupera el estado actual de la subimagen (activada o desactivada).</span><span class="sxs-lookup"><span data-stu-id="61168-106">The `SubpictureOn` property sets or retrieves the current subpicture state (on or off).</span></span>

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a><span data-ttu-id="61168-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61168-107">Return Value</span></span>

<span data-ttu-id="61168-108">Devuelve un valor booleano que indica si se muestra la subimagen.</span><span class="sxs-lookup"><span data-stu-id="61168-108">Returns a Boolean value indicating whether the subpicture is displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="61168-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61168-109">Remarks</span></span>

<span data-ttu-id="61168-110">Esta propiedad no afecta a la presentación de subtítulos cerrados.</span><span class="sxs-lookup"><span data-stu-id="61168-110">This property does not affect display of Closed Captions.</span></span> <span data-ttu-id="61168-111">Los subtítulos están insertados en el flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="61168-111">Closed Captions are embedded within the video stream.</span></span> <span data-ttu-id="61168-112">Las subimágenes de DVD se transportan en una secuencia independiente.</span><span class="sxs-lookup"><span data-stu-id="61168-112">DVD subpictures are transported on a separate stream.</span></span>

<span data-ttu-id="61168-113">Cuando se cambia la secuencia de subimagen mediante [**CurrentSubpictureStream**](currentsubpicturestream-property.md), la `SubpictureOn` propiedad cambia a **true**.</span><span class="sxs-lookup"><span data-stu-id="61168-113">When the subpicture stream is changed using [**CurrentSubpictureStream**](currentsubpicturestream-property.md), the `SubpictureOn` property toggles to **True**.</span></span>

<span data-ttu-id="61168-114">Esta propiedad es de lectura/escritura y su valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="61168-114">This property is read/write with a default value of false.</span></span>

 

 



