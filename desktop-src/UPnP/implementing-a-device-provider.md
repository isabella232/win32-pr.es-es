---
title: Implementación de un proveedor de dispositivos
description: Para implementar un proveedor de dispositivos, cree un objeto que exponga la interfaz IUPnPDeviceProvider.
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8cd2bea433b884bf6ddf3828fb148c726cd867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487026"
---
# <a name="implementing-a-device-provider"></a><span data-ttu-id="09ec5-103">Implementación de un proveedor de dispositivos</span><span class="sxs-lookup"><span data-stu-id="09ec5-103">Implementing a Device Provider</span></span>

<span data-ttu-id="09ec5-104">Para implementar un proveedor de dispositivos, cree un objeto que exponga la interfaz [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) .</span><span class="sxs-lookup"><span data-stu-id="09ec5-104">To implement a device provider, create an object that exposes the [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) interface.</span></span> <span data-ttu-id="09ec5-105">Este objeto se debe registrar con el host del dispositivo mediante el método [**IUPnPRegistrar:: RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) .</span><span class="sxs-lookup"><span data-stu-id="09ec5-105">This object must be registered with the device host using the [**IUPnPRegistrar::RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) method.</span></span> <span data-ttu-id="09ec5-106">Este método toma los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="09ec5-106">This method takes the following parameters:</span></span>

-   <span data-ttu-id="09ec5-107">Nombre del proveedor, que debe ser único en el equipo.</span><span class="sxs-lookup"><span data-stu-id="09ec5-107">The name of the provider, which must be unique on the computer.</span></span>
-   <span data-ttu-id="09ec5-108">Identificador de programa (ProgID) de la clase que implementa el proveedor de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="09ec5-108">The ProgID of the class that implements the device provider.</span></span>
-   <span data-ttu-id="09ec5-109">Una cadena de inicialización que se pasa al proveedor de dispositivos cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="09ec5-109">An initialization string that is passed to the device provider when it is started.</span></span>
-   <span data-ttu-id="09ec5-110">IDENTIFICADOR del contenedor.</span><span class="sxs-lookup"><span data-stu-id="09ec5-110">A container ID.</span></span> <span data-ttu-id="09ec5-111">Un identificador de contenedor es una cadena que identifica el grupo al que pertenece el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09ec5-111">A container ID is a string that identifies the group to which the device belongs.</span></span> <span data-ttu-id="09ec5-112">Todos los dispositivos con el mismo identificador de contenedor se hospedan en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="09ec5-112">All devices with the same container identifier are hosted in the same process.</span></span>

 

 




