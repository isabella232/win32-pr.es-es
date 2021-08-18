---
title: Referencia de la interfaz del protocolo de enrutamiento
description: En esta documentación se describen las funciones y estructuras que se usan para implementar un protocolo de enrutamiento como un archivo DLL en modo de usuario.
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- RRAS del servicio de enrutamiento y acceso remoto, interfaz de protocolo de enrutamiento, referencia
- RRAS de la interfaz de protocolo de enrutamiento , referencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0196a5cbad8919a07a6e9a19ee5f7848eb6378ad2c56f7f0977125e5e79133a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027355"
---
# <a name="routing-protocol-interface-reference"></a>Referencia de la interfaz del protocolo de enrutamiento

En esta documentación se describen las funciones y estructuras que se usan para implementar un protocolo de enrutamiento como un archivo DLL en modo de usuario.

MPR50 debe definirse en el archivo make para el protocolo de enrutamiento.

La **macro SIZEOF \_ IP \_ BINDING(x)** calcula el tamaño, en bytes, de una estructura DE INFORMACIÓN DE ENLACE DEL ADAPTADOR DE IP que contiene el número de direcciones IP. [**\_ \_ \_**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info)

Estos elementos de referencia se describen en los temas siguientes:

-   [Funciones de interfaz del protocolo de enrutamiento](routing-protocol-interface-functions.md)
-   [Estructuras de interfaz del protocolo de enrutamiento](routing-protocol-interface-structures.md)
-   [Administración de tablas de servicio IPX](ipx-service-table-management.md)

 

 




