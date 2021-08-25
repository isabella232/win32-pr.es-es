---
title: Introducción al proveedor WMI de DNS
description: Un proveedor es un elemento arquitectónico de Windows Management Instrumentation (WMI).
ms.assetid: e6ada7b5-dd46-4c47-8db8-55f910429e31
keywords:
- Sistema de nombres de dominio, proveedor WMI, arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea44103edba64a1f572beef9cff9b8aeb31f02344f172f42b2a7378a6fbf3677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913165"
---
# <a name="dns-wmi-provider-overview"></a>Introducción al proveedor WMI de DNS

Un proveedor es un elemento arquitectónico de *Windows Management Instrumentation (WMI)*. WMI define una arquitectura unificada para describir, obtener acceso e instrumentar objetos. Parte de esta arquitectura es una gran base de datos de clases WMI que se usa para llevar a cabo tareas de administración remota en objetos específicos.

Los proveedores WMI actúan como intermediarios entre WMI y uno o varios objetos administrados. Cuando WMI recibe una solicitud de una aplicación de administración para los datos que no están disponibles en el repositorio CIM o para las notificaciones de eventos que WMI no admite, reenvía la solicitud a un proveedor. Los proveedores proporcionan datos y notificaciones de eventos para objetos administrados específicos de su dominio particular. Un proveedor extiende el esquema WMI de clases para permitir que WMI funcione con nuevos tipos de objetos. El proveedor WMI de DNS define clases para consultar y configurar un servidor DNS, junto con sus zonas DNS asociadas y registros DNS.

El proveedor WMI de DNS expone una serie de objetos DNS a los clientes, incluidos los objetos DNS Server, DNS domain y DNS RR. A través de esos objetos, los clientes pueden realizar actividades de administración de DNS.

Con el proveedor WMI de DNS, puede crear sus propias herramientas para realizar la mayoría de las tareas de administración del servidor DNS. Por ejemplo, puede crear, eliminar y ver zonas y registros; restablecer las propiedades de servidor y zona; y realizan operaciones rutinarias de administración, como actualizar la zona, volver a cargarla, actualizarla, volver a escribir la zona en un archivo o Active Directory, pausar y reanudar la zona, borrar la caché, detener e iniciar el servicio DNS y ver estadísticas.

El proveedor WMI de DNS tiene un conjunto de comportamientos únicos que no se encuentran en otros proveedores. Vea la Referencia [del proveedor WMI de DNS para](dns-wmi-provider-reference.md) obtener detalles de clase.

 

 




