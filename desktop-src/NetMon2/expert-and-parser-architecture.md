---
description: En la siguiente ilustración se muestra la relación entre las aplicaciones de experto y de analizador y otros componentes de la arquitectura de Monitor de red.
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: Arquitectura de expertos y del analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa8477d97604acfb04686170ca6cb5cff8116a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153868"
---
# <a name="expert-and-parser-architecture"></a><span data-ttu-id="e70c3-103">Arquitectura de expertos y del analizador</span><span class="sxs-lookup"><span data-stu-id="e70c3-103">Expert and Parser Architecture</span></span>

<span data-ttu-id="e70c3-104">En la siguiente ilustración se muestra la relación entre las aplicaciones de [experto](experts.md) y de [analizador](parsers.md) y otros componentes de la arquitectura de monitor de red.</span><span class="sxs-lookup"><span data-stu-id="e70c3-104">The following figure shows the relationship between [expert](experts.md) and [parser](parsers.md) applications and other components of the Network Monitor architecture.</span></span>

![la relación entre las aplicaciones de expertos y de analizador](images/nm-arch1.png)

<span data-ttu-id="e70c3-106">El tráfico de red se recopila como fotogramas individuales del controlador NDIS.</span><span class="sxs-lookup"><span data-stu-id="e70c3-106">The network traffic is collected, as individual frames, from the NDIS driver.</span></span> <span data-ttu-id="e70c3-107">A continuación, el controlador de Monitor de red (Nmnt.sys) enruta los fotogramas a un proveedor de paquetes de red (NPP), que captura los datos y los coloca en uno o varios archivos de captura.</span><span class="sxs-lookup"><span data-stu-id="e70c3-107">The Network Monitor driver (Nmnt.sys) then routes the frames to a network packet provider (NPP), which captures the data and places it in one or more capture files.</span></span> <span data-ttu-id="e70c3-108">NPP es una colección de interfaces COM que se utiliza para capturar datos.</span><span class="sxs-lookup"><span data-stu-id="e70c3-108">The NPP is a collection of COM interfaces used to capture data.</span></span> <span data-ttu-id="e70c3-109">En este caso, la interfaz [**IDelaydC**](idelaydc.md) se utiliza para realizar una captura diferida.</span><span class="sxs-lookup"><span data-stu-id="e70c3-109">In this case, the [**IDelaydC**](idelaydc.md) interface is used to perform a delayed capture.</span></span>

> [!Note]  
> <span data-ttu-id="e70c3-110">El NPP se utiliza para las capturas retrasadas y en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="e70c3-110">The NPP is used for delayed and real-time captures.</span></span> <span data-ttu-id="e70c3-111">En el caso de las capturas en tiempo real, se usa la interfaz [**IRTC**](irtc.md) .</span><span class="sxs-lookup"><span data-stu-id="e70c3-111">For real-time captures, the [**IRTC**](irtc.md) interface is used.</span></span>

 

<span data-ttu-id="e70c3-112">Cuando los fotogramas de red se almacenan en el archivo de captura y se puede tener acceso al archivo, los expertos y analizadores pueden usar la interfaz de usuario de Monitor de red y las funciones de Monitor de red proporcionadas en Nmapi.dll para analizar los datos.</span><span class="sxs-lookup"><span data-stu-id="e70c3-112">When the network frames are stored in the capture file and the file is accessible, experts and parsers can use the Network Monitor UI and the Network Monitor functions provided in Nmapi.dll to analyze the data.</span></span> <span data-ttu-id="e70c3-113">No se puede acceder a los archivos de captura hasta que se complete la captura.</span><span class="sxs-lookup"><span data-stu-id="e70c3-113">Capture files are not accessible until the capture is complete.</span></span>

 

 



