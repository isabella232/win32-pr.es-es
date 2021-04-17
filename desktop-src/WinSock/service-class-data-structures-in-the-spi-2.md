---
description: Cuando se instala una nueva clase de servicio, se debe preparar y proporcionar una estructura WSASERVICECLASSINFO. Esta estructura también consta de subestructuras que contienen una serie de parámetros que se aplican a espacios de nombres específicos.
ms.assetid: fb225e0c-a0c7-44e1-80fb-7b924b371afa
title: Estructuras de datos de clase de servicio en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bf249c7437751e7c6d08b2fdf3830e92921ce7
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104560892"
---
# <a name="service-class-data-structures-in-the-spi"></a>Estructuras de datos de clase de servicio en el SPI

Cuando se instala una nueva clase de servicio, se debe preparar y proporcionar una estructura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) . Esta estructura también consta de subestructuras que contienen una serie de parámetros que se aplican a espacios de nombres específicos.

![Diagrama que muestra la estructura WSASERVICECLASSINFO, las subestructuras y los parámetros que se aplican a los espacios de nombres específicos.](images/ovrvw3-3.png)

Para cada clase de servicio, hay una única estructura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) . Dentro de la estructura **WSASERVICECLASSINFO** , el identificador único de la clase de servicio se encuentra en **lpServiceClassId** y **lpServiceClassName** hace referencia a una cadena de presentación asociada.

El miembro **lpClassInfos** de la estructura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) hace referencia a una matriz de estructuras [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) , cada una de las cuales proporciona un parámetro con nombre y con tipo que se aplica a un espacio de nombres especificado. Algunos ejemplos de valores para el miembro **lpszName** son: SAPID, TCPPORT, puertoudp, etc. Estas cadenas suelen ser específicas del espacio de nombres identificado en **dwNameSpace**. Los valores típicos de **dwValueType** podrían ser reg \_ DWORD, REG \_ SZ, etc. El miembro **dwValueSize** indica la longitud del elemento de datos al que apunta **lpValue**.

Toda la colección de datos representada en una estructura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) se proporciona a cada proveedor de espacios de nombres a través de [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass). Cada proveedor de espacios de nombres individual filtra la lista de estructuras [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) y conserva la información aplicable a ella. Esta arquitectura también aprovisiona la existencia futura de un proveedor de espacios de nombres especial que conservaría toda la información de esquema de clase de servicio para todos los espacios de nombres. El \_32.dll Ws2 consultar este proveedor para obtener los datos de **WSASERVICECLASSINFO** necesarios para proporcionar a los proveedores de espacios de nombres cuando se invoca [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) para iniciar una consulta y cuando se invoca [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice) para registrar un servicio. El proveedor de espacios de nombres no debe basarse en esta funcionalidad en el momento y, en su lugar, debe tener un medio específico del proveedor para obtener cualquier información de esquema de clase de servicio necesaria. En ausencia de un proveedor que almacena todo el esquema de clase de servicio para todos los espacios de nombres, el \_32.dll Ws2 utilizará [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) para obtener dicha información de cada proveedor de espacios de nombres individual.

 

 



