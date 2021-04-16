---
description: Puede declarar una instancia básica de una clase en el servicio de administración de Windows mediante Managed Object Format (MOF). También puede invalidar los valores predeterminados para una instancia de. Para obtener más información, vea establecer un valor de propiedad de instancia.
ms.assetid: 12eda062-9614-455d-ae99-7706c685137b
ms.tgt_platform: multiple
title: Crear una instancia mediante MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5078c5fcddaab4e8437a33e8cb3210d515360fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706173"
---
# <a name="creating-an-instance-using-mof"></a>Crear una instancia mediante MOF

Puede declarar una instancia básica de una clase en el servicio de administración de Windows mediante Managed Object Format (MOF). También puede invalidar los valores predeterminados para una instancia de. Para obtener más información, vea [establecer un valor de propiedad de instancia](#setting-an-instance-property-value).

En el procedimiento siguiente se describe cómo declarar una instancia básica de una clase mediante código MOF.

**Para declarar una instancia básica de una clase mediante código MOF**

1.  Use la **instancia de** Keywords seguida del nombre de clase, llaves y un punto y coma.

    En el ejemplo de código siguiente se muestra cómo declarar una instancia de una clase.

    ```mof
    instance of ClassName
    {
    };
    ```

    

2.  Cuando termine, inserte el código MOF en el repositorio WMI mediante el compilador MOF.

    Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).

Una instancia de una clase incluye todas las propiedades de la clase. Si la clase es una clase derivada, las instancias de incluyen las propiedades que pertenecen a todas las clases que se encuentran en una posición superior en la jerarquía. Cada clase de la que se crea una instancia tiene una o más propiedades de clave. No se puede crear una instancia de con más de 256 claves.

## <a name="setting-an-instance-property-value"></a>Establecer un valor de propiedad de instancia

Dado que las propiedades de los tipos fuertemente de WMI, no se pueden modificar los tipos de propiedad. Sin embargo, puede establecer valores de propiedad en instancias de. Cuando una clase asigna un valor predeterminado a una propiedad, WMI asigna el valor predeterminado a cada instancia. Puede invalidar este valor en la declaración de instancia.

En el procedimiento siguiente se describe cómo establecer un valor de propiedad o sobrescribir un valor predeterminado mediante código MOF.

**Para establecer un valor de propiedad o sobrescribir un valor predeterminado mediante código MOF**

1.  Coloque una instrucción de asignación entre las llaves de la declaración de instancia.

    En el ejemplo de código siguiente se muestra cómo establecer un valor de propiedad.

    ``` syntax
    instance of ClassName
    {
        Prop = "value";
    };
    ```

    WMI no requiere que se establezca ninguna propiedad durante la creación de la instancia. La excepción es cualquier propiedad marcada con el calificador de [**clave**](key-qualifier.md) . Dado que WMI utiliza propiedades de clave para identificar de forma única las instancias, debe establecer todas las propiedades clave a medida que se encuentren. Por el contrario, no debe establecer una propiedad del sistema en una declaración de instancia. En su lugar, WMI asigna los valores adecuados a una propiedad del sistema cuando es necesario.

2.  Cuando termine, inserte el código MOF en el repositorio WMI con una llamada al compilador MOF.

    Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).

En los ejemplos de código siguientes se muestra cómo una instancia de especifica los datos para las propiedades definidas por una clase.

``` syntax
class MyClass 
{
    [key] string   strProp;
    sint32   dwProp1;
    uint32       dwProp2;
};

instance of MyClass 
{
    strProp = "hello";
    dwProp1 = -1;
    dwProp2 = 0xffffffff;
};
```

En el ejemplo anterior, la clase define tres propiedades: una cadena de caracteres, un entero con signo de 32 bits y un entero de 32 bits sin signo. La instancia de proporciona valores de datos para cada una de estas propiedades.

 

 



