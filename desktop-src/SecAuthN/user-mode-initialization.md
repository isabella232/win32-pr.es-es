---
description: Las aplicaciones distribuidas (cliente/servidor) usan paquetes de seguridad para obtener conexiones autenticadas e intercambiar mensajes.
ms.assetid: 8f28177f-335a-4fa2-bf66-2ec1698bebec
title: Inicialización del modo de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473b06daf2e1c3612b02583d203ce4cd9afebabd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160909"
---
# <a name="user-mode-initialization"></a>Inicialización del modo de usuario

Las aplicaciones distribuidas (cliente/servidor) usan [*paquetes de seguridad*](../secgloss/s-gly.md) para obtener conexiones autenticadas e intercambiar mensajes. La aplicación llama a funciones de interfaz de proveedor de compatibilidad de seguridad (SSPI) que se asignan a funciones implementadas por [SSP/AP](authentication-functions.md)y funciones implementadas por [SSP/AP en](authentication-functions.md)modo de usuario. Esta asignación se realiza mediante el archivo DLL del proveedor de seguridad (Secur32.dll o Security.dll), que se puede cargar dinámicamente en los procesos de cliente y servidor. El archivo DLL también se puede vincular estáticamente mediante Secur32.lib. El archivo DLL y LIB se envían con microsoft Windows Software Development Kit (SDK).

El sistema controla la carga del paquete de seguridad en el proceso del cliente o servidor, si el archivo DLL de SSP/AP que contiene el paquete de seguridad está registrado correctamente.

El servidor comienza el proceso de obtener una conexión segura con un cliente mediante la supervisión de un puerto, esperando a que un cliente envíe un mensaje. El cliente comienza el proceso de obtener una conexión segura al servidor mediante una llamada a la función de SSPI [**InitializeSecurityContext (general).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) Esta función se asigna a la función [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) del paquete de seguridad personalizado. **SpInitLsaModeContext** devuelve un token al cliente, que lo reenvía al servidor.

Tras recibir el token del cliente, el servidor llama a la función [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)de SSPI, que se envía a la función [**SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) del paquete de seguridad. Si la **función SpAcceptLsaModeContext** se realiza correctamente y no se requiere más procesamiento para establecer el contexto de seguridad, la función debe devolver STATUS SUCCESS al \_ autor de la llamada. Si se requiere procesamiento adicional, la función debe devolver SEC \_ I CONTINUE NEEDED y devolver un token al \_ \_ servidor. El servidor reenvía el token al cliente, que vuelve a llamar [**a InitializeSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)

Este ciclo de llamada se puede repetir con la frecuencia necesaria hasta que se establezca o se produce un error en una conexión autenticada. Durante este proceso, si la función [**SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) o [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) se realiza correctamente y no se requiere más procesamiento para establecer el contexto de seguridad [*,*](../secgloss/s-gly.md)la función debe devolver STATUS SUCCESS al autor de la \_ llamada. Si se requiere procesamiento adicional, la función debe devolver SEC I CONTINUE NEEDED y devolver un token al autor de la llamada, que es responsable \_ \_ de \_ reenviarlo.

El protocolo implementado por el paquete de seguridad determina el número de veces que se repite este ciclo. Por ejemplo, en los paquetes de seguridad que admiten la autenticación mutua de tres fases, la secuencia de llamada es la siguiente:

1.  El cliente obtiene un token mediante una llamada a [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)y lo envía al servidor. El servidor llama [**a AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) la primera vez y devuelve un token de respuesta que envía al cliente.
2.  El cliente usa el token recibido del servidor en una segunda llamada a [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)y obtiene un token final. El cliente envía este token al servidor.
3.  El servidor recibe el token generado en la etapa 2 que usa en la llamada final a [**AcceptSecurityContext (general).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)

Cuando [**las funciones SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) y [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) se ejecuten correctamente y no se requiera más procesamiento para establecer el contexto de seguridad, las funciones deben devolver STATUS SUCCESS al autor de la \_ llamada. Además, si el paquete de seguridad personalizado admite las funciones implementadas por [SSP/APs](authentication-functions.md)en modo de usuario, **SpAcceptLsaModeContext** y **SpInitLsaModeContext** deben devolver **TRUE** mediante el parámetro *MappedContext.* El *valor mappedContext* no se vuelve a pasar a la aplicación; la intercepta el LSA.

Cuando *MappedContext* es **true,** el LSA llama a la función [**SpUsermodeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spusermodeinitializefn) del archivo DLL de SSP/AP. Esta función proporciona tablas de punteros a las funciones en modo de usuario implementadas por cada paquete de seguridad. Se llama a la [**función SpInstanceInit de**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinstanceinitfn) cada paquete mediante las tablas de función devueltas **por SpUsermodeInitialize.** **SpInstanceInit** recibe una tabla de punteros a funciones LSA llamadas por [SSP/AP en](authentication-functions.md)modo de usuario.

 

 
