---
description: El registro del sistema contiene datos relacionados con recursos.
ms.assetid: e66f1db8-a5f3-41d3-9835-34b81b9da5ed
ms.tgt_platform: multiple
title: Descripción de un recurso para el registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba175120b5abec238d1b9078010359effef8ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706813"
---
# <a name="describing-a-resource-for-the-registry"></a><span data-ttu-id="26946-103">Descripción de un recurso para el registro</span><span class="sxs-lookup"><span data-stu-id="26946-103">Describing a Resource for the Registry</span></span>

<span data-ttu-id="26946-104">El registro del sistema contiene datos relacionados con recursos.</span><span class="sxs-lookup"><span data-stu-id="26946-104">The system registry contains resource-related data.</span></span> <span data-ttu-id="26946-105">Estos datos se encuentran en la siguiente clave del registro y se conservan en un tipo de datos del registro especial denominado **reg \_ Resource \_ List**.</span><span class="sxs-lookup"><span data-stu-id="26946-105">This data is located under the following registry key and is kept in a special registry data type named **REG\_RESOURCE\_LIST**.</span></span> <span data-ttu-id="26946-106">Las aplicaciones pueden obtener los datos relacionados con los recursos a través del proveedor del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="26946-106">Applications can obtain the resource-related data through the System Registry provider.</span></span> <span data-ttu-id="26946-107">Puede Agregar y modificar los recursos del sistema en el registro.</span><span class="sxs-lookup"><span data-stu-id="26946-107">You can add and modify system resources in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   Hardware
      ResourceMap
```

<span data-ttu-id="26946-108">En el procedimiento siguiente se describe cómo almacenar información relacionada con recursos en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="26946-108">The following procedure describes how to store resource-related information in the system registry.</span></span>

<span data-ttu-id="26946-109">**Para almacenar información relacionada con recursos en el registro del sistema**</span><span class="sxs-lookup"><span data-stu-id="26946-109">**To store resource-related information in the system registry**</span></span>

1.  <span data-ttu-id="26946-110">Cree una cadena que contenga los campos siguientes.</span><span class="sxs-lookup"><span data-stu-id="26946-110">Create a string that contains the following fields.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="26946-111">Campo</span><span class="sxs-lookup"><span data-stu-id="26946-111">Field</span></span></th>
    <th><span data-ttu-id="26946-112">Contiene</span><span class="sxs-lookup"><span data-stu-id="26946-112">Contains</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="26946-113">Tipo de interfaz</span><span class="sxs-lookup"><span data-stu-id="26946-113">Interface type</span></span></td>
    <td><span data-ttu-id="26946-114">Uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="26946-114">One of the following values:</span></span><br/> <dl> <span data-ttu-id="26946-115">Interno</span><span class="sxs-lookup"><span data-stu-id="26946-115">Internal</span></span><br />
    <span data-ttu-id="26946-116">Ejecuta</span><span class="sxs-lookup"><span data-stu-id="26946-116">Isa</span></span><br />
    <span data-ttu-id="26946-117">Complementaria</span><span class="sxs-lookup"><span data-stu-id="26946-117">Eisa</span></span><br />
    <span data-ttu-id="26946-118">Microcanal</span><span class="sxs-lookup"><span data-stu-id="26946-118">MicroChannel</span></span><br />
    <span data-ttu-id="26946-119">TurboChannel</span><span class="sxs-lookup"><span data-stu-id="26946-119">TurboChannel</span></span><br />
    <span data-ttu-id="26946-120">PCIBus</span><span class="sxs-lookup"><span data-stu-id="26946-120">PCIBus</span></span><br />
    <span data-ttu-id="26946-121">VMEBus</span><span class="sxs-lookup"><span data-stu-id="26946-121">VMEBus</span></span><br />
    <span data-ttu-id="26946-122">NuBus</span><span class="sxs-lookup"><span data-stu-id="26946-122">NuBus</span></span><br />
    <span data-ttu-id="26946-123">PCMCIABus</span><span class="sxs-lookup"><span data-stu-id="26946-123">PCMCIABus</span></span><br />
    <span data-ttu-id="26946-124">CBus</span><span class="sxs-lookup"><span data-stu-id="26946-124">CBus</span></span><br />
    <span data-ttu-id="26946-125">MPIBus</span><span class="sxs-lookup"><span data-stu-id="26946-125">MPIBus</span></span><br />
    <span data-ttu-id="26946-126">MPSABus</span><span class="sxs-lookup"><span data-stu-id="26946-126">MPSABus</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="26946-127">Número de bus</span><span class="sxs-lookup"><span data-stu-id="26946-127">Bus number</span></span></td>
    <td><span data-ttu-id="26946-128">Entero que especifica el número de bus.</span><span class="sxs-lookup"><span data-stu-id="26946-128">Integer specifying the bus number.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="26946-129">Número de descriptor parcial</span><span class="sxs-lookup"><span data-stu-id="26946-129">Partial descriptor number</span></span></td>
    <td><span data-ttu-id="26946-130">Entero que especifica el número de descriptor.</span><span class="sxs-lookup"><span data-stu-id="26946-130">Integer specifying the descriptor number.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="26946-131">Desplazamiento o tipo de Unión</span><span class="sxs-lookup"><span data-stu-id="26946-131">Offset or union type</span></span></td>
    <td><span data-ttu-id="26946-132">Uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="26946-132">One of the following values:</span></span><br/> <dl> <span data-ttu-id="26946-133">Puerto. Inicio</span><span class="sxs-lookup"><span data-stu-id="26946-133">Port.Start</span></span><br />
    <span data-ttu-id="26946-134">Puerto. PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="26946-134">Port.PhysicalAddress</span></span><br />
    <span data-ttu-id="26946-135">Port. length</span><span class="sxs-lookup"><span data-stu-id="26946-135">Port.Length</span></span><br />
    <span data-ttu-id="26946-136">Nivel de interrupción</span><span class="sxs-lookup"><span data-stu-id="26946-136">Interrupt.Level</span></span><br />
    <span data-ttu-id="26946-137">Interrupt. Vector</span><span class="sxs-lookup"><span data-stu-id="26946-137">Interrupt.Vector</span></span><br />
    <span data-ttu-id="26946-138">Interrupt. Affinity</span><span class="sxs-lookup"><span data-stu-id="26946-138">Interrupt.Affinity</span></span><br />
    <span data-ttu-id="26946-139">Memoria. Inicio</span><span class="sxs-lookup"><span data-stu-id="26946-139">Memory.Start</span></span><br />
    <span data-ttu-id="26946-140">Memoria. PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="26946-140">Memory.PhysicalAddress</span></span><br />
    <span data-ttu-id="26946-141">Memoria. longitud</span><span class="sxs-lookup"><span data-stu-id="26946-141">Memory.Length</span></span><br />
    <span data-ttu-id="26946-142">DMA. canal</span><span class="sxs-lookup"><span data-stu-id="26946-142">Dma.Channel</span></span><br />
    <span data-ttu-id="26946-143">DMA. Puerto</span><span class="sxs-lookup"><span data-stu-id="26946-143">Dma.Port</span></span><br />
    <span data-ttu-id="26946-144">DMA. Reserved1</span><span class="sxs-lookup"><span data-stu-id="26946-144">Dma.Reserved1</span></span><br />
    <span data-ttu-id="26946-145">DeviceSpecificData. Datasize</span><span class="sxs-lookup"><span data-stu-id="26946-145">DeviceSpecificData.DataSize</span></span><br />
    <span data-ttu-id="26946-146">DeviceSpecificData. Reserved1</span><span class="sxs-lookup"><span data-stu-id="26946-146">DeviceSpecificData.Reserved1</span></span><br />
    <span data-ttu-id="26946-147">DeviceSpecificData.Reserved2</span><span class="sxs-lookup"><span data-stu-id="26946-147">DeviceSpecificData.Reserved2</span></span><br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="26946-148">Coloque la cadena en la clave adecuada en la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="26946-148">Place the string in the appropriate key under the registry key.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Hardware
          ResourceMap
    ```

<span data-ttu-id="26946-149">En el ejemplo de código siguiente se describe un descriptor de recursos válido.</span><span class="sxs-lookup"><span data-stu-id="26946-149">The following code example describes a valid resource descriptor.</span></span>

``` syntax
local|hkey_local_machine\hardware\resourcemap\
  hardware abstraction layer\
  pc compatible eisa/isa HAL|.raw("eisa",0,0,"interrupt.affinity")
```

<span data-ttu-id="26946-150">En el ejemplo de código siguiente se muestra la sintaxis MOF válida para recuperar un descriptor de recursos.</span><span class="sxs-lookup"><span data-stu-id="26946-150">The following code example shows valid MOF syntax for retrieving a resource descriptor.</span></span>

``` syntax
[DYNPROPS] 
class MyRegProp
{    
   [KEY]  
   STRING MyKey; 
   STRING MyReservedTranslated;
};

[DYNPROPS] 
instance of MyRegProp
{
   MyKey = "1";
   [PropertyContext("local|hkey_local_Machine\\hardware\\ResourceMap\\
                   System Resources\\Reserved|.Translated
                   (\"Internal\")(0)(1)(\"Memory.PhysicalAddress\")"),
   Dynamic, Provider("RegPropProv")] 
   MyReservedTranslated;
};
```

 

 




