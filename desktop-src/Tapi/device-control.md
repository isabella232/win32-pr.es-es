---
description: El control de dispositivos en el nivel de aplicación de servidor o de usuario final requiere un conjunto relativamente pequeño de información básica.
ms.assetid: 9c787656-93ef-4e0b-9516-8822ae49a83a
title: Control de dispositivo (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b17336941a55a529c6b436270f7b225a1cada3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686788"
---
# <a name="device-control-telephony-api"></a>Control de dispositivo (API de telefonía)

El control de dispositivos en el nivel de aplicación de servidor o de usuario final requiere un conjunto relativamente pequeño de información básica. La capa de abstracción del proveedor de servicios realiza el control detallado del dispositivo. Los proveedores de servicios notifican la información de dispositivo necesaria a una aplicación a través de TAPI.

Las categorías de dispositivos clave incluyen:

-   [Red](network-ovr.md): la capa de transporte para las comunicaciones. Desde el punto de vista de una aplicación, la información sobre la red normalmente se incrusta en el tipo de dirección, como LINEADDRESSTYPE \_ PHONENUMBER.
-   [Línea](line-ovr.md): conexión a una red. Este concepto se usa mucho en TAPI 2,2 (TAPI/C).
-   [Canal](channel-ovr.md): subdivisión de una línea. Normalmente, el conocimiento de los canales no es necesario para una aplicación porque el proveedor de servicios configura cómo aparecerán como direcciones.
-   [Dirección](address-ovr.md): una ubicación de red en una red. Cada línea o canal tiene una o más direcciones asociadas. La dirección es un concepto clave en TAPI 3,1 (TAPI/COM) y TAPI 2,2 (TAPI/C).
-   [Terminal](terminal-ovr.md): un origen o un representador para una dirección y un tipo de medio concretos.

Los proveedores de servicios notifican las características del dispositivo a TAPI en respuesta a las consultas de la aplicación. Los proveedores de servicios también inician informes de cambios en el estado del dispositivo. Estos cambios se notifican a una aplicación en función de las notificaciones solicitadas durante la inicialización.

Las características básicas del dispositivo son:

-   [Clase de dispositivo](device-class-ovr.md)
-   [Identificador de dispositivo](device-identifier-ovr.md)
-   [Tipo de dirección](address-type-ovr.md)
-   [Identificador de dirección](address-identifier-ovr.md)
-   [Eventos de dispositivo](device-events-ovr.md)
-   [Tipo de medio](media-type-ovr.md)
-   [Tipo de terminal](terminal-type-ovr.md)

Además, los proveedores de servicios proporcionan información sobre la capacidad de una dirección determinada para realizar varias operaciones de sesión.

Si los proveedores de servicios lo admiten, se pueden asociar características complementarias a determinados dispositivos. Una aplicación TAPI 2. x detecta funcionalidades mediante el uso de las funciones [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) y [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) . Las aplicaciones TAPI 3. x usan la interfaz [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) para este propósito.

TAPI 2. x proporciona un conjunto especial de operaciones adicionales que el proveedor de servicios puede implementar para su uso con dispositivos telefónicos. Consulte [dispositivos telefónicos](./opening-and-closing-phone-devices.md).

Las funcionalidades extendidas son específicas del proveedor y no están directamente representadas por la API de telefonía de Microsoft. Consulte [funciones de línea extendida](./extended-line-functions.md), [funciones de teléfono de telefonía extendidas](./extended-telephony-phone-functions.md)o [interfaces específicas del proveedor](provider-specific-interfaces.md).

A continuación se muestra un resumen de las operaciones de TAPI que consultan los proveedores de servicios en las características del dispositivo y proporcionan datos sobre el estado actual.



| Funciones de TAPI 2. x                                                  | Descripción                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)                   | Consulta un dispositivo de línea especificado para determinar las capacidades de telefonía de las direcciones asociadas.               |
| [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps)           | Consulta un dispositivo de línea especificado para determinar las capacidades de telefonía de una dirección específica.                   |
| [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig)               | Devuelve una estructura de datos "opaca" que almacena la configuración actual de un dispositivo.                          |
| [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig)               | Restaura la configuración del dispositivo.                                                                                 |
| [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog)               | Muestra un cuadro de diálogo que permite al usuario configurar los parámetros relacionados con el dispositivo.                       |
| [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid)                             | Recupera un identificador de dispositivo estable que se puede usar en otras llamadas a funciones TAPI o con una API diferente. |
| [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus)       | Consulta el estado actual del dispositivo, como el número de llamadas activas.                                             |
| [**lineSetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linesetlinedevstatus)       | Establece el estado del dispositivo, como la configuración de un dispositivo como no en servicio.                                                |
| [**lineGetIcon**](/windows/win32/api/tapi/nf-tapi-linegeticon)                         | Recupera el icono específico del proveedor que se va a mostrar al usuario.                                                      |
| [**lineNegotiateExtVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) | Permite que una aplicación negocie una versión de extensión para usarla con el dispositivo de línea especificado.                 |
| [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific)                 | Proporciona acceso a las características específicas del dispositivo.                                                                      |
| [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature)   | Envía características específicas del dispositivo al proveedor de servicios.                                                        |



 



| Interfaces o métodos TAPI 3. x                                   | Descripción                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)           | Obtiene información sobre las funciones de una dirección.                                                  |
| [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat)                       | Establece y obtiene el formato multimedia de™ DirectShow.                                                                 |
| [**ITBasicAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal)             | Establece y obtiene características estándar del terminal de audio, como el volumen.                                  |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                         | Obtiene información relativa a las capacidades de soporte de multimedia de una dirección.                                    |
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                 | Interfaz base para el objeto terminal. Obtiene información como la clase de terminal y los medios admitidos. |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                   | Obtiene información sobre los terminales disponibles y crea terminales adicionales.                               |
| [Interfaces específicas del proveedor](provider-specific-interfaces.md) | Dependiente del proveedor de servicios.                                                                             |



 

 

 
