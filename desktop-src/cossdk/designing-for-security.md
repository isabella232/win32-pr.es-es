---
description: Diseñar para la seguridad
ms.assetid: 436f9d86-fbfa-4d5a-8580-fa1d4065c0aa
title: Diseñar para la seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69bc59b06cfcb7432806e548cc9808199b194e6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714842"
---
# <a name="designing-for-security"></a><span data-ttu-id="57b59-103">Diseñar para la seguridad</span><span class="sxs-lookup"><span data-stu-id="57b59-103">Designing for Security</span></span>

<span data-ttu-id="57b59-104">La estrategia de un extremo a otro para la seguridad obviamente depende del tipo de aplicación distribuida que esté desarrollando.</span><span class="sxs-lookup"><span data-stu-id="57b59-104">Your end-to-end strategy for security obviously depends on the type of distributed application you are developing.</span></span> <span data-ttu-id="57b59-105">A continuación se muestran varias sugerencias para abordar la seguridad con respecto a la lógica de aplicación de nivel intermedio:</span><span class="sxs-lookup"><span data-stu-id="57b59-105">Following are several suggestions for addressing security with respect to middle-tier application logic:</span></span>

-   <span data-ttu-id="57b59-106">Para mejorar la eficacia y el rendimiento, autentique lo más cerca posible del usuario.</span><span class="sxs-lookup"><span data-stu-id="57b59-106">For efficiency and performance, authenticate as close to the user as you can.</span></span> <span data-ttu-id="57b59-107">Si la aplicación implica una arquitectura de lógica a base de datos de explorador a empresa, considere la posibilidad de asignar los clientes del explorador a las identidades de dominio, ejecutar la aplicación COM+ bajo identidades específicas de cada aplicación y configurar tablas en la capa de datos para que solo sean accesibles por una identidad de aplicación concreta.</span><span class="sxs-lookup"><span data-stu-id="57b59-107">If your application involves a browser-to-business-logic-to-database architecture, consider mapping the browser clients to domain identities, run the COM+ application under identities specific to each application, and configure tables in the data tier to be accessible only by a particular application identity.</span></span> <span data-ttu-id="57b59-108">Este escenario de servidor de confianza es más escalable y menos problemático que el uso del DBMS para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="57b59-108">This trusted server scenario is more scalable and less problematic than using the DBMS for authenticating.</span></span>
-   <span data-ttu-id="57b59-109">Si está diseñando un componente que se usará en una aplicación distribuida mediante la seguridad basada en roles, puede usar la funcionalidad de [seguridad de com+](com--security.md) .</span><span class="sxs-lookup"><span data-stu-id="57b59-109">If you are designing a component that will be used in a distributed application using role-based security, you can use the [COM+ security](com--security.md) functionality.</span></span> <span data-ttu-id="57b59-110">Esta funcionalidad le permite llamar a métodos como [**IObjectContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) y [**IObjectContext:: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) para ayudar a proteger los bloques de código frente al acceso no autorizado.</span><span class="sxs-lookup"><span data-stu-id="57b59-110">This functionality allows you to call methods such as [**IObjectContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) and [**IObjectContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) to help protect blocks of code from unauthorized access.</span></span> <span data-ttu-id="57b59-111">También puede utilizar el contexto de la llamada de seguridad para obtener información sobre los llamadores de un objeto.</span><span class="sxs-lookup"><span data-stu-id="57b59-111">You can also use the security call context to get information about an object's callers.</span></span>
-   <span data-ttu-id="57b59-112">Si está diseñando un componente que se usará en una aplicación distribuida sin usar la seguridad basada en roles, la seguridad se comprueba automáticamente solo en el nivel de proceso.</span><span class="sxs-lookup"><span data-stu-id="57b59-112">If you are designing a component that will be used in a distributed application without using role-based security, security is automatically checked only at the process level.</span></span> <span data-ttu-id="57b59-113">Los permisos de acceso al proceso determinan quién tiene acceso a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="57b59-113">Process access permissions determine who is given access to the application.</span></span> <span data-ttu-id="57b59-114">Si necesita un control granular más preciso sobre la configuración de seguridad en el proceso o en el nivel de interfaz, utilice la funcionalidad de seguridad mediante programación proporcionada por COM.</span><span class="sxs-lookup"><span data-stu-id="57b59-114">If you need finer grain control over security settings at the process or at the interface level, use the programmatic security functionality provided by COM.</span></span>
-   <span data-ttu-id="57b59-115">Si un componente que utiliza la seguridad mediante programación de COM+ se ejecuta sin integrarse en una aplicación COM+, se producirán excepciones.</span><span class="sxs-lookup"><span data-stu-id="57b59-115">If a component using COM+ programmatic security is run without being integrated into a COM+ application, exceptions will be thrown.</span></span> <span data-ttu-id="57b59-116">Por lo tanto, si desea que este componente se integre correctamente en una aplicación que no forma parte del entorno de COM+, debe controlar todas las excepciones de manera adecuada.</span><span class="sxs-lookup"><span data-stu-id="57b59-116">Therefore, if you want such a component to be successfully integrated into an application that is not part of the COM+ environment, you must handle all exceptions appropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57b59-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57b59-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57b59-118">Diseño para disponibilidad</span><span class="sxs-lookup"><span data-stu-id="57b59-118">Designing for Availability</span></span>](designing-for-availability.md)
</dt> <dt>

[<span data-ttu-id="57b59-119">Diseñar para la implementación</span><span class="sxs-lookup"><span data-stu-id="57b59-119">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> <dt>

[<span data-ttu-id="57b59-120">Diseño para la escalabilidad</span><span class="sxs-lookup"><span data-stu-id="57b59-120">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="57b59-121">Seguridad de componentes mediante programación</span><span class="sxs-lookup"><span data-stu-id="57b59-121">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 



