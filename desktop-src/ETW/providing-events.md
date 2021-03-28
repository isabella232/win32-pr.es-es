---
description: Los proveedores son aplicaciones que contienen instrumentación de seguimiento de eventos.
ms.assetid: b522f16d-8d61-4db3-9194-d965b6d859ec
title: Proporcionar eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc53daa602662dfabd163560e8e9d69a888be610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984478"
---
# <a name="providing-events"></a>Proporcionar eventos

Los proveedores son aplicaciones que contienen instrumentación de seguimiento de eventos. Después de que un proveedor se registra a sí mismo, un controlador puede habilitar o deshabilitar el seguimiento de eventos en el proveedor. El proveedor define su interpretación de que está habilitada o deshabilitada. Normalmente, un proveedor habilitado genera eventos y un proveedor deshabilitado no lo hace. Esto le permite agregar seguimiento de eventos a la aplicación sin necesidad de que genere eventos en todo momento.

Esta sección le muestra cómo:

-   [Escritura de eventos](writing-events.md)
-   [Escribir eventos relacionados](writing-related-events-in-an-end-to-end-scenario.md)
-   [Publicar el esquema de eventos para compartirlo con los consumidores](publishing-your-event-schema.md)

Para obtener información sobre cómo controlar las sesiones de seguimiento de eventos, vea [controlar las sesiones de seguimiento de eventos](controlling-event-tracing-sessions.md). Para obtener información sobre cómo consumir eventos de un proveedor de seguimiento de eventos, vea [consumir eventos](consuming-events.md).

 

 



