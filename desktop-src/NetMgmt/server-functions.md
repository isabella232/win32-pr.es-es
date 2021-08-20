---
title: Funciones del servidor (administración de redes)
description: Las funciones del servidor de administración de red realizan tareas administrativas en un servidor local o remoto. Las funciones de servidor se enumeran a continuación.
ms.assetid: 43e1285b-8c86-4af4-9834-fcd5ee8aceb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086abbd23682c17bb1bbfee6180067ca0947a848a4a8dfadb36ba1b87ef13c11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983139"
---
# <a name="server-functions-network-management"></a>Funciones del servidor (administración de redes)

Las funciones del servidor de administración de red realizan tareas administrativas en un servidor local o remoto. Las funciones de servidor se enumeran a continuación.



| Función                                       | Descripción                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**NetServerDiskEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Devuelve una lista de unidades de disco locales en un servidor.                                   |
| [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Enumera todos los servidores visibles de un tipo determinado (o tipos) en el dominio especificado. |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Devuelve información de configuración sobre un servidor especificado.                        |
| [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Establece los parámetros operativos de un servidor.                                        |



 

Solo un usuario o aplicación con pertenencia a grupos de administración en un servidor local o remoto puede realizar tareas administrativas en ese servidor para controlar el funcionamiento del servidor, el acceso de los usuarios y el uso compartido de recursos. Los parámetros de bajo nivel que afectan a la operación de un servidor se pueden examinar y modificar llamando a las funciones [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) y [**NetServerSetInfo.**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) Estos parámetros se definen en el archivo de LANMAN.INI servidor.

La mayoría de las funciones del servidor de administración de red solo se ejecutan en un servidor remoto. La [**función NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) se ejecuta en una estación de trabajo local o en un servidor remoto. Si intenta ejecutar otras funciones de servidor en una estación de trabajo local, las funciones devuelven el error NERR \_ RemoteOnly.

La información específica del servidor está disponible en los niveles siguientes:

-   [**SERVER \_ INFO \_ 100**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_100)
-   [**SERVER \_ INFO \_ 101**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_101)
-   [**SERVER \_ INFO \_ 102**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_102)
-   [**SERVER \_ INFO \_ 402**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_402)
-   [**SERVER \_ INFO \_ 403**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_403)
-   [**SERVER \_ INFO \_ 1501**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1501)
-   [**SERVER \_ INFO \_ 1502**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1502)
-   [**SERVER \_ INFO \_ 1503**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1503)
-   [**SERVER \_ INFO \_ 1506**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1506)
-   [**SERVER \_ INFO \_ 1509**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1509)
-   [**SERVER \_ INFO \_ 1510**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1510)
-   [**SERVER \_ INFO \_ 1511**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1511)
-   [**SERVER \_ INFO \_ 1512**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1512)
-   [**SERVER \_ INFO \_ 1513**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1513)
-   [**SERVER \_ INFO \_ 1515**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1515)
-   [**SERVER \_ INFO \_ 1516**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1516)
-   [**SERVER \_ INFO \_ 1518**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1518)
-   [**SERVER \_ INFO \_ 1523**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1523)
-   [**SERVER \_ INFO \_ 1528**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1528)
-   [**SERVER \_ INFO \_ 1529**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1529)
-   [**SERVER \_ INFO \_ 1530**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1530)
-   [**SERVER \_ INFO \_ 1533**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1533)
-   [**SERVER \_ INFO \_ 1536**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1536)
-   [**SERVER \_ INFO \_ 1538**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1538)
-   [**SERVER \_ INFO \_ 1539**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1539)
-   [**SERVER \_ INFO \_ 1540**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1540)
-   [**SERVER \_ INFO \_ 1541**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1541)
-   [**SERVER \_ INFO \_ 1542**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1542)
-   [**SERVER \_ INFO \_ 1544**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1544)
-   [**SERVER \_ INFO \_ 1550**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1550)
-   [**SERVER \_ INFO \_ 1552**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1552)

Si está programando para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz de servicio (ADSI) de Active Directory para lograr la misma funcionalidad que puede lograr llamando a las funciones del servidor de administración de redes. Para obtener más información, [**vea IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).

Para obtener más información, vea Funciones de transporte de [servidor y estación de trabajo](server-and-workstation-transport-functions.md).

 

 
