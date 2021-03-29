---
title: Establecimiento de permisos en directorios virtuales
description: Por motivos de seguridad, Servicio de transferencia inteligente en segundo plano (BITS) no carga los archivos en un directorio virtual que tenga habilitados los permisos de ejecución y scripting.
ms.assetid: cf5c8b50-066f-431e-8bdf-ed0692219b20
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6753c326e926724a57e1905c3fb9fe24e28fdc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077970"
---
# <a name="setting-permissions-on-virtual-directories"></a>Establecimiento de permisos en directorios virtuales

Por motivos de seguridad, Servicio de transferencia inteligente en segundo plano (BITS) no carga los archivos en un directorio virtual que tenga habilitados los permisos de ejecución y scripting. Si carga un archivo en un directorio virtual que tiene estos permisos habilitados, se produce un error en el trabajo con un código de error de BG \_ E \_ Server \_ Execute \_ enabled.

BITS no requiere que el directorio virtual esté habilitado para escritura, por lo que se recomienda que desactive el acceso de escritura al directorio virtual.

El usuario autenticado (o el usuario anónimo de IIS para la autenticación anónima) debe tener permisos de cambio en el directorio físico al que está asignado el directorio virtual. la concesión de permisos de escritura no es suficiente.

## <a name="specifying-permissions-for-notifications"></a>Especificar permisos para las notificaciones

El esquema de autenticación que especifique para el directorio virtual y la dirección URL de notificación (consulte la propiedad [BITSServerNotificationURL](bits-iis-extension-properties.md) ) debe ser compatible. BITS usa el esquema de autenticación especificado para que el directorio virtual tenga acceso a la dirección URL de notificación. Se produce un error en el trabajo de carga si BITS no puede tener acceso a la dirección URL de notificación debido a un error de autenticación.

Si el tipo de notificación (vea la propiedad [BITSServerNotificationType](bits-iis-extension-properties.md) ) es [por referencia](using-bits-notification-request-response-headers.md), la aplicación debe asegurarse de que el usuario tiene acceso al archivo al que se hace referencia (vea el encabezado [bits-request-DataType-Name](notification-protocol-for-server-applications.md) ). BITS establece las ACL del archivo al que se hace referencia en las del directorio físico al que está asignado el directorio virtual.

> [!Note]  
> La aplicación notificada debe ser capaz de asignar y tener acceso al archivo remoto, incluso si un servidor Web que se encuentra en un equipo diferente al de la dirección URL de la notificación es un servicio que está en un equipo distinto del directorio de carga físico. El encabezado [bits-request-File-Name](notification-protocol-for-server-applications.md) siempre contiene una especificación de ruta de acceso relativa al equipo que hospeda el componente de extensiones bits. Es posible que una aplicación que se ejecuta en otro equipo tenga que convertir la ruta de acceso a una ruta de acceso UNC antes de tener acceso a ella.

 

BITS admite muchas combinaciones de esquemas de autenticación. Sin embargo, debe usar el esquema de autenticación siguiente para el directorio virtual y la dirección URL de notificación correspondiente.

-   Para admitir las notificaciones de referencia, el directorio virtual se debe configurar para usar la autenticación NTLM (Negotiate) si el directorio de carga física (el directorio al que apunta el directorio virtual) usa un esquema de autenticación distinto de anónimo. Si el directorio de carga física permite solicitudes anónimas (sin autenticación), el directorio virtual debe habilitar anónimo (sin autenticación).

    Las ACL del directorio de carga física deben establecerse de modo que el usuario autenticado pueda leer archivos en el directorio al que apunta la dirección URL de notificación. BITS usa las ACL del directorio de carga física para establecer las ACL del archivo de carga temporal (el encabezado [bits-solicitud-archivo de nombre de archivo](notification-protocol-for-server-applications.md) contiene la ruta de acceso al archivo temporal).

-   Dado que las notificaciones [por valor](using-bits-notification-request-response-headers.md) no requieren que la aplicación notificada tenga acceso a un archivo temporal que contiene el contenido de carga, el esquema de autenticación puede ser anónimo o de negociación (NTLM). El único requisito es que el usuario autenticado para el directorio virtual también debe estar autorizado para tener acceso a la dirección URL de notificación.

## <a name="specifying-permissions-for-remote-shares"></a>Especificar permisos para recursos compartidos remotos

Un directorio virtual puede apuntar a una unidad asignada en un equipo diferente o en un recurso compartido de red. Si apunta a una unidad de red asignada, las credenciales usadas para asignar la unidad deben tener control total en el recurso compartido remoto.

Si el directorio virtual apunta a un recurso compartido de red, BITS usa las credenciales de usuario **Connect as** del directorio virtual para tener acceso al recurso compartido remoto. Para tener acceso a un recurso compartido remoto, la cuenta de **conexión** debe tener privilegios, tal como se describe en la documentación de la función [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) . BITS inicia sesión con los \_ \_ tipos de inicio de \_ \_ sesión interactivo de LOGON32 de inicio de sesión o LOGON32 de inicio de sesión. La cuenta de usuario de **conexión como** necesita Full-Access permisos para el recurso compartido remoto; la concesión de permisos de escritura no es suficiente.

Cuando el directorio de carga física se asigna a un recurso compartido de red, la identidad del autor de la llamada que solicita la dirección URL de notificación es el usuario de **conexión** o el usuario autenticado del directorio de carga física (solo disponible en IIS 6,0 y versiones posteriores, cuando la casilla **usar siempre las credenciales del usuario autenticado al validar el acceso al recurso de red** está seleccionada **en el cuadro de**

 

 