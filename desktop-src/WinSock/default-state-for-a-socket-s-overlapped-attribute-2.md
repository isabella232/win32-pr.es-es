---
description: La función de socket creó sockets con el atributo OVERLAPPED establecido de forma predeterminada en la primera Wsock32.dll, la versión de 32 bits de Windows Sockets 1,1.
ms.assetid: 2ebf71fd-fcb3-4f2f-bf52-14cd13af012f
title: Estado predeterminado para el atributo superpuesto de un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bc46fbf08731b0f73d841291f6815b43d02785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154289"
---
# <a name="default-state-for-a-sockets-overlapped-attribute"></a>Estado predeterminado para el atributo superpuesto de un socket

La función de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) creó sockets con el atributo OVERLAPPED establecido de forma predeterminada en la primera Wsock32.dll, la versión de 32 bits de Windows sockets 1,1. Con el fin de garantizar la compatibilidad con las implementaciones de Wsock32.dll implementadas actualmente, esto seguirá siendo también el caso de Windows Sockets 2. Es decir, en sockets de Windows Sockets 2 creados con la función **socket** tendrá el atributo OVERLAPPED. Sin embargo, para que sea más compatible con el resto de la API de Windows, los sockets creados con [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) no tendrán, de forma predeterminada, el atributo superpuesto. Este atributo solo se aplicará si \_ \_ se establece el bit superpuesto de la etiqueta WSA.

 

 



