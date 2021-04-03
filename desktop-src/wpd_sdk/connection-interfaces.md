---
description: Interfaces de conexión de MTP/Bluetooth
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: Interfaces de conexión de MTP/Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e5194b8a6ababc05c36590ef30ae19ab185efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083305"
---
# <a name="mtpbluetooth-connection-interfaces"></a><span data-ttu-id="89643-103">Interfaces de conexión de MTP/Bluetooth</span><span class="sxs-lookup"><span data-stu-id="89643-103">MTP/Bluetooth Connection Interfaces</span></span>

<span data-ttu-id="89643-104">Las siguientes interfaces permiten a las aplicaciones enumerar y conectarse solo a los dispositivos que admiten el protocolo de transferencia multimedia (MTP) a través de Bluetooth (MTP/Bluetooth).</span><span class="sxs-lookup"><span data-stu-id="89643-104">The following interfaces allow applications to enumerate and connect only to devices that support the Media Transfer Protocol (MTP) over Bluetooth (MTP/Bluetooth).</span></span> <span data-ttu-id="89643-105">El controlador de WPD, la colección y las interfaces de cliente no están restringidos al protocolo MTP/Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="89643-105">The WPD driver-, collection-, and client-interfaces are not restricted to the MTP/ Bluetooth protocol.</span></span>



| <span data-ttu-id="89643-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="89643-106">Interface</span></span>                                                              | <span data-ttu-id="89643-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="89643-107">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89643-108">**IConnectionRequestCallback**</span><span class="sxs-lookup"><span data-stu-id="89643-108">**IConnectionRequestCallback**</span></span>](iconnectionrequestcallback.md)       | <span data-ttu-id="89643-109">Define un método de devolución de llamada único que las aplicaciones usan para recibir la notificación de las solicitudes completadas y canceladas.</span><span class="sxs-lookup"><span data-stu-id="89643-109">Defines a single callback method that applications use to receive notification of completed and cancelled requests.</span></span> |
| [<span data-ttu-id="89643-110">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="89643-110">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md) | <span data-ttu-id="89643-111">Enumera las interfaces de **IPortableDeviceConnector** .</span><span class="sxs-lookup"><span data-stu-id="89643-111">Enumerates **IPortableDeviceConnector** interfaces.</span></span>                                                                 |
| [<span data-ttu-id="89643-112">**IPortableDeviceConnector**</span><span class="sxs-lookup"><span data-stu-id="89643-112">**IPortableDeviceConnector**</span></span>](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | <span data-ttu-id="89643-113">Admite métodos que las aplicaciones llaman para establecer conexiones con dispositivos Bluetooth MTP.</span><span class="sxs-lookup"><span data-stu-id="89643-113">Supports methods that applications call to establish connections to MTP Bluetooth devices.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="89643-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89643-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89643-115">**Referencia de programación**</span><span class="sxs-lookup"><span data-stu-id="89643-115">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



