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
# <a name="describing-a-resource-for-the-registry"></a>Descripción de un recurso para el registro

El registro del sistema contiene datos relacionados con recursos. Estos datos se encuentran en la siguiente clave del registro y se conservan en un tipo de datos del registro especial denominado **reg \_ Resource \_ List**. Las aplicaciones pueden obtener los datos relacionados con los recursos a través del proveedor del registro del sistema. Puede Agregar y modificar los recursos del sistema en el registro.

```
HKEY_LOCAL_MACHINE
   Hardware
      ResourceMap
```

En el procedimiento siguiente se describe cómo almacenar información relacionada con recursos en el registro del sistema.

**Para almacenar información relacionada con recursos en el registro del sistema**

1.  Cree una cadena que contenga los campos siguientes.

    

    <table>
    <thead>
    <tr class="header">
    <th>Campo</th>
    <th>Contiene</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Tipo de interfaz</td>
    <td>Uno de los siguientes valores:<br/> <dl> Interno<br />
    Ejecuta<br />
    Complementaria<br />
    Microcanal<br />
    TurboChannel<br />
    PCIBus<br />
    VMEBus<br />
    NuBus<br />
    PCMCIABus<br />
    CBus<br />
    MPIBus<br />
    MPSABus<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Número de bus</td>
    <td>Entero que especifica el número de bus.</td>
    </tr>
    <tr class="odd">
    <td>Número de descriptor parcial</td>
    <td>Entero que especifica el número de descriptor.</td>
    </tr>
    <tr class="even">
    <td>Desplazamiento o tipo de Unión</td>
    <td>Uno de los siguientes valores:<br/> <dl> Puerto. Inicio<br />
    Puerto. PhysicalAddress<br />
    Port. length<br />
    Nivel de interrupción<br />
    Interrupt. Vector<br />
    Interrupt. Affinity<br />
    Memoria. Inicio<br />
    Memoria. PhysicalAddress<br />
    Memoria. longitud<br />
    DMA. canal<br />
    DMA. Puerto<br />
    DMA. Reserved1<br />
    DeviceSpecificData. Datasize<br />
    DeviceSpecificData. Reserved1<br />
    DeviceSpecificData.Reserved2<br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Coloque la cadena en la clave adecuada en la clave del registro.

    ```
    HKEY_LOCAL_MACHINE
       Hardware
          ResourceMap
    ```

En el ejemplo de código siguiente se describe un descriptor de recursos válido.

``` syntax
local|hkey_local_machine\hardware\resourcemap\
  hardware abstraction layer\
  pc compatible eisa/isa HAL|.raw("eisa",0,0,"interrupt.affinity")
```

En el ejemplo de código siguiente se muestra la sintaxis MOF válida para recuperar un descriptor de recursos.

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

 

 




