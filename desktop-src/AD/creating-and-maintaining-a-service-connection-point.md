---
title: Crear y mantener un punto de conexión de servicio
description: Al publicar con un SCP, recuerde que debe contener los datos actuales sobre la instancia de servicio.
ms.assetid: 2350cb65-3439-4a5f-adc5-b71476793247
ms.tgt_platform: multiple
keywords:
- Creación y mantenimiento de un punto de conexión de servicio AD
- punto de conexión de servicio AD, creación y mantenimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c4ad02b92fa6567fc3b709e45f2f64ce66318
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077541"
---
# <a name="creating-and-maintaining-a-service-connection-point"></a><span data-ttu-id="a6ef3-105">Crear y mantener un punto de conexión de servicio</span><span class="sxs-lookup"><span data-stu-id="a6ef3-105">Creating and Maintaining a Service Connection Point</span></span>

<span data-ttu-id="a6ef3-106">Al publicar con un SCP, recuerde que debe contener los datos actuales sobre la instancia de servicio.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-106">When publishing with an SCP, remember that it must contain current data about the service instance.</span></span> <span data-ttu-id="a6ef3-107">De lo contrario, los clientes que se enlazan al SCP recuperan datos obsoletos.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-107">Otherwise, clients that bind to the SCP retrieve outdated data.</span></span> <span data-ttu-id="a6ef3-108">El instalador del servicio, que crea un SCP, especifica los valores iniciales para los atributos de los SCP.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-108">Your service installer, that creates an SCP, specifies the initial values for the SCPs attributes.</span></span> <span data-ttu-id="a6ef3-109">A continuación, cuando se inicia la instancia de servicio, debe buscar el SCP y actualizar los valores de atributo, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-109">Then, when the service instance starts, it must locate the SCP and update the attribute values, if necessary.</span></span> <span data-ttu-id="a6ef3-110">De esta manera, los clientes están seguros de los datos más actuales.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-110">In this way, clients are assured the most current data.</span></span>

<span data-ttu-id="a6ef3-111">Después de crear el SCP, el instalador del servicio realiza dos pasos adicionales que permiten al servicio actualizar el SCP:</span><span class="sxs-lookup"><span data-stu-id="a6ef3-111">After creating the SCP, your service installer performs two additional steps that enable your service to update the SCP:</span></span>

-   <span data-ttu-id="a6ef3-112">Establezca ACE en el descriptor de seguridad del objeto SCP para permitir que el servicio modifique los atributos SCP en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-112">Set ACEs in the security descriptor of the SCP object to enable the service to modify SCP attributes at run time.</span></span> <span data-ttu-id="a6ef3-113">Para obtener más información y un ejemplo de código, consulte [habilitación de la cuenta de servicio para acceder a las propiedades de SCP](enabling-service-account-to-access-scp-properties.md).</span><span class="sxs-lookup"><span data-stu-id="a6ef3-113">For more information and a code example, see [Enabling Service Account to Access SCP Properties](enabling-service-account-to-access-scp-properties.md).</span></span>
-   <span data-ttu-id="a6ef3-114">Almacene en caché el **objectGUID** del SCP en el registro del equipo host del servicio.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-114">Cache the **objectGUID** of the SCP in the registry on the service host computer.</span></span> <span data-ttu-id="a6ef3-115">El servicio recupera el GUID almacenado en caché que se va a enlazar al SCP para comprobar y actualizar sus atributos.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-115">The service retrieves the cached GUID to bind to the SCP to verify and update its attributes.</span></span>

<span data-ttu-id="a6ef3-116">El instalador del servicio almacena en caché el **objectGUID** del SCP en lugar de su DN.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-116">The service installer caches the SCP's **objectGUID** rather than its DN.</span></span> <span data-ttu-id="a6ef3-117">**ObjectGUID** nunca cambia, independientemente de si se mueve o se cambia el nombre del SCP.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-117">The **objectGUID** never changes, regardless of whether the SCP is moved or renamed.</span></span> <span data-ttu-id="a6ef3-118">El DN puede cambiar si un administrador mueve o cambia el nombre del SCP.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-118">The DN can change if an administrator moves or renames the SCP.</span></span> <span data-ttu-id="a6ef3-119">Por ejemplo, si crea un SCP como un elemento secundario de un objeto de equipo, el nombre distintivo del SCP cambia si se cambia el nombre del equipo o se mueve a otro dominio o unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-119">For example, if you create an SCP as a child of a computer object, the distinguished name of the SCP changes if the computer is renamed or moved to a different domain or organizational unit.</span></span>

<span data-ttu-id="a6ef3-120">Cuando un instalador de servicio crea un SCP, debe leer el **objectGUID** del objeto recién creado y almacenarlo en caché en el registro del equipo host del servicio.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-120">When a service installer creates an SCP, it must read the **objectGUID** of the newly created object and cache it in the registry of the service host computer.</span></span> <span data-ttu-id="a6ef3-121">Use el método [**IADs:: get \_ GUID**](/windows/desktop/ADSI/iads-property-methods) para obtener el valor **objectGUID** en formato de cadena adecuado para el enlace.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-121">Use the [**IADs::get\_GUID**](/windows/desktop/ADSI/iads-property-methods) method to get the **objectGUID** value in string format suitable for binding.</span></span> <span data-ttu-id="a6ef3-122">Almacene en caché la cadena de GUID como un valor en la siguiente clave del registro.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-122">Cache the GUID string as a value under the following registry key.</span></span>

```
HKEY_LOCAL_MACHINE
   vendor name
      product name
```

<span data-ttu-id="a6ef3-123">Donde "Vendor name" y "Product Name" identifican el proveedor y el producto.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-123">Where "vendor name" and "product name" identify the vendor and product.</span></span>

<span data-ttu-id="a6ef3-124">Cuando se inicia el servicio, recupera la cadena de GUID en caché del registro y la usa para enlazar con el SCP.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-124">When the service starts, it retrieves the cached GUID string from the registry and uses it to bind to the SCP.</span></span> <span data-ttu-id="a6ef3-125">El servicio Lee los atributos de SCP importantes y los compara con los valores actuales.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-125">The service reads the important SCP attributes and compares them to current values.</span></span> <span data-ttu-id="a6ef3-126">Si los valores de SCP no están actualizados, el servicio los actualiza.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-126">If the SCP values are outdated, the service updates them.</span></span> <span data-ttu-id="a6ef3-127">Los valores que el servicio puede necesitar para actualizar incluyen **palabras clave**, **serviceBindingInformation**, **serviceDNSName** y **serviceDNSNameType**.</span><span class="sxs-lookup"><span data-stu-id="a6ef3-127">Values that the service might require to update include **keywords**, **serviceBindingInformation**, **serviceDNSName**, and **serviceDNSNameType**.</span></span>

## <a name="examples"></a><span data-ttu-id="a6ef3-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a6ef3-128">Examples</span></span>

-   [<span data-ttu-id="a6ef3-129">Ejemplos de scripts</span><span class="sxs-lookup"><span data-stu-id="a6ef3-129">Script samples</span></span>](script-samples-for-managing-service-connection-points.md)
-   [<span data-ttu-id="a6ef3-130">Ejemplos de código (C/C++)</span><span class="sxs-lookup"><span data-stu-id="a6ef3-130">Code (C/C++) samples</span></span>](code-samples-for-managing-service-connection-points.md)

 

 