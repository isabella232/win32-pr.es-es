---
description: Una clase de asociación es un tipo especial de clase que define una relación entre otras dos clases.
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: Declarar una clase de asociación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd569d1dc20ba40be6d19f3009ab4311f69e04ca3e8a01031e74a9c84b461552
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244426"
---
# <a name="declaring-an-association-class"></a>Declarar una clase de asociación

Una clase de asociación es un tipo especial de clase que define una relación entre otras dos clases.

En el procedimiento siguiente se describe cómo crear una clase de asociación mediante código MOF.

**Para crear una clase de asociación mediante código MOF**

1.  Asigne el **calificador Association** a la clase.

    Aunque es posible crear una clase con referencias a objetos o clases, el uso del calificador **Association** no solo deja claro que la clase es una clase de asociación, sino que, como procedimiento recomendado, garantiza que la clase funcione completamente como una clase de asociación.

2.  Cree dos referencias dentro de la clase que describan las dos instancias de objeto que desea asociar mediante el **tipo ref.**

    Las referencias enlazan los dos objetos de la asociación mediante rutas de acceso a los objetos . Aunque no es necesario, use también las propiedades de referencia como propiedades clave.

    Aunque puede crear referencias completa o relativas a espacios de nombres, WMI solo tiene compatibilidad limitada con referencias entre espacios de nombres. En concreto, solo los objetos definidos estáticamente pueden hacer referencia entre sí a través de los límites del espacio de nombres. Los objetos admitidos dinámicamente no pueden hacer referencia entre sí.

    Si es necesario, use los **calificadores HasClassRef** y **Classref** junto con el tipo **ref** de objeto para hacer referencia a una clase.

    WMI admite tener un punto **de** referencia ref a una instancia de y el **otro** punto de referencia de objeto a una clase. En este caso, la clase de asociación describiría una asociación que enlaza instancias a clases.

    En el ejemplo de código siguiente se describe la sintaxis para usar **HasClassRef** y **Classref** con un **tipo de** objeto.

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    En el ejemplo anterior, la referencia **ep1** puede apuntar a las definiciones de clase para la **clase MyEndpoint** o **la clase OtherContainer.** Tenga en cuenta que, aunque debe escribir débilmente la clase de referencia, no puede escribir débilmente el propio **calificador Classref;** Si lo hace, se reduciría considerablemente la eficacia del motor de consultas WMI. La escritura débil crea una referencia que puede contener cualquier tipo de datos mediante la palabra clave **object** y el tipo de datos **ref.** Para usar correctamente **HasClassRef**, debe establecer los tipos de calificador pertinentes para que se propaguen a todas las instancias y subclases.

3.  Cree cualquier otra propiedad según sea necesario.

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

    Para obtener más información, [vea Compilar archivos MOF.](compiling-mof-files.md)

El ejemplo de código del paso 3 define la **clase de asociación MyAssocClass.** La **clase MyAssocClass** define una relación entre **ClassX** y **ClassY.** Las **propiedades PathToClassX** **y PathToClassY** contienen rutas de acceso de objeto a las instancias de las clases que se asociarán. La palabra clave **ToInstance** es una de varias marcas de tipo que WMI define para proporcionar información sobre el uso de un calificador. La **palabra clave ToInstance** indica que WMI debe propagar el calificador **Association** a todas las instancias de la clase de asociación. Al comprobar este calificador de instancia, el software cliente puede determinar que una instancia pertenece a una clase de asociación, sin tener que recuperar la definición de clase para buscar el **calificador Association.** Para obtener más información, vea [Describing a Qualifier With a Qualifier Flavor](describing-a-qualifier-with-a-qualifier-flavor.md) and [References](references.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



