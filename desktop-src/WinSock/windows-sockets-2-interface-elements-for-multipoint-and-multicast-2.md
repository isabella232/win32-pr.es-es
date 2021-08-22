---
description: Windows Sockets 2 (Winsock) elementos de interfaz para multipunto y multidifusión.
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: Windows Sockets 2 Elementos de interfaz para multipunto y multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf2422d8171a041f75ba8abed6ea490982187af3affb3d3c3d1349984210ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558857"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a>Windows Sockets 2 Elementos de interfaz para multipunto y multidifusión

Los mecanismos que se han incorporado a Windows Sockets 2 para usar funcionalidades multipunto se pueden resumir de la siguiente manera:

-   Tres bits de atributo en la [**estructura INFO de WSAPROTOCOL. \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
-   Cuatro marcas definidas para el *parámetro dwFlags* [**de WSASocket.**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
-   Una función, [**WSAJoinLeaf,**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)para agregar nodos hoja a una sesión de varios puntos.
-   Dos [**códigos de comando WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para controlar el bucle de retorno de varios puntos y el ámbito de las transmisiones de multidifusión.

En las secciones siguientes se describen estos elementos de interfaz con más detalle:

-   [Semántica para unir hojas de varios puntos](semantics-for-joining-multipoint-leaves-2.md)
-   [Compatibilidad de los protocolos multipunto existentes con estas extensiones](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
