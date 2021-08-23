---
title: Usar funciones
description: Las funciones de uso de administración de red examinan y administran las conexiones (usos) entre estaciones de trabajo y servidores. Las funciones de uso se enumeran a continuación.
ms.assetid: ddf1b8dc-f13b-402a-9e4e-e4944a29ac31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f61019f6c6e2785f03eb4e2e9a47ed1953e14662c5664dca41465bc83d7c683d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779515"
---
# <a name="use-functions"></a>Usar funciones

Las funciones de uso de administración de red examinan y administran las conexiones (usos) entre estaciones de trabajo y servidores. Las funciones de uso se enumeran a continuación.



| Función                               | Descripción                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | Crea una conexión entre un equipo local y un servidor.                               |
| [**NetUseDel**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | Finaliza una conexión a un recurso compartido.                                                   |
| [**NetUseEnum**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | Enumera todas las conexiones actuales entre el equipo local y los recursos de los servidores remotos. |
| [**NetUseGetInfo**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | Devuelve información sobre una conexión a un recurso compartido.                              |



 

Esta función solo se aplica al cliente del bloque de mensajes del servidor (estación de trabajo del administrador de LAN). La **función NetUseGetInfo** no admite recursos compartidos Sistema de archivos distribuido (DFS). Para recuperar información de conexión para un recurso compartido mediante un proveedor de red diferente (WebDAV o un recurso compartido DFS, por ejemplo), use la [**función WNetGetConnection.**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona)

Las conexiones se distinguen de las sesiones: se *establece* una sesión la primera vez que una estación de trabajo realiza una conexión a un recurso compartido en el servidor. Todas las conexiones adicionales entre la estación de trabajo y el servidor forman parte de esta misma sesión hasta que finaliza la sesión. Se pueden realizar dos tipos de conexiones: conexiones de nombre de dispositivo (que solo pueden ser explícitas) y conexiones de convención de nomenclatura universal (UNC) (que pueden ser explícitas o implícitas).

*Las* conexiones se realizan por usuario. Una conexión realizada por un usuario se elimina cuando ese usuario cierra la sesión. Por este motivo, las funciones de uso de administración de red son solo locales, ya que una conexión configurada por un usuario remoto no sería accesible para ningún otro usuario, incluso el usuario que inició sesión de forma interactiva en ese equipo.

La [**función NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd) establece una conexión explícita entre el equipo local y un recurso compartido en un servidor mediante el redireccionamiento de un nombre de dispositivo local al nombre del recurso compartido de un recurso de servidor remoto \\ \\ *(nombreDeServidor* \\ *sharename*). Una vez que se establece una conexión de nombre de dispositivo, los usuarios o las aplicaciones pueden usar el recurso remoto especificando el nombre del dispositivo local.

La función responsable de la conexión realiza las conexiones UNC implícitas. Para establecer una conexión UNC implícita, una aplicación pasa el nombre del recurso compartido de un recurso a cualquier función que acepte rutas de acceso UNC. La función acepta el nombre UNC y establece una conexión con el nombre del recurso compartido especificado. Todas las solicitudes lejos de esta conexión requieren el nombre completo del recurso compartido.

Las funciones de uso están disponibles en los siguientes niveles de información:

-   [**USO \_ DE INFO \_ 0**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_0)
-   [**USE \_ INFO \_ 1**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_1)
-   [**USO \_ DE INFO \_ 2**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_2)

 

 