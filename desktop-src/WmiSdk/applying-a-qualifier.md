---
description: Al igual que muchas otras técnicas de Managed Object Format (MOF), aplicar un calificador al código es un proceso relativamente sencillo.
ms.assetid: aaa5c921-bdcd-40e6-ab4b-9441a1957e5b
ms.tgt_platform: multiple
title: Aplicación de un calificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a393c7d3764338a8365ad3959803a8a3f665dbf1b9bdb0bebaaa7121ee6cb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320142"
---
# <a name="applying-a-qualifier"></a>Aplicación de un calificador

Al igual que muchas otras técnicas de Managed Object Format (MOF), aplicar un calificador al código es un proceso relativamente sencillo.

Los únicos desafíos reales son las restricciones siguientes en las convenciones de nomenclatura que aplica WMI:

-   Un calificador puede describir una clase, instancia, propiedad, método o parámetro de método.
-   Los nombres de calificador no pueden tener caracteres de subrayado iniciales o finales.
-   Un nombre de calificador no puede comenzar con un dígito.
-   Un nombre de calificador no puede contener caracteres especiales como & \* @ ! ~ \\ /.
-   Todos los nombres de calificador no tienen en cuenta las mayúsculas y minúsculas.
-   No se pueden volver a definir los calificadores WMI estándar ni los calificadores descritos en la especificación DE CIM de DMTF.
-   Los tipos de calificador no se declaran explícitamente.

    Si no declara un tipo de calificador, WMI asume el tipo como booleano con un valor **true.** De lo contrario, WMI tipos calificadores en función de los valores de calificador que declare.

-   Al crear sus propios calificadores, debe antefique el nombre del esquema en el nombre del calificador.

    El propósito de esta regla es evitar confusiones con nuevos calificadores.

-   Puede crear matrices homogéneos de calificadores.

    En el ejemplo de código siguiente se muestra cómo se especifican las matrices de calificador con llaves que rodean los valores.

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   WMI no admite tipos de automatización que no aparecen en la referencia, como VT \_ NULL. Para obtener más información, vea [Tipos de datos MOF](mof-data-types.md).

El procedimiento siguiente le ayuda a usar C++ para agregar un calificador a una propiedad.

**Para aplicar un calificador mediante C++**

-   Aplique el calificador con una llamada [**al método IWbemQualifierSet::P ut.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put)

    Puede usar otros métodos de [**IWbemQualifierSet para**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) recuperar o eliminar calificadores existentes.

El procedimiento siguiente le ayuda a aplicar un calificador en archivos MOF.

**Para describir una palabra clave o un identificador con un calificador mediante MOF**

-   Coloque un calificador entre corchetes antes de la palabra clave o identificador que describe el calificador.

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

    En el ejemplo siguiente se describe la ubicación adecuada de los calificadores.

    ``` syntax
    [Abstract]
    class MyClass
    {
        [Amendment, InstanceOf]  uint32 dwNumber;
        sint32 MyMethod ([in] sint32 Param);
    };
    ```

 

 



