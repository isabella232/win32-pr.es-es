---
title: Introducción al proveedor WMI de DNS
description: Un proveedor es un elemento arquitectónico de Instrumental de administración de Windows (WMI).
ms.assetid: e6ada7b5-dd46-4c47-8db8-55f910429e31
keywords:
- Sistema de nombres de dominio, proveedor WMI, arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6aed54d0d9cbac4070483e8e72e9917607e824c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075593"
---
# <a name="dns-wmi-provider-overview"></a>Introducción al proveedor WMI de DNS

Un proveedor es un elemento arquitectónico de *instrumental de administración de Windows (WMI)*. WMI define una arquitectura unificada para describir, obtener acceso e instrumentar objetos. Parte de esta arquitectura es una base de datos grande de clases WMI que se usa para llevar a cabo tareas de administración remota en objetos específicos.

Los proveedores de WMI actúan como intermediarios entre WMI y uno o varios objetos administrados. Cuando WMI recibe una solicitud de una aplicación de administración para datos que no están disponibles en el repositorio CIM o para notificaciones de eventos que WMI no admite, reenvía la solicitud a un proveedor. Los proveedores proporcionan datos y notificaciones de eventos para objetos administrados específicos de su dominio particular. Un proveedor extiende el esquema WMI de las clases para permitir que WMI funcione con nuevos tipos de objetos. El proveedor WMI de DNS define las clases para consultar y configurar un servidor DNS, junto con sus registros DNS y zonas DNS asociados.

El proveedor WMI de DNS expone una serie de objetos DNS a los clientes, incluido el servidor DNS, el dominio DNS y los objetos RR DNS. A través de estos objetos, los clientes pueden realizar actividades de administración de DNS.

Con el proveedor WMI de DNS, puede crear sus propias herramientas para realizar la mayoría de las tareas de administración del servidor DNS. Por ejemplo, puede crear, eliminar y ver las zonas y los registros; restablecer las propiedades del servidor y de la zona; y realizan operaciones de administración rutinarias, como actualizar la zona, volver a cargar la zona, actualizar la zona, escribir la zona en un archivo o Active Directory, pausar y reanudar la zona, borrar la memoria caché, detener e iniciar el servicio DNS y ver las estadísticas.

El proveedor WMI de DNS tiene un conjunto de comportamientos únicos que no se encuentran en otros proveedores. Vea la [Referencia del proveedor WMI de DNS](dns-wmi-provider-reference.md) para obtener información sobre la clase.

 

 




