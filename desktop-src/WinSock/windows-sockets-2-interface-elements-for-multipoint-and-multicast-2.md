---
description: Elementos de la interfaz de Windows Sockets 2 (Winsock) para multipoint y multidifusión.
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: Elementos de la interfaz de Windows Sockets 2 para multipoint y multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86905fe19c5c4c603db488874039b7cc8a0b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715473"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a>Elementos de la interfaz de Windows Sockets 2 para multipoint y multidifusión

Los mecanismos que se han incorporado a Windows Sockets 2 para usar las capacidades de Multipoint se pueden resumir de la manera siguiente:

-   Tres bits de atributo en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .
-   Cuatro marcas definidas para el parámetro *dwFlags* de [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).
-   Una función, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), para agregar nodos hoja en una sesión multipoint.
-   Dos códigos de comando [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para controlar el bucle invertido multipoint y el ámbito de las transmisiones de multidifusión.

En las secciones siguientes se describen estos elementos de interfaz con más detalle:

-   [Semántica para combinar hojas de Multipoint](semantics-for-joining-multipoint-leaves-2.md)
-   [Cómo los protocolos Multipoint existentes admiten estas extensiones](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
