---
description: El funcionamiento correcto de los componentes de TAPI requiere configurar el entorno de comunicaciones en un equipo.
ms.assetid: 3df3d974-629e-4d78-b97d-b8121b185309
title: Inicialización de TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 973d67931fb9f33751fedc638ab77021d3d3d34c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476319"
---
# <a name="tapi-initialization"></a>Inicialización de TAPI

El funcionamiento correcto de los componentes de TAPI requiere configurar el entorno de comunicaciones en un equipo de la siguiente manera:

-   [La](installation.md) instalación se realiza cuando se agrega software o hardware al equipo por primera vez. Los procedimientos detallados dependen del sistema operativo y del propio software.
-   [La inicialización principal](primary-initialization.md) crea los objetos y las rutas de comunicación.
-   [La negociación](version-negotiation.md) de versiones garantiza que los componentes tapi podrán intercambiar datos.
-   [El inventario de](resource-inventory.md) recursos recupera información relativa a los dispositivos disponibles para su uso por una aplicación TAPI.
-   [La notificación de](event-notification.md) eventos especifica cómo TAPI y los proveedores de servicios pasan los resultados de la operación asincrónica y la información de cambio de estado a la aplicación.

## <a name="summary-of-related-reference-pages"></a>Resumen de páginas de referencia relacionadas



| Funciones TAPI 2.x                                        | Descripción                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)     | Configura el entorno de telefonía, devuelve el identificador de la aplicación y el número de dispositivos.                                                   |
| [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)         | Obtiene las funcionalidades del dispositivo, como la versión de TAPI o los tipos de medios admitidos.                                                          |
| [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) | Obtiene funcionalidades de dirección, como si se admite call park.                                                                |
| [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen)                     | Notifica a TAPI que la aplicación va a usar la línea y de qué manera.                                                       |
| [**lineGetMessage**](/windows/win32/api/tapi/nf-tapi-linegetmessage)         | Devuelve el siguiente mensaje TAPI que se pone en cola para la entrega a una aplicación que usa el mecanismo de notificación del identificador de eventos. |



 



| Interfaces o métodos tapi 3.x                                                | Descripción                                                                                                                                |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITTAPI::Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize)                               | Configura el entorno de telefonía.                                                                                                             |
| [**ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)               | Enumera las direcciones disponibles actualmente.                                                                                                  |
| [**ITTAPI::get \_ Addresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses)                        | Crea una colección de direcciones disponibles actualmente. Se proporciona para las aplicaciones cliente de Automation, como las escritas en Visual Basic. |
| [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)       | Determina la respuesta a una notificación de eventos asincrónica. Implementado por la aplicación, invocado por TAPI.                                |
| [**ITTAPI::put \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter)                    | Establece la máscara de filtro de eventos, que notifica a TAPI qué eventos requiere la aplicación.                                                     |
| [**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) | Indica a TAPI que pase las sesiones entrantes de la aplicación para una dirección y un conjunto de tipos de medios especificados.                                   |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                                      | Permite que una aplicación detecte las funcionalidades de soporte técnico multimedia de una dirección.                                                           |



 

 

 
