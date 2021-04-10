---
description: Puede configurar un componente para que se bloquee solo cuando se escribe correctamente para admitir que se agrupa. Para más información sobre estos requisitos, consulte requisitos de los objetos agrupables.
ms.assetid: ffd812cc-811e-4f2a-8736-d1cb22d5abb7
title: Configuración de un componente que se va a agrupar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780f7e1d9128b213b138e63b9dfa7e0f40642681
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153469"
---
# <a name="configuring-a-component-to-be-pooled"></a><span data-ttu-id="3f9b0-104">Configuración de un componente que se va a agrupar</span><span class="sxs-lookup"><span data-stu-id="3f9b0-104">Configuring a Component to Be Pooled</span></span>

<span data-ttu-id="3f9b0-105">Puede configurar un componente para que se bloquee solo cuando se escribe correctamente para admitir que se agrupa.</span><span class="sxs-lookup"><span data-stu-id="3f9b0-105">You can configure a component to be pooled only when it is correctly written to support being pooled.</span></span> <span data-ttu-id="3f9b0-106">Para más información sobre estos requisitos, consulte [requisitos de los objetos agrupables](requirements-for-poolable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3f9b0-106">For details of these requirements, see [Requirements for Poolable Objects](requirements-for-poolable-objects.md).</span></span>

> [!Note]  
> <span data-ttu-id="3f9b0-107">De forma predeterminada, un componente no está configurado para ser agrupado.</span><span class="sxs-lookup"><span data-stu-id="3f9b0-107">By default, a component is not configured to be pooled.</span></span>

 

<span data-ttu-id="3f9b0-108">Al configurar un componente que se va a agrupar, puede especificar las siguientes propiedades para determinar cómo mantiene COM+ el Grupo:</span><span class="sxs-lookup"><span data-stu-id="3f9b0-108">When you configure a component to be pooled, you can specify the following properties to determine how COM+ maintains the pool:</span></span>

-   <span data-ttu-id="3f9b0-109">**Tamaño mínimo del grupo.**</span><span class="sxs-lookup"><span data-stu-id="3f9b0-109">**Minimum pool size.**</span></span> <span data-ttu-id="3f9b0-110">Representa el número de objetos que se crean cuando se inicia la aplicación y el número mínimo de objetos que se mantienen en el grupo mientras la aplicación se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="3f9b0-110">Represents the number of objects that are created when the application starts and the minimum number of objects that are maintained in the pool while the application is running.</span></span> <span data-ttu-id="3f9b0-111">Si el número de objetos disponibles en el grupo cae por debajo del mínimo especificado, se crean nuevos objetos para cumplir cualquier solicitud de objeto pendiente y rellenar el grupo.</span><span class="sxs-lookup"><span data-stu-id="3f9b0-111">If the number of available objects in the pool drops below the specified minimum, new objects are created to meet any outstanding object requests and refill the pool.</span></span> <span data-ttu-id="3f9b0-112">Si el número de objetos disponibles en el grupo es mayor que el número mínimo, esos objetos excedentes se destruyen durante un ciclo de limpieza.</span><span class="sxs-lookup"><span data-stu-id="3f9b0-112">If the number of available objects in the pool is greater than the minimum number, those surplus objects are destroyed during a clean-up cycle.</span></span>
-   <span data-ttu-id="3f9b0-113">**Tamaño máximo del grupo.**</span><span class="sxs-lookup"><span data-stu-id="3f9b0-113">**Maximum pool size.**</span></span> <span data-ttu-id="3f9b0-114">Representa el número máximo de objetos agrupados que creará el administrador de agrupación, que los clientes usan activamente y que están inactivos en el grupo.</span><span class="sxs-lookup"><span data-stu-id="3f9b0-114">Represents the maximum number of pooled objects that the pooling manager will create, both actively used by clients and inactive in the pool.</span></span> <span data-ttu-id="3f9b0-115">Al crear objetos, el administrador de agrupación comprueba para comprobar que no se ha alcanzado el tamaño máximo del grupo y, si no lo ha hecho, el administrador del grupo crea una nueva instancia del objeto para dispensar al cliente.</span><span class="sxs-lookup"><span data-stu-id="3f9b0-115">When creating objects, the pooling manager checks to verify that the maximum pool size has not been reached and, if it hasn't, the pool manager creates a new instance of the object to dispense to the client.</span></span> <span data-ttu-id="3f9b0-116">Si se ha alcanzado el tamaño máximo del grupo, las solicitudes de cliente se pondrán en cola y recibirán el primer objeto disponible del grupo en función del primer servido.</span><span class="sxs-lookup"><span data-stu-id="3f9b0-116">If the maximum pool size has been reached, client requests will be queued and will receive the first available object from the pool on a first-come first-served basis.</span></span> <span data-ttu-id="3f9b0-117">Las solicitudes de creación de objetos agotarán el tiempo de espera después de un período especificado.</span><span class="sxs-lookup"><span data-stu-id="3f9b0-117">Object creation requests will time-out after a specified period.</span></span>
-   <span data-ttu-id="3f9b0-118">**Tiempo de espera de creación (MS).**</span><span class="sxs-lookup"><span data-stu-id="3f9b0-118">**Creation timeout (ms).**</span></span> <span data-ttu-id="3f9b0-119">Especifica cuánto tiempo esperará un cliente, en milisegundos, para que se devuelva un objeto desde el grupo después de una llamada a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="3f9b0-119">Specifies how long a client will wait, in milliseconds, for an object to be returned from the pool after a call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="3f9b0-120">Si la llamada de cliente no se realiza correctamente, se devuelve el tiempo de espera de error E \_ .</span><span class="sxs-lookup"><span data-stu-id="3f9b0-120">If the client call is unsuccessful, the error E\_TIMEOUT is returned.</span></span>

<span data-ttu-id="3f9b0-121">**Para establecer las propiedades relacionadas con la agrupación**</span><span class="sxs-lookup"><span data-stu-id="3f9b0-121">**To set pooling-related properties**</span></span>

1.  <span data-ttu-id="3f9b0-122">En el panel de detalles de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en el componente que desee configurar y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="3f9b0-122">In the details pane of the Component Services administrative tool, right-click the component that you want to configure, and then click **Properties**.</span></span>

2.  <span data-ttu-id="3f9b0-123">En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **activación** .</span><span class="sxs-lookup"><span data-stu-id="3f9b0-123">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="3f9b0-124">Para habilitar la agrupación de objetos para el componente, active la casilla **habilitar agrupación de objetos** .</span><span class="sxs-lookup"><span data-stu-id="3f9b0-124">To enable object pooling for the component, select the **Enable object pooling** check box.</span></span>

4.  <span data-ttu-id="3f9b0-125">En el cuadro **tamaño mínimo del grupo** , escriba el número mínimo de objetos de este tipo en el grupo.</span><span class="sxs-lookup"><span data-stu-id="3f9b0-125">In the **Minimum pool size** box, enter the minimum number of objects of this type in the pool.</span></span> <span data-ttu-id="3f9b0-126">El grupo se mantendrá para tener al menos este número de objetos.</span><span class="sxs-lookup"><span data-stu-id="3f9b0-126">The pool will be maintained to have at least this many objects.</span></span>

5.  <span data-ttu-id="3f9b0-127">En el cuadro u, escriba el número máximo de objetos de este tipo en el grupo.</span><span class="sxs-lookup"><span data-stu-id="3f9b0-127">In the u box, enter the maximum number of objects of this type in the pool.</span></span> <span data-ttu-id="3f9b0-128">El número de objetos, tanto activados como desactivados, no superará nunca este valor.</span><span class="sxs-lookup"><span data-stu-id="3f9b0-128">The number of objects, both activated and deactivated, will never exceed this value.</span></span>

6.  <span data-ttu-id="3f9b0-129">En el cuadro tiempo de **espera de creación (MS)** , escriba la cantidad de tiempo, en milisegundos, que un cliente esperará a un objeto agrupado si uno no está disponible inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="3f9b0-129">In the **Creation timeout (ms)** box, enter the amount of time, in milliseconds, a client will wait for a pooled object if one is not immediately available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f9b0-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3f9b0-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f9b0-131">Supervisión de estadísticas de objetos</span><span class="sxs-lookup"><span data-stu-id="3f9b0-131">Monitoring Object Statistics</span></span>](monitoring-object-statistics.md)
</dt> </dl>

 

 
