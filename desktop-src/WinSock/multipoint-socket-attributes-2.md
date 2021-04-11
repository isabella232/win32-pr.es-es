---
description: Atributos de Multipoint socket en Windows Sockets (Winsock).
ms.assetid: f6e779c6-dd9d-470e-aad9-715b69ad8c5f
title: Atributos de Multipoint socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da67fd40c7c3bc7f1e9dbff22a3fef6cdaee4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275394"
---
# <a name="multipoint-socket-attributes"></a>Atributos de Multipoint socket

En algunos casos, los sockets Unidos a una sesión de Multipoint pueden tener algunas diferencias de comportamiento con los sockets de punto a punto. Por ejemplo, un \_ socket de hoja d en un esquema de plano de datos raíz solo puede enviar información al \_ participante raíz d. Esto crea una necesidad de que el cliente pueda indicar el uso previsto de un coincidente de socket con su creación. Esto se hace a través de cuatro marcas de atributo multipunto que se pueden establecer a través del parámetro *dwFlags* en [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket):

-   WSA \_ marca \_ \_ \_ la raíz de Multipoint c, para la creación de un socket que actúa como una raíz de c \_ y solo se permite si un plano de control con raíz se indica en la entrada de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente.
-   WSA \_ marca \_ la hoja Multipoint- \_ c \_ , para la creación de un socket que actúa como hoja de c \_ y solo se permite si XP1 \_ admite \_ Multipoint en la entrada de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente.
-   WSA \_ marca \_ \_ \_ la raíz de Multipoint d, para la creación de un socket que actúa como \_ raíz d y solo se permite si un plano de datos raíz se indica en la entrada de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente.
-   WSA \_ marca \_ \_ \_ la hoja multipunto d, para la creación de un socket que actúa como \_ hoja d y solo se permite si XP1 \_ admite \_ Multipoint en la entrada [**de \_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente.

Al crear un Multipoint socket, exactamente una de las dos marcas de plano de control, y una de las dos marcas de plano de datos debe establecerse en el parámetro *dwFlags* de [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). Por lo tanto, las cuatro posibilidades para crear Multipoint Sockets son: "c raíz \_ /d \_ raíz", "c \_ raíz/d \_ hoja", "c \_ hoja/d \_ raíz" o "c \_ hoja/d \_ hoja".

 

 
