---
title: Asignación de identificadores de WinEvent
description: Cada WinEvent está pensado para usarse solo para un propósito específico. El uso de un WinEvent para un propósito imprevisto puede provocar colisiones con otras aplicaciones o con el sistema operativo, lo que puede hacer que las aplicaciones o el sistema operativo sean inestables.
ms.assetid: 956d6db4-f342-4b11-bfd9-92725284223f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f339641e5a3b679f572bc3b60c3e68be7b65f2a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685718"
---
# <a name="allocation-of-winevent-ids"></a>Asignación de identificadores de WinEvent

Cada WinEvent está pensado para usarse solo para un propósito específico. El uso de un WinEvent para un propósito imprevisto puede provocar colisiones con otras aplicaciones o con el sistema operativo, lo que puede hacer que las aplicaciones o el sistema operativo sean inestables.

Microsoft ha definido varias categorías diferentes de WinEvents y, para cada categoría, ha definido uno o más rangos de valores para su uso como ID. de WinEvent. El intervalo reservado de la comunidad (0xA000 — 0xAFFF) está disponible para las aplicaciones que necesitan definir nuevas WinEvents. El uso de valores de este intervalo ayuda a reducir el riesgo de colisiones; sin embargo, los desarrolladores que creen nuevos WinEvents todavía necesitan colaborar para evitar colisiones entre sus aplicaciones.

En la tabla siguiente se muestran las categorías WinEvent y los intervalos de valores definidos para cada categoría.



| Category                                                | Intervalo         | Actualmente en uso | Comentarios                                                                                        |
|---------------------------------------------------------|---------------|------------------|-------------------------------------------------------------------------------------------------|
| Eventos de Microsoft Active Accessibility (reservado para el sistema) | 0x0001-0x00FF | 0x0001-0x0020    | ID. de \_ \_ \* evento del sistema de eventos                                                                     |
| Eventos de Microsoft Active Accessibility (reservado para el sistema) | 0x4001-0x40FF | 0x4001-0x4007    | ID. de \_ \_ \* evento de consola de eventos                                                                    |
| Eventos de automatización de la interfaz de usuario (reservado por el sistema)                  | 0x4E00-0x4EFF | 0x4E20-0x4E33    | Identificadores de eventos de UI Automation                                                                         |
| Eventos de automatización de la interfaz de usuario (reservado por el sistema)                  | 0x7500-0x75FF | 0x7530-0x759B    | Identificadores de eventos de cambio de propiedad de UI Automation                                                        |
| Eventos de Microsoft Active Accessibility (reservado para el sistema) | 0x8000-0x80FF | 0x8000-0x8015    | ID. de \_ \_ \* evento de objeto de evento                                                                     |
| OEM reservado                                            | 0x0101-0x01FF | 0x0101-0x0122    | Identificadores de evento de IAccessible2                                                                          |
| Comunidad reservada                                      | 0xA000-0xAFFF | None             | Reservado para nuevos eventos definidos por las especificaciones de la Alianza de interoperabilidad de accesibilidad (AIA) |
| ATOM                                                    | 0xC000-0xFFFF | 0xC000-0xFFFF    | Reservado para eventos personalizados asignados en tiempo de ejecución                                                 |



 

En los temas siguientes se describen los intervalos de WinEvent con mayor detalle.

## <a name="microsoft-active-accessibility-and-ui-automation-events"></a>Eventos de Microsoft Active Accessibility y UI Automation

Los cinco intervalos de identificadores de WinEvent se reservan para su uso por parte de Microsoft Active Accessibility y Microsoft UI Automation. El primer intervalo (0x0001 — 0x00FF) está reservado para los eventos de nivel de sistema, que normalmente se usa para describir situaciones que afectan a todas las aplicaciones del sistema. El segundo intervalo (0x4001 — 0x40FF) está reservado para eventos específicos de la consola de Windows. El tercer (0x4E00 — 0x4EFF) y el cuarto rangos (0x7500, 0x75FF) son para la reflexión de eventos de automatización de la interfaz de usuario. Por último, el quinto intervalo (0x8000, 0x80FF) es para los eventos de nivel de objeto que pertenecen a situaciones específicas de objetos dentro de una aplicación.

Todos los eventos de Microsoft Active Accessibility y de automatización de la interfaz de usuario se definen en los archivos de encabezado WinUser. h y UIAutomationClient. h.

## <a name="oem-reserved-events"></a>Eventos reservados para OEM

El intervalo reservado de OEM está abierto para cualquier persona que necesite usar WinEvents como mecanismo de comunicación. Los desarrolladores deben definir y publicar definiciones de eventos junto con sus parámetros (o también con tipos de objetos asociados) para el procesamiento de eventos, de modo que se puedan evitar colisiones accidentales de los identificadores de eventos. La especificación IAccessible2 usa parte del intervalo reservado de OEM.

## <a name="community-reserved-events"></a>Eventos reservados de la comunidad

El intervalo reservado de la comunidad es para los WinEvents especificados por la Alianza de interoperabilidad de accesibilidad (AIA) para su uso en todo el sector. Se recomienda a los desarrolladores definir y publicar una especificación oficial antes de usar los valores de este intervalo.

## <a name="atom-events"></a>Eventos ATOM

El intervalo ATOM está reservado para los identificadores de evento que se asignan en tiempo de ejecución a través de la API de extensibilidad de automatización de la interfaz de usuario. No use los valores del intervalo ATOM para ningún otro propósito. El uso de la función [**GlobalAddAtom**](/windows/desktop/api/winbase/nf-winbase-globaladdatoma) con un GUID de cadena es el método recomendado para asignar WinEvents desde el intervalo Atom.

## <a name="using-values-from-a-reserved-range"></a>Usar valores de un intervalo reservado

Según la especificación de WinEvent, los valores del intervalo reservado del sistema o cualquier otro intervalo no definido no se pueden usar sin revisar el SDK. En el caso de los nuevos WinEvents, las aplicaciones deben usar valores de los intervalos reservados de OEM o reservados de la comunidad. Antes de usar un nuevo WinEvent, se recomienda encarecidamente a los desarrolladores que compartan sus especificaciones de una vez a otra y que funcionen con la Alianza de interoperabilidad de accesibilidad para definir especificaciones de WinEvent.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[WinEvents](winevents-infrastructure.md)
</dt> <dt>

[Alianza de interoperabilidad de accesibilidad](https://www.atia.org/)
</dt> </dl>

 

 