---
title: Asignación de los iDs de WinEvent
description: Cada WinEvent está pensado para usarse solo para un propósito específico. El uso de WinEvent para un propósito no intencionado puede provocar colisiones con otras aplicaciones o con el sistema operativo, lo que puede hacer que las aplicaciones o el sistema operativo se vuelvan inestables.
ms.assetid: 956d6db4-f342-4b11-bfd9-92725284223f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e877c6adcba79870d887e0bdb0d2eb9137d9e04fda4c1cc770414d0dd01f96d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326887"
---
# <a name="allocation-of-winevent-ids"></a>Asignación de los iDs de WinEvent

Cada WinEvent está pensado para usarse solo para un propósito específico. El uso de WinEvent para un propósito no intencionado puede provocar colisiones con otras aplicaciones o con el sistema operativo, lo que puede hacer que las aplicaciones o el sistema operativo se vuelvan inestables.

Microsoft ha definido varias categorías diferentes de WinEvents y, para cada categoría, ha definido uno o varios intervalos de valores para su uso como IDs de WinEvent. El Community reservado (0xA000 0xAFFF) está disponible para las aplicaciones que necesitan definir nuevos WinEvents. El uso de valores de este intervalo ayuda a reducir el riesgo de colisiones. sin embargo, los desarrolladores que crean nuevos WinEvents todavía necesitan colaborar para evitar colisiones entre sus aplicaciones.

En la tabla siguiente se muestran las categorías de WinEvent y los intervalos de valores definidos para cada categoría.



| Categoría                                                | Intervalo         | Actualmente en uso | Comentarios                                                                                        |
|---------------------------------------------------------|---------------|------------------|-------------------------------------------------------------------------------------------------|
| Microsoft Active Accessibility eventos (reservados del sistema) | 0x0001-0x00FF | 0x0001-0x0020    | EVENT \_ SYSTEM \_ \* event IDs                                                                     |
| Microsoft Active Accessibility eventos (reservados del sistema) | 0x4001-0x40FF | 0x4001-0x4007    | Event \_ CONSOLE \_ \* event IDs (IDs de eventos de EVENT CONSOLE)                                                                    |
| Automatización de la interfaz de usuario eventos (reservados para el sistema)                  | 0x4E00-0x4EFF | 0x4E20-0x4E33    | Automatización de la interfaz de usuario de eventos                                                                         |
| Automatización de la interfaz de usuario eventos (reservados para el sistema)                  | 0x7500-0x75FF | 0x7530-0x759B    | Automatización de la interfaz de usuario de eventos cambiados por la propiedad                                                        |
| Microsoft Active Accessibility eventos (reservados del sistema) | 0x8000-0x80FF | 0x8000-0x8015    | EVENT \_ OBJECT \_ \* event IDs                                                                     |
| Reservada para OEM                                            | 0x0101-0x01FF | 0x0101-0x0122    | IAccessible2 event IDs                                                                          |
| Community Reservados                                      | 0xA000-0xAFFF | Ninguno             | Reservado para nuevos eventos definidos por las especificaciones de Accessibility Interoperability Alliance (AIA) |
| ATOM                                                    | 0xC000-0xFFFF | 0xC000-0xFFFF    | Reservado para eventos personalizados asignados en tiempo de ejecución                                                 |



 

En los temas siguientes se describen los intervalos de WinEvent con más detalle.

## <a name="microsoft-active-accessibility-and-ui-automation-events"></a>Microsoft Active Accessibility y eventos Automatización de la interfaz de usuario eventos

Los Microsoft Active Accessibility y Microsoft Automatización de la interfaz de usuario reservan cinco intervalos de ID de WinEvent. El primer intervalo (0x0001 0x00FF) está reservado para eventos de nivel de sistema, que normalmente se usan para describir situaciones que afectan a todas las aplicaciones del sistema. El segundo intervalo (0x4001 0x40FF) está reservado para Windows eventos específicos de la consola. El tercer (0x4E00,0x4EFF) y el cuarto intervalo (0x7500 0x75FF) son para la reflexión de Automatización de la interfaz de usuario eventos. Por último, el quinto intervalo (0x8000 0x80FF) es para eventos de nivel de objeto que pertenecen a situaciones específicas de objetos dentro de una aplicación.

Todos Microsoft Active Accessibility eventos Automatización de la interfaz de usuario se definen en los archivos de encabezado WinUser.h y UIAutomationClient.h.

## <a name="oem-reserved-events"></a>Eventos reservados de OEM

El intervalo reservado de OEM está abierto a cualquier persona que necesite usar WinEvents como mecanismo de comunicación. Los desarrolladores deben definir y publicar definiciones de eventos junto con sus parámetros (o también con los tipos de objeto asociados) para el procesamiento de eventos, de modo que se puedan evitar colisiones accidentales de los iDs de evento. La especificación IAccessible2 usa parte del intervalo reservado de OEM.

## <a name="community-reserved-events"></a>Community Eventos reservados

El Community reservado es para WinEvents especificado por Accessibility Interoperability Alliance (AIA) para su uso en todo el sector. Se recomienda encarecidamente a los desarrolladores que definan y publiquen una especificación oficial antes de usar valores de este intervalo.

## <a name="atom-events"></a>Eventos ATOM

El intervalo ATOM está reservado para los iD de eventos que se asignan en tiempo de ejecución a través de la API Automatización de la interfaz de usuario extensibilidad. No use los valores del intervalo ATOM para ningún otro propósito. El uso [**de la función GlobalAddAtom**](/windows/desktop/api/winbase/nf-winbase-globaladdatoma) con un GUID de cadena es el método recomendado para asignar WinEvents desde el intervalo ATOM.

## <a name="using-values-from-a-reserved-range"></a>Usar valores de un intervalo reservado

Según la especificación de WinEvent, los valores del intervalo reservado del sistema o cualquier otro intervalo no definido no se pueden usar sin revisar el SDK. En el caso de los nuevos WinEvents, las aplicaciones deben usar valores de los intervalos reservados o reservados Community OEM. Antes de usar un nuevo WinEvent, se recomienda encarecidamente a los desarrolladores que compartan sus especificaciones de forma abierta y amplia, y deben trabajar con Accessibility Interoperability Alliance para definir las especificaciones de WinEvent.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[WinEvents](winevents-infrastructure.md)
</dt> <dt>

[Accessibility Interoperability Alliance](https://www.atia.org/)
</dt> </dl>

 

 