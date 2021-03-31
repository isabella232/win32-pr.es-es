---
title: Usar funciones
description: Las funciones de uso de administración de redes examinan y administran las conexiones (usos) entre estaciones de trabajo y servidores. A continuación se enumeran las funciones de uso.
ms.assetid: ddf1b8dc-f13b-402a-9e4e-e4944a29ac31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbd2660b911fd87c39b9db10b0dbfea0e47c484c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904777"
---
# <a name="use-functions"></a>Usar funciones

Las funciones de uso de administración de redes examinan y administran las conexiones (usos) entre estaciones de trabajo y servidores. A continuación se enumeran las funciones de uso.



| Función                               | Descripción                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | Crea una conexión entre un equipo local y un servidor.                               |
| [**NetUseDel**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | Finaliza una conexión a un recurso compartido.                                                   |
| [**NetUseEnum**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | Muestra todas las conexiones actuales entre el equipo local y los recursos de los servidores remotos. |
| [**NetUseGetInfo**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | Devuelve información sobre una conexión a un recurso compartido.                              |



 

Estas funciones solo se aplican al cliente bloque de mensajes del servidor (LAN Manager Workstation). La función **NetUseGetInfo** no admite recursos compartidos de sistema de archivos distribuido (DFS). Para recuperar la información de conexión de un recurso compartido mediante un proveedor de red diferente (por ejemplo, WebDAV o un recurso compartido DFS), use la función [**WNetGetConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona) .

Las conexiones se distinguen de las sesiones: se establece una *sesión* la primera vez que una estación de trabajo realiza una conexión a un recurso compartido en el servidor. Todas las conexiones adicionales entre la estación de trabajo y el servidor forman parte de esta misma sesión hasta que finaliza la sesión. Se pueden realizar dos tipos de conexiones: conexiones de nombre de dispositivo (que solo pueden ser explícitas) y conexiones UNC (Convención de nomenclatura universal) (que pueden ser explícitas o implícitas).

*Las conexiones* se realizan por usuario. Cuando el usuario cierra la sesión, se elimina una conexión realizada por un usuario. Por este motivo, las funciones de uso de administración de red solo son locales, ya que una conexión configurada por un usuario remoto no es accesible para otros usuarios, ni siquiera el usuario que ha iniciado sesión de forma interactiva en dicho equipo.

La función [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd) establece una conexión explícita entre el equipo local y un recurso compartido en un servidor redirigiendo un nombre de dispositivo local al nombre de recurso compartido de un recurso de servidor remoto ( \\ \\ *nombreServidor* \\ *nombreDeRecursoCompartido*). Una vez que se establece una conexión de nombre de dispositivo, los usuarios o las aplicaciones pueden usar el recurso remoto especificando el nombre del dispositivo local.

Las conexiones UNC implícitas se realizan mediante la función responsable de la conexión. Para establecer una conexión UNC implícita, una aplicación pasa el nombre de recurso compartido de un recurso a cualquier función que acepte rutas de acceso UNC. La función acepta el nombre UNC y establece una conexión con el nombre de recurso compartido especificado. Todas las solicitudes posteriores de esta conexión requieren el nombre completo del recurso compartido.

Las funciones de uso están disponibles en los siguientes niveles de información:

-   [**USAR la \_ información \_ 0**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_0)
-   [**USO de la \_ información \_ 1**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_1)
-   [**USAR \_ info \_ 2**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_2)

 

 