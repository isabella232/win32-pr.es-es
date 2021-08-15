---
description: Puede encontrar propiedades estáticas mediante asignaciones de valores parciales.
ms.assetid: 67e91454-c065-4ab2-a373-245c9392c71c
ms.tgt_platform: multiple
title: Localización de propiedades estáticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c51999c68a05e8d7b8cf3fd8c5218bc171931303d86a50c04f32c5d80efb308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050733"
---
# <a name="localizing-static-properties"></a>Localización de propiedades estáticas

Puede encontrar propiedades estáticas mediante asignaciones de valores parciales.

En el procedimiento siguiente se describe cómo se pueden localizar las propiedades estáticas mediante mapas de valores parciales con expresiones regulares.

**Para usar asignaciones de valores para localización de propiedades estáticas**

1.  Cree un archivo MOF maestro (Mastervm.mof).

    El ejemplo de código siguiente se puede usar para crear un archivo MOF maestro (Mastervm.mof).

    ```syntax
    [Locale(0x409)]
    class Group1
    {
        [key] string ID;
        [DisplayName("Numbers"),
            ValueMap{0,1,2,3}:amended,
            Values{"Zero", "One", "Two", "Three"}:amended]
        Uint32 Numbers;
    };
    ```

2.  Cree las versiones neutras del idioma y específicas del idioma del archivo MOF.

    Escriba el siguiente comando en un símbolo del sistema para crear las versiones neutras del lenguaje y específicas del lenguaje del archivo MOF.

    ```syntax
    mofcomp -MOF:LnVm.mof -MFL:LsVm.mfl -Amendment:MS_409 MasterVm.mof
    ```

    El compilador de MOF genera los archivos MOF específicos y neutrales del lenguaje, LnVm.mof y LsVm.mfl. Los valores de inglés estadounidense para la [propiedad Numbers](numbers.md) se colocan en el archivo .mfl para el espacio de nombres inglés de Estados Unidos.

    En el ejemplo de código siguiente se muestra el contenido del archivo LsVm.mfl.

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_409";};
    #pragma namespace("\\\\.\\root\\default\\ms_409")

    [AMENDMENT, LOCALE(0x409)] 
    class Group1
    {
      [ValueMap{0, 1, 2, 3} : Amended,
          Values{"Zero", "One", "Two", "Three"} : Amended] 
      Uint32 Numbers;
    };
    ```

3.  Compile los dos archivos MOF y almacene la información de clase en el repositorio CIM.

    Escriba el siguiente comando en un símbolo del sistema para compilar los dos archivos MOF.

    ```syntax
    Mofcomp LnVm.mof 
    Mofcomp LsVm.mfl
    ```

4.  Localice el archivo MFL para otras configuraciones regionales.

    En el ejemplo de código siguiente se muestra el contenido de un archivo MFL para el espacio de nombres francés.

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_40C";};
    #pragma namespace("\\\\.\\root\\default\\ms_40C")

    [AMENDMENT, LOCALE(0x40C)] 
    class Group1
    {
        [key] string ID;
        [ValueMap{0, 1, 2, 3} : Amended,
            Values{"Zero", "Un", "Deux", "Trois"} : Amended]
        Uint32 Numbers;
    };
    ```

El resultado neto es que tanto el nombre para mostrar como el valor de la propiedad [Numbers](numbers.md) dependen de la configuración regional del usuario que ha iniciado sesión. Si el usuario especifica una configuración regional que no se ha proporcionado, los datos de calificador predeterminados proceden del espacio de nombres inglés (ms \_ 409).

La implicación de este diseño es que cada valor de cadena se usa como identificador de búsqueda, que no se puede localizar. Al definir este esquema, debe asegurarse de que el valor que coloca el proveedor es independiente de la configuración regional.

> [!Note]  
> WMI no proporciona actualmente compatibilidad en tiempo de ejecución para asignar valores a cadenas definidas por calificadores. La interpretación de la sintaxis sugerida es responsabilidad de la aplicación.

 

 

 



