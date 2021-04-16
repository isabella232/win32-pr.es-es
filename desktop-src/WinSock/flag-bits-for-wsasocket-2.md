---
description: En algunos casos, los sockets Unidos a una sesión de Multipoint pueden tener algunas diferencias de comportamiento con los sockets de punto a punto.
ms.assetid: e59b701f-f85f-4fd6-8d6d-e46199250c22
title: Marcar bits para WSASocket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51fede5d160d89b08064d8dff1c1a901c048526f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705623"
---
# <a name="flag-bits-for-wsasocket"></a>Marcar bits para WSASocket

En algunos casos, los sockets Unidos a una sesión de Multipoint pueden tener algunas diferencias de comportamiento con los sockets de punto a punto. Por ejemplo, un \_ socket de hoja d en un esquema de plano de datos raíz solo puede enviar información al \_ participante raíz d. Esto crea una necesidad de que la aplicación pueda indicar el uso previsto de un coincidente de socket con su creación. Esto se hace a través de los cuatro bits de marca que se pueden establecer en el parámetro *dwFlags* en [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa):

-   WSA \_ marca \_ \_ \_ la raíz de Multipoint c, para la creación de un socket que actúa como una raíz de c \_ y solo se permite si un plano de control con raíz se indica en la entrada de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente.
-   WSA \_ marca \_ la hoja Multipoint- \_ c \_ , para la creación de un socket que actúa como hoja de c \_ y solo se permite si XP1 \_ admite \_ Multipoint en la entrada de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente.
-   WSA \_ marca \_ \_ \_ la raíz de Multipoint d, para la creación de un socket que actúa como \_ raíz d y solo se permite si un plano de datos raíz se indica en la entrada de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente.
-   WSA \_ marca \_ \_ \_ la hoja multipunto d, para la creación de un socket que actúa como \_ hoja d y solo se permite si XP1 \_ admite \_ Multipoint en la entrada [**de \_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente.

Tenga en cuenta que al crear un Multipoint socket, exactamente una de las dos marcas de plano de control y una de las dos marcas de plano de datos debe establecerse en el parámetro *dwFlags* de [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa). Por lo tanto, las cuatro posibilidades para crear Multipoint Sockets son:

-   " \_ raíz raíz/d de c \_ "
-   " \_ hoja raíz/d de c \_ "
-   "raíz de c \_ /d \_ "
-   " \_ hoja c/d \_ hoja"

 

 
