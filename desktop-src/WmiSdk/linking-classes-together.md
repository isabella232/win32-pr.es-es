---
description: Los proveedores de WMI normalmente están diseñados para proporcionar información sobre un objeto administrado específico en un único equipo.
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: Vincular clases juntas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c36956d20d9390462577332e7ac7b644d4ffc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697644"
---
# <a name="linking-classes-together"></a>Vincular clases juntas

Los proveedores de WMI normalmente están diseñados para proporcionar información sobre un objeto administrado específico en un único equipo. Si hay una propiedad común que puede actuar como una clave para identificar de forma exclusiva todas las instancias de origen diferentes, use el [proveedor de vistas](view-provider.md) para combinar propiedades de diferentes clases, espacios de nombres o equipos en una sola clase.

Primero debe [registrar el proveedor de vistas](registering-the-view-provider.md). Después del registro, puede crear los siguientes tipos de clases de vista:

-   [Vista de combinación](creating-a-new-instance-from-old-properties.md)

    Instancias de clases diferentes conectadas por un valor de propiedad común.

-   [Vista de asociación](associating-instances-between-namespaces.md)

    Vistas de clases de asociación existentes en el límite del espacio de nombres.

-   [Vista Unión](creating-a-union-view-class.md)

    Unión de una o más instancias.

 

 



