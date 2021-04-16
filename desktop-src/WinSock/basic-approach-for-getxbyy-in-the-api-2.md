---
description: La mayoría de las funciones de getXbyY se traducen mediante el Ws2 \_32.dll a una secuencia WSALookupServiceBegin, WSALookupServiceNext y WSALookupServiceEnd que usa uno de los conjuntos de GUID especiales como clase de servicio.
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: Enfoque básico para GetXbyY en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4c038c87d6eb6e7ab2a4476271662d5b9567ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541635"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a>Enfoque básico para GetXbyY en la API

La mayoría de las funciones de **getXbyY** se traducen mediante el Ws2 \_32.dll a una secuencia [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)y [**WSALOOKUPSERVICEEND**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) que usa uno de los conjuntos de GUID especiales como clase de servicio. Estos GUID identifican el tipo de operación **getXbyY** que se está emulando. La consulta está restringida a los proveedores de servicios de nombres que admiten AF \_ inet. Cada vez que una función **getXbyY** devuelve una estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) o [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) , el \_32.dll Ws2 especifica el \_ indicador LUP Return \_ BLOB en **WSALookupServiceBegin** para que el proveedor de servicios de nombres devuelva la información deseada. Estas estructuras deben modificarse ligeramente en que los punteros contenidos en deben reemplazarse por desplazamientos que son relativos al inicio de los datos del BLOB. Todos los valores a los que hacen referencia estos parámetros de puntero deben, por supuesto, estar contenidos completamente dentro del BLOB y todas las cadenas son ASCII.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolución de nombres independiente del Protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



