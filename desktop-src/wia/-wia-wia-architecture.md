---
description: WIA se implementa como un servidor fuera de proceso del modelo de objetos componentes (COM) para garantizar el funcionamiento eficaz de las aplicaciones cliente.
ms.assetid: 9f3d1848-36ab-4e0f-a7f4-312bc85ecc00
title: Arquitectura WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09652258ee249fb3c68e65472e863ccd35154ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563960"
---
# <a name="wia-architecture"></a><span data-ttu-id="5caf8-103">Arquitectura WIA</span><span class="sxs-lookup"><span data-stu-id="5caf8-103">WIA Architecture</span></span>

<span data-ttu-id="5caf8-104">WIA se implementa como un servidor fuera de proceso del modelo de objetos componentes (COM) para garantizar el funcionamiento eficaz de las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="5caf8-104">WIA is implemented as a Component Object Model (COM) out-of-process server to ensure the robust operation of client applications.</span></span> <span data-ttu-id="5caf8-105">A diferencia de la mayoría de las aplicaciones de servidor de proceso, la adquisición de imágenes de Windows (WIA) evita penalizaciones de rendimiento durante la transferencia de datos de imagen al proporcionar su propio mecanismo de transferencia de datos, [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span><span class="sxs-lookup"><span data-stu-id="5caf8-105">Unlike most out of process server applications, Windows Image Acquisition (WIA) avoids performance penalties during image data transfer by providing its own data transfer mechanism, [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span> <span data-ttu-id="5caf8-106">Esta interfaz de alto rendimiento utiliza una ventana de memoria compartida para transferir datos al cliente.</span><span class="sxs-lookup"><span data-stu-id="5caf8-106">This high performance interface uses a shared memory window to transfer data to the client.</span></span>

<span data-ttu-id="5caf8-107">WIA tiene tres componentes principales: un Administrador de dispositivos, una biblioteca de servicio de minicontrolador y un minicontrolador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5caf8-107">WIA has three main components: a Device Manager, a Minidriver Service Library, and a Device Minidriver.</span></span>

-   <span data-ttu-id="5caf8-108">En el Administrador de dispositivos se enumeran los dispositivos de creación de imágenes, se recuperan las propiedades del dispositivo, se configuran los eventos de los dispositivos y se crean objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5caf8-108">The Device Manager enumerates imaging devices, retrieves device properties, sets up events for devices, and creates device objects.</span></span>
-   <span data-ttu-id="5caf8-109">La biblioteca de servicio de minicontrolador implementa todos los servicios que son independientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5caf8-109">The Minidriver Service Library implements all services that are device independent.</span></span>
-   <span data-ttu-id="5caf8-110">El minicontrolador de dispositivo asigna propiedades y comandos de WIA al dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="5caf8-110">The Device Minidriver maps WIA properties and commands to the specific device.</span></span>

<span data-ttu-id="5caf8-111">En el diagrama siguiente se ilustra la arquitectura de WIA:</span><span class="sxs-lookup"><span data-stu-id="5caf8-111">The following diagram illustrates the WIA architecture:</span></span>

![arquitectura WIA](images/wiarch.gif)

 

 



