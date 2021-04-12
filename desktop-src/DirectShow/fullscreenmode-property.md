---
description: La propiedad FullScreenMode establece o recupera un valor que indica si la presentación está en modo de pantalla completa.
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: Propiedad FullScreenMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96b3c0ca8261eb934e95eb7235b51e76e8c7579
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152014"
---
# <a name="fullscreenmode-property"></a><span data-ttu-id="66cdb-103">Propiedad FullScreenMode</span><span class="sxs-lookup"><span data-stu-id="66cdb-103">FullScreenMode Property</span></span>

> [!Note]  
> <span data-ttu-id="66cdb-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="66cdb-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="66cdb-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="66cdb-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="66cdb-106">La `FullScreenMode` propiedad establece o recupera un valor que indica si la presentación está en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="66cdb-106">The `FullScreenMode` property sets or retrieves a value indicating whether the display is in full-screen mode.</span></span>

``` syntax
[ bFullScreen = ] MSWebDVD.FullScreenMode
```

## <a name="return-value"></a><span data-ttu-id="66cdb-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66cdb-107">Return Value</span></span>

<span data-ttu-id="66cdb-108">Devuelve un valor booleano que indica si se va a habilitar o deshabilitar la reproducción de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="66cdb-108">Returns a Boolean value indicating whether to enable or disable full-screen playback.</span></span>

## <a name="remarks"></a><span data-ttu-id="66cdb-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66cdb-109">Remarks</span></span>

<span data-ttu-id="66cdb-110">Esta propiedad es de lectura/escritura y su valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="66cdb-110">This property is read/write with a default value of false.</span></span>



| <span data-ttu-id="66cdb-111">Value</span><span class="sxs-lookup"><span data-stu-id="66cdb-111">Value</span></span> | <span data-ttu-id="66cdb-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="66cdb-112">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="66cdb-113">true</span><span class="sxs-lookup"><span data-stu-id="66cdb-113">true</span></span>  | <span data-ttu-id="66cdb-114">Habilitar la reproducción a pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="66cdb-114">Enable full-screen playback.</span></span> <span data-ttu-id="66cdb-115">Este es el valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="66cdb-115">This is the default value</span></span> |
| <span data-ttu-id="66cdb-116">false</span><span class="sxs-lookup"><span data-stu-id="66cdb-116">false</span></span> | <span data-ttu-id="66cdb-117">Deshabilite la reproducción de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="66cdb-117">Disable full-screen playback.</span></span>                          |



 

<span data-ttu-id="66cdb-118">El modo de pantalla completa solo está disponible cuando el control MSWebDVD se está ejecutando en modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="66cdb-118">Full screen mode is only available when the MSWebDVD control is running in windowed mode.</span></span>

 

 



