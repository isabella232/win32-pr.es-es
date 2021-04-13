---
title: Qué es el modelo de objetos de punto de control
description: En la ilustración siguiente se muestra el modelo de objetos de punto de control básico.
ms.assetid: 6c5a32a1-932e-4868-b4c6-8701e90a7c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e491d3ec89b1074fb09a9f7632a886fb67b59863
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357714"
---
# <a name="what-is-the-control-point-object-model"></a><span data-ttu-id="80cf8-103">¿Qué es el modelo de objetos de punto de control?</span><span class="sxs-lookup"><span data-stu-id="80cf8-103">What is the Control Point Object Model?</span></span>

<span data-ttu-id="80cf8-104">En la ilustración siguiente se muestra el modelo de objetos de punto de control básico.</span><span class="sxs-lookup"><span data-stu-id="80cf8-104">The following illustration shows the basic Control Point object model.</span></span>

![modelo de objetos de punto de control](images/upnp-object-model.png)

<span data-ttu-id="80cf8-106">La búsqueda de dispositivos con la interfaz del buscador de dispositivos crea una recopilación de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="80cf8-106">Searching for devices with the Device Finder interface creates a Devices collection.</span></span> <span data-ttu-id="80cf8-107">Una recopilación de dispositivos contiene cero o más objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="80cf8-107">A Devices collection contains zero or more Device objects.</span></span> <span data-ttu-id="80cf8-108">Las aplicaciones pueden usar los distintos métodos de recopilación de dispositivos para tener acceso a objetos de dispositivo individuales.</span><span class="sxs-lookup"><span data-stu-id="80cf8-108">Applications can use the various Devices collection methods to access individual Device objects.</span></span>

<span data-ttu-id="80cf8-109">Los objetos de dispositivo siempre contienen una colección de servicios que contiene uno o más objetos de servicio.</span><span class="sxs-lookup"><span data-stu-id="80cf8-109">Device objects always contain a Services collection that contains one or more Service objects.</span></span> <span data-ttu-id="80cf8-110">Las aplicaciones usan estos objetos de servicio para comunicarse con dispositivos y controlarlos.</span><span class="sxs-lookup"><span data-stu-id="80cf8-110">These service objects are used by applications to communicate with and control devices.</span></span>

 

 




