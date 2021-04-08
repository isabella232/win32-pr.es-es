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
# <a name="installing-as-a-service-application"></a><span data-ttu-id="f6b5e-103">Instalar como una aplicación de servicio</span><span class="sxs-lookup"><span data-stu-id="f6b5e-103">Installing as a Service Application</span></span>

<span data-ttu-id="f6b5e-104">Además de ejecutarse como un ejecutable del servidor local (EXE), un objeto COM también puede empaquetarse para ejecutarse como una aplicación de servicio cuando se activa mediante un cliente local o remoto.</span><span class="sxs-lookup"><span data-stu-id="f6b5e-104">In addition to running as a local server executable (EXE), a COM object may also package itself to run as a service application when activated by a local or remote client.</span></span> <span data-ttu-id="f6b5e-105">Los servicios admiten numerosas características administrativas integradas de interfaceâ de usuario y útiles, como el inicio, la detención, la pausa y el reinicio local y remoto, así como la capacidad de establecer el servidor para que se ejecute en una [cuenta de usuario](/windows/desktop/Services/service-user-accounts) específica y una [estación de ventana](/windows/desktop/winstation/window-stations).</span><span class="sxs-lookup"><span data-stu-id="f6b5e-105">Services support numerous useful and user interfaceâ€“integrated administrative features, including local and remote starting, stopping, pausing, and restarting, as well as the ability to establish the server to run under a specific [user account](/windows/desktop/Services/service-user-accounts) and [window station](/windows/desktop/winstation/window-stations).</span></span>

<span data-ttu-id="f6b5e-106">Un objeto escrito como un servicio se instala para que lo use COM mediante el establecimiento de un valor [LocalService](localservice.md) bajo su clave [AppID](appid-key.md) y la realización de una instalación de servicio estándar.</span><span class="sxs-lookup"><span data-stu-id="f6b5e-106">An object written as a service is installed for use by COM by establishing a [LocalService](localservice.md) value under its [AppID](appid-key.md) key and performing a standard service installation.</span></span>

<span data-ttu-id="f6b5e-107">Las clases también se pueden configurar para que se ejecuten en una cuenta de usuario específica cuando se activen por un cliente remoto sin escribirse como una aplicación de servicio.</span><span class="sxs-lookup"><span data-stu-id="f6b5e-107">Classes may also be configured to run under a specific user account when activated by a remote client without being written as a service application.</span></span> <span data-ttu-id="f6b5e-108">Para ello, la clase instala un nombre de usuario y una contraseña que se usarán cuando el SCM inicie su proceso de servidor local.</span><span class="sxs-lookup"><span data-stu-id="f6b5e-108">To do this, the class installs a user name and a password to be used when the SCM launches its local server process.</span></span>

<span data-ttu-id="f6b5e-109">Cuando una clase está configurada de este modo, se producirá un error en las llamadas a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con este CLSID a menos que com inicie el proceso en nombre de una solicitud de activación real.</span><span class="sxs-lookup"><span data-stu-id="f6b5e-109">When a class is configured in this fashion, calls to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) with this CLSID will fail unless the process was launched by COM on behalf of an actual activation request.</span></span> <span data-ttu-id="f6b5e-110">Es decir, es posible que las clases configuradas para ejecutarse como un usuario determinado no se registren en ninguna otra identidad.</span><span class="sxs-lookup"><span data-stu-id="f6b5e-110">In other words, classes configured to run as a particular user may not be registered under any other identity.</span></span>

<span data-ttu-id="f6b5e-111">El nombre de usuario se toma del valor con nombre de [runas](runas.md) en la clave AppID de la clase.</span><span class="sxs-lookup"><span data-stu-id="f6b5e-111">The user name is taken from the [RunAs](runas.md) named-value under the class's APPID key.</span></span> <span data-ttu-id="f6b5e-112">Si el nombre de usuario es "usuario interactivo", el código de la clase se ejecuta en el contexto de seguridad del usuario que ha iniciado la sesión actual y está conectado a la estación de ventana interactiva.</span><span class="sxs-lookup"><span data-stu-id="f6b5e-112">If the user name is "Interactive User", the class code is run in the security context of the currently logged on user and is connected to the interactive window station.</span></span>

<span data-ttu-id="f6b5e-113">De lo contrario, la contraseña se recupera de una parte oculta del registro disponible únicamente para los administradores de la máquina y del sistema.</span><span class="sxs-lookup"><span data-stu-id="f6b5e-113">Otherwise, the password is retrieved from a hidden portion of the registry available only to administrators of the machine and to the system.</span></span> <span data-ttu-id="f6b5e-114">El nombre de usuario y la contraseña se usan para crear una sesión de inicio de sesión en la que se ejecuta el código de clase.</span><span class="sxs-lookup"><span data-stu-id="f6b5e-114">The user name and password are then used to create a logon session in which the class code is run.</span></span> <span data-ttu-id="f6b5e-115">Cuando se inicia de esta manera, el código de la clase se ejecuta con su propio escritorio y estación de ventana, y no comparte los identificadores de ventana, el portapapeles u otros elementos de la interfaz de usuario con el usuario interactivo u otras clases que se ejecutan en otras cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="f6b5e-115">When launched in this way, the class code runs with its own desktop and window-station and does not share window handles, the clipboard, or other user interface elements with the interactive user or other classes running in other user accounts.</span></span>

<span data-ttu-id="f6b5e-116">Un servidor registrado con **LocalService** o **runas** puede registrar un objeto en la tabla de objetos en ejecución para permitir que cualquier cliente se conecte a él.</span><span class="sxs-lookup"><span data-stu-id="f6b5e-116">A server registered either with **LocalService** or **RunAs** can register an object in the running object table to allow any client to connect to it.</span></span> <span data-ttu-id="f6b5e-117">Para ello, la llamada del servidor a [**IRunningObjectTable:: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) debe establecer la \_ marca ALLOWANYCLIENT de ROTFLAGS.</span><span class="sxs-lookup"><span data-stu-id="f6b5e-117">To do so, the server's call to [**IRunningObjectTable::Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) must set the ROTFLAGS\_ALLOWANYCLIENT flag.</span></span> <span data-ttu-id="f6b5e-118">Un valor de configuración de servidor este bit debe tener el nombre del archivo ejecutable en la sección AppID del registro que hace referencia al AppID del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="f6b5e-118">A server setting this bit must have its executable name in the AppID section of the registry that refers to the AppID for the executable.</span></span> <span data-ttu-id="f6b5e-119">Un servidor "activar como activador" (no registrado como **LocalService** o **runas**) no puede registrar un objeto con esta marca.</span><span class="sxs-lookup"><span data-stu-id="f6b5e-119">An "activate as activator" server (not registered as either **LocalService** or **RunAs**) may not register an object with this flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6b5e-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6b5e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6b5e-121">Registrar una clase durante la instalación</span><span class="sxs-lookup"><span data-stu-id="f6b5e-121">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="f6b5e-122">Registrar un servidor EXE en ejecución</span><span class="sxs-lookup"><span data-stu-id="f6b5e-122">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
</dt> <dt>

[<span data-ttu-id="f6b5e-123">Registrar objetos en la tabla ROT</span><span class="sxs-lookup"><span data-stu-id="f6b5e-123">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> <dt>

[<span data-ttu-id="f6b5e-124">Registro automático</span><span class="sxs-lookup"><span data-stu-id="f6b5e-124">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 