---
description: Una aplicación que se ejecuta como un usuario estándar se comunica con un servicio que se ejecuta como sistema mediante la llamada a procedimiento remoto (RPC).
ms.assetid: c0bcebe3-f7eb-471f-a21d-5840d2e26729
title: Modelo de servicio del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce545c60da8e480247c8fc8b02cfc01e4487340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002353"
---
# <a name="operating-system-service-model"></a><span data-ttu-id="8fd81-103">Modelo de servicio del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8fd81-103">Operating System Service Model</span></span>

<span data-ttu-id="8fd81-104">En el modelo de servicio del sistema operativo, una aplicación que se ejecuta como un usuario estándar se comunica con un servicio que se ejecuta como **sistema** mediante la [llamada a procedimiento remoto](/windows/desktop/Rpc/rpc-start-page) (RPC).</span><span class="sxs-lookup"><span data-stu-id="8fd81-104">In the operating system service model, an application running as a standard user communicates with a service running as **SYSTEM** by using [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) (RPC).</span></span>

<span data-ttu-id="8fd81-105">La aplicación de usuario estándar se marca en el manifiesto de aplicación con un **requestedExecutionLevel** de **asInvoker**.</span><span class="sxs-lookup"><span data-stu-id="8fd81-105">The standard user application is marked in the application manifest with a **requestedExecutionLevel** of **asInvoker**.</span></span> <span data-ttu-id="8fd81-106">Para realizar una operación que requiere privilegios de administrador, la aplicación de usuario estándar realiza una solicitud al servicio.</span><span class="sxs-lookup"><span data-stu-id="8fd81-106">To perform an operation that requires administrator privilege, the standard user application makes a request to the service.</span></span>

<span data-ttu-id="8fd81-107">Un uso del modelo de servicio del sistema operativo consiste en administrar aplicaciones que podrían afectar al sistema, como antivirus u otro software y spyware no deseados.</span><span class="sxs-lookup"><span data-stu-id="8fd81-107">One use for the operating system service model is to manage applications that could impact the system, such as antivirus or other unwanted software and spyware.</span></span> <span data-ttu-id="8fd81-108">La aplicación de usuario estándar permite que el usuario que ha iniciado sesión controle algunos aspectos del servicio.</span><span class="sxs-lookup"><span data-stu-id="8fd81-108">The standard user application allows the logged on user to control some aspects of the service.</span></span> <span data-ttu-id="8fd81-109">El servicio es responsable de determinar qué operaciones realiza para una aplicación de usuario estándar.</span><span class="sxs-lookup"><span data-stu-id="8fd81-109">The service is responsible for determining which operations it performs for a standard user application.</span></span> <span data-ttu-id="8fd81-110">Por ejemplo, un servicio antivirus podría permitir a un usuario estándar iniciar un examen del sistema, pero es posible que no permita que un usuario estándar deshabilite la comprobación de virus en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="8fd81-110">For example, an antivirus service might allow a standard user to start a scan of the system, but it might not allow a standard user to disable real-time virus checking.</span></span>

<span data-ttu-id="8fd81-111">Una ventaja importante del uso del modelo de servicio del sistema operativo es que no se requiere ninguna solicitud de elevación.</span><span class="sxs-lookup"><span data-stu-id="8fd81-111">A major benefit of using the operating system service model is that no elevation prompting is required.</span></span>

<span data-ttu-id="8fd81-112">Un inconveniente de usar el modelo de servicio del sistema operativo es que un servicio que se ejecuta en el sistema utiliza más recursos que una tarea y un usuario estándar no puede detener un servicio.</span><span class="sxs-lookup"><span data-stu-id="8fd81-112">One drawback of using the operating system service model is that a service running on the system uses more resources than a task, and a service cannot be stopped by a standard user.</span></span> <span data-ttu-id="8fd81-113">Considere la posibilidad de usar el [modelo de tarea elevado](elevated-task-model.md) si es suficiente.</span><span class="sxs-lookup"><span data-stu-id="8fd81-113">Consider using the [Elevated Task Model](elevated-task-model.md) if it suffices.</span></span>

<span data-ttu-id="8fd81-114">Para implementar el modelo de servicio del sistema operativo, cree una aplicación cliente de usuario estándar y un servicio de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8fd81-114">To implement the operating system service model, create a standard user client application and an operating system service.</span></span> <span data-ttu-id="8fd81-115">Instale el servicio en el sistema operativo durante la instalación del producto.</span><span class="sxs-lookup"><span data-stu-id="8fd81-115">Install the service in the operating system during product installation time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fd81-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8fd81-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fd81-117">Desarrollo de aplicaciones que requieren privilegios de administrador</span><span class="sxs-lookup"><span data-stu-id="8fd81-117">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="8fd81-118">Modelo de agente de administrador</span><span class="sxs-lookup"><span data-stu-id="8fd81-118">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="8fd81-119">Modelo de objetos COM de administrador</span><span class="sxs-lookup"><span data-stu-id="8fd81-119">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="8fd81-120">Modelo de tareas elevado</span><span class="sxs-lookup"><span data-stu-id="8fd81-120">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> </dl>

 

 
