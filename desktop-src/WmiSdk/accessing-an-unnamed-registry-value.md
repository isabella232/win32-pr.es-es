---
description: Acceso a un valor del Registro sin nombre
ms.assetid: 1095da4c-8b9f-4674-9801-f2d25c4f372b
ms.tgt_platform: multiple
title: Acceso a un valor del Registro sin nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92860d240598f0353d1f4c9f41a77306942d272b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465785"
---
# <a name="accessing-an-unnamed-registry-value"></a>Acceso a un valor del Registro sin nombre

El valor predeterminado o sin nombre de una clave del Registro se muestra como (valor predeterminado) o en el <No Name> editor del Registro Regedit. Puede usar el proveedor del Registro del sistema para acceder a una clave del Registro sin nombre. De forma similar, también puede usar el proveedor del Registro del sistema para tener acceso a las descripciones de mapa de bits, que se definen como valores sin nombre.

En el procedimiento siguiente se describe cómo recuperar un valor del Registro sin nombre.

**Para recuperar un valor del Registro sin nombre**

1.  Defina una propiedad y establezca el **calificador PropertyContext** de esa propiedad en una cadena vacía.

    En el ejemplo de código siguiente se muestra cómo la clase define las propiedades para contener valores para la clave especificada por el **calificador ClassContext.** El valor predeterminado se almacena en la **propiedad Default.**

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

    La clave Transports no usa el valor sin nombre, por lo que la compilación de este archivo MOF no genera ningún valor para la propiedad **Default** a menos que se use una herramienta de edición del Registro para cambiar el valor sin nombre.

2.  Para un archivo de mapa de bits, defina una propiedad y establezca **el PropertyContext** de esa propiedad.

    En el ejemplo de código siguiente se muestra cómo definir una propiedad .

    ```mof
    Local|hkey_classes_root\\.bmp
    ```

    

 

 



