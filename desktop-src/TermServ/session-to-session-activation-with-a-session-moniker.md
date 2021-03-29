---
title: Activación de sesión a sesión con un moniker de sesión
description: La activación de sesión a sesión (también denominada activación entre sesiones) permite que un proceso de cliente inicie (Active) un proceso de servidor local en una sesión especificada.
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2714f3dbe7b23c8b7f04d4271018891960b87f76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793365"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a><span data-ttu-id="a44b9-103">Activación de sesión a sesión con un moniker de sesión</span><span class="sxs-lookup"><span data-stu-id="a44b9-103">Session-to-Session Activation with a Session Moniker</span></span>

<span data-ttu-id="a44b9-104">La activación de sesión a sesión (también denominada activación entre sesiones) permite que un proceso de cliente inicie (Active) un proceso de servidor local en una sesión especificada.</span><span class="sxs-lookup"><span data-stu-id="a44b9-104">Session-to-session activation (also called cross-session activation) allows a client process to start (activate) a local server process on a specified session.</span></span> <span data-ttu-id="a44b9-105">Esta característica está disponible para las aplicaciones que están configuradas para ejecutarse en el contexto de seguridad del usuario interactivo, también conocido como el modo de activación de objetos de "usuario interactivo de runas".</span><span class="sxs-lookup"><span data-stu-id="a44b9-105">This feature is available for applications that are configured to run in the security context of the interactive user, also known as the "RunAs Interactive User" object activation mode.</span></span> <span data-ttu-id="a44b9-106">Para obtener más información sobre los contextos de seguridad, vea [el contexto de seguridad del cliente](/windows/desktop/SecAuthZ/the-client-security-context).</span><span class="sxs-lookup"><span data-stu-id="a44b9-106">For more information about security contexts, see [The Client's Security Context](/windows/desktop/SecAuthZ/the-client-security-context).</span></span>

<span data-ttu-id="a44b9-107">COM distribuido (DCOM) permite la activación de objetos por sesión mediante el uso de un [moniker de sesión](session-monikers.md)proporcionado por el sistema.</span><span class="sxs-lookup"><span data-stu-id="a44b9-107">Distributed COM (DCOM) enables object activation on a per-session basis by using a system-supplied [Session Moniker](session-monikers.md).</span></span> <span data-ttu-id="a44b9-108">Otros monikers proporcionados por el sistema son monikers de [archivo](../com/file-monikers.md), monikers de [elemento](../com/item-monikers.md), monikers [compuestos](../com/composite-monikers.md)genéricos, [anti-monikers](../com/anti-monikers.md), monikers de [puntero](../com/pointer-monikers.md)y [monikers de dirección URL](../com/url-monikers.md).</span><span class="sxs-lookup"><span data-stu-id="a44b9-108">Other system-supplied monikers include [file monikers](../com/file-monikers.md), [item monikers](../com/item-monikers.md), generic [composite monikers](../com/composite-monikers.md), [anti-monikers](../com/anti-monikers.md), [pointer monikers](../com/pointer-monikers.md), and [URL monikers](../com/url-monikers.md).</span></span>

<span data-ttu-id="a44b9-109">Para poder utilizar el moniker de sesión, la aplicación DCOM debe estar configurada para ejecutarse como usuario interactivo.</span><span class="sxs-lookup"><span data-stu-id="a44b9-109">To be able to use the session moniker, the DCOM application must be set to run as the interactive user.</span></span> <span data-ttu-id="a44b9-110">Esto se puede establecer mediante la herramienta administrativa Servicios de componentes, viendo las propiedades de la aplicación DCOM y seleccionando **el usuario interactivo** en la pestaña **identidad** . Para obtener más información sobre los posibles riesgos de seguridad asociados con la configuración de una aplicación DCOM para que se ejecute como usuario interactivo en un entorno de Servicios de Escritorio remoto, vea la sección "identidad de la aplicación (COM)" de la documentación de COM en el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="a44b9-110">This can be set by using the Component Services Administrative tool, viewing the Properties of the DCOM application, and selecting **The interactive user** on the **Identity** tab. For more information about the possible security risks associated with setting a DCOM application to run as the interactive user in a Remote Desktop Services environment, see the "Application Identity (COM)" section of the COM documentation in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="a44b9-111">Si se selecciona cualquier otro tipo de usuario para ejecutar la aplicación, la aplicación omitirá el moniker de la sesión.</span><span class="sxs-lookup"><span data-stu-id="a44b9-111">If any other type of user is selected to run the application, the session moniker will be ignored by the application.</span></span> <span data-ttu-id="a44b9-112">Las aplicaciones de servidor COM+ también omiten el moniker de la sesión.</span><span class="sxs-lookup"><span data-stu-id="a44b9-112">The session moniker is also ignored by COM+ server applications.</span></span> <span data-ttu-id="a44b9-113">Para obtener más información acerca de otros métodos para seleccionar el tipo de usuario para ejecutar la aplicación, consulte la documentación de COM en el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="a44b9-113">For more information about other methods for selecting the type of user to run the application, see the COM documentation in the Platform SDK.</span></span>

<span data-ttu-id="a44b9-114">Para crear un moniker de sesión, debe componer el ID. de sesión de la sesión de Servicios de Escritorio remoto con un moniker de clase que especifique el identificador de clase del servidor de procesos.</span><span class="sxs-lookup"><span data-stu-id="a44b9-114">To create a session moniker, you must compose the session ID of the Remote Desktop Services session with a class moniker that specifies the process server's class ID.</span></span>

<span data-ttu-id="a44b9-115">**Para crear un moniker de sesión**</span><span class="sxs-lookup"><span data-stu-id="a44b9-115">**To create a session moniker**</span></span>

1.  <span data-ttu-id="a44b9-116">Prefije el nombre para mostrar del moniker de clase con el nombre para mostrar del moniker de la sesión mediante la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="a44b9-116">Prefix the display name of the class moniker with the display name of the session moniker by using the following syntax:</span></span>

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    <span data-ttu-id="a44b9-117">donde *digits* representa el ID. de sesión de la sesión en la que se iniciará el proceso de servidor y donde ID. de *clase* representa el ID. de clase del servidor.</span><span class="sxs-lookup"><span data-stu-id="a44b9-117">where *digits* represents the session ID of the session on which the server process will be started, and where *class id* represents the class ID of the server.</span></span> <span data-ttu-id="a44b9-118">Tenga en cuenta que el identificador de sesión es un número de base 10.</span><span class="sxs-lookup"><span data-stu-id="a44b9-118">Note that the session ID is a base-10 number.</span></span>

    <span data-ttu-id="a44b9-119">En el caso de los equipos que ejecutan Windows XP o versiones posteriores, el uso de la siguiente sintaxis dará como resultado que COM envíe la activación a la sesión de consola física activa actualmente, sea cual sea su identificador de sesión:</span><span class="sxs-lookup"><span data-stu-id="a44b9-119">For computers that are running Windows XP or later, using the following syntax will result in COM sending the activation to the currently active physical console session, whatever its session ID is:</span></span>

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  <span data-ttu-id="a44b9-120">Después de haber creado el moniker de la sesión, puede pasar el resultado a la función [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) o a la función [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a44b9-120">After you have created the session moniker, you can pass the result to either the [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) function or the [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) function.</span></span>

<span data-ttu-id="a44b9-121">Puede utilizar un moniker de la sesión de la misma manera que usaría cualquier otro moniker.</span><span class="sxs-lookup"><span data-stu-id="a44b9-121">You can use a session moniker in the same way as you would use any other moniker.</span></span>

<span data-ttu-id="a44b9-122">Para obtener un ejemplo de código que muestra cómo activar un proceso de servidor local en una sesión especificada, vea [usar un moniker de sesión](using-a-session-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="a44b9-122">For a code sample that demonstrates how to activate a local server process on a specified session, see [Using a Session Moniker](using-a-session-moniker.md).</span></span>

<span data-ttu-id="a44b9-123">Para obtener más información sobre la activación de objetos, monikers y monikers proporcionados por el sistema, vea la documentación de COM en Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="a44b9-123">For more information about object activation, system-supplied monikers and class monikers, see the COM documentation in the Platform SDK.</span></span>

> [!Note]  
> <span data-ttu-id="a44b9-124">Los procesos que se crean en las sesiones tienen un límite superior en el tamaño del bloque de entorno.</span><span class="sxs-lookup"><span data-stu-id="a44b9-124">Processes that are created across sessions have an upper limit on the size of the environment block.</span></span> <span data-ttu-id="a44b9-125">Este límite es de aproximadamente 4 KB, pero puede ser mayor o menor en función de la información que se necesite para crear el proceso (por ejemplo, nombres de archivo, directorios y parámetros para el nuevo proceso).</span><span class="sxs-lookup"><span data-stu-id="a44b9-125">This limit is around 4 KB, but it can be larger or smaller depending on what other information is needed to create the process (for example file names, directories, and parameters for the new process).</span></span>

 

 

 