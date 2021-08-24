---
description: La instalación de clases de servicio, el registro de instancias de servicio y las operaciones de consulta básicas se asignan de forma bastante directa desde la API al SPI.
ms.assetid: 2ae937f6-e0a6-4a02-9838-0a42575bae66
title: Asignación de resolución de nombres entre las funciones DE API y SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad02896ea15fb1b7c7e2aa2e01d9ec0727492da43d0446819dd1f2e04ad591d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733629"
---
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a>Asignación de resolución de nombres entre las funciones DE API y SPI

La instalación de clases de servicio, el registro de instancias de servicio y las operaciones de consulta básicas se asignan de forma bastante directa desde la API al SPI. La función [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) no tiene una función correspondiente en el SPI, ya que esta función se implementa en Ws232.dll mediante una llamada \_ a [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).

Las funciones auxiliares [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) y [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) se asignan a las funciones correspondientes de la API de transporte, ya que solo un proveedor de transporte sabrá necesariamente cómo realizar la traducción en una [**estructura sockaddr.**](sockaddr-2.md)

 

 



