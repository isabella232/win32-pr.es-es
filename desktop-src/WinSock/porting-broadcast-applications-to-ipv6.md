---
description: En esta sección se describen los procedimientos recomendados para portear una aplicación de difusión IPv6 a las funcionalidades de multidifusión disponibles Windows Sockets.
ms.assetid: 12e491fd-650f-43b4-afa1-9f37b1c30240
title: Porte de aplicaciones de difusión a IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb54fec87be2aa6174de603d2c3e4d0e640156902002b1e87fab149a70e3d1ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641707"
---
# <a name="porting-broadcast-applications-to-ipv6"></a>Porte de aplicaciones de difusión a IPv6

En esta sección se describen los procedimientos recomendados para portear una aplicación de difusión IPv6 a las funcionalidades de multidifusión disponibles Windows Sockets.

## <a name="comparing-ipv4-to-ipv6"></a>Comparación de IPv4 con IPv6

La consideración más importante al preparar la portabilidad de una aplicación de difusión IPv4 a IPv6 es esta: IPv6 no tiene ningún concepto implementado de difusión. En su lugar, IPv6 usa multidifusión.

La multidifusión para IPv6 puede emular las funcionalidades de difusión tradicionales que se encuentran en IPv4. Establecer la opción de socket [ \_ ADD \_ MEMBERSHIP de IPV6](ipproto-ipv6-socket-options.md) con la dirección IPv6 establecida en el ámbito local del vínculo, la dirección de todos los nodos (FF02::1) equivale a la difusión en direcciones de difusión IPv4 mediante la opción de socket [SO \_ BROADCAST.](socket-options.md) A veces, esta dirección se denomina *grupo de multidifusión de todos los nodos.* Para las aplicaciones que simplemente desean emulación de difusión para IPv6, ese enfoque es operativamente equivalente. Sin embargo, una diferencia importante con IPv6 es que las multidifusión en la dirección del grupo de multidifusión de todos los nodos no se reciben de forma predeterminada (las difusiones IPv4 se reciben de forma predeterminada). Los programadores de aplicaciones deben usar la opción de socket ADD MEMBERSHIP de IPV6 para habilitar la recepción de multidifusión desde cualquier origen, incluida la dirección del grupo de multidifusión de todos los \_ \_ nodos.

> [!Note]  
> En IPv6, la selección de interfaz se especifica en la estructura de argumentos que se pasa a la opción de socket de multidifusión o IOCTL.

 

Pero para transmisiones más enriquecibles, más sólidas, más selectivas y más fáciles de administrar a varios hosts, los desarrolladores de aplicaciones deben considerar la posibilidad de pasar a un modelo de multidifusión.

## <a name="moving-to-multicast"></a>Pasar a multidifusión

Con la multidifusión, los programadores de aplicaciones pueden elegir de forma selectiva un par de origen o grupo determinado, lo que permite un modelo de recepción selectiva. La detección de agentes de escucha de multidifusión (MLD) en IPv6 y la versión 3 del Protocolo de administración de grupos de Internet (IGMPv3) en IPv4 admiten la programación de multidifusión. Además, la multidifusión permite que las aplicaciones bloqueen (o desbloqueen) específicamente los remitentes dentro de un grupo, lo que protege aún más las aplicaciones de emisores no deseados. Esta funcionalidad está disponible para IPv4 (requiere IGMPv3), así como para IPv6 (requiere MLDv2).

Hay dos escenarios principales para los programadores de aplicaciones que usan multidifusión: los que se transmiten desde aplicaciones de difusión (o multidifusión) IPv4 a IPv6 y los que crean nuevas aplicaciones de multidifusión IPv6.

Para portear aplicaciones existentes, hay dos opciones para pasar a multidifusión IPv6: usar opciones de socket y usar IOCTL.

-   El uso de opciones de socket es un enfoque basado en cambios, que permite a los desarrolladores cambiar las propiedades del socket según sea necesario (por ejemplo, bloquear o desbloquear un remitente, agregar un nuevo origen, y así sucesivamente). Este enfoque es más intuitivo y el enfoque recomendado. Para obtener más información sobre el enfoque basado en cambios para la programación de multidifusión, vea [MLD y IGMP Using Windows Sockets](igmp-and-windows-sockets.md).
-   El uso de IOCTLs es un enfoque basado en el estado final, ya que permite a los desarrolladores proporcionar un estado de socket totalmente configurado, incluidas las listas de inclusión y exclusión, con una llamada. Para obtener más información sobre el enfoque basado en el estado final, vea [Programación de multidifusión basada en estado final](final-state-based-multicast-programming.md).

Para aquellos que crean nuevas aplicaciones de multidifusión IPv6, la práctica recomendada es usar opciones de socket, en lugar de usar IOCTL.

Hay otro enfoque para crear aplicaciones de multidifusión con IPv6, lo que implica el uso de la [**función WSAJoinLeaf.**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) Aunque el uso de la función **WSAJoinLeaf** no es la práctica recomendada, hay situaciones que pueden dictar su uso. Por ejemplo, un inconveniente de usar las opciones de socket en Windows Server 2003 y versiones anteriores es que son específicas de la versión ip. En estas versiones anteriores de Windows, las distintas opciones de sockets deben ser para IPv6 e IPv4. En Windows Vista y versiones posteriores, se admiten nuevas opciones de socket que se pueden usar con IPv4 e IPv6. Por el contrario, la función **WSAJoinLeaf** es independiente de la versión de IP y el protocolo y, por lo tanto, puede ser un enfoque útil para compilar una aplicación que debe funcionar con varias versiones IP en Windows Server 2003 y versiones anteriores. El uso de la función **WSAJoinLeaf** puede ser más adecuado en determinadas situaciones en las que se requiere el protocolo y el agnóstico de la versión IP.

 

 



