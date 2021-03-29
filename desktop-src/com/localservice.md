---
title: LocalService (Servicio local)
description: Instala un objeto como una aplicación de servicio.
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- Valor del registro LocalService COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f630c7c0a6f5e3bbf4b9c26ad82e5a104be238
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904855"
---
# <a name="localservice"></a><span data-ttu-id="c3c9e-104">LocalService (Servicio local)</span><span class="sxs-lookup"><span data-stu-id="c3c9e-104">LocalService</span></span>

<span data-ttu-id="c3c9e-105">Instala un objeto como una aplicación de servicio.</span><span class="sxs-lookup"><span data-stu-id="c3c9e-105">Installs an object as a service application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c3c9e-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="c3c9e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LocalService = name
```

## <a name="remarks"></a><span data-ttu-id="c3c9e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3c9e-107">Remarks</span></span>

<span data-ttu-id="c3c9e-108">Además de ejecutarse como un ejecutable del servidor local (EXE), un objeto COM también puede optar por empaquetarse para ejecutarse como una aplicación de servicio cuando se activa mediante un cliente local o remoto.</span><span class="sxs-lookup"><span data-stu-id="c3c9e-108">In addition to running as a local server executable (EXE), a COM object may also choose to package itself to run as a service application when activated by a local or remote client.</span></span> <span data-ttu-id="c3c9e-109">Los servicios admiten numerosas características administrativas útiles e integradas en la interfaz de usuario, como iniciar, detener, pausar y reiniciar, así como la capacidad de establecer el servidor para que se ejecute en una cuenta de usuario específica y en una estación de ventana.</span><span class="sxs-lookup"><span data-stu-id="c3c9e-109">Services support numerous useful and UI-integrated administrative features, including local and remote starting, stopping, pausing, and restarting, as well as the ability to establish the server to run under a specific user account and window station.</span></span>

<span data-ttu-id="c3c9e-110">Un objeto escrito como un servicio se instala para que lo use COM mediante el establecimiento de un valor de **LocalService** y la realización de una instalación de servicio estándar.</span><span class="sxs-lookup"><span data-stu-id="c3c9e-110">An object written as a service is installed for use by COM by establishing a **LocalService** value and performing a standard service installation.</span></span> <span data-ttu-id="c3c9e-111">El valor **LocalService** debe establecerse en el nombre del servicio, tal y como se ha configurado en **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services**, como valor predeterminado de **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="c3c9e-111">The **LocalService** value must be set to the service name, as configured in **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services**, as the default **REG\_SZ** value.</span></span>

<span data-ttu-id="c3c9e-112">Cuando se establece **LocalService** , cualquier cadena asignada a [**ServiceParameters**](serviceparameters.md) se pasa como un argumento de línea de comandos al servicio cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="c3c9e-112">When **LocalService** is set, any string assigned to [**ServiceParameters**](serviceparameters.md) is passed as a command-line argument to the service as it is being launched.</span></span>

<span data-ttu-id="c3c9e-113">La configuración del servicio se prefiere en muchas situaciones en las que las capacidades de las API de administración de servicios locales y remotos y la interfaz de usuario pueden ser útiles para los servicios que proporciona el objeto.</span><span class="sxs-lookup"><span data-stu-id="c3c9e-113">The service configuration is preferred in many situations where the capabilities of the local and remote service management APIs and user interface might be useful for the services that the object provides.</span></span> <span data-ttu-id="c3c9e-114">Por ejemplo, el uso del marco administrativo existente de la arquitectura del servicio debe ser una opción obvia si el objeto es de larga duración o admite fácilmente conceptos como iniciar, detener, restablecer o pausar.</span><span class="sxs-lookup"><span data-stu-id="c3c9e-114">For example, leveraging the existing administrative framework of the service architecture should be an obvious choice if the object is long-lived or readily supports concepts such as starting, stopping, resetting, or pausing.</span></span>

<span data-ttu-id="c3c9e-115">Los servicios se pueden configurar dinámicamente y se pueden configurar para que se ejecuten automáticamente cuando se arranque el equipo, o para que se inicien cuando una aplicación cliente los solicite.</span><span class="sxs-lookup"><span data-stu-id="c3c9e-115">Services can be dynamically configured and can be configured to run automatically when the machine boots, or to be launched when requested by a client application.</span></span>

<span data-ttu-id="c3c9e-116">Si va a implementar clases como servicios, debe tener en cuenta los siguientes puntos:</span><span class="sxs-lookup"><span data-stu-id="c3c9e-116">If you are implementing classes as services, you should be aware of the following points:</span></span>

-   <span data-ttu-id="c3c9e-117">Este valor se usa en preferencia a la clave [**LocalServer32**](localserver32.md) para la activación local y remota requestsâ € "Si **LocalService** existe y hace referencia a un servicio válido, se omite la clave **LocalServer32** .</span><span class="sxs-lookup"><span data-stu-id="c3c9e-117">This value is used in preference to the [**LocalServer32**](localserver32.md) key for local and remote activation requestsâ€”if **LocalService** exists and refers to a valid service, the **LocalServer32** key is ignored.</span></span>
-   <span data-ttu-id="c3c9e-118">Actualmente, solo se puede ejecutar una instancia de una aplicación de servicio en un momento dado de un equipo.</span><span class="sxs-lookup"><span data-stu-id="c3c9e-118">Currently, only a single instance of a service application may be running at a given time on a computer.</span></span> <span data-ttu-id="c3c9e-119">Por tanto, los servicios COM deben registrar sus objetos de clase en el inicio mediante REGCLS \_ MULTIPLEUSE para admitir varios clientes.</span><span class="sxs-lookup"><span data-stu-id="c3c9e-119">COM services must therefore register their class objects on launch using REGCLS\_MULTIPLEUSE to support multiple clients.</span></span>
-   <span data-ttu-id="c3c9e-120">Para iniciarse e inicializarse correctamente, los servicios COM configurados para ejecutarse automáticamente cuando se inicia un equipo deben incluir RPCSS en su lista de servicios dependientes.</span><span class="sxs-lookup"><span data-stu-id="c3c9e-120">To launch and initialize properly, COM services configured to run automatically when a machine boots must include RPCSS in their list of dependent services.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3c9e-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c3c9e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3c9e-122">Registrar servidores COM</span><span class="sxs-lookup"><span data-stu-id="c3c9e-122">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="c3c9e-123">**ServiceParameters**</span><span class="sxs-lookup"><span data-stu-id="c3c9e-123">**ServiceParameters**</span></span>](serviceparameters.md)
</dt> <dt>

[<span data-ttu-id="c3c9e-124">Servicios</span><span class="sxs-lookup"><span data-stu-id="c3c9e-124">Services</span></span>](/windows/desktop/Services/services)
</dt> </dl>

 

 