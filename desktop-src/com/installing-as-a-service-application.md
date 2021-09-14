---
title: Instalación como una aplicación de servicio
description: Instalación como una aplicación de servicio
ms.assetid: 0dd4b348-3d12-49ba-8098-4adb9df01a0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed5c474d73c74b3be40bae773c3d51eadf6c69a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060906"
---
# <a name="installing-as-a-service-application"></a>Instalación como una aplicación de servicio

Además de ejecutarse como un archivo ejecutable de servidor local (EXE), un objeto COM también puede empaquetarse para ejecutarse como una aplicación de servicio cuando lo activa un cliente local o remoto. Los servicios admiten numerosas características administrativas integradas e útiles de la interfaz de usuario, como el inicio, la detención, [](/windows/desktop/Services/service-user-accounts) la pausa y el reinicio locales y remotos, así como la capacidad de establecer el servidor para que se ejecute en una cuenta de usuario y una estación de [ventana](/windows/desktop/winstation/window-stations)específicas.

Un objeto escrito como servicio se instala para su uso por COM estableciendo un valor [LocalService](localservice.md) bajo su clave [AppID](appid-key.md) y realizando una instalación de servicio estándar.

Las clases también se pueden configurar para ejecutarse en una cuenta de usuario específica cuando las activa un cliente remoto sin escribirse como una aplicación de servicio. Para ello, la clase instala un nombre de usuario y una contraseña que se usarán cuando el SCM inicie su proceso de servidor local.

Cuando se configura una clase de esta manera, se producirá un error en las llamadas a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con este CLSID a menos que COM haya iniciado el proceso en nombre de una solicitud de activación real. En otras palabras, es posible que las clases configuradas para ejecutarse como un usuario determinado no se registren en ninguna otra identidad.

El nombre de usuario se toma de [runAs](runas.md) named-value en la clave APPID de la clase. Si el nombre de usuario es "Usuario interactivo", el código de clase se ejecuta en el contexto de seguridad del usuario que ha iniciado sesión actualmente y está conectado a la estación de ventana interactiva.

De lo contrario, la contraseña se recupera de una parte oculta del registro disponible solo para los administradores de la máquina y para el sistema. A continuación, el nombre de usuario y la contraseña se usan para crear una sesión de inicio de sesión en la que se ejecuta el código de clase. Cuando se inicia de esta manera, el código de clase se ejecuta con su propia estación de escritorio y ventana y no comparte identificadores de ventana, el Portapapeles u otros elementos de interfaz de usuario con el usuario interactivo u otras clases que se ejecutan en otras cuentas de usuario.

Un servidor registrado con **LocalService** o **RunAs** puede registrar un objeto en la tabla de objetos en ejecución para permitir que cualquier cliente se conecte a él. Para ello, la llamada del servidor a [**IRunningObjectTable::Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) debe establecer la marca ROTFLAGS \_ ALLOWANYCLIENT. Un servidor que establece este bit debe tener su nombre ejecutable en la sección AppID del Registro que hace referencia al AppID del ejecutable. Es posible que un servidor "activar como activador" (no registrado como **LocalService** o **RunAs)** no registre un objeto con esta marca.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de una clase durante la instalación](registering-a-class-at-installation.md)
</dt> <dt>

[Registro de un servidor EXE en ejecución](registering-a-running-exe-server.md)
</dt> <dt>

[Registrar objetos en ROT](registering-objects-in-the-rot.md)
</dt> <dt>

[Registro propio](self-registration.md)
</dt> </dl>

 

 