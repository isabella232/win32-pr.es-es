---
title: Bluetooth y WSASetService
description: Bluetooth usa la función WSASetService para registrar o quitar una instancia de servicio en el espacio de nombres Bluetooth (NS \_ BTH) del registro.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth Bluetooth
- Bluetooth de WSASetService
- Bluetooth y WSASetService Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70399b73bf24477ee1a0ec0c7585a9f46b7657ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487786"
---
# <a name="bluetooth-and-wsasetservice"></a>Bluetooth y WSASetService

Bluetooth usa la función [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) para registrar o quitar una instancia de servicio en el espacio de nombres Bluetooth (NS \_ BTH) del registro. El identificador devuelto por esta operación solo se puede usar para eliminar el servicio.

Bluetooth tiene dos formas de anunciar servicios mediante la función [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) :

-   La aplicación puede hacer que el sistema anuncie un registro del Servicio SDP Bluetooth simple, construido a partir de los miembros estándar de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .
-   La aplicación puede hacer que el sistema anuncie su propio registro SDP Bluetooth pasando una estructura de [**\_ \_ servicio del conjunto BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) en el miembro **lpBlob** de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) . Se trata de un enfoque más complejo.

> [!Note]  
> Los registros SDP anunciados por [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) no se conservan después de que se cierre el proceso que los publicó.

 

El uso de [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) con Bluetooth tiene los siguientes requisitos:

-   El parámetro *lpqsRegInfo* es la dirección de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) que se va a registrar.
-   El parámetro *essOperation* es una enumeración que contiene una de las operaciones que se muestran en la tabla siguiente.



| Value                  | Descripción                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| registro de RNRSERVICE \_   | Comienza a anunciar el servicio a las radios remotas que consultan mediante el protocolo SDP Bluetooth. |
| \_anular registro de RNRSERVICE | No es válido. Devuelve un error.                                                               |
| RNRSERVICE \_ eliminar     | Deja de anunciar el servicio.                                                             |



 

> [!Note]  
> Los identificadores de servicio detectados durante una llamada a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) o [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) son incompatibles con la operación de eliminación de RNRSERVICE \_ .

 

-   El parámetro *dwControlFlags* está reservado y debe ser cero.

Para obtener más información y una lista de opciones de Socket Bluetooth, consulte [Opciones de Bluetooth y socket](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 