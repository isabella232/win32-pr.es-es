---
title: Funciones de uso compartido
description: Las funciones de recurso compartido de administración de red controlan los recursos compartidos. Un recurso compartido es un recurso local de un servidor (por ejemplo, un directorio de disco, un dispositivo de impresión o una canalización con nombre) al que pueden tener acceso los usuarios y las aplicaciones de la red.
ms.assetid: 3764c667-2290-48e6-ba3a-c74eee2c27f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5034d46e233ebb7ed4de691bd79942a3ecdf5263
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421268"
---
# <a name="share-functions"></a>Funciones de uso compartido

Las funciones de recurso compartido de administración de red controlan los recursos compartidos. Un recurso compartido es un recurso local de un servidor (por ejemplo, un directorio de disco, un dispositivo de impresión o una canalización con nombre) al que pueden tener acceso los usuarios y las aplicaciones de la red.

A continuación se enumeran las funciones de uso compartido.



| Función                                  | Descripción                                                          |
|-------------------------------------------|----------------------------------------------------------------------|
| [**NetShareAdd**](/windows/desktop/api/lmshare/nf-lmshare-netshareadd)         | Comparte un recurso en un servidor.                                       |
| [**NetShareCheck**](/windows/desktop/api/lmshare/nf-lmshare-netsharecheck)     | Consulta si un servidor está compartiendo un dispositivo.                        |
| [**NetShareDel**](/windows/desktop/api/lmshare/nf-lmshare-netsharedel)         | Elimina un nombre de recurso compartido de la lista de recursos compartidos de un servidor.       |
| [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum)       | Recupera información de recursos compartidos sobre cada recurso compartido en un servidor.  |
| [**NetShareGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) | Recupera información sobre un recurso compartido especificado en un servidor. |
| [**NetShareSetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo) | Establece los parámetros de un recurso compartido.                                 |



 

Esta función de recurso compartido se aplica solo a los recursos compartidos de un servidor de bloque de mensajes del servidor (LAN Manager). Estas funciones de recurso compartido no admiten recursos compartidos de Sistema de archivos distribuido (DFS). Por ejemplo, la función [**NetShareGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) solo puede recuperar información de un recurso compartido especificado en un servidor SMB. Para recuperar información de un recurso compartido mediante un proveedor de red diferente (por ejemplo, WebDAV o un recurso compartido DFS), use la función [**WNetGetConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona) .

La función [**NetShareAdd**](/windows/desktop/api/lmshare/nf-lmshare-netshareadd) permite a un usuario o una aplicación compartir un recurso de un tipo específico usando el nombre de recurso compartido especificado. La función **NetShareAdd** requiere que el nombre del recurso compartido y el nombre del dispositivo local compartan el recurso. Un usuario o una aplicación debe tener una cuenta en el servidor para tener acceso al recurso.

También puede especificar un descriptor de seguridad que se va a asociar a un recurso compartido. Los descriptores de seguridad especifican qué usuarios pueden tener acceso a los archivos a través del recurso compartido y con qué tipo de acceso. Especifique un [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) con el nivel de información del [**recurso compartido \_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) al llamar a **NetShareAdd** o [**NetShareSetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo). **NetShareSetInfo** admite el nivel de información de [**recurso compartido \_ \_ 1501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501) . Para obtener más información acerca de los descriptores de seguridad, vea [Access Control](/windows/desktop/SecAuthZ/access-control).

Las funciones de administración de red usan los siguientes nombres de recursos compartidos especiales para la comunicación entre procesos (IPC) y la administración remota del servidor:

-   IPC $, reservado para la comunicación entre procesos
-   ADMIN $, reservado para la administración remota
-   A $, B $, C $ (y otros nombres de disco locales seguidos de un signo de dólar), asignados a los dispositivos de disco local

Para enumerar todas las conexiones realizadas a un recurso compartido en un servidor o para enumerar todas las conexiones establecidas desde un equipo determinado, llame a la función [**NetConnectionEnum**](/windows/desktop/api/lmshare/nf-lmshare-netconnectionenum) . Puede llamar a **NetConnectionEnum** en los niveles de información de [**conexión \_ \_ e**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_0) información de conexión [**\_ \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_1) .

Las funciones de uso compartido están disponibles en los siguientes niveles de información, aunque algunos niveles de recursos compartidos solo se pueden aplicar a algunas de las funciones de uso compartido:

-   [**COMPARTIR \_ información \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-share_info_0)
-   [**COMPARTIR \_ información \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1)
-   [**COMPARTIR \_ información \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-share_info_2)
-   [**Información del recurso compartido \_ \_ 501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_501)
-   [**Información del recurso compartido \_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)
-   [**Información del recurso compartido \_ \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503)
-   [**Información del recurso compartido \_ \_ 1004**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1004)
-   [**Información del recurso compartido \_ \_ 1005**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1005)
-   [**Información del recurso compartido \_ \_ 1006**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1006)
-   [**Información del recurso compartido \_ \_ 1501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501)

Revise la documentación de una función de recurso compartido específica para obtener más información.

Si programa para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz de servicio Active Directory (ADSI) para lograr la misma funcionalidad que puede lograr mediante una llamada a las funciones de recurso compartido de administración de red. Para obtener más información, vea [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).

 

 