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
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a>Asignación de resolución de nombres entre las funciones de API y SPI

La instalación de las clases de servicio, el registro de las instancias de servicio y las operaciones básicas de consulta se asignan de manera bastante directa desde la API al SPI. La función [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) no tiene una función correspondiente en el SPI, ya que esta función se implementa en Ws2 \_32.dll realizando una llamada a [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).

Las funciones auxiliares [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) y [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) se asignan a las funciones correspondientes de la API de transporte, ya que solo un proveedor de transporte sabrá necesariamente cómo realizar la traducción en una estructura [**sockaddr**](sockaddr-2.md) .

 

 



