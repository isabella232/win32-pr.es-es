---
description: Las aplicaciones distribuidas (cliente/servidor) usan paquetes de seguridad para obtener conexiones autenticadas y intercambiar mensajes.
ms.assetid: 8f28177f-335a-4fa2-bf66-2ec1698bebec
title: Inicialización del modo de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473b06daf2e1c3612b02583d203ce4cd9afebabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002546"
---
# <a name="user-mode-initialization"></a>Inicialización del modo de usuario

Las aplicaciones distribuidas (cliente/servidor) usan [*paquetes de seguridad*](../secgloss/s-gly.md) para obtener conexiones autenticadas y intercambiar mensajes. La aplicación llama a las funciones de la interfaz del proveedor de compatibilidad con seguridad (SSPI) que se asignan a [las funciones implementadas por SSP/APS](authentication-functions.md)y a [las funciones implementadas por SSP/APS en modo de usuario](authentication-functions.md). Esta asignación la realiza el archivo DLL del proveedor de seguridad (Secur32.dll o Security.dll), que se puede cargar de forma dinámica en los procesos de cliente y servidor. El archivo DLL también se puede vincular estáticamente mediante SECUR32. lib. Tanto DLL como LIB se distribuyen con el kit de desarrollo de software (SDK) de Microsoft Windows.

El sistema controla la carga del paquete de seguridad en el proceso del cliente o del servidor, si el archivo DLL SSP/AP que contiene el paquete de seguridad está registrado correctamente.

El servidor comienza el proceso de obtención de una conexión segura con un cliente mediante la supervisión de un puerto, a la espera de que un cliente envíe un mensaje. El cliente comienza el proceso de obtención de una conexión segura al servidor mediante una llamada a la función InitializeSecurityContext de SSPI [**(general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta). Esta función se asigna a la función [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) del paquete de seguridad personalizado. **SpInitLsaModeContext** devuelve un token al cliente, que lo reenvía al servidor.

Al recibir el token del cliente, el servidor llama a la función SSPI [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), que se envía a la función [**SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) del paquete de seguridad. Si la función **SpAcceptLsaModeContext** se ejecuta correctamente y no se requiere más procesamiento para establecer el contexto de seguridad, la función debe devolver el estado \_ correcto al llamador. Si se requiere un procesamiento adicional, la función debe devolver los segundos \_ que se \_ \_ necesitan y devolver un token al servidor. El servidor reenvía el token al cliente, que llama de nuevo a [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .

Este ciclo de llamada se puede repetir tantas veces como sea necesario hasta que se establezca una conexión autenticada o se produzca un error. Durante este proceso, si la función [**SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) o [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) se realiza correctamente y no se requiere más procesamiento para establecer el [*contexto de seguridad*](../secgloss/s-gly.md), la función debe devolver el estado \_ correcto al llamador. Si se requiere un procesamiento adicional, la función debe devolver los segundos que se \_ \_ \_ necesitan y devolver un token al llamador, que es responsable de reenviarlo.

El protocolo implementado por el paquete de seguridad determina el número de veces que se repite este ciclo. Por ejemplo, en los paquetes de seguridad que admiten la autenticación mutua de tres tramos, la secuencia de llamada es la siguiente:

1.  El cliente obtiene un token mediante una llamada a [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)y lo envía al servidor. El servidor llama a [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) la primera vez y recupera un token de respuesta que envía al cliente.
2.  El cliente utiliza el token recibido del servidor en una segunda llamada a [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)y devuelve un token final. El cliente envía este token al servidor.
3.  El servidor recibe el token generado en la pierna 2 que usa en la llamada final a [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).

Cuando las funciones [**SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) y [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) se realizan correctamente y no se requiere más procesamiento para establecer el contexto de seguridad, las funciones deben devolver el estado \_ correcto al llamador. Además, si el paquete de seguridad personalizado admite las [funciones implementadas por SSP/APS en modo de usuario](authentication-functions.md), **SpAcceptLsaModeContext** y **SpInitLsaModeContext** deben devolver **true** mediante el parámetro *MappedContext* . El valor *MappedContext* no se devuelve a la aplicación; lo intercepta la LSA.

Cuando *MappedContext* es **true**, LSA llama a la función [**SpUsermodeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spusermodeinitializefn) de la dll SSP/AP. Esta función proporciona tablas de punteros a las funciones de modo de usuario implementadas por cada paquete de seguridad. Se llama a la función [**SpInstanceInit**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinstanceinitfn) de cada paquete, con las tablas de funciones devueltas por **SpUsermodeInitialize**. **SpInstanceInit** recibe una tabla de punteros a [las funciones de LSA llamadas por SSP/APS en modo de usuario](authentication-functions.md).

 

 
