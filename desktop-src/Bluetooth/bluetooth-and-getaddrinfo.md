---
title: Bluetooth y getaddrinfo
description: La función getaddrinfo proporciona la traducción del nombre de host a la dirección de los transportes basados en IP. Dado que la función getaddrinfo es específica de los transportes basados en IP, se produce un error en Bluetooth sockets.
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- Bluetooth y getaddrinfo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c2e62b83ac947b74479ff435b93914661aa8da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974621"
---
# <a name="bluetooth-and-getaddrinfo"></a>Bluetooth y getaddrinfo

La [**función getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) proporciona la traducción del nombre de host a la dirección de los transportes basados en IP. Dado que **la función getaddrinfo** es específica de los transportes basados en IP, se produce un error en Bluetooth sockets.

Para realizar la traducción del nombre de host a la dirección de los sockets de Bluetooth, use la función [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) con **LUP \_ CONTAINERS** para consultar dispositivos remotos y, a continuación, busque un nombre remoto correspondiente y la dirección correspondiente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 