---
title: Bluetooth y función getaddrinfo
description: La función función getaddrinfo proporciona traducción desde el nombre de host a la dirección para los transportes basados en IP. Dado que la función función getaddrinfo es específica de los transportes basados en IP, se produce un error en los sockets Bluetooth.
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- Bluetooth y función getaddrinfo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c2e62b83ac947b74479ff435b93914661aa8da
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793539"
---
# <a name="bluetooth-and-getaddrinfo"></a>Bluetooth y función getaddrinfo

La función [**función getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) proporciona traducción desde el nombre de host a la dirección para los transportes basados en IP. Dado que la función **función getaddrinfo** es específica de los transportes basados en IP, se produce un error en los sockets Bluetooth.

Para realizar la traducción desde el nombre de host a la dirección para los sockets de Bluetooth, use la función [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) con **\_ contenedores LUP** para consultar los dispositivos remotos y, a continuación, busque un nombre remoto coincidente específico y la dirección correspondiente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 