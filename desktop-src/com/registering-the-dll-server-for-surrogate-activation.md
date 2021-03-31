---
title: Registrando el servidor DLL para la activación de suplentes
description: Registrando el servidor DLL para la activación de suplentes
ms.assetid: 7133daa4-43b2-402e-a8ac-b357bea745d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca0af764bebf54590442f87f0b4ffdb1a681012
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794001"
---
# <a name="registering-the-dll-server-for-surrogate-activation"></a><span data-ttu-id="cd42a-103">Registrando el servidor DLL para la activación de suplentes</span><span class="sxs-lookup"><span data-stu-id="cd42a-103">Registering the DLL Server for Surrogate Activation</span></span>

<span data-ttu-id="cd42a-104">Un servidor DLL se cargará en un proceso suplente en las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="cd42a-104">A DLL server will be loaded into a surrogate process under the following conditions:</span></span>

-   <span data-ttu-id="cd42a-105">Debe haber un valor AppID especificado en la clave CLSID en el registro y una clave [AppID](appid-key.md) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="cd42a-105">There must be an AppID value specified under the CLSID key in the registry, and a corresponding [AppID](appid-key.md) key.</span></span>
-   <span data-ttu-id="cd42a-106">En una llamada de activación, se establece el bit del [**\_ \_ servidor local CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) y la clave CLSID no especifica [LocalServer32](localserver32.md), [LocalServer](localserver.md)o [LocalService](localservice.md).</span><span class="sxs-lookup"><span data-stu-id="cd42a-106">In an activation call, the [**CLSCTX\_LOCAL\_SERVER**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) bit is set and the CLSID key does not specify [LocalServer32](localserver32.md), [LocalServer](localserver.md), or [LocalService](localservice.md).</span></span> <span data-ttu-id="cd42a-107">Si se establecen otros bits **CLSCTX** , se sigue el [**algoritmo de procesamiento**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)para las marcas de ejecución in-Process, local o remota.</span><span class="sxs-lookup"><span data-stu-id="cd42a-107">If other **CLSCTX** bits are set, the [**processing algorithm**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)for the in-process, local, or remote execution flags is followed.</span></span>
-   <span data-ttu-id="cd42a-108">La clave CLSID contiene la subclave [InProcServer32](inprocserver32.md) .</span><span class="sxs-lookup"><span data-stu-id="cd42a-108">The CLSID key contains the [InprocServer32](inprocserver32.md) subkey.</span></span>
-   <span data-ttu-id="cd42a-109">La DLL de proxy/stub especificada en la clave **InProcServer32** existe.</span><span class="sxs-lookup"><span data-stu-id="cd42a-109">The proxy/stub DLL specified in the **InprocServer32** key exists.</span></span>
-   <span data-ttu-id="cd42a-110">El valor [DllSurrogate](dllsurrogate.md) existe en la clave **AppID** .</span><span class="sxs-lookup"><span data-stu-id="cd42a-110">The [DllSurrogate](dllsurrogate.md) value exists under the **AppID** key.</span></span>

<span data-ttu-id="cd42a-111">Si hay un servidor **LocalServer**, **LocalServer32** o **LocalService**, que indica la existencia de un archivo exe, siempre se iniciará el servidor o el servicio exe en su preferencia para cargar un servidor dll en un proceso suplente.</span><span class="sxs-lookup"><span data-stu-id="cd42a-111">If there is a **LocalServer**, **LocalServer32**, or **LocalService**, indicating the existence of an EXE, the EXE server or service will always be launched in preference to loading a DLL server into a surrogate process.</span></span>

<span data-ttu-id="cd42a-112">Se debe especificar el valor con nombre **DllSurrogate** para que se produzca la activación de suplentes.</span><span class="sxs-lookup"><span data-stu-id="cd42a-112">The **DllSurrogate** named-value must be specified for surrogate activation to occur.</span></span> <span data-ttu-id="cd42a-113">La activación hace referencia a las llamadas a cualquiera de las siguientes funciones de activación:</span><span class="sxs-lookup"><span data-stu-id="cd42a-113">Activation refers to calls to any of the following activation functions:</span></span>

-   [<span data-ttu-id="cd42a-114">**CoGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="cd42a-114">**CoGetClassObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)
-   [<span data-ttu-id="cd42a-115">**CoCreateInstanceEx**</span><span class="sxs-lookup"><span data-stu-id="cd42a-115">**CoCreateInstanceEx**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [<span data-ttu-id="cd42a-116">**CoGetInstanceFromFile**</span><span class="sxs-lookup"><span data-stu-id="cd42a-116">**CoGetInstanceFromFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [<span data-ttu-id="cd42a-117">**CoGetInstanceFromIStorage**</span><span class="sxs-lookup"><span data-stu-id="cd42a-117">**CoGetInstanceFromIStorage**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
-   [<span data-ttu-id="cd42a-118">**IMoniker:: BindToObject**</span><span class="sxs-lookup"><span data-stu-id="cd42a-118">**IMoniker::BindToObject**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)

<span data-ttu-id="cd42a-119">Para iniciar una instancia del suplente proporcionado por el sistema, establezca el valor de **DllSurrogate** en una cadena vacía o en **null**.</span><span class="sxs-lookup"><span data-stu-id="cd42a-119">To launch an instance of the system-supplied surrogate, set the value of **DllSurrogate** either to an empty string or to **NULL**.</span></span> <span data-ttu-id="cd42a-120">Para especificar el inicio de un suplente personalizado, establezca el valor en la ruta de acceso del suplente.</span><span class="sxs-lookup"><span data-stu-id="cd42a-120">To specify the launch of a custom surrogate, set the value to the path of the surrogate.</span></span>

<span data-ttu-id="cd42a-121">Si se especifica [RemoteServerName](remoteservername.md) y **DllSurrogate** para el mismo AppID, se omite el valor **remoteservername** y el valor **DllSurrogate** provoca una activación en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="cd42a-121">If both [RemoteServerName](remoteservername.md) and **DllSurrogate** are specified for the same AppID, the **RemoteServerName** value is ignored and the **DllSurrogate** value causes an activation on the local computer.</span></span> <span data-ttu-id="cd42a-122">Para la activación de suplentes remotos, especifique **RemoteServerName** pero no **DllSurrogate** en el cliente y especifique **DllSurrogate** en el servidor.</span><span class="sxs-lookup"><span data-stu-id="cd42a-122">For remote surrogate activation, specify **RemoteServerName** but not **DllSurrogate** on the client, and specify **DllSurrogate** on the server.</span></span>

<span data-ttu-id="cd42a-123">Un servidor DLL diseñado para ejecutarse siempre en su propio proceso suplente se configura mejor con un AppID igual a su CLSID.</span><span class="sxs-lookup"><span data-stu-id="cd42a-123">A DLL server that is designed to always run alone in its own surrogate process is best configured with an AppID equal its CLSID.</span></span> <span data-ttu-id="cd42a-124">En **AppID**, solo hay que especificar un valor con nombre de **DllSurrogate** con un valor de cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="cd42a-124">Under **AppID**, simply specify a **DllSurrogate** named-value with an empty string value.</span></span>

<span data-ttu-id="cd42a-125">Es mejor configurar un servidor DLL diseñado para ejecutarse por sí solo en su propio proceso suplente y para el servicio de varios clientes a través de una red con un valor [runas](runas.md) especificado en la clave del registro **AppID** .</span><span class="sxs-lookup"><span data-stu-id="cd42a-125">It is best to configure a DLL server that is designed to run alone in its own surrogate process and to service multiple clients across a network with a [RunAs](runas.md) value specified under the **AppID** registry key.</span></span> <span data-ttu-id="cd42a-126">El hecho de que **runas** especifique "usuario interactivo" o una identidad de usuario específica depende de la interfaz de usuario, la seguridad y otros requisitos del servidor.</span><span class="sxs-lookup"><span data-stu-id="cd42a-126">Whether the **RunAs** specifies "Interactive User" or a specific user identity depends upon the user interface, security, and other server requirements.</span></span> <span data-ttu-id="cd42a-127">Cuando se especifica un valor **runas** , solo se carga una instancia del servidor para atender a todos los clientes, independientemente de la identidad del cliente.</span><span class="sxs-lookup"><span data-stu-id="cd42a-127">When a **RunAs** value is specified, only one instance of the server is loaded to service all of the clients, regardless of the identity of the client.</span></span> <span data-ttu-id="cd42a-128">Por otro lado, no configure el servidor con **runas** si la intención es tener una instancia del servidor dll que se ejecuta en suplente para atender cada identidad de cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="cd42a-128">On the other hand, do not configure the server with **RunAs** if the intention is to have one instance of the DLL server running in surrogate to service each remote client identity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd42a-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cd42a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd42a-130">Requisitos del servidor DLL</span><span class="sxs-lookup"><span data-stu-id="cd42a-130">DLL Server Requirements</span></span>](dll-server-requirements.md)
</dt> <dt>

[<span data-ttu-id="cd42a-131">Uso compartido de suplentes</span><span class="sxs-lookup"><span data-stu-id="cd42a-131">Surrogate Sharing</span></span>](surrogate-sharing.md)
</dt> </dl>

 

 