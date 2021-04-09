---
description: Una ruta de acceso del objeto de espacio de nombres describe la ubicación de un espacio de nombres determinado en un servidor. Una ruta de acceso de objeto de espacio de nombres contiene elementos de servidor y de espacio de nombres y se le da formato mediante barras diagonales o hacia atrás.
ms.assetid: 6d8da19e-0914-4267-870e-c203176b895e
ms.tgt_platform: multiple
title: Describir una ruta de acceso de objeto de espacio de nombres WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586104a1c193f1c229b0fbb27437d22e3686585b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082448"
---
# <a name="describing-a-wmi-namespace-object-path"></a><span data-ttu-id="be2d3-104">Describir una ruta de acceso de objeto de espacio de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="be2d3-104">Describing a WMI Namespace Object Path</span></span>

<span data-ttu-id="be2d3-105">Una ruta de acceso del objeto de espacio de nombres describe la ubicación de un espacio de nombres determinado en un servidor.</span><span class="sxs-lookup"><span data-stu-id="be2d3-105">A namespace object path describes the location of a particular namespace on a server.</span></span> <span data-ttu-id="be2d3-106">Una ruta de acceso de objeto de espacio de nombres contiene elementos de servidor y de espacio de nombres y se le da formato mediante barras diagonales o hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="be2d3-106">A namespace object path contains server and namespace elements, and is formatted using either forward or backward slashes.</span></span>

<span data-ttu-id="be2d3-107">El elemento Server especifica el nombre de red del equipo que hospeda el espacio de nombres, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="be2d3-107">The server element specifies the network name of the computer that is hosting the namespace, as shown in the following example.</span></span>

``` syntax
\\Server\Namespace
```

<span data-ttu-id="be2d3-108">\- o -</span><span class="sxs-lookup"><span data-stu-id="be2d3-108">\- or -</span></span>

``` syntax
//Server/Namespace
```

<span data-ttu-id="be2d3-109">Si el servidor es el equipo local, use un solo punto en lugar del nombre del servidor, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="be2d3-109">If the server is the local computer, use a single dot instead of the server name, as shown in the following example.</span></span>

``` syntax
\\.\Namespace
```

<span data-ttu-id="be2d3-110">El elemento namespace especifica cualquier espacio de nombres válido.</span><span class="sxs-lookup"><span data-stu-id="be2d3-110">The namespace element specifies any valid namespace.</span></span> <span data-ttu-id="be2d3-111">Un espacio de nombres se representa con una cadena jerárquica que contiene elementos delimitados por barras diagonales inversas, como la raíz \\ cimv2.</span><span class="sxs-lookup"><span data-stu-id="be2d3-111">A namespace is represented with a hierarchical string containing elements delimited by single backslashes, such as root\\cimv2.</span></span> <span data-ttu-id="be2d3-112">No se pueden usar barras diagonales en los nombres de los espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="be2d3-112">You cannot use forward slashes within namespace names.</span></span>

 

 



