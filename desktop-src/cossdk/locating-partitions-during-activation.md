---
description: Localizar particiones durante la activación
ms.assetid: a5452ed6-ab0f-4d38-bc16-1de6cbf57486
title: Localizar particiones durante la activación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e8912c8277d79c1a20300a1a880644801d0bcb
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104568673"
---
# <a name="locating-partitions-during-activation"></a><span data-ttu-id="6b2bc-103">Localizar particiones durante la activación</span><span class="sxs-lookup"><span data-stu-id="6b2bc-103">Locating Partitions During Activation</span></span>

<span data-ttu-id="6b2bc-104">La ubicación de la partición correcta en la que se va a activar un componente depende de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6b2bc-104">Locating the correct partition in which to activate a component depends on the following:</span></span>

-   <span data-ttu-id="6b2bc-105">La llamada de función y los parámetros utilizados en el programa que realiza la llamada para activar el componente</span><span class="sxs-lookup"><span data-stu-id="6b2bc-105">The function call and parameters used in the calling program to activate the component</span></span>
-   <span data-ttu-id="6b2bc-106">Si el componente que se va a activar es local o remoto</span><span class="sxs-lookup"><span data-stu-id="6b2bc-106">Whether the component being activated is local or remote</span></span>
-   <span data-ttu-id="6b2bc-107">Uso interno de la memoria caché de partición</span><span class="sxs-lookup"><span data-stu-id="6b2bc-107">The internal use of the partition cache</span></span>

## <a name="the-calling-program"></a><span data-ttu-id="6b2bc-108">El programa que realiza la llamada</span><span class="sxs-lookup"><span data-stu-id="6b2bc-108">The Calling Program</span></span>

<span data-ttu-id="6b2bc-109">COM+ selecciona la partición para la activación de componentes en función de cómo el programa de llamada activa el componente.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-109">COM+ selects the partition for component activation based on how the calling program activates the component.</span></span>

<span data-ttu-id="6b2bc-110">Hay tres acciones diferentes que COM+ puede llevar a cabo al seleccionar una partición para la activación de componentes.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-110">There are three different actions that COM+ can take when selecting a partition for component activation.</span></span> <span data-ttu-id="6b2bc-111">La acción realizada depende de la forma en que el programa de llamada crea instancias del objeto, es decir, si la llamada de función incluye un moniker de partición, que consta de un identificador de partición y un CLSID, o solo incluye un CLSID.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-111">The action taken depends on how the calling program instantiates the object that is, whether the function call includes a partition moniker, which consists of a partition ID and a CLSID, or includes a CLSID only.</span></span>

<span data-ttu-id="6b2bc-112">En la tabla siguiente se muestran las distintas acciones que COM+ puede realizar, en orden de prioridad, para buscar una partición.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-112">The following table shows the various actions that COM+ can take, in order of precedence, to locate a partition.</span></span>



| <span data-ttu-id="6b2bc-113">Llamada a función</span><span class="sxs-lookup"><span data-stu-id="6b2bc-113">Function call</span></span>                                                  | <span data-ttu-id="6b2bc-114">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6b2bc-114">Parameter</span></span>                                                      | <span data-ttu-id="6b2bc-115">Acción COM+</span><span class="sxs-lookup"><span data-stu-id="6b2bc-115">COM+ action</span></span>                                                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b2bc-116">[**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) o **GetObject**</span><span class="sxs-lookup"><span data-stu-id="6b2bc-116">[**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) or **GetObject**</span></span><br/> | <span data-ttu-id="6b2bc-117">Moniker de partición (incluye el identificador de partición y el CLSID)</span><span class="sxs-lookup"><span data-stu-id="6b2bc-117">Partition moniker (includes partition ID and CLSID)</span></span><br/> | <span data-ttu-id="6b2bc-118">Usa el ID. de partición especificado en el moniker de la partición.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-118">Uses the partition ID specified in the partition moniker.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="6b2bc-119">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="6b2bc-119">**CoCreateInstance**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)<br/>        | <span data-ttu-id="6b2bc-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="6b2bc-120">CLSID</span></span><br/>                                               | <span data-ttu-id="6b2bc-121">Usa el ID. de partición de la partición predeterminada de la identidad del usuario o el ID. de partición que se agregó al contexto durante una activación de componente anterior en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-121">Uses either the partition ID of the user identity's default partition or the partition ID that was added to the context during a previous component activation in the same process.</span></span><br/> |



 

<span data-ttu-id="6b2bc-122">Las acciones de COM+ enumeradas en la tabla anterior se explican en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-122">The COM+ actions listed in the preceding table are explained in the following sections.</span></span>

## <a name="use-of-partition-monikers"></a><span data-ttu-id="6b2bc-123">Uso de monikers de partición</span><span class="sxs-lookup"><span data-stu-id="6b2bc-123">Use of Partition Monikers</span></span>

<span data-ttu-id="6b2bc-124">Una partición se puede seleccionar explícitamente dentro de una llamada de función mediante el *moniker* de la partición.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-124">A partition can be selected explicitly within a function call by using a *partition moniker*.</span></span> <span data-ttu-id="6b2bc-125">Se usa un moniker de partición dentro del código para especificar explícitamente la partición del componente activado.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-125">A partition moniker is used within code to explicitly specify the partition of the activated component.</span></span> <span data-ttu-id="6b2bc-126">Si se usa un moniker de partición para buscar la partición, la activación se produce desde esa partición.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-126">If a partition moniker is used to locate the partition, the activation occurs from that partition.</span></span> <span data-ttu-id="6b2bc-127">Es decir, el ID. de partición incluido en el moniker tiene prioridad sobre la partición predeterminada del usuario o sobre un identificador de partición que existe en el contexto del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-127">That is, the partition ID included in the moniker takes precedence over the user's default partition or over a partition ID that exists in the caller's context.</span></span>

<span data-ttu-id="6b2bc-128">En el código de C++, la sintaxis para el uso de un moniker de partición es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="6b2bc-128">In C++ code, the syntax for the use of a partition moniker is as follows:</span></span>


```C++
HRESULT CoGetObject(
  L"partition:partitionGUID/new:clsid",
  pBindOptions,
  IID_IUnknown,
  (void**)&pIUnknown);
```



<span data-ttu-id="6b2bc-129">En el ejemplo siguiente se muestra un fragmento de código de C++, en el que se usa un moniker de partición como argumento para la función [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) :</span><span class="sxs-lookup"><span data-stu-id="6b2bc-129">The following example shows a snippet of C++ code, in which a partition moniker is being used as an argument to the [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) function:</span></span>


```C++
// Create CLSID1 configured in the Production partition.
HRESULT hr = CoGetObject(
  L"partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1",
  pBindOptions, IID_IUnknown, (void**)&pIUnknown);
```



<span data-ttu-id="6b2bc-130">En Visual Basic código, la sintaxis de un moniker de la partición es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="6b2bc-130">In Visual Basic code, the syntax for a partition moniker is as follows:</span></span>


```VB
GetObject("partition:partitionGUID/new:CLSID") As Object
```



<span data-ttu-id="6b2bc-131">En el ejemplo siguiente se muestra un fragmento de código de Visual Basic, en el que se usa un moniker de partición como argumento para la función **GetObject** :</span><span class="sxs-lookup"><span data-stu-id="6b2bc-131">The following example shows a snippet of Visual Basic code, in which a partition moniker is being used as an argument to the **GetObject** function:</span></span>


```VB
Dim objCLSID1 As Object
Set objCLSID1 = GetObject( _
   "partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1")
```



## <a name="use-of-default-mapping"></a><span data-ttu-id="6b2bc-132">Uso de la asignación predeterminada</span><span class="sxs-lookup"><span data-stu-id="6b2bc-132">Use of Default Mapping</span></span>

<span data-ttu-id="6b2bc-133">Cuando se usa la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para activar un componente, mediante el CLSID del componente, com+ utiliza la asignación de identidad de usuario predeterminada, que es el conjunto de particiones al que está asignado el usuario dentro de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-133">When the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function is used to activate a component, using the component's CLSID, COM+ uses the default user-identity mapping that is, the partition set that the user is mapped to within Active Directory.</span></span> <span data-ttu-id="6b2bc-134">Sin embargo, si el usuario no está asignado a un conjunto de particiones dentro de Active Directory, se selecciona la partición global.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-134">However, if the user is not mapped to a partition set within Active Directory, the Global Partition is selected.</span></span>

## <a name="use-of-partition-ids-and-object-context"></a><span data-ttu-id="6b2bc-135">Uso de ID. de partición y contexto del objeto</span><span class="sxs-lookup"><span data-stu-id="6b2bc-135">Use of Partition IDs and Object Context</span></span>

<span data-ttu-id="6b2bc-136">Una de las cinco propiedades asignadas a una nueva partición es el identificador de la partición.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-136">One of the five properties assigned to a new partition is the partition ID.</span></span> <span data-ttu-id="6b2bc-137">Cuando el programa cliente llama a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una instancia de un objeto, el identificador de la partición se agrega al contexto.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-137">When the client program calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to instantiate an object, the partition ID is added to the context.</span></span> <span data-ttu-id="6b2bc-138">Es importante usar el ID. de partición del contexto para encontrar la partición, ya que garantiza que, una vez iniciada una cadena de activaciones, el identificador de la partición sigue siendo el mismo, a menos que se cambie explícitamente a través de un moniker de la partición.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-138">Using the partition ID from the context to locate the partition is important because it ensures that after a chain of activations has begun, the partition ID remains the same unless it is changed explicitly through a partition moniker.</span></span>

<span data-ttu-id="6b2bc-139">Para obtener información adicional sobre cómo localizar particiones durante la activación, vea [componentes y particiones en cola de com+](com--queued-components-and-partitions.md).</span><span class="sxs-lookup"><span data-stu-id="6b2bc-139">For additional information on locating partitions during activation, see [COM+ Queued Components and Partitions](com--queued-components-and-partitions.md).</span></span>

## <a name="local-and-remote-activation"></a><span data-ttu-id="6b2bc-140">Activación local y remota</span><span class="sxs-lookup"><span data-stu-id="6b2bc-140">Local and Remote Activation</span></span>

-   <span data-ttu-id="6b2bc-141">Si el componente al que se llama existe en otro equipo, se calculan las referencias de las propiedades de la partición (incluido el ID. de partición) al otro equipo y el componente se activa desde la partición serializada.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-141">If the component being called exists on another computer, the partition properties (including the partition ID) are marshaled to the other computer and the component is activated from the marshaled partition.</span></span> <span data-ttu-id="6b2bc-142">Si no se serializó ningún ID. de partición, COM+ utiliza el conjunto de particiones predeterminado asignado a la identidad del usuario en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-142">If no partition ID was marshaled, COM+ uses the default partition set mapped to the user identity within Active Directory.</span></span>

## <a name="the-partition-cache"></a><span data-ttu-id="6b2bc-143">La memoria caché de partición</span><span class="sxs-lookup"><span data-stu-id="6b2bc-143">The Partition Cache</span></span>

<span data-ttu-id="6b2bc-144">En un entorno de dominio, COM+ usa las asignaciones en Active Directory para encontrar la partición correcta para la activación de componentes.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-144">In a domain environment, COM+ uses the mappings in Active Directory to locate the correct partition for component activation.</span></span> <span data-ttu-id="6b2bc-145">Sin embargo, las búsquedas frecuentes en Active Directory pueden dar lugar a un tráfico de red excesivo.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-145">However, frequent lookups in Active Directory can result in excessive network traffic.</span></span> <span data-ttu-id="6b2bc-146">Para minimizar el tráfico de red resultante de búsquedas frecuentes de asignación de conjunto de usuarios a particiones en Active Directory, COM+ utiliza una *memoria caché de particiones*.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-146">To minimize network traffic resulting from frequent lookups of user-to-partition-set mapping in Active Directory, COM+ uses a *partition cache*.</span></span>

<span data-ttu-id="6b2bc-147">La memoria caché de particiones contiene las asignaciones que se realizaron en Active Directory entre las identidades de usuario o las unidades organizativas y sus conjuntos de particiones.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-147">The partition cache contains the mappings that were made in Active Directory between user identities or OUs and their partition sets.</span></span> <span data-ttu-id="6b2bc-148">Esta memoria caché de particiones se encuentra en el servidor de aplicaciones en el que residen las aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-148">This partition cache is located on the application server on which the COM+ applications reside.</span></span>

<span data-ttu-id="6b2bc-149">Cuando COM+ necesita determinar la partición predeterminada de un usuario o validar los derechos de acceso de un usuario en una partición, comprueba la caché de particiones localmente para buscar la asignación del usuario, en lugar de comprobar Active Directory de forma remota.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-149">When COM+ needs to determine a user's default partition or validate a user's access rights to a partition, it checks the partition cache locally to look up the user's mapping, instead of checking Active Directory remotely.</span></span>

<span data-ttu-id="6b2bc-150">Si se produce un error en la búsqueda en la caché de particiones, COM+ comprueba Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-150">If the lookup in the partition cache fails, COM+ then checks Active Directory.</span></span> <span data-ttu-id="6b2bc-151">Si la búsqueda se realiza correctamente en Active Directory, COM+ almacena esa asignación en la memoria caché de la partición.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-151">If the lookup is successful in Active Directory, COM+ stores that mapping in the partition cache.</span></span> <span data-ttu-id="6b2bc-152">La próxima vez que se realice una búsqueda para esa asignación de usuario a partición, COM+ la encontrará en la memoria caché de la partición.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-152">The next time a lookup is done for that user-to-partition mapping, COM+ will find it in the partition cache.</span></span>

<span data-ttu-id="6b2bc-153">En la ilustración siguiente se muestra el proceso que usa COM+ para buscar una partición para la activación de componentes.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-153">The following illustration shows the process that COM+ uses to locate a partition for component activation.</span></span>

![Diagrama que muestra un árbol de solución de problemas para el proceso que usa COM+ para buscar una partición para la activación de componentes.](images/5d00eb4e-4572-491c-85e9-33ceed2cd753.png)

<span data-ttu-id="6b2bc-155">El tamaño de la memoria caché y el tiempo de expiración de las entradas de caché se establecen a través de las claves del registro.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-155">The size of the cache and the expiration time for the cache entries are set via registry keys.</span></span> <span data-ttu-id="6b2bc-156">Para obtener información sobre la configuración de estas claves del registro, vea [crear y configurar particiones com+](creating-and-configuring-com--partitions.md).</span><span class="sxs-lookup"><span data-stu-id="6b2bc-156">For information on configuring these registry keys, see [Creating and Configuring COM+ Partitions](creating-and-configuring-com--partitions.md).</span></span>

> [!Note]  
> <span data-ttu-id="6b2bc-157">Si un equipo servidor está desconectado de la red y se cambia la asignación de usuario a partición mientras el servidor está desconectado, es posible que la memoria caché de particiones contenga una asignación de usuario a partición no actualizada.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-157">If a server computer is disconnected from the network and the user-to-partition mapping is changed while the server is disconnected, the partition cache might contain outdated user-to-partition mapping.</span></span> <span data-ttu-id="6b2bc-158">Esto podría producir un error de activación si la asignación de usuario a partición es el mecanismo que se usa para activar un componente.</span><span class="sxs-lookup"><span data-stu-id="6b2bc-158">This could result in an activation error if user-to-partition mapping is the mechanism used to activate a component.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6b2bc-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6b2bc-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b2bc-160">Buscar un componente para la activación</span><span class="sxs-lookup"><span data-stu-id="6b2bc-160">Locating a Component for Activation</span></span>](locating-a-component-for-activation.md)
</dt> </dl>

 

