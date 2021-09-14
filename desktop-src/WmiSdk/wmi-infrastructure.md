---
description: En la infraestructura WMI, el servicio WMI (Winmgmt) es el componente del sistema operativo que actúa como mediador entre las aplicaciones de administración y los proveedores de datos WMI. El repositorio WMI es un área de almacenamiento para datos estáticos relacionados con WMI.
ms.assetid: 6ef157be-fb75-4453-bc20-4568a3dc18c0
ms.tgt_platform: multiple
title: Infraestructura wmi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4370af9ec062ffa845d54eafda054357a76dc07c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967012"
---
# <a name="wmi-infrastructure"></a>Infraestructura wmi

En la infraestructura WMI, el servicio WMI (Winmgmt) es el componente del sistema operativo que actúa como mediador entre las aplicaciones de administración y los proveedores de [*datos*](gloss-p.md)WMI . El [*repositorio WMI es*](gloss-w.md) un área de almacenamiento para datos estáticos relacionados con WMI.

El servicio WMI se implementa como un proceso de servicio dentro de un proceso de host de servicio compartido (SVCHOST). Para obtener más información, vea [Provider Hosting and Security](provider-hosting-and-security.md).

El servicio WMI se inicia cuando la primera aplicación de administración o script realiza una llamada para conectarse a un espacio de nombres WMI. En función de la configuración, el servicio WMI puede apagarse o entrar en un perfil de memoria baja cuando una aplicación de administración no lo llama.

El servicio WMI interactúa con las aplicaciones de administración a través de la interfaz COM. Cuando una aplicación realiza una solicitud a través de la interfaz , WMI determina si la solicitud es para datos estáticos o dinámicos. Si la solicitud implica datos estáticos, como el nombre de un objeto administrado, WMI recupera los datos del repositorio. Si la solicitud implica datos dinámicos, como la cantidad de memoria que usa actualmente un objeto administrado, WMI pasa la solicitud a un proveedor.

Los proveedores registran su ubicación con el servicio WMI, que permite a WMI enrutar las solicitudes de datos. Un proveedor también registra la compatibilidad con operaciones concretas, como la recuperación de datos, la modificación, la eliminación, la enumeración o el procesamiento de consultas. El servicio WMI usa la información de registro del proveedor para hacer coincidir las solicitudes de aplicación con el proveedor adecuado. WMI también usa la información de registro para cargar y descargar proveedores, según sea necesario. Cuando un proveedor termina de procesar una solicitud, el proveedor devuelve el resultado al servicio WMI. WMI reenvía el resultado a la aplicación a través de la interfaz COM. Para obtener más información, vea [Proporcionar datos a WMI.](providing-data-to-wmi.md)

WMI usa [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW) para registrar la actividad del servicio WMI.

Dado que la infraestructura controla todo el tráfico entre los proveedores y las aplicaciones de administración, la infraestructura proporciona las siguientes características:

-   Compatibilidad con notificaciones de eventos

    Para obtener más información, vea [Monitoring Events](monitoring-events.md).

-   Compatibilidad con el lenguaje de consulta

    Para obtener más información, [vea Consulta con WQL.](querying-with-wql.md)

-   Soporte técnico de seguridad

    Para obtener más información, vea [Mantener la seguridad de WMI.](maintaining-wmi-security.md)

-   Scripting Access to Performance Counter Data

    Para obtener más información, vea [Supervisión de datos de rendimiento.](monitoring-performance-data.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Arquitectura de WMI](wmi-architecture.md)
</dt> </dl>

 

 
