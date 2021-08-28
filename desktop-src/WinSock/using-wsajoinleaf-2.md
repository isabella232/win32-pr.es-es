---
description: Como se mencionó anteriormente, la función WSAJoinLeaf se usa para unir un nodo hoja a una sesión de varios puntos.
ms.assetid: eaa1593a-36eb-4d92-a3d9-91566fc0216b
title: Uso de WSAJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd13b6d82960f74135fa519a1284a1274b878e18c32f59d9c2b8c46ebd592c3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121025"
---
# <a name="using-wsajoinleaf"></a>Uso de WSAJoinLeaf

Como se mencionó anteriormente, la función [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) se usa para unir un nodo hoja a una sesión de varios puntos. **WSAJoinLeaf** tiene los mismos parámetros y semántica que [**WSAConnect,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) salvo que devuelve un descriptor de socket (como en [**WSAAccept)**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)y tiene un parámetro *dwFlags* adicional.

El *parámetro dwFlags* se usa para indicar si el socket actuará solo como remitente, solo como receptor o ambos. Solo se pueden usar sockets multipunto para los parámetros *de entrada de* esta función. Si el socket multipunto está en modo de no bloqueo, el descriptor de socket devuelto no se puede utiliza hasta después de que se reciba una indicación de FD \_ CONNECT correspondiente. Una aplicación raíz en una sesión multipunto puede llamar a [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) una o varias veces para agregar varios nodos hoja, pero como máximo una solicitud de conexión multipunto puede estar pendiente a la vez.

El descriptor de socket devuelto por [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) difiere en función de si el descriptor de socket de entrada, *s*, es una raíz c o \_ una hoja \_ c. Cuando se usa con un socket raíz de c, el parámetro name designa un nodo hoja determinado que se va a agregar y el descriptor de socket devuelto es un socket hoja de c correspondiente al nodo hoja recién \_  \_ agregado. No está pensado para usarse para el intercambio de datos de varios puntos, sino que se usa para recibir indicaciones XXX de FD (por ejemplo, FD CLOSE) para la conexión que existe con la hoja \_ \_ c \_ concreta. Algunas implementaciones de varios puntos también pueden permitir que este socket se utilice para los chats paralelos entre la raíz y un nodo hoja individual. Se recibe una indicación FD CLOSE para este socket si el nodo hoja correspondiente llama a \_ [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) para salir de la sesión de varios puntos. Simétricamente, la invocación de **closesocket** en el socket hoja c devuelto desde \_ **WSAJoinLeaf** hace que el socket del nodo hoja correspondiente obtenga una notificación FD \_ CLOSE.

Cuando se invoca [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) con un socket hoja c, el parámetro name contiene la dirección de la aplicación raíz (para un esquema de control raíz) o una sesión multipunto existente (esquema de control no raíz) y el descriptor de socket devuelto es el mismo que el descriptor de \_ socket de entrada.  En un esquema de control root, la aplicación raíz coloca su socket raíz c en modo de escucha \_ mediante una llamada a [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen). La notificación ESTÁNDAR DE FD ACCEPT se entrega cuando el nodo hoja solicita unirse \_ a la sesión multipunto. La aplicación raíz [](/windows/desktop/api/Winsock2/nf-winsock2-accept)usa las funciones / [**WSAAccept de aceptación habituales**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) para admitir el nuevo nodo hoja. El valor devuelto por **accept** o **WSAAccept** también es un descriptor de socket hoja c igual que los devueltos de \_ **WSAJoinLeaf.** Para dar cabida a esquemas de varios puntos que permiten combinaciones iniciadas por raíz y iniciadas por hoja, es aceptable que un socket raíz de c que ya está en modo de escucha se utilice como entrada para \_ **WSAJoinLeaf.**

Por lo general, una aplicación raíz de varios puntos es responsable de la ordenación de una sesión de varios puntos. Este tipo de aplicación puede usar [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) o [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) en un socket raíz c para hacer que todos los sockets hoja \_ c asociados, incluidos los devueltos de \_ [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) y sus sockets hoja c correspondientes en los nodos hoja remotos, obtengan una notificación \_ FD \_ CLOSE.

 

 



