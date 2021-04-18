---
title: Registrar un servidor EXE en ejecución
description: Registrar un servidor EXE en ejecución
ms.assetid: 277f44bb-72b7-4409-955d-2cd53bc99467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0c6cae15818e5cdb3931f71f0d4be1ac1baef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357499"
---
# <a name="registering-a-running-exe-server"></a><span data-ttu-id="f2382-103">Registrar un servidor EXE en ejecución</span><span class="sxs-lookup"><span data-stu-id="f2382-103">Registering a Running EXE Server</span></span>

<span data-ttu-id="f2382-104">Cuando se inicia un servidor ejecutable (EXE), debe llamar a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), que registra el CLSID para el servidor en lo que se denomina la tabla de clases (una tabla diferente de la tabla de objetos en ejecución).</span><span class="sxs-lookup"><span data-stu-id="f2382-104">When an executable (EXE) server is launched, it should call [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), which registers the CLSID for the server in what is called the class table (a different table than the running object table).</span></span> <span data-ttu-id="f2382-105">Cuando se registra un servidor en la tabla de clases, permite al administrador de control de servicios (SCM) determinar que no es necesario volver a iniciar la clase, porque el servidor ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="f2382-105">When a server is registered in the class table, it allows the service control manager (SCM) to determine that it is not necessary to launch the class again, because the server is already running.</span></span> <span data-ttu-id="f2382-106">Solo si el servidor no aparece en la lista de clases, el SCM comprobará en el registro los valores adecuados y iniciará el servidor asociado al CLSID dado.</span><span class="sxs-lookup"><span data-stu-id="f2382-106">Only if the server is not listed in the class table will the SCM check the registry for appropriate values and launch the server associated with the given CLSID.</span></span>

<span data-ttu-id="f2382-107">Se pasa [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) como CLSID para la clase y un puntero a su interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f2382-107">You pass [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) the CLSID for the class and a pointer to its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f2382-108">Los clientes que llaman posteriormente a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) con este CLSID recuperarán un puntero a su interfaz solicitada, siempre y cuando la seguridad no lo prohíba.</span><span class="sxs-lookup"><span data-stu-id="f2382-108">Clients who subsequently call [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) with this CLSID will retrieve a pointer to their requested interface, as long as security does not forbid it.</span></span> <span data-ttu-id="f2382-109">(Consulte [funciones auxiliares de creación de instancias](instance-creation-helper-functions.md) para obtener una descripción de varias funciones de creación y activación de instancias).</span><span class="sxs-lookup"><span data-stu-id="f2382-109">(See [Instance Creation Helper Functions](instance-creation-helper-functions.md) for a description of several instance creation and activation functions.)</span></span>

<span data-ttu-id="f2382-110">El servidor de un objeto de clase debe llamar a [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) para revocar el objeto de clase (quite su registro) cuando se cumplan todas las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="f2382-110">The server for a class object should call [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) to revoke the class object (remove its registration) when all of the following are true:</span></span>

-   <span data-ttu-id="f2382-111">No hay ninguna instancia existente de la definición del objeto.</span><span class="sxs-lookup"><span data-stu-id="f2382-111">There are no existing instances of the object definition.</span></span>
-   <span data-ttu-id="f2382-112">No hay bloqueos en el objeto de clase.</span><span class="sxs-lookup"><span data-stu-id="f2382-112">There are no locks on the class object.</span></span>
-   <span data-ttu-id="f2382-113">La aplicación que proporciona servicios al objeto de clase no está bajo el control de usuario (no es visible para el usuario en la pantalla).</span><span class="sxs-lookup"><span data-stu-id="f2382-113">The application providing services to the class object is not under user control (not visible to the user on the display).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2382-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f2382-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2382-115">Instalar como una aplicación de servicio</span><span class="sxs-lookup"><span data-stu-id="f2382-115">Installing as a Service Application</span></span>](installing-as-a-service-application.md)
</dt> <dt>

[<span data-ttu-id="f2382-116">Registrar una clase durante la instalación</span><span class="sxs-lookup"><span data-stu-id="f2382-116">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="f2382-117">Registrar objetos en la tabla ROT</span><span class="sxs-lookup"><span data-stu-id="f2382-117">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> <dt>

[<span data-ttu-id="f2382-118">Registro automático</span><span class="sxs-lookup"><span data-stu-id="f2382-118">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 




