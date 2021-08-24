---
description: En algunos casos, los sockets unidos a una sesión de varios puntos pueden tener algunas diferencias en el comportamiento de los sockets de punto a punto.
ms.assetid: e59b701f-f85f-4fd6-8d6d-e46199250c22
title: Bits de marca para WSASocket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd1bbe8a282fe0255e3efd9889216b7d44aee2a41feedb611ba5c2b1d38bae68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132478"
---
# <a name="flag-bits-for-wsasocket"></a>Bits de marca para WSASocket

En algunos casos, los sockets unidos a una sesión de varios puntos pueden tener algunas diferencias en el comportamiento de los sockets de punto a punto. Por ejemplo, un socket de hoja d en un esquema de plano de datos con raíz solo puede enviar \_ información al participante raíz \_ d. Esto crea la necesidad de que la aplicación pueda indicar el uso previsto de un socket coincidente con su creación. Esto se realiza a través de bits de cuatro marcas que se pueden establecer en el *parámetro dwFlags* en [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa):

-   WSA FLAG MULTIPOINT C ROOT, para la creación de un socket que actúa como raíz c y solo se permite si se indica un plano de control con raíz en la entrada INFO de \_ \_ \_ \_ \_ [**WSAPROTOCOL correspondiente. \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
-   WSA FLAG MULTIPOINT C LEAF, para la creación de un socket que actúa como hoja c y solo se permite si XP1 SUPPORT MULTIPOINT se indica en la entrada INFO de \_ \_ \_ \_ \_ \_ \_ [**WSAPROTOCOL \_ correspondiente.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
-   WSA FLAG MULTIPOINT D ROOT, para la creación de un socket que actúa como raíz d y solo se permite si se indica un plano de datos con raíz en la entrada INFO de \_ \_ \_ \_ \_ [**WSAPROTOCOL correspondiente. \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
-   WSA FLAG MULTIPOINT D LEAF, para la creación de un socket que actúa como hoja d y solo se permite si XP1 SUPPORT MULTIPOINT se indica en la entrada INFO de \_ \_ \_ \_ \_ \_ \_ [**WSAPROTOCOL \_ correspondiente.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)

Tenga en cuenta que al crear un socket multipunto, debe establecerse exactamente una de las dos marcas del plano de control y una de las dos marcas del plano de datos en el parámetro *dwFlags* de [**WSASocket.**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) Por lo tanto, las cuatro posibilidades para crear sockets multipunto son:

-   "c \_ root/d \_ root"
-   "c \_ root/d \_ leaf"
-   "c \_ leaf/d \_ root"
-   "c \_ leaf /d \_ leaf"

 

 
