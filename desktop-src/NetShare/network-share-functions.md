---
description: Las funciones de recurso compartido de red controlan los recursos compartidos. Un recurso compartido es un recurso local en un servidor (por ejemplo, un directorio de disco, un dispositivo de impresión o una canalización con nombre) al que pueden acceder los usuarios y las aplicaciones de la red.
ms.assetid: 14886bb0-e597-4728-a64f-bc16e82874da
title: Funciones de recurso compartido de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 640dc877c9b482cb8ebdcef0d36e6dff562fcd8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074064"
---
# <a name="network-share-functions"></a>Funciones de recurso compartido de red

Las funciones de recurso compartido de red controlan los recursos compartidos. Un recurso compartido es un recurso local en un servidor (por ejemplo, un directorio de disco, un dispositivo de impresión o una canalización con nombre) al que pueden acceder los usuarios y las aplicaciones de la red.

Las funciones de recurso compartido se enumeran a continuación.



| Función                                   | Descripción                                                          |
|--------------------------------------------|----------------------------------------------------------------------|
| [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd)         | Comparte un recurso en un servidor.                                       |
| [**NetShareCheck**](/windows/desktop/api/Lmshare/nf-lmshare-netsharecheck)     | Consulta si un servidor comparte un dispositivo.                        |
| [**NetShareDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsharedel)         | Elimina un nombre de recurso compartido de la lista de recursos compartidos de un servidor.       |
| [**NetShareEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netshareenum)       | Recupera información de recursos compartidos sobre cada recurso compartido en un servidor.  |
| [**NetShareGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharegetinfo) | Recupera información sobre un recurso compartido especificado en un servidor. |
| [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo) | Establece los parámetros de un recurso compartido.                                 |



 

La [**función NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) permite que un usuario o una aplicación compartan un recurso de un tipo específico con el nombre de recurso compartido especificado. La **función NetShareAdd** requiere el nombre del recurso compartido y el nombre del dispositivo local para compartir el recurso. Un usuario o aplicación debe tener una cuenta en el servidor para acceder al recurso.

También puede especificar un descriptor de seguridad que se va a asociar a un recurso compartido. Los descriptores de seguridad especifican qué usuarios pueden acceder a los archivos a través del recurso compartido y con qué tipo de acceso. Especifique un [**\_ DESCRIPTOR DE SEGURIDAD con**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) el nivel de información SHARE INFO [**\_ \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502) al llamar a [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) o [**NetShareSetInfo.**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo) **NetShareSetInfo admite** el nivel [**de información SHARE INFO \_ \_ 1501.**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) Para obtener más información sobre los descriptores de seguridad, [vea Access Control](/windows/desktop/SecAuthZ/access-control).

Las funciones de administración de red usan los siguientes nombres de recursos compartidos especiales para la comunicación entre procesos (IPC) y la administración remota del servidor:

-   IPC$, reservado para la comunicación entre procesos
-   ADMIN$, reservado para la administración remota
-   A$, B$, C$ (y otros nombres de disco local seguidos de un signo de dólar), asignados a dispositivos de disco local

Para enumerar todas las conexiones realizadas a un recurso compartido en un servidor o para enumerar todas las conexiones establecidas desde un equipo determinado, llame a la [**función NetConnectionEnum.**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) Puede llamar a **NetConnectionEnum en los** niveles de información [**CONNECTION INFO \_ \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0) y [**CONNECTION INFO \_ \_ 1.**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1)

Las funciones de recurso compartido están disponibles en los siguientes niveles de información:

<dl>

[**COMPARTIR \_ INFORMACIÓN \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_0)  
[**COMPARTIR \_ INFORMACIÓN \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1)  
[**COMPARTIR \_ INFORMACIÓN \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_2)  
[**COMPARTIR \_ INFORMACIÓN \_ 501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_501)  
[**COMPARTIR \_ INFORMACIÓN \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502)  
[**COMPARTIR \_ INFORMACIÓN \_ 1005**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1005)  
</dl>

Los siguientes niveles de información solo son válidos [**para NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo):

<dl>

[**SHARE \_ INFO \_ 1004**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1004)  
[**COMPARTIR \_ INFORMACIÓN \_ 1006**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1006)  
[**COMPARTIR \_ INFORMACIÓN \_ 1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501)  
</dl>

Si está programando para Active Directory, es posible que pueda llamar a ciertos métodos de interfaz de servicio (ADSI) de Active Directory para lograr la misma funcionalidad que puede lograr llamando a las funciones del recurso compartido de administración de red. Para obtener más información, [**vea IADsFileShare.**](/windows/desktop/api/iads/nn-iads-iadsfileshare)

 

 
