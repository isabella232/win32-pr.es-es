---
title: Bluetooth y WSASetService
description: Bluetooth usa la función WSASetService para registrar o quitar una instancia de servicio dentro del espacio de nombres Bluetooth (NS \_ BTH) del registro.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth Bluetooth
- WSASetService Bluetooth
- Bluetooth y WSASetService Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70399b73bf24477ee1a0ec0c7585a9f46b7657ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261900"
---
# <a name="bluetooth-and-wsasetservice"></a>Bluetooth y WSASetService

Bluetooth usa la función [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) para registrar o quitar una instancia de servicio dentro del espacio de nombres Bluetooth (NS \_ BTH) del registro. El identificador devuelto por esta operación solo se puede usar para eliminar el servicio.

Bluetooth tiene dos medios para anunciar servicios mediante la [**función WSASetService:**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea)

-   La aplicación puede hacer que el sistema anuncie un registro de servicio Bluetooth SDP simple, construido a partir de miembros estándar en la [**estructura WSAQUERYSET.**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
-   La aplicación puede hacer que el sistema anuncie su propio registro de SDP Bluetooth pasando una estructura [**BTH \_ SET \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) en el miembro **lpBlob** de la estructura [**WSAQUERYSET.**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) Se trata de un enfoque más complejo.

> [!Note]  
> Los registros SDP anunciados [**por WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) no se conservan después de que el proceso que los publicó haya dejado de realizarse.

 

El uso [**de WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) con Bluetooth tiene los siguientes requisitos:

-   El *parámetro lpqsRegInfo* es la dirección de la [**estructura WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) que se va a registrar.
-   El *parámetro essOperation* es una enumeración que contiene una de las operaciones que se muestran en la tabla siguiente.



| Value                  | Descripción                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| REGISTRO DE \_ RNRSERVICE   | Comienza a anunciar el servicio a las consultas remotas de radios mediante Bluetooth protocolo SDP. |
| RNRSERVICE \_ DEREGISTER | No válido. Devuelve un error.                                                               |
| RNRSERVICE \_ DELETE     | Deja de anunciar el servicio.                                                             |



 

> [!Note]  
> Los identificadores de servicio detectados durante una llamada [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) o [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) no son compatibles con la operación DELETE de RNRSERVICE. \_

 

-   El *parámetro dwControlFlags* está reservado y debe ser cero.

Para obtener más información y una lista de las opciones Bluetooth socket, [vea Bluetooth y Opciones de socket](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 