---
description: Una aplicación COM+ es la unidad principal de administración y seguridad para servicios de componentes y consta de un grupo de componentes COM que, por lo general, realizan funciones relacionadas.
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: Información general de la aplicación COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3365e0c0e7598d8f1eb2f466e8a2cea2d93edf4
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "105670047"
---
# <a name="com-application-overview"></a><span data-ttu-id="3cbd0-103">Información general de la aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="3cbd0-103">COM+ Application Overview</span></span>

<span data-ttu-id="3cbd0-104">Una aplicación COM+ es la unidad principal de administración y seguridad para servicios de componentes y consta de un grupo de componentes COM que, por lo general, realizan funciones relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3cbd0-104">A COM+ application is the primary unit of administration and security for Component Services and consists of a group of COM components that generally perform related functions.</span></span> <span data-ttu-id="3cbd0-105">Estos componentes se componen además de interfaces y métodos, tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="3cbd0-105">These components further consist of interfaces and methods, as shown in the following illustration.</span></span>

![Diagrama que muestra las interfaces y los métodos dentro de los cuadros, en el orden del método dentro de la interfaz dentro del componente dentro de la aplicación COM+.](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

<span data-ttu-id="3cbd0-107">Puede usar la herramienta administrativa Servicios de componentes para crear nuevas aplicaciones COM+, agregar componentes a las aplicaciones y establecer los atributos de una aplicación y sus componentes.</span><span class="sxs-lookup"><span data-stu-id="3cbd0-107">You can use the Component Services administrative tool to create new COM+ applications, add components to applications, and set the attributes for an application and its components.</span></span>

<span data-ttu-id="3cbd0-108">Al crear grupos lógicos de componentes COM como aplicaciones COM+, puede aprovechar las ventajas de COM+ siguientes:</span><span class="sxs-lookup"><span data-stu-id="3cbd0-108">By creating logical groups of COM components as COM+ applications, you can take advantage of the following benefits of COM+:</span></span>

-   <span data-ttu-id="3cbd0-109">Un ámbito de implementación para los componentes COM.</span><span class="sxs-lookup"><span data-stu-id="3cbd0-109">A deployment scope for COM components.</span></span>
-   <span data-ttu-id="3cbd0-110">Un ámbito de configuración común para los componentes COM, incluidos los límites de seguridad y la puesta en cola.</span><span class="sxs-lookup"><span data-stu-id="3cbd0-110">A common configuration scope for COM components, including security boundaries and queuing.</span></span>
-   <span data-ttu-id="3cbd0-111">Almacenamiento de atributos de componentes no proporcionados por el desarrollador de componentes (por ejemplo, transacciones y sincronización).</span><span class="sxs-lookup"><span data-stu-id="3cbd0-111">Storage of component attributes not provided by the component developer (for example, transactions and synchronization).</span></span>
-   <span data-ttu-id="3cbd0-112">Bibliotecas de vínculos dinámicos (dll) de componentes cargadas en procesos (DLLHost.exe) a petición.</span><span class="sxs-lookup"><span data-stu-id="3cbd0-112">Component dynamic-link libraries (DLLs) loaded into processes (DLLHost.exe) on demand.</span></span>
-   <span data-ttu-id="3cbd0-113">Procesos de servidor administrados para hospedar componentes de.</span><span class="sxs-lookup"><span data-stu-id="3cbd0-113">Managed server processes to host components.</span></span>
-   <span data-ttu-id="3cbd0-114">Creación y administración de subprocesos utilizados por los componentes de.</span><span class="sxs-lookup"><span data-stu-id="3cbd0-114">Creation and management of threads used by components.</span></span>
-   <span data-ttu-id="3cbd0-115">Acceso al objeto de contexto para los distribuidores de recursos, permitiendo que los recursos adquiridos se asocien automáticamente al contexto.</span><span class="sxs-lookup"><span data-stu-id="3cbd0-115">Access to the context object for resource dispensers, allowing acquired resources to be automatically associated with the context.</span></span> <span data-ttu-id="3cbd0-116">(Para obtener más información sobre los componentes y contextos COM, vea [contextos com+](com--contexts.md)).</span><span class="sxs-lookup"><span data-stu-id="3cbd0-116">(For more information on COM components and contexts, see [COM+ Contexts](com--contexts.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cbd0-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3cbd0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cbd0-118">Desarrollo de aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="3cbd0-118">Developing COM+ Applications</span></span>](developing-com--applications.md)
</dt> <dt>

[<span data-ttu-id="3cbd0-119">Partes de una aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="3cbd0-119">Parts of a COM+ Application</span></span>](parts-of-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="3cbd0-120">Tipos de aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="3cbd0-120">Types of COM+ Applications</span></span>](types-of-com--applications.md)
</dt> </dl>

 

 



