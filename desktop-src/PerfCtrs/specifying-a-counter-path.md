---
description: El sistema utiliza contadores para recopilar datos de rendimiento.
ms.assetid: d1f1a90c-425a-4606-b86d-2948305ea84a
title: Specifying a Counter Path (Especificar una ruta de acceso de contador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3a92f94b4bf3d2252903d92785f43bb0cac110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667247"
---
# <a name="specifying-a-counter-path"></a><span data-ttu-id="5f581-103">Specifying a Counter Path (Especificar una ruta de acceso de contador)</span><span class="sxs-lookup"><span data-stu-id="5f581-103">Specifying a Counter Path</span></span>

<span data-ttu-id="5f581-104">El sistema utiliza contadores para recopilar datos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="5f581-104">The system uses counters to collect performance data.</span></span> <span data-ttu-id="5f581-105">Cada contador se identifica de forma única a través de su nombre y su ruta de acceso, o ubicación.</span><span class="sxs-lookup"><span data-stu-id="5f581-105">Each counter is uniquely identified through its name and its path, or location.</span></span> <span data-ttu-id="5f581-106">La sintaxis de una ruta de contador es:</span><span class="sxs-lookup"><span data-stu-id="5f581-106">The syntax of a counter path is:</span></span>

``` syntax
\\Computer\PerfObject(ParentInstance/ObjectInstance#InstanceIndex)\Counter
```

<span data-ttu-id="5f581-107">El elemento Computer especifica el nombre o la dirección IP del equipo desde el que desea consultar los datos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="5f581-107">The Computer element specifies the name or IP address of the computer from which you want to query performance data.</span></span> <span data-ttu-id="5f581-108">El nombre del equipo es opcional si el contador se encuentra en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="5f581-108">The computer name is optional if the counter is located on the local computer.</span></span>

<span data-ttu-id="5f581-109">El elemento PerfObject especifica el objeto de rendimiento que se va a consultar.</span><span class="sxs-lookup"><span data-stu-id="5f581-109">The PerfObject element specifies the performance object to query.</span></span> <span data-ttu-id="5f581-110">Un objeto de rendimiento puede ser un componente físico, como procesadores, discos y memoria, o un objeto del sistema, como procesos y subprocesos.</span><span class="sxs-lookup"><span data-stu-id="5f581-110">A performance object can be a physical component, such as processors, disks, and memory, or a system object, such as processes and threads.</span></span> <span data-ttu-id="5f581-111">Cada objeto del sistema está relacionado con un elemento funcional del equipo y tiene un conjunto de contadores estándar asignados.</span><span class="sxs-lookup"><span data-stu-id="5f581-111">Each system object is related to a functional element within the computer and has a set of standard counters assigned to it.</span></span> <span data-ttu-id="5f581-112">Cada equipo puede tener un conjunto diferente de objetos y contadores de rendimiento instalados en él, ya que las aplicaciones pueden instalar sus propios objetos y contadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="5f581-112">Each computer may have a different set of performance objects and counters installed on it because applications can install their own performance objects and counters.</span></span> <span data-ttu-id="5f581-113">Para obtener una lista de los objetos y contadores de rendimiento instalados en el equipo, vea el cuadro de diálogo **Agregar contadores** en la herramienta rendimiento del equipo.</span><span class="sxs-lookup"><span data-stu-id="5f581-113">For a list of the performance objects and counters installed on your computer, see the **Add Counters** dialog box in the Performance tool on your computer.</span></span> <span data-ttu-id="5f581-114">Estos objetos también se muestran en el cuadro de diálogo examinar de PDH (vea [contadores de exploración](browsing-counters.md)).</span><span class="sxs-lookup"><span data-stu-id="5f581-114">These objects are also listed in the PDH browse dialog box (see [Browsing Counters](browsing-counters.md)).</span></span> <span data-ttu-id="5f581-115">Para obtener una lista de los objetos y contadores de rendimiento del sistema, vea [contadores por objeto](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="5f581-115">For a list of system performance objects and counters, see [Counters by Object](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).</span></span>

<span data-ttu-id="5f581-116">ParentInstance, ObjectInstance y InstanceIndex se incluyen en la ruta de acceso si pueden existir varias instancias del objeto.</span><span class="sxs-lookup"><span data-stu-id="5f581-116">The ParentInstance, ObjectInstance, and InstanceIndex are included in the path if multiple instances of the object can exist.</span></span> <span data-ttu-id="5f581-117">Por ejemplo, los procesos y subprocesos son varios objetos de instancia porque se puede ejecutar más de un proceso o subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="5f581-117">For example, processes and threads are multiple instance objects because more than one process or thread can run at the same time.</span></span> <span data-ttu-id="5f581-118">Si un objeto puede tener más de una instancia, la ruta de acceso del contador debe especificar una instancia de objeto.</span><span class="sxs-lookup"><span data-stu-id="5f581-118">If an object can have more than one instance, the counter path must specify an object instance.</span></span>

<span data-ttu-id="5f581-119">El formato de los elementos relacionados con la instancia depende del tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="5f581-119">The format of the instance related elements depends on the object type.</span></span> <span data-ttu-id="5f581-120">Si el objeto tiene instancias simples, el formato es solo el nombre de la instancia entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="5f581-120">If the object has simple instances, then the format is only the instance name enclosed in parentheses.</span></span> <span data-ttu-id="5f581-121">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5f581-121">For example:</span></span>

``` syntax
(Explorer)
```

<span data-ttu-id="5f581-122">Si la instancia de este objeto también requiere un nombre de instancia primaria, el nombre de la instancia primaria debe ir delante de la instancia del objeto y estar separado por un carácter de barra diagonal.</span><span class="sxs-lookup"><span data-stu-id="5f581-122">If the instance of this object also requires a parent instance name, the parent instance name must come before the object instance and be separated by a forward slash character.</span></span> <span data-ttu-id="5f581-123">Por ejemplo, los subprocesos pertenecen a procesos.</span><span class="sxs-lookup"><span data-stu-id="5f581-123">For example, threads belong to processes.</span></span> <span data-ttu-id="5f581-124">Si consulta un objeto de subproceso, también debe especificar el proceso al que pertenece, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5f581-124">If you query a thread object, you must also specify the process to which it belongs as shown in the following example:</span></span>

``` syntax
(Explorer/0)
```

<span data-ttu-id="5f581-125">Si el objeto tiene varias instancias que tienen la misma cadena de nombre, se pueden indexar secuencialmente especificando el índice de instancia precedido por un signo de almohadilla.</span><span class="sxs-lookup"><span data-stu-id="5f581-125">If the object has multiple instances that have the same name string, they can be indexed sequentially by specifying the instance index prefixed by a pound sign.</span></span> <span data-ttu-id="5f581-126">Los índices de instancia se basan en 0.</span><span class="sxs-lookup"><span data-stu-id="5f581-126">Instance indexes are 0-based.</span></span> <span data-ttu-id="5f581-127">Si desea consultar la primera instancia, no incluya \# 0, simplemente especifique el nombre de la instancia.</span><span class="sxs-lookup"><span data-stu-id="5f581-127">If you want to query the first instance, do not include \#0—just specify the instance name.</span></span> <span data-ttu-id="5f581-128">Para especificar la segunda instancia, use \# 1; para especificar la tercera instancia, use \# 2; y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="5f581-128">To specify the second instance, use \#1; to specify the third instance, use \#2; and so on.</span></span> <span data-ttu-id="5f581-129">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5f581-129">For example:</span></span>

``` syntax
(Explorer/0#1)
```

<span data-ttu-id="5f581-130">El elemento Counter especifica el contador de rendimiento que desea consultar para el objeto de rendimiento dado.</span><span class="sxs-lookup"><span data-stu-id="5f581-130">The Counter element specifies the performance counter that you want to query for the given the performance object.</span></span>

<span data-ttu-id="5f581-131">PDH usa los siguientes caracteres especiales en una ruta de acceso de contador.</span><span class="sxs-lookup"><span data-stu-id="5f581-131">PDH uses the following special characters in a counter path.</span></span> <span data-ttu-id="5f581-132">Los proveedores no deben usar estos caracteres en sus nombres.</span><span class="sxs-lookup"><span data-stu-id="5f581-132">Providers should not use these characters in their names.</span></span> <span data-ttu-id="5f581-133">Si un proveedor usa estos caracteres especiales, PDH no puede analizar la ruta de acceso completa del contador para obtener los nombres del contador y de las instancias.</span><span class="sxs-lookup"><span data-stu-id="5f581-133">If a provider uses these special characters, PDH cannot parse the full counter path to obtain the counter and instances names.</span></span>



| <span data-ttu-id="5f581-134">Carácter</span><span class="sxs-lookup"><span data-stu-id="5f581-134">Character</span></span> | <span data-ttu-id="5f581-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f581-135">Description</span></span>                                                |
|-----------|------------------------------------------------------------|
| \\        | <span data-ttu-id="5f581-136">Separador genérico para el equipo, el objeto y el contador.</span><span class="sxs-lookup"><span data-stu-id="5f581-136">Generic separator for computer, object, and counter.</span></span>       |
| <span data-ttu-id="5f581-137">(</span><span class="sxs-lookup"><span data-stu-id="5f581-137">(</span></span>         | <span data-ttu-id="5f581-138">Inicio del nombre de instancia.</span><span class="sxs-lookup"><span data-stu-id="5f581-138">Beginning of instance name.</span></span>                                |
| <span data-ttu-id="5f581-139">)</span><span class="sxs-lookup"><span data-stu-id="5f581-139">)</span></span>         | <span data-ttu-id="5f581-140">Final del nombre de instancia.</span><span class="sxs-lookup"><span data-stu-id="5f581-140">Ending of instance name.</span></span>                                   |
| /         | <span data-ttu-id="5f581-141">Separa la instancia y la instancia primaria.</span><span class="sxs-lookup"><span data-stu-id="5f581-141">Separates instance and parent instance.</span></span>                    |
| <span data-ttu-id="5f581-142">\#n</span><span class="sxs-lookup"><span data-stu-id="5f581-142">\#n</span></span>       | <span data-ttu-id="5f581-143">Identifica una aparición específica de una instancia con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="5f581-143">Identifies a specific occurrence of a same-named instance.</span></span> |
| \*        | <span data-ttu-id="5f581-144">Carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="5f581-144">Wildcard character.</span></span>                                        |



 

<span data-ttu-id="5f581-145">En los ejemplos siguientes se muestran los posibles formatos de las rutas de acceso de contador:</span><span class="sxs-lookup"><span data-stu-id="5f581-145">The following examples show the possible formats for counter paths:</span></span>

-   <span data-ttu-id="5f581-146">\\\\contador de objeto de equipo \\ (índice de instancia/principal \# ) \\</span><span class="sxs-lookup"><span data-stu-id="5f581-146">\\\\computer\\object(parent/instance\#index)\\counter</span></span>
-   <span data-ttu-id="5f581-147">\\\\\\contador objeto de equipo (principal/instancia) \\</span><span class="sxs-lookup"><span data-stu-id="5f581-147">\\\\computer\\object(parent/instance)\\counter</span></span>
-   <span data-ttu-id="5f581-148">\\\\contador de objeto de equipo \\ (índice de instancia \# ) \\</span><span class="sxs-lookup"><span data-stu-id="5f581-148">\\\\computer\\object(instance\#index)\\counter</span></span>
-   <span data-ttu-id="5f581-149">\\\\contador de objeto de equipo \\ (instancia) \\</span><span class="sxs-lookup"><span data-stu-id="5f581-149">\\\\computer\\object(instance)\\counter</span></span>
-   <span data-ttu-id="5f581-150">\\\\\\contador de objetos de equipo \\</span><span class="sxs-lookup"><span data-stu-id="5f581-150">\\\\computer\\object\\counter</span></span>
-   <span data-ttu-id="5f581-151">\\contador de objeto (índice de instancia/principal \# ) \\</span><span class="sxs-lookup"><span data-stu-id="5f581-151">\\object(parent/instance\#index)\\counter</span></span>
-   <span data-ttu-id="5f581-152">\\contador de objeto (primario/instancia) \\</span><span class="sxs-lookup"><span data-stu-id="5f581-152">\\object(parent/instance)\\counter</span></span>
-   <span data-ttu-id="5f581-153">\\contador de objeto (índice de instancia \# ) \\</span><span class="sxs-lookup"><span data-stu-id="5f581-153">\\object(instance\#index)\\counter</span></span>
-   <span data-ttu-id="5f581-154">\\contador de objeto (instancia) \\</span><span class="sxs-lookup"><span data-stu-id="5f581-154">\\object(instance)\\counter</span></span>
-   <span data-ttu-id="5f581-155">\\contador de objetos \\</span><span class="sxs-lookup"><span data-stu-id="5f581-155">\\object\\counter</span></span>

## <a name="using-wildcard-characters"></a><span data-ttu-id="5f581-156">Usar caracteres comodín</span><span class="sxs-lookup"><span data-stu-id="5f581-156">Using wildcard characters</span></span>

<span data-ttu-id="5f581-157">Las rutas de acceso de contador solo pueden contener un carácter comodín para el nombre de instancia, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="5f581-157">Counter paths may contain a wildcard character only for the instance name as shown in the following example.</span></span>

``` syntax
\Process(*)\% Processor Time
```

<span data-ttu-id="5f581-158">Para expandir el carácter comodín en una lista de rutas de acceso de contador que contengan instancias encontradas en el equipo o en el archivo de registro, llame a [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).</span><span class="sxs-lookup"><span data-stu-id="5f581-158">To expand the wildcard into a list of counter paths that contain instances found on the computer or in the log file, call [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).</span></span>

 

 
