---
description: Atributos de socket multipunto en Windows sockets (Winsock).
ms.assetid: f6e779c6-dd9d-470e-aad9-715b69ad8c5f
title: Atributos de socket multipunto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992f574420743ec8e6a339fe14a29accb68beff2c416de0dde19c0fafc707acb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858155"
---
# <a name="multipoint-socket-attributes"></a>Atributos de socket multipunto

En algunos casos, los sockets unidos a una sesión multipunto pueden tener algunas diferencias de comportamiento con respecto a los sockets de punto a punto. Por ejemplo, un socket de hoja d en un esquema de plano de datos raíz solo puede \_ enviar información al participante raíz \_ d. Esto crea una necesidad de que el cliente pueda indicar el uso previsto de un socket coincidente con su creación. Esto se hace a través de cuatro marcas de atributos multipunto que se pueden establecer a través del *parámetro dwFlags* en [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket):

-   WSA FLAG MULTIPOINT C ROOT, para la creación de un socket que actúa como raíz c y solo se permite si se indica un plano de control raíz en la entrada INFO de \_ \_ \_ \_ \_ [**WSAPROTOCOL correspondiente. \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
-   WSA FLAG MULTIPOINT C LEAF, para la creación de un socket que actúa como hoja c y solo se permite si XP1 SUPPORT MULTIPOINT se indica en la entrada INFO de \_ \_ \_ \_ \_ \_ \_ [**\_ WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente.
-   WSA FLAG MULTIPOINT D ROOT, para la creación de un socket que actúa como raíz d y solo se permite si se indica un plano de datos raíz en la entrada INFO de \_ \_ \_ \_ \_ [**WSAPROTOCOL correspondiente. \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
-   WSA FLAG MULTIPOINT D LEAF, para la creación de un socket que actúa como hoja d y solo se permite si XP1 SUPPORT MULTIPOINT se indica en la entrada INFO de \_ \_ \_ \_ \_ \_ \_ [**WSAPROTOCOL \_ correspondiente.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)

Al crear un socket multipunto, debe establecerse exactamente una de las dos marcas del plano de control y una de las dos marcas del plano de datos en el parámetro *dwFlags* de [**WSPSocket.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) Por lo tanto, las cuatro posibilidades para crear sockets multipunto son: "c \_ root/d \_ root", "c \_ root/d \_ leaf", "c \_ leaf/d root" o \_ "c \_ leaf /d \_ leaf".

 

 
