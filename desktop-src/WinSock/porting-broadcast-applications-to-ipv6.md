---
description: En esta sección se describen los procedimientos recomendados para portar una aplicación de difusión IPv6 a las capacidades de multidifusión disponibles con Windows Sockets.
ms.assetid: 12e491fd-650f-43b4-afa1-9f37b1c30240
title: Trasladar aplicaciones de difusión a IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f7dce09db6822a6f9b0a61873ca6bbff5a256b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497441"
---
# <a name="porting-broadcast-applications-to-ipv6"></a>Trasladar aplicaciones de difusión a IPv6

En esta sección se describen los procedimientos recomendados para portar una aplicación de difusión IPv6 a las capacidades de multidifusión disponibles con Windows Sockets.

## <a name="comparing-ipv4-to-ipv6"></a>Comparar IPv4 con IPv6

La consideración más importante a la hora de preparar la migración de una aplicación de difusión IPv4 a IPv6 es la siguiente: IPv6 no tiene ningún concepto de difusión implementado. En su lugar, IPv6 utiliza multidifusión.

La multidifusión para IPv6 puede emular las capacidades de difusión tradicionales que se encuentran en IPv4. El establecimiento de la opción [IPv6 agregar socket de \_ \_ pertenencia](ipproto-ipv6-socket-options.md) con la dirección IPv6 establecida en el ámbito local del vínculo todos los nodos (FF02:: 1) es equivalente a la difusión en direcciones IPv4 de difusión mediante la opción de socket de [ \_ difusión](socket-options.md) . Esta dirección se denomina a veces *grupo de multidifusión todos los nodos*. En el caso de las aplicaciones que simplemente quieren emulación de difusión para IPv6, ese enfoque es operativo equivalente. Sin embargo, una diferencia importante con IPv6 es que las multidifusiones en la dirección del grupo de multidifusión de todos los nodos no se reciben de forma predeterminada (las difusiones IPv4 se reciben de forma predeterminada). Los programadores de aplicaciones deben usar \_ la \_ opción IPv6 agregar socket de pertenencia para habilitar la recepción de multidifusión desde cualquier origen, incluida la dirección del grupo de multidifusión todos los nodos.

> [!Note]  
> En IPv6, la selección de la interfaz se especifica en la estructura del argumento que se pasa a la opción de socket de multidifusión o IOCTL.

 

Pero para las transmisiones más enriquecidas, más sólidas, más selectivas y más fáciles de administrar a varios hosts, los desarrolladores de aplicaciones deben considerar la posibilidad de pasar a un modelo de multidifusión.

## <a name="moving-to-multicast"></a>Mover a multidifusión

Con la multidifusión, los programadores de aplicaciones pueden elegir selectivamente un par de origen y grupo determinado, habilitando un modelo de recepción selectivo. La detección del agente de escucha de multidifusión (MLD) en IPv6 y la versión 3 del Protocolo de administración de grupos de Internet (IGMPv3) en IPv4 admiten la programación multidifusión. Además, la multidifusión permite a las aplicaciones bloquear (o desbloquear) remitentes de forma específica dentro de un grupo, lo que protege aún más las aplicaciones de emisores no autorizados. Esta capacidad está disponible para IPv4 (requiere IGMPv3), así como IPv6 (requiere MLDv2).

Hay dos escenarios principales para los programadores de aplicaciones que usan multidifusión: los que se trasladan de las aplicaciones IPv4 de difusión (o multidifusión) a IPv6, y que crean nuevas aplicaciones IPv6 de multidifusión.

Para migrar las aplicaciones existentes, hay dos opciones para moverse a IPv6 multicast: usar las opciones de socket y usar ioctl.

-   El uso de las opciones de socket es un enfoque basado en el cambio que permite a los desarrolladores cambiar las propiedades del socket según sea necesario (por ejemplo, bloquear o desbloquear un remitente, agregar un nuevo origen, etc.). Este enfoque es más intuitivo y el enfoque recomendado. Para obtener más información sobre el enfoque basado en cambios para la programación de multidifusión, consulte [MLD y IGMP con Windows Sockets](igmp-and-windows-sockets.md).
-   El uso de ioctl es un enfoque basado en el estado final, ya que permite a los desarrolladores proporcionar un estado de socket totalmente configurado, incluidas listas de inclusión y exclusión, con una llamada. Para obtener más información sobre el enfoque basado en el estado final, vea [programación de multidifusión basada en el estado final](final-state-based-multicast-programming.md).

En el caso de los que crean nuevas aplicaciones de multidifusión IPv6, el procedimiento recomendado es usar las opciones de socket, en lugar de usar ioctl.

Hay otro enfoque para crear aplicaciones de multidifusión con IPv6 y que conlleva el uso de la función [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) . Aunque no se recomienda usar la función **WSAJoinLeaf** , hay situaciones que pueden dictar su uso. Por ejemplo, un inconveniente de usar las opciones de socket en Windows Server 2003 y versiones anteriores es que son específicas de la versión de IP. En estas versiones anteriores de Windows, las distintas opciones de sockets deben ser para IPv6 e IPv4. En Windows Vista y versiones posteriores, se admiten las nuevas opciones de socket que se pueden usar con IPv4 e IPv6. Por el contrario, la función **WSAJoinLeaf** es independiente del protocolo y la versión de IP y, por lo tanto, puede ser un enfoque útil para crear una aplicación que deba trabajar con varias versiones IP en Windows Server 2003 y versiones anteriores. El uso de la función **WSAJoinLeaf** puede ser más adecuado en algunas situaciones en las que se requiere el protocolo y el agnóstico de la versión de IP.

 

 



