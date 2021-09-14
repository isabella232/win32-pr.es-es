---
title: Establecer permisos en directorios virtuales
description: Por motivos de seguridad, Servicio de transferencia inteligente en segundo plano (BITS) no carga archivos en un directorio virtual que tenga habilitados los permisos de scripting y ejecución.
ms.assetid: cf5c8b50-066f-431e-8bdf-ed0692219b20
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6753c326e926724a57e1905c3fb9fe24e28fdc7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061584"
---
# <a name="setting-permissions-on-virtual-directories"></a>Establecer permisos en directorios virtuales

Por motivos de seguridad, Servicio de transferencia inteligente en segundo plano (BITS) no carga archivos en un directorio virtual que tenga habilitados los permisos de scripting y ejecución. Si carga un archivo en un directorio virtual que tiene habilitados estos permisos, se produce un error en el trabajo con un código de error de BG \_ E \_ SERVER EXECUTE \_ \_ ENABLED.

BITS no requiere que el directorio virtual esté habilitado para escritura, por lo que se recomienda desactivar el acceso de escritura al directorio virtual.

El usuario autenticado (o el usuario anónimo de IIS para la autenticación anónima) debe tener permisos de cambio en el directorio físico al que está asignado el directorio virtual; Conceder permisos de escritura no es suficiente.

## <a name="specifying-permissions-for-notifications"></a>Especificar permisos para notificaciones

El esquema de autenticación que especifique para el directorio virtual y la dirección URL de notificación (consulte la [propiedad BITSServerNotificationURL)](bits-iis-extension-properties.md) debe ser compatible. BITS usa el esquema de autenticación especificado para que el directorio virtual acceda a la dirección URL de notificación. Se produce un error en el trabajo de carga si BITS no puede acceder a la dirección URL de notificación debido a un error de autenticación.

Si el tipo de notificación (vea la propiedad [BITSServerNotificationType)](bits-iis-extension-properties.md) es por referencia [,](using-bits-notification-request-response-headers.md)la aplicación debe asegurarse de que el usuario tiene acceso al archivo al que se hace referencia (vea el encabezado [BITS-Request-DataFile-Name).](notification-protocol-for-server-applications.md) BITS establece las ACL del archivo al que se hace referencia en las del directorio físico al que está asignado el directorio virtual.

> [!Note]  
> La aplicación notificada debe ser capaz de asignar y acceder al archivo remoto incluso si la dirección URL de notificación está atendidas por un servidor web que se encuentra en un equipo diferente al directorio de carga físico. El [encabezado BITS-Request-DataFile-Name](notification-protocol-for-server-applications.md) siempre contiene una especificación de ruta de acceso relativa al equipo que hospeda el componente de extensiones de BITS. Es posible que una aplicación que se ejecuta en otro equipo tenga que convertir la ruta de acceso a una ruta de acceso UNC antes de acceder a ella.

 

BITS admite muchas combinaciones de esquemas de autenticación. Sin embargo, debe usar el siguiente esquema de autenticación para el directorio virtual y la dirección URL de notificación correspondiente.

-   Para admitir mediante notificaciones de referencia, el directorio virtual debe configurarse para usar la autenticación NTLM (negociación) si el directorio de carga físico (el directorio al que apunta el directorio virtual) usa un esquema de autenticación distinto del anónimo. Si el directorio de carga físico permite solicitudes anónimas (sin autenticación), el directorio virtual debe habilitar el anónimo (sin autenticación).

    Las ACL del directorio de carga física deben establecerse de forma que el usuario autenticado pueda leer archivos en el directorio al que apunta la dirección URL de notificación. BITS usa las ACL del directorio de carga física para establecer las ACL del archivo de carga temporal (el encabezado [BITS-Request-DataFile-Name](notification-protocol-for-server-applications.md) contiene la ruta de acceso al archivo temporal).

-   Dado [que las notificaciones](using-bits-notification-request-response-headers.md) por valor no requieren que la aplicación notificada acceda a un archivo temporal que contiene el contenido de carga, el esquema de autenticación puede ser anónimo o negociar (NTLM). El único requisito es que el usuario autenticado para el directorio virtual también tenga autorización para acceder a la dirección URL de notificación.

## <a name="specifying-permissions-for-remote-shares"></a>Especificar permisos para recursos compartidos remotos

Un directorio virtual puede apuntar a una unidad asignada en un equipo diferente o un recurso compartido de red. Si apunta a una unidad de red asignada, las credenciales usadas para asignar la unidad deben tener control total sobre el recurso compartido remoto.

Si el directorio virtual apunta a un recurso compartido  de red, BITS usa las credenciales Conectar usuario del directorio virtual para acceder al recurso compartido remoto. Para acceder a un recurso compartido remoto, la cuenta **Conectar como** debe tener privilegios, tal y como se describe en la documentación de la [**función LogonUser.**](/windows/desktop/api/winbase/nf-winbase-logonusera) BITS inicia sesión con los tipos de inicio de sesión \_ LOGON32 LOGON BATCH o \_ LOGON32 \_ LOGON \_ INTERACTIVE. La **Conectar como** usuario necesita Full-Access permisos para el recurso compartido remoto; Conceder permisos de escritura no es suficiente.

Cuando el directorio de carga físico se asigna a un recurso compartido de red, la identidad del autor de la llamada que solicita la dirección URL de notificación es **Conectar** Como usuario o el usuario autenticado del directorio de carga física (solo disponible en IIS 6.0 y versiones posteriores, cuando la casilla Usar siempre las credenciales del usuario autenticado al validar el acceso al recurso de red está seleccionada en el cuadro de diálogo **Conectar** Como). 

 

 