---
description: La mayoría de las funciones getXbyY se traducen mediante el32.dll de Ws2 a una secuencia \_ WSALookupServiceBegin, WSALookupServiceNext y WSALookupServiceEnd que usa uno de un conjunto de GUID especiales como clase de servicio.
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: Enfoque básico de GetXbyY en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9e6dd0e5569bd11de813e28eaec1ee04f6b5f206277f695cdb9aaab05ec4a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322629"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a>Enfoque básico de GetXbyY en la API

La mayoría de las funciones **getXbyY** se traducen mediante el32.dll de Ws2 a una secuencia \_ [**WSALookupServiceBegin,**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)y [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) que usa uno de un conjunto de GUID especiales como clase de servicio. Estos GUID identifican el tipo de **operación getXbyY** que se emula. La consulta está restringida a los proveedores de servicios de nombres que admiten AF \_ INET. Cada vez que una función **getXbyY** devuelve una estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) o [**SER SERIALIZA,**](/windows/desktop/api/winsock/ns-winsock-servent) el32.dll de Ws2 especifica la marca LUP RETURN BLOB en \_ \_ \_ **WSALookupServiceBegin** para que el proveedor de servicios de nombre devuelva la información deseada. Estas estructuras deben modificarse ligeramente, ya que los punteros contenidos en deben reemplazarse por desplazamientos relativos al inicio de los datos del blob. Por supuesto, todos los valores a los que hacen referencia estos parámetros de puntero deben estar completamente contenidos en el blob y todas las cadenas son ASCII.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resolución de nombres compatible para TCP/IP en la API Windows Sockets 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Resolución de nombres independientes del protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



