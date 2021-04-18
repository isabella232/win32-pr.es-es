---
title: Detección de dispositivos y servicios Bluetooth
description: Para facilitar la detección de dispositivos y servicios Bluetooth, Windows asigna el protocolo de detección de servicios Bluetooth (SDP) a las interfaces del espacio de nombres de Windows Sockets.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, tareas, detectar dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46f2582ceca35668e717c09524e855e585fff0f
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2020
ms.locfileid: "105656313"
---
# <a name="discovering-bluetooth-devices-and-services"></a><span data-ttu-id="34820-104">Detección de dispositivos y servicios Bluetooth</span><span class="sxs-lookup"><span data-stu-id="34820-104">Discovering Bluetooth Devices and Services</span></span>

<span data-ttu-id="34820-105">Para facilitar la detección de dispositivos y servicios Bluetooth, Windows asigna el protocolo de detección de servicios Bluetooth (SDP) a las interfaces del espacio de nombres de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="34820-105">To facilitate the discovery of Bluetooth devices and services, Windows maps the Bluetooth Service Discovery Protocol (SDP) onto the Windows Sockets namespace interfaces.</span></span> <span data-ttu-id="34820-106">Las funciones principales que se usan para esta asignación son las funciones [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)y [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) .</span><span class="sxs-lookup"><span data-stu-id="34820-106">The primary functions used for this mapping are the [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), and [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) functions.</span></span> <span data-ttu-id="34820-107">La estructura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) también se utiliza junto con estas funciones.</span><span class="sxs-lookup"><span data-stu-id="34820-107">The [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure is also used in conjunction with these functions.</span></span>

<span data-ttu-id="34820-108">Dado que determinados conceptos y parámetros del SDP de Bluetooth no se asignan necesariamente directamente a la estructura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) , se debe prestar atención a cómo se crean y se usan sus miembros.</span><span class="sxs-lookup"><span data-stu-id="34820-108">Because certain concepts and parameters from the Bluetooth SDP do not necessarily map directly into the [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure, attention must be paid to how its members are created and used.</span></span> <span data-ttu-id="34820-109">Para muchas operaciones de Bluetooth complejas, como la creación de registros SDP, se usa el miembro **lpBlob** de **WSAQUERYSET** .</span><span class="sxs-lookup"><span data-stu-id="34820-109">For many complex Bluetooth operations, such as the creation of SDP records, the **lpBlob** member of the **WSAQUERYSET** is used.</span></span> <span data-ttu-id="34820-110">Cuando es necesaria una consideración especial, se describe específicamente, como en páginas de referencia como [**Bluetooth y WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), entre otros.</span><span class="sxs-lookup"><span data-stu-id="34820-110">When such special consideration is necessary, it is specifically described, such as in reference pages like [**Bluetooth and WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), and others.</span></span>

<span data-ttu-id="34820-111">Es importante comprender que el registro de SDP es independiente del control de socket.</span><span class="sxs-lookup"><span data-stu-id="34820-111">It is important to understand that SDP registration is separate from socket control.</span></span> <span data-ttu-id="34820-112">Cuando una aplicación de servidor está preparada para aceptar la conexión de cliente, debe llamar a la función [**WSASetService**](bluetooth-and-wsasetservice.md) para registrar un registro SDP de Bluetooth que se corresponda con ese servicio.</span><span class="sxs-lookup"><span data-stu-id="34820-112">When a server application is prepared to accept client connection, it should call the [**WSASetService**](bluetooth-and-wsasetservice.md) function to register a Bluetooth SDP record that corresponds to that service.</span></span> <span data-ttu-id="34820-113">La aplicación Bluetooth debe volver a llamar a la función **WSASetService** antes de cerrar, para anular el registro del registro SDP de Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="34820-113">That Bluetooth application must call the **WSASetService** function again before closing, to deregister the Bluetooth SDP record.</span></span>

<span data-ttu-id="34820-114">Al usar las funciones de asignación descritas en esta página, \_ se asigna el espacio de nombres NS BTH.</span><span class="sxs-lookup"><span data-stu-id="34820-114">When using the mapping functions described on this page, the NS\_BTH namespace is assigned.</span></span>

<span data-ttu-id="34820-115">Para obtener más información acerca de la detección de dispositivos y servicios, consulte las siguientes páginas de referencia:</span><span class="sxs-lookup"><span data-stu-id="34820-115">For further information about discovering devices and services, consult the following reference pages:</span></span>

-   [<span data-ttu-id="34820-116">**Bluetooth y WSASetService**</span><span class="sxs-lookup"><span data-stu-id="34820-116">**Bluetooth and WSASetService**</span></span>](bluetooth-and-wsasetservice.md)
-   [<span data-ttu-id="34820-117">**Bluetooth y WSALookupServiceBegin para la consulta de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="34820-117">**Bluetooth and WSALookupServiceBegin for Device Inquiry**</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [<span data-ttu-id="34820-118">**Bluetooth y WSALookupServiceBegin para la detección de servicios**</span><span class="sxs-lookup"><span data-stu-id="34820-118">**Bluetooth and WSALookupServiceBegin for Service Discovery**</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [<span data-ttu-id="34820-119">**Bluetooth y WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="34820-119">**Bluetooth and WSALookupServiceNext**</span></span>](bluetooth-and-wsalookupservicenext.md)
-   [<span data-ttu-id="34820-120">**Bluetooth y WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="34820-120">**Bluetooth and WSALookupServiceEnd**</span></span>](bluetooth-and-wsalookupserviceend.md)
-   [<span data-ttu-id="34820-121">**Bluetooth y BLOB**</span><span class="sxs-lookup"><span data-stu-id="34820-121">**Bluetooth and BLOB**</span></span>](bluetooth-and-blob.md)
-   [<span data-ttu-id="34820-122">**Bluetooth y WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="34820-122">**Bluetooth and WSAQUERYSET**</span></span>](bluetooth-and-wsaqueryset-for-set-service.md)

<span data-ttu-id="34820-123">También puede descargar el [ejemplo de conexión Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) para obtener un ejemplo completo.</span><span class="sxs-lookup"><span data-stu-id="34820-123">You can also download the [Bluetooth connection sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) for a complete example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34820-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="34820-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34820-125">Programación de Bluetooth con Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="34820-125">Bluetooth Programming with Windows Sockets</span></span>](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[<span data-ttu-id="34820-126">Ejemplo de conexión Bluetooth</span><span class="sxs-lookup"><span data-stu-id="34820-126">Bluetooth connection sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 




