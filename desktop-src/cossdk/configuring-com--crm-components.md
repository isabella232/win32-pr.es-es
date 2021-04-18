---
description: Los componentes de CRM se pueden instalar en una aplicación de servidor COM+ o en una aplicación de biblioteca COM+.
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: Configuración de componentes de COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3614c2c34d36cb140f08529c05b31bcc5a4c7f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705378"
---
# <a name="configuring-com-crm-components"></a><span data-ttu-id="44c01-103">Configuración de componentes de COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="44c01-103">Configuring COM+ CRM Components</span></span>

<span data-ttu-id="44c01-104">Los componentes de CRM se pueden instalar en una aplicación de servidor COM+ o en una aplicación de biblioteca COM+.</span><span class="sxs-lookup"><span data-stu-id="44c01-104">CRM components can be installed into either a COM+ server application or a COM+ library application.</span></span> <span data-ttu-id="44c01-105">Sin embargo, siempre deben ejecutarse en una aplicación de servidor COM+.</span><span class="sxs-lookup"><span data-stu-id="44c01-105">However, they must always run in a COM+ server application.</span></span> <span data-ttu-id="44c01-106">Si se instalan en una aplicación de biblioteca COM+, no estarán disponibles para su uso en procesos de cliente.</span><span class="sxs-lookup"><span data-stu-id="44c01-106">If they are installed in a COM+ library application, they are not available for use in client processes.</span></span>

<span data-ttu-id="44c01-107">Si los componentes de CRM están instalados en una aplicación de biblioteca, están disponibles para más de una aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="44c01-107">If the CRM components they are installed in a library application, they are available to more than one server application.</span></span> <span data-ttu-id="44c01-108">Si se instala en una aplicación de servidor específica, solo estarán disponibles para esa aplicación de servidor específica.</span><span class="sxs-lookup"><span data-stu-id="44c01-108">If installed in a specific server application, they are available only to that specific server application.</span></span>

<span data-ttu-id="44c01-109">Para habilitar el uso de un CRM en una aplicación de servidor, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="44c01-109">To enable use of a CRM in a server application, use the following steps:</span></span>

1.  <span data-ttu-id="44c01-110">En servicios de componentes, en la página Propiedades de la aplicación de servidor, haga clic en la pestaña **Opciones avanzadas** .</span><span class="sxs-lookup"><span data-stu-id="44c01-110">From Component Services, under the server application properties page, click the **Advanced** tab.</span></span>

2.  <span data-ttu-id="44c01-111">Seleccione la opción **habilitar los administradores de compensación de recursos** para esa aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="44c01-111">Select the **Enable compensating Resource Managers** option for that server application.</span></span> <span data-ttu-id="44c01-112">Si no se selecciona esta opción, se producirá un error en los intentos de usar un CRM dentro de esta aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="44c01-112">If this option is not selected, attempts to use a CRM within this server application will fail.</span></span>

    > [!Note]  
    > <span data-ttu-id="44c01-113">Si se instala en una aplicación de biblioteca, no es necesario seleccionar la opción **habilitar los administradores de compensación de recursos** para esa aplicación de biblioteca, pero se debe seleccionar esta opción para la aplicación de servidor en la que se va a ejecutar el CRM.</span><span class="sxs-lookup"><span data-stu-id="44c01-113">If installed in a library application, it is not necessary to select the **Enable compensating Resource Managers** option for that library application, but this option must be selected for the server application in which the CRM is intended to run.</span></span>

     

<span data-ttu-id="44c01-114">Se recomienda que los componentes de CRM y de compensador de CRM para un CRM específico se instalen en la misma aplicación.</span><span class="sxs-lookup"><span data-stu-id="44c01-114">It is recommended that the CRM Worker and CRM Compensator components for a specific CRM be installed in the same application.</span></span>

<span data-ttu-id="44c01-115">La configuración recomendada para los componentes de CRM es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="44c01-115">The recommended settings for CRM components are as follows.</span></span>



| <span data-ttu-id="44c01-116">Componente</span><span class="sxs-lookup"><span data-stu-id="44c01-116">Component</span></span>           | <span data-ttu-id="44c01-117">Configuración</span><span class="sxs-lookup"><span data-stu-id="44c01-117">Settings</span></span>                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44c01-118">**Trabajador de CRM**</span><span class="sxs-lookup"><span data-stu-id="44c01-118">**CRM Worker**</span></span>      | <span data-ttu-id="44c01-119">Transaction = requiredsync = yesJIT = yesthreading Model = both (o modelo de subprocesos = apartamento)</span><span class="sxs-lookup"><span data-stu-id="44c01-119">transaction = requiredsync = yesJIT = yesthreading model = Both (or threading model = Apartment)</span></span>     |
| <span data-ttu-id="44c01-120">**Compensator de CRM**</span><span class="sxs-lookup"><span data-stu-id="44c01-120">**CRM Compensator**</span></span> | <span data-ttu-id="44c01-121">Transaction = disabledsync = disabledJIT = nothreading Model = both (o el modelo de subprocesos = Apartment)</span><span class="sxs-lookup"><span data-stu-id="44c01-121">transaction = disabledsync = disabledJIT = nothreading model = Both (or threading model = Apartment)</span></span> |



 

> [!Note]  
> <span data-ttu-id="44c01-122">Los componentes que utilizan el CRM deben especificar explícitamente un modelo de subprocesos cuando se registran.</span><span class="sxs-lookup"><span data-stu-id="44c01-122">Components that use the CRM must explicitly specify a threading model when they are registered.</span></span> <span data-ttu-id="44c01-123">No se admite el valor predeterminado "apartamento del subproceso principal".</span><span class="sxs-lookup"><span data-stu-id="44c01-123">The default, 'Main Thread Apartment,' is not supported.</span></span> <span data-ttu-id="44c01-124">Los únicos dos modelos de subprocesos admitidos son Apartment y both.</span><span class="sxs-lookup"><span data-stu-id="44c01-124">The only two threading models supported are Apartment and Both.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="44c01-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="44c01-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44c01-126">Conceptos de Administrador de recursos de compensación de COM+</span><span class="sxs-lookup"><span data-stu-id="44c01-126">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



