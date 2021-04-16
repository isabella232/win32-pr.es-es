---
title: Self-Registration
description: El registro automático es el medio estándar a través del cual un módulo de servidor puede empaquetar sus propias operaciones del registro, tanto el registro como la anulación del registro, en el propio módulo.
ms.assetid: fb5dcb2b-b0e3-4f37-a8e7-b84b9a265227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c95d422213b8e33ac89b89408ed95724f0769b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488339"
---
# <a name="self-registration"></a><span data-ttu-id="32783-103">Self-Registration</span><span class="sxs-lookup"><span data-stu-id="32783-103">Self-Registration</span></span>

<span data-ttu-id="32783-104">A medida que el software de componentes sigue creciendo como un mercado, habrá más instancias en las que un usuario obtiene un nuevo componente de software como un solo módulo DLL o EXE, como cuando se descarga un componente nuevo desde un servicio en línea o se recibe uno de un amigo en un disquete.</span><span class="sxs-lookup"><span data-stu-id="32783-104">As component software continues to grow as a market, there will be more and more instances where a user obtains a new software component as a single DLL or EXE module, such as when downloading a new component from an on-line service or receiving one from a friend on a floppy disk.</span></span> <span data-ttu-id="32783-105">En estos casos, no es práctico requerir al usuario que realice un procedimiento de instalación o un programa de instalación largo.</span><span class="sxs-lookup"><span data-stu-id="32783-105">In these cases, it is not practical to require the user to go through a lengthy installation procedure or setup program.</span></span> <span data-ttu-id="32783-106">Además de los problemas de licencia, que se administran a través de [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), un procedimiento de instalación crea normalmente las entradas del registro necesarias para que un componente se ejecute correctamente en el contexto com y OLE.</span><span class="sxs-lookup"><span data-stu-id="32783-106">Besides the licensing issues, which are handled through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), an installation procedure typically creates the necessary registry entries for a component to run properly in the COM and OLE context.</span></span>

<span data-ttu-id="32783-107">El registro automático es el medio estándar a través del cual un módulo de servidor puede empaquetar sus propias operaciones del registro, tanto el registro como la anulación del registro, en el propio módulo.</span><span class="sxs-lookup"><span data-stu-id="32783-107">Self-registration is the standard means through which a server module can package its own registry operations, both registration and unregistration, into the module itself.</span></span> <span data-ttu-id="32783-108">Cuando se usa con licencias que se administran a través de [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), un servidor puede convertirse en un módulo totalmente independiente sin necesidad de programas de instalación externos o archivos. reg.</span><span class="sxs-lookup"><span data-stu-id="32783-108">When used with licensing handled through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), a server can become an entirely self-contained module with no need for external installation programs or .reg files.</span></span>

<span data-ttu-id="32783-109">Cualquier módulo de registro automático, DLL o EXE, debe incluir primero una cadena "OleSelfRegister" en la sección [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) de su recurso de información de versión, como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="32783-109">Any self-registering module, DLL or EXE, should first include an "OleSelfRegister" string in the [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) section of its version information resource, as shown here.</span></span>

``` syntax
VS_VERSION_INFO VERSIONINFO 
 
 ... 
 
 BEGIN 
   BLOCK "StringFileInfo" 
    BEGIN 
#ifdef UNICODE 
     BLOCK "040904B0" // Lang=US English, CharSet=Unicode 
#else 
     BLOCK "040904E4" // Lang=US English, CharSet=Windows Multilingual 
#endif 
      BEGIN 
       ... 
       VALUE "OLESelfRegister", "\0" 
      END 
 
   ... 
 
   END 
 
 ... 
 
 END 
 
```

<span data-ttu-id="32783-110">La existencia de estos datos permite que cualquier parte interesada, como una aplicación que desee integrar este nuevo componente, determine si el servidor admite el registro automático sin tener que cargar primero el archivo DLL o EXE.</span><span class="sxs-lookup"><span data-stu-id="32783-110">The existence of this data allows any interested party, such as an application that wishes to integrate this new component, to determine whether the server supports self-registration without having to load the DLL or EXE first.</span></span>

<span data-ttu-id="32783-111">Si el servidor está empaquetado en un módulo DLL, el archivo DLL debe exportar las funciones [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span><span class="sxs-lookup"><span data-stu-id="32783-111">If the server is packaged in a DLL module, the DLL must export the functions [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="32783-112">Cualquier aplicación que desee indicar al servidor que se registre (es decir, todos sus CLSID e identificadores de biblioteca de tipos) puede obtener un puntero a **DllRegisterServer** a través de la función [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="32783-112">Any application that wishes to instruct the server to register itself (that is, all its CLSIDs and type library IDs) can obtain a pointer to **DllRegisterServer** through the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function.</span></span> <span data-ttu-id="32783-113">En **DllRegisterServer**, el archivo dll crea todas las entradas del registro necesarias, almacenando la ruta de acceso correcta a la dll para todas las entradas [InProcServer32](inprocserver32.md) o [InprocHandler32](inprochandler32.md) .</span><span class="sxs-lookup"><span data-stu-id="32783-113">Within **DllRegisterServer**, the DLL creates all its necessary registry entries, storing the correct path to the DLL for all [InprocServer32](inprocserver32.md) or [InprocHandler32](inprochandler32.md) entries.</span></span>

<span data-ttu-id="32783-114">Cuando una aplicación desea quitar el componente del sistema, debe anular el registro de ese componente llamando a [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span><span class="sxs-lookup"><span data-stu-id="32783-114">When an application wishes to remove the component from the system, it should unregister that component by calling [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="32783-115">Dentro de esta llamada, el servidor quita exactamente las entradas creadas anteriormente en [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span><span class="sxs-lookup"><span data-stu-id="32783-115">Within this call, the server removes exactly those entries it previously created in [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span></span> <span data-ttu-id="32783-116">El servidor no debe quitar ciegamente todas las entradas de sus clases porque es posible que otro software haya almacenado entradas adicionales, como una clave [treatAs](treatas.md) .</span><span class="sxs-lookup"><span data-stu-id="32783-116">The server should not blindly remove all entries for its classes because other software may have stored additional entries, such as a [TreatAs](treatas.md) key.</span></span>

<span data-ttu-id="32783-117">Si el servidor está empaquetado en un módulo EXE, la aplicación que desea registrar el servidor inicia el servidor EXE con el argumento de línea de comandos **/regserver** o **-regserver** (no distingue mayúsculas de minúsculas).</span><span class="sxs-lookup"><span data-stu-id="32783-117">If the server is packaged in an EXE module, the application wishing to register the server launches the EXE server with the command-line argument **/RegServer** or **-RegServer** (case-insensitive).</span></span> <span data-ttu-id="32783-118">Si la aplicación desea anular el registro del servidor, inicia el archivo EXE con el argumento de línea de comandos **modificador/unregserver** o **-UnregServer**.</span><span class="sxs-lookup"><span data-stu-id="32783-118">If the application wishes to unregister the server, it launches the EXE with the command-line argument **/UnregServer** or **-UnregServer**.</span></span> <span data-ttu-id="32783-119">El archivo EXE de registro automático detecta estos argumentos de línea de comandos e invoca las mismas operaciones que una DLL en [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)y [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver), respectivamente, registrando la ruta de acceso del módulo en [LocalServer32](localserver32.md) en lugar de **InProcServer32** o **InprocHandler32**.</span><span class="sxs-lookup"><span data-stu-id="32783-119">The self-registering EXE detects these command-line arguments and invokes the same operations as a DLL would within [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver), respectively, registering its module path under [LocalServer32](localserver32.md) instead of **InprocServer32** or **InprocHandler32**.</span></span>

<span data-ttu-id="32783-120">El servidor debe registrar la ruta de acceso completa a la ubicación de instalación del módulo DLL o EXE para sus correspondientes claves **InProcServer32**, **InprocHandler32** y **LocalServer32** en el registro.</span><span class="sxs-lookup"><span data-stu-id="32783-120">The server must register the full path to the installation location of the DLL or EXE module for their respective **InprocServer32**, **InprocHandler32**, and **LocalServer32** keys in the registry.</span></span> <span data-ttu-id="32783-121">La ruta de acceso del módulo se obtiene fácilmente a través de la función [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .</span><span class="sxs-lookup"><span data-stu-id="32783-121">The module path is easily obtained through the [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32783-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32783-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32783-123">Instalar como una aplicación de servicio</span><span class="sxs-lookup"><span data-stu-id="32783-123">Installing as a Service Application</span></span>](installing-as-a-service-application.md)
</dt> <dt>

[<span data-ttu-id="32783-124">Registrar una clase durante la instalación</span><span class="sxs-lookup"><span data-stu-id="32783-124">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="32783-125">Registrar un servidor EXE en ejecución</span><span class="sxs-lookup"><span data-stu-id="32783-125">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
</dt> <dt>

[<span data-ttu-id="32783-126">Registrar objetos en la tabla ROT</span><span class="sxs-lookup"><span data-stu-id="32783-126">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> </dl>

 

 