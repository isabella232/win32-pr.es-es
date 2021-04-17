---
description: El funcionamiento correcto de los componentes de TAPI requiere la configuración del entorno de comunicaciones en un equipo.
ms.assetid: 3df3d974-629e-4d78-b97d-b8121b185309
title: Inicialización de TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 973d67931fb9f33751fedc638ab77021d3d3d34c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688319"
---
# <a name="tapi-initialization"></a>Inicialización de TAPI

El funcionamiento correcto de los componentes de TAPI requiere la configuración del entorno de comunicaciones en un equipo como se indica a continuación:

-   La [instalación](installation.md) se realiza cuando el software o hardware se agrega por primera vez al equipo. Los procedimientos detallados dependen del sistema operativo y el propio software.
-   La [inicialización principal](primary-initialization.md) crea los objetos y las rutas de comunicación.
-   La negociación de la [versión](version-negotiation.md) garantiza que los componentes de TAPI podrán intercambiar datos.
-   El [inventario de recursos](resource-inventory.md) recupera información acerca de los dispositivos disponibles para su uso en una aplicación TAPI.
-   [Notificación de eventos](event-notification.md) especifica cómo TAPI y los proveedores de servicios pasan los resultados de operación asincrónicos y la información de cambio de estado a la aplicación.

## <a name="summary-of-related-reference-pages"></a>Resumen de páginas de referencia relacionadas



| Funciones de TAPI 2. x                                        | Descripción                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)     | Configura el entorno de telefonía, devuelve el identificador de la aplicación y el recuento de dispositivos.                                                   |
| [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)         | Obtiene las funcionalidades del dispositivo, como la versión de TAPI o los tipos de medios admitidos.                                                          |
| [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) | Obtiene las capacidades de dirección, por ejemplo, si se admite el estacionamiento de llamadas.                                                                |
| [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen)                     | Notifica a TAPI que la aplicación va a utilizar la línea y de qué manera.                                                       |
| [**lineGetMessage**](/windows/win32/api/tapi/nf-tapi-linegetmessage)         | Devuelve el siguiente mensaje de TAPI que está en cola para su entrega en una aplicación que utiliza el mecanismo de notificación de identificadores de eventos. |



 



| Interfaces o métodos TAPI 3. x                                                | Descripción                                                                                                                                |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITTAPI:: Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize)                               | Configura el entorno de telefonía.                                                                                                             |
| [**ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)               | Enumera las direcciones disponibles actualmente.                                                                                                  |
| [**ITTAPI:: get \_ Addresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses)                        | Crea una colección de direcciones disponibles actualmente. Se proporciona para las aplicaciones cliente de automatización, como las escritas en Visual Basic. |
| [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)       | Determina la respuesta a una notificación de eventos asincrónica. Implementado por la aplicación, invocada por TAPI.                                |
| [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter)                    | Establece la máscara del filtro de eventos, que notifica a TAPI los eventos que requiere la aplicación.                                                     |
| [**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) | Indica a TAPI que pase las sesiones de entrada de la aplicación para una dirección especificada y un conjunto de tipos de medios.                                   |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                                      | Permite a una aplicación detectar las capacidades de soporte de medios para una dirección.                                                           |



 

 

 
