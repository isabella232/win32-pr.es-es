---
title: Instalar como una aplicación de servicio
description: Instalar como una aplicación de servicio
ms.assetid: 0dd4b348-3d12-49ba-8098-4adb9df01a0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed5c474d73c74b3be40bae773c3d51eadf6c69a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078416"
---
# <a name="installing-as-a-service-application"></a>Instalar como una aplicación de servicio

Además de ejecutarse como un ejecutable del servidor local (EXE), un objeto COM también puede empaquetarse para ejecutarse como una aplicación de servicio cuando se activa mediante un cliente local o remoto. Los servicios admiten numerosas características administrativas integradas de interfaceâ de usuario y útiles, como el inicio, la detención, la pausa y el reinicio local y remoto, así como la capacidad de establecer el servidor para que se ejecute en una [cuenta de usuario](/windows/desktop/Services/service-user-accounts) específica y una [estación de ventana](/windows/desktop/winstation/window-stations).

Un objeto escrito como un servicio se instala para que lo use COM mediante el establecimiento de un valor [LocalService](localservice.md) bajo su clave [AppID](appid-key.md) y la realización de una instalación de servicio estándar.

Las clases también se pueden configurar para que se ejecuten en una cuenta de usuario específica cuando se activen por un cliente remoto sin escribirse como una aplicación de servicio. Para ello, la clase instala un nombre de usuario y una contraseña que se usarán cuando el SCM inicie su proceso de servidor local.

Cuando una clase está configurada de este modo, se producirá un error en las llamadas a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con este CLSID a menos que com inicie el proceso en nombre de una solicitud de activación real. Es decir, es posible que las clases configuradas para ejecutarse como un usuario determinado no se registren en ninguna otra identidad.

El nombre de usuario se toma del valor con nombre de [runas](runas.md) en la clave AppID de la clase. Si el nombre de usuario es "usuario interactivo", el código de la clase se ejecuta en el contexto de seguridad del usuario que ha iniciado la sesión actual y está conectado a la estación de ventana interactiva.

De lo contrario, la contraseña se recupera de una parte oculta del registro disponible únicamente para los administradores de la máquina y del sistema. El nombre de usuario y la contraseña se usan para crear una sesión de inicio de sesión en la que se ejecuta el código de clase. Cuando se inicia de esta manera, el código de la clase se ejecuta con su propio escritorio y estación de ventana, y no comparte los identificadores de ventana, el portapapeles u otros elementos de la interfaz de usuario con el usuario interactivo u otras clases que se ejecutan en otras cuentas de usuario.

Un servidor registrado con **LocalService** o **runas** puede registrar un objeto en la tabla de objetos en ejecución para permitir que cualquier cliente se conecte a él. Para ello, la llamada del servidor a [**IRunningObjectTable:: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) debe establecer la \_ marca ALLOWANYCLIENT de ROTFLAGS. Un valor de configuración de servidor este bit debe tener el nombre del archivo ejecutable en la sección AppID del registro que hace referencia al AppID del archivo ejecutable. Un servidor "activar como activador" (no registrado como **LocalService** o **runas**) no puede registrar un objeto con esta marca.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registrar una clase durante la instalación](registering-a-class-at-installation.md)
</dt> <dt>

[Registrar un servidor EXE en ejecución](registering-a-running-exe-server.md)
</dt> <dt>

[Registrar objetos en la tabla ROT](registering-objects-in-the-rot.md)
</dt> <dt>

[Registro automático](self-registration.md)
</dt> </dl>

 

 