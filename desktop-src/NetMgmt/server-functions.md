---
title: Funciones de servidor (administración de red)
description: Las funciones de servidor de administración de red realizan tareas administrativas en un servidor local o remoto. A continuación se enumeran las funciones de servidor.
ms.assetid: 43e1285b-8c86-4af4-9834-fcd5ee8aceb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43758fa822ce60d484418431941a386681bb77d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078772"
---
# <a name="server-functions-network-management"></a>Funciones de servidor (administración de red)

Las funciones de servidor de administración de red realizan tareas administrativas en un servidor local o remoto. A continuación se enumeran las funciones de servidor.



| Función                                       | Descripción                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**NetServerDiskEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Devuelve una lista de unidades de disco locales en un servidor.                                   |
| [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Enumera todos los servidores visibles de un tipo (o tipos) determinado en el dominio especificado. |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Devuelve información de configuración sobre un servidor especificado.                        |
| [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Establece los parámetros operativos para un servidor.                                        |



 

Solo un usuario o una aplicación con pertenencia a un grupo de administración en un servidor local o remoto puede realizar tareas administrativas en ese servidor para controlar el funcionamiento del servidor, el acceso de los usuarios y el uso compartido de recursos. Los parámetros de nivel inferior que afectan a la operación de un servidor se pueden examinar y modificar llamando a las funciones [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) y [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) . Estos parámetros se definen en el archivo de LANMAN.INI del servidor.

La mayoría de las funciones de servidor de administración de red solo se ejecutan en un servidor remoto. La función [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) se ejecuta en una estación de trabajo local o en un servidor remoto. Si intenta ejecutar otras funciones de servidor en una estación de trabajo local, las funciones devuelven el error NERR \_ RemoteOnly.

La información específica del servidor está disponible en los siguientes niveles:

-   [**Información del servidor \_ \_ 100**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_100)
-   [**Información del servidor \_ \_ 101**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_101)
-   [**Información del servidor \_ \_ 102**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_102)
-   [**Información del servidor \_ \_ 402**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_402)
-   [**Información del servidor \_ \_ 403**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_403)
-   [**Información del servidor \_ \_ 1501**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1501)
-   [**Información del servidor \_ \_ 1502**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1502)
-   [**Información del servidor \_ \_ 1503**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1503)
-   [**Información del servidor \_ \_ 1506**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1506)
-   [**Información del servidor \_ \_ 1509**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1509)
-   [**Información del servidor \_ \_ 1510**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1510)
-   [**Información del servidor \_ \_ 1511**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1511)
-   [**Información del servidor \_ \_ 1512**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1512)
-   [**Información del servidor \_ \_ 1513**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1513)
-   [**Información del servidor \_ \_ 1515**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1515)
-   [**Información del servidor \_ \_ 1516**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1516)
-   [**Información del servidor \_ \_ 1518**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1518)
-   [**Información del servidor \_ \_ 1523**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1523)
-   [**Información del servidor \_ \_ 1528**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1528)
-   [**Información del servidor \_ \_ 1529**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1529)
-   [**Información del servidor \_ \_ 1530**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1530)
-   [**Información del servidor \_ \_ 1533**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1533)
-   [**Información del servidor \_ \_ 1536**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1536)
-   [**Información del servidor \_ \_ 1538**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1538)
-   [**Información del servidor \_ \_ 1539**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1539)
-   [**Información del servidor \_ \_ 1540**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1540)
-   [**Información del servidor \_ \_ 1541**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1541)
-   [**Información del servidor \_ \_ 1542**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1542)
-   [**Información del servidor \_ \_ 1544**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1544)
-   [**Información del servidor \_ \_ 1550**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1550)
-   [**Información del servidor \_ \_ 1552**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1552)

Si programa para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz de servicio Active Directory (ADSI) para lograr la misma funcionalidad que puede lograr mediante una llamada a las funciones de servidor de administración de red. Para obtener más información, vea [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).

Para obtener más información, consulte las [funciones de transporte de servidor y estación de trabajo](server-and-workstation-transport-functions.md).

 

 
