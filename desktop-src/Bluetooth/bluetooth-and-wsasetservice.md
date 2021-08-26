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
ms.openlocfilehash: 671e43636de67cee1e1c3c945a3647b5db59e7b0dd22b6eefd70b51f4977c31e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004175"
---
# <a name="bluetooth-and-wsasetservice"></a>Bluetooth y WSASetService

Bluetooth usa la función [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) para registrar o quitar una instancia de servicio dentro del espacio de nombres Bluetooth (NS \_ BTH) del registro. El identificador devuelto por esta operación solo se puede usar para eliminar el servicio.

Bluetooth tiene dos medios para anunciar servicios mediante la [**función WSASetService:**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea)

-   La aplicación puede hacer que el sistema anuncie un registro Bluetooth servicio SDP simple, construido a partir de miembros estándar en la [**estructura WSAQUERYSET.**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
-   La aplicación puede hacer que el sistema anuncie su propio registro Bluetooth SDP pasando una estructura [**BTH \_ SET \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) en el miembro **lpBlob** de la estructura [**WSAQUERYSET.**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) Se trata de un enfoque más complejo.

> [!Note]  
> Los registros SDP anunciados [**por WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) no se conservan después de que el proceso que los publicó haya dejado de hacerlo.

 

El uso [**de WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) con Bluetooth tiene los siguientes requisitos:

-   El *parámetro lpqsRegInfo* es la dirección de la [**estructura WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) que se va a registrar.
-   El *parámetro essOperation* es una enumeración que contiene una de las operaciones que se muestran en la tabla siguiente.



| Value                  | Descripción                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| REGISTRO DE \_ RNRSERVICE   | Comienza a anunciar el servicio a las radios remotas que consultan mediante Bluetooth protocolo SDP. |
| RNRSERVICE \_ DEREGISTER | No es válido. Devuelve un error.                                                               |
| RNRSERVICE \_ DELETE     | Deja de anunciar el servicio.                                                             |



 

> [!Note]  
> Los identificadores de servicio detectados durante una llamada [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) o [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) no son compatibles con la operación DELETE de RNRSERVICE. \_

 

-   El *parámetro dwControlFlags* está reservado y debe ser cero.

Para obtener más información y una lista de las Bluetooth de socket, [vea Bluetooth y Opciones de socket](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 