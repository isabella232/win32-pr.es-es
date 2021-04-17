---
description: Obtener acceso a un valor del registro sin nombre
ms.assetid: 1095da4c-8b9f-4674-9801-f2d25c4f372b
ms.tgt_platform: multiple
title: Obtener acceso a un valor del registro sin nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92860d240598f0353d1f4c9f41a77306942d272b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707101"
---
# <a name="accessing-an-unnamed-registry-value"></a>Obtener acceso a un valor del registro sin nombre

El valor predeterminado o sin nombre de una clave del registro se muestra como (valor predeterminado) o <No Name> en el editor del registro de regedit. Puede utilizar el proveedor del registro del sistema para tener acceso a una clave del registro sin nombre. Del mismo modo, también puede utilizar el proveedor del registro del sistema para obtener acceso a las descripciones de mapas de bits, que se definen como valores sin nombre.

En el procedimiento siguiente se describe cómo recuperar un valor del registro sin nombre.

**Para recuperar un valor del registro sin nombre**

1.  Defina una propiedad y establezca el calificador **PropertyContext** de esa propiedad en una cadena vacía.

    En el ejemplo de código siguiente se muestra cómo la clase define las propiedades para contener los valores de la clave especificada por el calificador **ClassContext** . El valor predeterminado se almacena en la propiedad **predeterminada** .

    ``` syntax
    [dynamic, 
     provider("RegProv"), 
     ClassContext("local|hkey_local_machine\\software\\"
     "microsoft\\Active Setup\\Installed Components")]

    class RegTrans{
      [key] String Transports="";
      [PropertyContext("")] String Default;
      [PropertyContext("ComponentId")] String ComponentID;
      [PropertyContext("Locale")] String Locale;
    };
    ```

    La clave de transportes no utiliza el valor sin nombre, por lo que la compilación de este archivo MOF no genera ningún valor para la propiedad **predeterminada** a menos que se use una herramienta de edición del registro para cambiar el valor sin nombre.

2.  Para un archivo de mapa de bits, defina una propiedad y establezca el valor de **PropertyContext** de esa propiedad.

    En el ejemplo de código siguiente se muestra cómo definir una propiedad.

    ```mof
    Local|hkey_classes_root\\.bmp
    ```

    

 

 



