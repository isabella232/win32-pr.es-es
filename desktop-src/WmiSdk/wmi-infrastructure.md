---
description: En la infraestructura de WMI, el servicio WMI (WinMgmt) es el componente del sistema operativo que actúa como el mediador entre las aplicaciones de administración y los proveedores de datos de WMI. El repositorio WMI es un área de almacenamiento para los datos estáticos relacionados con WMI.
ms.assetid: 6ef157be-fb75-4453-bc20-4568a3dc18c0
ms.tgt_platform: multiple
title: Infraestructura WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4370af9ec062ffa845d54eafda054357a76dc07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706151"
---
# <a name="wmi-infrastructure"></a>Infraestructura WMI

En la infraestructura de WMI, el servicio WMI (WinMgmt) es el componente del sistema operativo que actúa como el mediador entre las aplicaciones de administración y los [*proveedores*](gloss-p.md)de datos de WMI. El [*repositorio WMI*](gloss-w.md) es un área de almacenamiento para los datos estáticos relacionados con WMI.

El servicio WMI se implementa como un proceso de servicio dentro de un proceso de host de servicio compartido (SVCHOST). Para obtener más información, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).

El servicio WMI se inicia cuando la primera aplicación o script de administración realiza una llamada para conectarse a un espacio de nombres WMI. Dependiendo de la configuración, el servicio WMI puede cerrarse o entrar en un perfil de memoria insuficiente cuando una aplicación de administración no lo llama.

El servicio WMI interactúa con las aplicaciones de administración a través de la interfaz COM. Cuando una aplicación realiza una solicitud a través de la interfaz, WMI determina si la solicitud es para datos estáticos o dinámicos. Si la solicitud implica datos estáticos, como el nombre de un objeto administrado, WMI recupera los datos del repositorio. Si la solicitud implica datos dinámicos, como la cantidad de memoria que está usando un objeto administrado actualmente, WMI pasa la solicitud a un proveedor.

Los proveedores registran su ubicación con el servicio WMI, que permite a WMI enrutar las solicitudes de datos. Un proveedor también registra la compatibilidad con operaciones particulares, como la recuperación de datos, la modificación, la eliminación, la enumeración o el procesamiento de consultas. El servicio WMI utiliza la información de registro del proveedor para hacer coincidir las solicitudes de la aplicación con el proveedor adecuado. WMI también usa la información de registro para cargar y descargar los proveedores, según sea necesario. Cuando un proveedor finaliza el procesamiento de una solicitud, el proveedor devuelve el resultado al servicio WMI. Después, WMI reenvía el resultado a la aplicación a través de la interfaz COM. Para obtener más información, consulte [proporcionar datos a WMI](providing-data-to-wmi.md).

WMI utiliza el [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW) para registrar la actividad del servicio WMI.

Dado que la infraestructura controla todo el tráfico entre los proveedores y las aplicaciones de administración, la infraestructura proporciona las siguientes características:

-   Compatibilidad con la notificación de eventos

    Para obtener más información, consulte [supervisión de eventos](monitoring-events.md).

-   Compatibilidad con el lenguaje de consulta

    Para obtener más información, vea [consultas con WQL](querying-with-wql.md).

-   Compatibilidad con la seguridad

    Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md).

-   Scripting de acceso a los datos del contador de rendimiento

    Para obtener más información, vea [supervisar datos de rendimiento](monitoring-performance-data.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Arquitectura de WMI](wmi-architecture.md)
</dt> </dl>

 

 
