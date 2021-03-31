---
description: La instalación de las clases de servicio, el registro de las instancias de servicio y las operaciones básicas de consulta se asignan de manera bastante directa desde la API al SPI.
ms.assetid: 2ae937f6-e0a6-4a02-9838-0a42575bae66
title: Asignación de resolución de nombres entre las funciones de API y SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a031ea8af72bb2733fc647c817a850ab7f311b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907944"
---
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a><span data-ttu-id="0e77e-103">Asignación de resolución de nombres entre las funciones de API y SPI</span><span class="sxs-lookup"><span data-stu-id="0e77e-103">Name Resolution Mapping Between API and SPI Functions</span></span>

<span data-ttu-id="0e77e-104">La instalación de las clases de servicio, el registro de las instancias de servicio y las operaciones básicas de consulta se asignan de manera bastante directa desde la API al SPI.</span><span class="sxs-lookup"><span data-stu-id="0e77e-104">The installation of service classes, registration of service instances and basic query operations all map fairly directly from the API to the SPI.</span></span> <span data-ttu-id="0e77e-105">La función [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) no tiene una función correspondiente en el SPI, ya que esta función se implementa en Ws2 \_32.dll realizando una llamada a [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).</span><span class="sxs-lookup"><span data-stu-id="0e77e-105">The [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) function does not have a corresponding function in the SPI, as this function is implemented in Ws2\_32.dll by making a call to [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).</span></span>

<span data-ttu-id="0e77e-106">Las funciones auxiliares [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) y [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) se asignan a las funciones correspondientes de la API de transporte, ya que solo un proveedor de transporte sabrá necesariamente cómo realizar la traducción en una estructura [**sockaddr**](sockaddr-2.md) .</span><span class="sxs-lookup"><span data-stu-id="0e77e-106">The helper functions [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) and [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) are mapped to the corresponding functions in the transport API, as only a transport provider will necessarily know how to perform the translation on a [**sockaddr**](sockaddr-2.md) structure.</span></span>

 

 



