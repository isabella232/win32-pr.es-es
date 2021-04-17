---
description: La propiedad WindowlessActivation inicializa el objeto MSWebDVD en tiempo de diseño para el modo en ventanas o sin ventanas.
ms.assetid: 290a9459-154a-4ec7-a013-d696e6b27341
title: Propiedad WindowlessActivation
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427fdcb265d60200bfe8716cd1ece384861fbdf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688485"
---
# <a name="windowlessactivation-property"></a><span data-ttu-id="0eda8-103">Propiedad WindowlessActivation</span><span class="sxs-lookup"><span data-stu-id="0eda8-103">WindowlessActivation Property</span></span>

> [!Note]  
> <span data-ttu-id="0eda8-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0eda8-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0eda8-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="0eda8-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0eda8-106">La `WindowlessActivation` propiedad inicializa el objeto **MSWebDVD** en tiempo de diseño para el modo en ventanas o sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="0eda8-106">The `WindowlessActivation` property initializes the **MSWebDVD** object at design time for either windowed or windowless mode.</span></span>

``` syntax
[ bWindowless = ] MSWebDVD.WindowlessActivation
```

## <a name="return-value"></a><span data-ttu-id="0eda8-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0eda8-107">Return Value</span></span>

<span data-ttu-id="0eda8-108">Devuelve un valor que indica si el objeto está en modo de ventana como booleano.</span><span class="sxs-lookup"><span data-stu-id="0eda8-108">Returns whether the object is in windowed mode as a Boolean.</span></span>

## <a name="remarks"></a><span data-ttu-id="0eda8-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0eda8-109">Remarks</span></span>

<span data-ttu-id="0eda8-110">Esta propiedad es de lectura/escritura y su valor predeterminado es true.</span><span class="sxs-lookup"><span data-stu-id="0eda8-110">This property is read/write with a default value of true.</span></span> <span data-ttu-id="0eda8-111">Por lo tanto, solo tiene que establecer esta propiedad si está ejecutando el objeto **MSWebDVD** en un contenedor en ventana.</span><span class="sxs-lookup"><span data-stu-id="0eda8-111">Therefore, you only need to set this property if you are running the **MSWebDVD** object in a windowed container.</span></span> <span data-ttu-id="0eda8-112">Cuando se encuentra en una página web de Microsoft® Internet Explorer, **MSWebDVD** siempre está en modo sin ventanas y no es necesario establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0eda8-112">When contained in a Web page in Microsoft® Internet Explorer, **MSWebDVD** is always in windowless mode, and you don't need to set this property.</span></span>

 

 



