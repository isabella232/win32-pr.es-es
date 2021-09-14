---
description: Normalmente, los proveedores wmi están diseñados para proporcionar información sobre un objeto administrado específico en un único equipo.
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: Vincular clases juntas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c36956d20d9390462577332e7ac7b644d4ffc7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967168"
---
# <a name="linking-classes-together"></a>Vincular clases juntas

Normalmente, los proveedores wmi están diseñados para proporcionar información sobre un objeto administrado específico en un único equipo. Si hay una propiedad común que puede actuar como clave para identificar de [](view-provider.md) forma única todas las instancias de origen diferentes, use el proveedor de vistas para combinar propiedades de diferentes clases, espacios de nombres o equipos en una sola clase.

Primero debe registrar [el proveedor de vistas](registering-the-view-provider.md). Después del registro, puede crear los siguientes tipos de clases de vista:

-   [Vista de combinación](creating-a-new-instance-from-old-properties.md)

    Instancias de diferentes clases conectadas por un valor de propiedad común.

-   [Vista asociación](associating-instances-between-namespaces.md)

    Vistas de clases de asociación existentes en el límite del espacio de nombres.

-   [Vista Unión](creating-a-union-view-class.md)

    Unión de una o varias instancias.

 

 



