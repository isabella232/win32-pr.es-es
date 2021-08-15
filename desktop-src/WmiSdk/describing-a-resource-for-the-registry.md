---
description: El registro del sistema contiene datos relacionados con los recursos.
ms.assetid: e66f1db8-a5f3-41d3-9835-34b81b9da5ed
ms.tgt_platform: multiple
title: Descripción de un recurso para el Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30be25eed569f212e435827023eed132cf1c6ead49be37eabb6fe4ac30e8e3b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097275"
---
# <a name="describing-a-resource-for-the-registry"></a>Descripción de un recurso para el Registro

El registro del sistema contiene datos relacionados con los recursos. Estos datos se encuentran en la siguiente clave del Registro y se mantienen en un tipo de datos del Registro especial denominado **REG \_ RESOURCE \_ LIST**. Las aplicaciones pueden obtener los datos relacionados con los recursos a través del proveedor del Registro del sistema. Puede agregar y modificar recursos del sistema en el Registro.

```
HKEY_LOCAL_MACHINE
   Hardware
      ResourceMap
```

En el procedimiento siguiente se describe cómo almacenar información relacionada con los recursos en el registro del sistema.

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
    Isa<br />
    Eisa<br />
    Microchannel<br />
    TurboChannel<br />
    PCIBus<br />
    Vmebus<br />
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
    <td>Desplazamiento o tipo de unión</td>
    <td>Uno de los siguientes valores:<br/> <dl> Port.Start<br />
    Port.PhysicalAddress<br />
    Port.Length<br />
    Interrupt.Level<br />
    Interrupt.Vector<br />
    Interrupt.Affinity<br />
    Memory.Start<br />
    Memory.PhysicalAddress<br />
    Memory.Length<br />
    Dma.Channel<br />
    Dma.Port<br />
    Dma.Reserved1<br />
    DeviceSpecificData.DataSize<br />
    DeviceSpecificData.Reserved1<br />
    DeviceSpecificData.Reserved2<br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Coloque la cadena en la clave adecuada debajo de la clave del Registro.

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

En el ejemplo de código siguiente se muestra una sintaxis MOF válida para recuperar un descriptor de recursos.

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

 

 




