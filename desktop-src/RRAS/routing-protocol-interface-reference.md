---
title: Referencia de la interfaz de protocolo de enrutamiento
description: En esta documentación se describen las funciones y estructuras que se usan para implementar un protocolo de enrutamiento como un archivo DLL de modo usuario.
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- Servicio de enrutamiento y acceso remoto RRAS, interfaz de protocolo de enrutamiento, referencia
- Interfaz de protocolo de enrutamiento RRAS, referencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9341dd8dbd304da84fd675aee92e378a44271056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903450"
---
# <a name="routing-protocol-interface-reference"></a>Referencia de la interfaz de protocolo de enrutamiento

En esta documentación se describen las funciones y estructuras que se usan para implementar un protocolo de enrutamiento como un archivo DLL de modo usuario.

MPR50 debe definirse en el archivo make para el protocolo de enrutamiento.

La macro **sizeof \_ IP \_ Binding (x)** calcula el tamaño, en bytes, de una estructura de [**\_ información de \_ enlace \_ del adaptador de IP**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) que contiene el número de direcciones IP.

Estos elementos de referencia se describen en los temas siguientes:

-   [Funciones de interfaz de protocolo de enrutamiento](routing-protocol-interface-functions.md)
-   [Estructuras de interfaz de protocolo de enrutamiento](routing-protocol-interface-structures.md)
-   [Administración de tablas del servicio IPX](ipx-service-table-management.md)

 

 




