---
description: Una clase de asociación es un tipo especial de clase que define una relación entre otras dos clases.
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: Declarar una clase de asociación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ce578ca912290fd026f225799793f89685aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083138"
---
# <a name="declaring-an-association-class"></a>Declarar una clase de asociación

Una clase de asociación es un tipo especial de clase que define una relación entre otras dos clases.

En el procedimiento siguiente se describe cómo crear una clase de asociación mediante código MOF.

**Para crear una clase de asociación mediante código MOF**

1.  Asigne el calificador de **Asociación** a la clase.

    Aunque es posible crear una clase con referencias a objetos o clases, el uso del calificador de **Asociación** no solo hace evidente que la clase es una clase de asociación, pero, como procedimiento recomendado, garantiza que la clase funcionará completamente como una clase de asociación.

2.  Cree dos referencias en la clase que describen las dos instancias de objeto que desea asociar con el tipo de **referencia** .

    Las referencias enlazan los dos objetos de la asociación mediante el contenedor de rutas de acceso a los objetos. Aunque no es necesario, utilice también las propiedades de referencia como propiedades clave.

    Aunque puede crear referencias completas o relativas al espacio de nombres, WMI solo tiene compatibilidad limitada para las referencias entre espacios de nombres. En concreto, solo los objetos definidos estáticamente pueden hacer referencia entre sí a través de los límites del espacio de nombres; los objetos admitidos dinámicamente no pueden hacer referencia entre sí.

    Si es necesario, use los calificadores **HasClassRef** y **Classref** junto con el tipo **ref del objeto** para hacer referencia a una clase.

    WMI admite tener un punto **de referencia de referencia a** una instancia de y la otra referencia de **objeto** apunta a una clase. En este caso, la clase de asociación describiría una asociación que enlaza instancias a clases.

    En el ejemplo de código siguiente se describe la sintaxis para usar **HasClassRef** y **Classref** con un tipo de **objeto** .

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    En el ejemplo anterior, la referencia de **EP1** puede apuntar a las definiciones de clase **para la clase** OtherContainer o la clase  . Tenga en cuenta que, aunque debe escribir la clase de referencia de un tipo débil, no se puede escribir el calificador **Classref** en sí. al hacerlo, se reduciría seriamente la eficacia del motor de consultas de WMI. La escritura débil es crear una referencia que puede contener cualquier tipo de datos mediante la palabra clave de **objeto** y el tipo de datos **ref** . Para usar correctamente **HasClassRef**, debe establecer los tipos de calificador pertinentes para propagarse a todas las instancias y subclases.

3.  Cree otras propiedades según sea necesario.

    En el ejemplo de código siguiente se muestra que WMI no admite actualmente clases de asociación que tengan menos o más de dos propiedades de referencia.

    ``` syntax
    [Association : ToInstance] 
    class MyAssocClass
    {
        ClassX ref PathToClassX ;
        ClassY ref PathToClassY ;
    };
    ```

4.  Cuando termine, compile el código MOF con el compilador MOF.

    Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).

En el ejemplo de código del paso 3 se define la clase de asociación **MyAssocClass** . La clase **MyAssocClass** define una relación entre **ClassX** y **Classy**. Las propiedades **PathToClassX** y **PathToClassY** contienen rutas de acceso de objeto a las instancias de las clases que se van a asociar. La palabra clave **ToInstance** es una de las diversas marcas de sabor que define WMI para proporcionar información sobre el uso de un calificador. La palabra clave **ToInstance** indica que WMI debe propagar el calificador de **Asociación** a todas las instancias de la clase Association. Al activar este calificador de instancia, el software cliente puede determinar que una instancia pertenece a una clase de asociación, sin tener que recuperar la definición de clase para buscar el calificador de **Asociación** . Para obtener más información, vea [Descripción de un calificador con un tipo de calificador](describing-a-qualifier-with-a-qualifier-flavor.md) y [referencias](references.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar clases de Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



