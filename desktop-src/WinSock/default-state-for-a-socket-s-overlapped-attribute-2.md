---
description: La función de socket creó sockets con el atributo superpuesto establecido de forma predeterminada en el primer Wsock32.dll, la versión de 32 bits de Windows Sockets 1.1.
ms.assetid: 2ebf71fd-fcb3-4f2f-bf52-14cd13af012f
title: Estado predeterminado para el atributo superpuesto de un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae64f5ba1481c62faf0798fa45aafdd98dde0696dfde68f79132d533ec3abce0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860935"
---
# <a name="default-state-for-a-sockets-overlapped-attribute"></a>Estado predeterminado para el atributo superpuesto de un socket

La [**función de socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) creó sockets con el atributo superpuesto establecido de forma predeterminada en el primer Wsock32.dll, la versión de 32 bits de Windows Sockets 1.1. Para garantizar la compatibilidad con versiones anteriores con las implementaciones Wsock32.dll implementadas actualmente, esto seguirá siendo así para Windows Sockets 2. Es decir, en Windows sockets 2 creados con la función **de socket** tendrán el atributo superpuesto. Sin embargo, para ser más compatibles con el resto de la API de Windows, los sockets creados con [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) no tendrán, de forma predeterminada, el atributo superpuesto. Este atributo solo se aplicará si se establece el bit OVERLAPPED de WSA \_ \_ FLAG.

 

 



