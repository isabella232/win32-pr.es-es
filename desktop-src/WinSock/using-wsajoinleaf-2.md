---
description: Como se mencionó anteriormente, la función WSAJoinLeaf se usa para unir un nodo hoja a una sesión multipoint.
ms.assetid: eaa1593a-36eb-4d92-a3d9-91566fc0216b
title: Usar WSAJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 027262a117edc5541a4809481aa4607837343b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910298"
---
# <a name="using-wsajoinleaf"></a>Usar WSAJoinLeaf

Como se mencionó anteriormente, la función [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) se usa para unir un nodo hoja a una sesión multipoint. **WSAJoinLeaf** tiene los mismos parámetros y semántica que [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) , salvo que devuelve un descriptor de socket (como en [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)) y tiene un parámetro *dwFlags* adicional.

El parámetro *dwFlags* se usa para indicar si el socket actuará solo como remitente, solo como receptor o ambos. Solo se pueden usar Multipoint Sockets para los *parámetros de* entrada de esta función. Si el socket Multipoint está en modo de no bloqueo, el descriptor de socket devuelto no se puede usar hasta que \_ se reciba la indicación FD Connect correspondiente. Una aplicación raíz en una sesión Multipoint puede llamar a [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) una o más veces para agregar un número de nodos hoja; sin embargo, puede que al menos una solicitud de conexión multipunto esté pendiente a la vez.

El descriptor de socket devuelto por [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) varía en función de si el descriptor de *socket de entrada* es una raíz de c \_ o una hoja de c \_ . Cuando se usa con un \_ socket raíz de c, el parámetro de *nombre* designa un nodo de hoja determinado que se va a agregar y el descriptor de socket devuelto es un \_ socket hoja de c que corresponde al nodo hoja recién agregado. No está diseñado para el intercambio de datos multipunto, sino que se usa para recibir las \_ indicaciones FD xxx (por ejemplo, \_ el cierre FD) para la conexión que existe en la hoja de c determinada \_ . Algunas implementaciones de Multipoint también pueden permitir el uso de este socket para chats laterales entre la raíz y un nodo hoja individual. \_Se recibe una indicación FD de cierre para este socket si el nodo hoja correspondiente llama a [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) para quitarlo de la sesión de multipoint. Simétricamente, al invocar **closesocket** en el \_ socket hoja de c devuelto desde **WSAJoinLeaf** , el socket del nodo hoja correspondiente obtiene una \_ notificación FD Close.

Cuando [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) se invoca con un socket de \_ hoja de c, el parámetro *Name* contiene la dirección de la aplicación raíz (para un esquema de control con raíz) o una sesión de Multipoint existente (esquema de control sin raíz) y el descriptor de sockets devuelto es el mismo que el descriptor de socket de entrada. En un esquema de control con raíz, la aplicación raíz coloca su \_ socket raíz de c en modo de escucha mediante una llamada a [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen). La notificación de aceptación de FD estándar \_ se entrega cuando el nodo hoja solicita unirse a la sesión de multipoint. La aplicación raíz usa las funciones de [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) / [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) habituales para admitir el nuevo nodo hoja. El valor devuelto de **Accept** o **WSAAccept** es también un \_ descriptor de socket de hoja de c como el devuelto por **WSAJoinLeaf**. Para dar cabida a esquemas Multipoint que permitan combinaciones iniciadas por raíz y iniciadas por hojas, es aceptable que un \_ socket raíz de c que ya esté en modo de escucha se use como entrada para **WSAJoinLeaf**.

Una aplicación de Multipoint root es generalmente responsable del desmontaje ordenado de una sesión de multipoint. Este tipo de aplicación puede usar [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) o [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) en un \_ socket raíz de c para producir todos los sockets de hoja de c asociados \_ , incluidos los devueltos de [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) y sus sockets de hoja de c correspondientes \_ en los nodos de hoja remotos, para obtener la \_ notificación FD Close.

 

 



