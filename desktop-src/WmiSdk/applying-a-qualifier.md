---
description: Al igual que muchas otras técnicas de Managed Object Format (MOF), la aplicación de un calificador al código es un proceso relativamente sencillo.
ms.assetid: aaa5c921-bdcd-40e6-ab4b-9441a1957e5b
ms.tgt_platform: multiple
title: Aplicar un calificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042a3cdbf7236dc838735ce0cbf18a6315dd02e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819395"
---
# <a name="applying-a-qualifier"></a>Aplicar un calificador

Al igual que muchas otras técnicas de Managed Object Format (MOF), la aplicación de un calificador al código es un proceso relativamente sencillo.

Los únicos desafíos reales son las siguientes restricciones en las convenciones de nomenclatura que aplica WMI:

-   Un calificador puede describir una clase, una instancia, una propiedad, un método o un parámetro de método.
-   Los nombres de calificador no pueden tener un carácter de subrayado inicial ni final.
-   Un nombre de calificador no puede comenzar con un dígito.
-   Un nombre de calificador no puede contener caracteres especiales como & \* @! ~ \\ /.
-   Todos los nombres de calificador distinguen mayúsculas de minúsculas.
-   No se pueden volver a definir los calificadores WMI estándar ni los calificadores descritos en la especificación CIM de DMTF.
-   Los tipos de calificador no se declaran explícitamente.

    Si no declara un tipo de calificador, WMI supone que el tipo es booleano con un valor de **true**. De lo contrario, WMI escribe los calificadores basados en los valores de calificador que se declaran.

-   Al crear sus propios calificadores, debe anteponer el nombre del esquema al nombre del calificador.

    El objetivo de esta regla es evitar la confusión con los nuevos calificadores.

-   Puede crear matrices homogéneas de calificadores.

    En el ejemplo de código siguiente se muestra cómo se especifican las matrices de calificador con llaves que rodean los valores.

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   WMI no admite los tipos de automatización que no se enumeran en la referencia, como VT \_ null. Para obtener más información, vea [tipos de datos MOF](mof-data-types.md).

El siguiente procedimiento le ayudará a usar C++ para agregar un calificador a una propiedad.

**Para aplicar un calificador mediante C++**

-   Aplique el calificador con una llamada al método [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .

    Puede usar otros métodos de [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) para recuperar o eliminar calificadores existentes.

El siguiente procedimiento le ayuda a aplicar un calificador en archivos MOF.

**Para describir una palabra clave o un identificador con un calificador mediante MOF**

-   Coloque un calificador entre corchetes antes de la palabra clave o el identificador descrito por el calificador.

    En el ejemplo de código siguiente se muestra cómo se usan los calificadores.

    ``` syntax
    [qualifiers...]
    class StdDisk
    {
      [qualifiers...]  uint32 dwNumCylinders;
      [qualifiers...]  uint32 dwNumHeads;
      [qualifiers...]  sint32 Method1();
      sint32 Method2([qualifiers...] Parameter1);
    };
    ```

    En el siguiente ejemplo se describe la colocación adecuada de los calificadores.

    ``` syntax
    [Abstract]
    class MyClass
    {
        [Amendment, InstanceOf]  uint32 dwNumber;
        sint32 MyMethod ([in] sint32 Param);
    };
    ```

 

 



