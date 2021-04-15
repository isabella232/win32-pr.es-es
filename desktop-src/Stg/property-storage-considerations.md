---
title: Consideraciones sobre el almacenamiento de propiedades
description: IPropertyStorage ReadMultiple lee todas las propiedades especificadas en la matriz rgpspec que se encuentran en el conjunto de propiedades.
ms.assetid: 7540966f-a3b2-46c9-9e04-b15133a517eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aad6aabf8b22a7c01f91a090136e6cc8156c791
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665829"
---
# <a name="property-storage-considerations"></a>Consideraciones sobre el almacenamiento de propiedades

[**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) lee todas las propiedades especificadas en la matriz *rgpspec* que se encuentran en el conjunto de propiedades. Siempre que se lea cualquiera de las propiedades solicitadas, una solicitud para recuperar una propiedad que no existe no es un error. En su lugar, debe provocar que \_ se escriba VT en blanco para esa propiedad en la matriz *rgvar* \[ \] en la devolución. Cuando no existe ninguna de las propiedades solicitadas, el método debe devolver S \_ false y establecer VT \_ vacío en cada [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). Si se devuelve cualquier otro error, no se recupera ningún valor de propiedad y el autor de la llamada no tiene que preocuparse por liberarlos.

El parámetro *rgpspec* es una matriz de estructuras [**PROPSPEC**](/windows/win32/api/propidlbase/ns-propidlbase-propspec) , que especifican para cada propiedad su identificador de propiedad o, si se ha asignado una, un identificador de cadena. Puede asignar una cadena a un identificador de propiedad llamando a [**IPropertyStorage:: WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames). El uso de identificadores de propiedad es, sin embargo, que probablemente sea mucho más eficaz que el uso de cadenas.

Las propiedades que se solicitan por nombre de cadena (PRSPEC \_ LPWStr) se asignan sin distinción entre mayúsculas y minúsculas en los identificadores de propiedad (ID), ya que se especifican en el conjunto de propiedades actual (y según la configuración regional actual del sistema).

Cuando el tipo de propiedad es VT \_ LPSTR y la propiedad se lee desde un conjunto de propiedades ANSI, es decir, la página de códigos del conjunto de propiedades se establece en un valor distinto de Unicode, el valor de la propiedad utiliza la misma página de códigos que el conjunto de propiedades. Cuando \_ se lee una propiedad VT LPSTR desde un conjunto de propiedades Unicode, el valor de la propiedad utiliza la página de códigos ANSI predeterminada actual del sistema, es decir, la página de códigos devuelta por la función **GetACP** .

Un [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), excepto aquellos que son punteros a flujos y almacenamientos, se denomina **PROPVARIANT** simple. Estos sencillos **PROPVARIANT** s reciben datos por valor, por lo que una llamada a [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) proporciona una copia de los datos a los que pertenece el llamador. Para crear o actualizar estas propiedades, llame a [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple).

En cambio, los tipos de variante VT \_ Stream, el \_ objeto de secuencia VT, el \_ \_ almacenamiento VT y el \_ objeto almacenado VT \_ son propiedades no simples, porque en lugar de proporcionar un valor, el método recupera un puntero a la interfaz indicada, desde la que se pueden leer los datos. Estos tipos permiten el almacenamiento de grandes cantidades de información a través de una sola propiedad. Hay varios problemas que surgen al usar propiedades no simples.

Para crear estas propiedades, como en el caso de las demás propiedades, llame a [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Sin embargo, en lugar de llamar al mismo método para actualizar, es más eficaz llamar primero a [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) para obtener el puntero de interfaz a la secuencia o almacenamiento y, después, escribir datos mediante los métodos [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) o [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Un flujo o almacenamiento abierto a través de una propiedad siempre se abre en modo directo, por lo que no se introduce un nivel adicional de transacción anidada. No obstante, puede haber una transacción en el conjunto de propiedades como un todo, en función de cómo se haya abierto o creado a través de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage). Además, las etiquetas de modo de acceso y uso compartido especificadas cuando se abre o se crea el conjunto de propiedades, se pasan a las secuencias o los almacenamientos basados en propiedades.

La duración de los punteros de flujo o de almacenamiento basados en propiedades, aunque teóricamente independiente de sus punteros [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) y [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) asociados, de hecho, depende de forma efectiva de ellos. Los datos visibles a través de la secuencia o el almacenamiento se relacionan con la transacción en el objeto de almacenamiento de propiedad del que se recuperan, al igual que para un objeto de almacenamiento (compatible con [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)) con subobjetos de almacenamiento y flujo contenidos. Si se anula la transacción en el objeto primario, los punteros [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) y **IStorage** existentes subordinados a ese objeto dejarán de estar accesibles. Dado que **IPropertyStorage** es la única interfaz en el objeto de almacenamiento de propiedades, la duración útil de los punteros **IStream** y **IStorage** contenidos está limitada por la duración de la interfaz **IPropertyStorage** .

La implementación también debe tratar la situación en la que se solicita la misma propiedad de streaming o con valores de almacenamiento varias veces a través de la misma instancia de la interfaz [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . Por ejemplo, en la implementación de archivo compuesto COM, el abierto se realizará correctamente o producirá un error dependiendo de si la propiedad ya está abierta o no.

Otro problema es que se abren varias en el modo de transacción. El resultado depende del nivel de aislamiento que se especificó mediante una llamada a los métodos de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) , (ya sea el método [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) o [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) , a través de las marcas STGM) en el momento en que se abrió el almacenamiento de propiedades.

Si la llamada para abrir el conjunto de propiedades especifica el acceso de lectura y escritura, las propiedades de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) y de valor de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)siempre se abren con acceso de lectura y escritura. Después, los datos se pueden escribir a través de estas interfaces, cambiando el valor de la propiedad, que es la manera más eficaz de actualizar estas propiedades. El propio valor de la propiedad no tiene un nivel adicional de anidamiento de transacciones, por lo que los cambios se encuentran en el ámbito de la transacción (si existe) en el objeto de almacenamiento de propiedades.

## <a name="storage-and-stream-properties"></a>Propiedades de flujo y almacenamiento

Para escribir un flujo o un objeto de almacenamiento en un conjunto de propiedades, el conjunto de propiedades debe haberse creado como nonsimple. Para obtener más información sobre los conjuntos de propiedades simples y no simples, vea la sección titulada [Storage and Stream Objects for a Property Set](storage-vs--stream-for-a-property-set.md). Los siguientes tipos de propiedades, como se especifica en el campo *VT* de los elementos de la matriz *rgvar* , son tipos de flujo o almacenamiento: VT \_ Stream, VT \_ Storage, VT \_ Streamed Object \_ y VT \_ Stored \_ Object.

Para escribir un flujo o un objeto de almacenamiento como una propiedad en un conjunto de propiedades no simples, llame a [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Aunque también llamaría a este método para actualizar las propiedades simples, no es una manera eficaz de actualizar los objetos de flujo y almacenamiento en un conjunto de propiedades. Esto se debe a que la actualización de una de estas propiedades a través de una llamada a **WriteMultiple** crea en el objeto de almacenamiento de propiedades una copia de los datos pasados, y los punteros [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) no se conservan más allá de la duración de esta llamada. Normalmente, es más eficaz actualizar los objetos de flujo o de almacenamiento directamente mediante una llamada a [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) para obtener el puntero de interfaz a la secuencia o el almacenamiento, y después escribir los datos mediante los métodos **IStream** o **IStorage** .

Por ejemplo, puede llamar a [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) para escribir una secuencia **null** o un objeto de almacenamiento. La implementación creará un objeto vacío en el conjunto de propiedades. Después, puede obtener acceso a este objeto llamando a [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple). Cuando termine de actualizar este objeto, no es necesario que lo escriba en el conjunto de propiedades, ya que las actualizaciones estaban directamente en el conjunto de propiedades.

Un flujo o almacenamiento abierto a través de una propiedad siempre se abre en modo directo, por lo que no se introduce un nivel adicional de transacción anidada. Todavía puede haber una transacción en el conjunto de propiedades como un todo. (Por ejemplo, si el [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) se obtuvo llamando a [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) con STGM \_ Marca de transacción establecida en el parámetro *grfmode* ). Además, un flujo o almacenamiento basado en propiedad se abre en modo de lectura y escritura, si es posible, dado el modo en el conjunto de propiedades. de lo contrario, se usa el modo de lectura.

Como se mencionó anteriormente, cuando un flujo o un objeto de almacenamiento se escribe en un conjunto de propiedades con el método [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) , se realiza una copia del objeto. Cuando se realiza una copia de este tipo en un objeto de secuencia, la operación de copia se inicia en la posición de búsqueda actual del origen. La posición de búsqueda no está definida en caso de error, pero si se realiza correctamente, se encuentra al final de la secuencia. el puntero de búsqueda no se restaura a su posición original.

Si se ha leído una secuencia o una propiedad de almacenamiento de una propiedad establecida con [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple), sigue estando abierta y se realiza una llamada subsiguiente a [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) para la misma propiedad, la operación **WriteMultiple** se realizará correctamente. La propiedad de almacenamiento o secuencia abierta anteriormente se coloca en el estado revertido (todas las llamadas a ella devolverán el \_ error STG E \_ revertido).

Si el método [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) devuelve un error al escribir una matriz de propiedades, o incluso propiedades individuales no simples, la cantidad de datos escritos realmente es indefinida.

## <a name="reference-properties"></a>Propiedades de referencia

Si una estructura de [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) especificada incluye la \_ marca de la BYREF de VT en su miembro de **VT** , la propiedad asociada es una propiedad de referencia. Se desreferencia automáticamente una propiedad de referencia antes de escribir el valor en el conjunto de propiedades. Por ejemplo, si el miembro **VT** de la estructura **PROPVARIANT** especifica un valor de tipo VT \_ BYREF \| VT \_ I4, el valor real escrito es un tipo de VT \_ . Una llamada subsiguiente al método [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) devuelve un valor como VT \_ I4. El uso de propiedades de referencia es similar a llamar a la función [VariantCopyInd](/windows/win32/api/oleauto/nf-oleauto-variantcopyind) . [VariantCopyInd](/windows/win32/api/oleauto/nf-oleauto-variantcopyind) libera la variante de destino y realiza una copia del VARIANTARG de origen, lo que realiza el direccionamiento indirecto necesario si se especifica que el origen sea VT \_ BYREF. Esta función es útil cuando se necesita una copia de una variante y para garantizar que no es VT \_ BYREF, por ejemplo, al controlar argumentos en una implementación de [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke).

## <a name="notes-to-callers"></a>Notas a los autores de las llamadas

Se recomienda que los conjuntos de propiedades se creen como Unicode, si no se establece la \_ marca ANSI PROPSETFLAG en el parámetro *GrfFlags* de [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). También se recomienda evitar el uso de \_ valores de VT LPSTR y usar valores de VT \_ LPWStr en su lugar. Cuando la página de códigos del conjunto de propiedades es Unicode, \_ los valores de cadena de VT LPSTR se convierten a Unicode cuando se almacenan y de nuevo a valores de cadena multibyte cuando se recuperan. Cuando la página de códigos de la propiedad establecida no es Unicode, los nombres de propiedad, las \_ cadenas VT BSTR y los valores de propiedad no simples se convierten en cadenas multibyte cuando se almacenan y se convierten de nuevo a Unicode cuando se recuperan, todo el uso de la página de códigos ANSI del sistema actual.

## <a name="notes-to-implementers"></a>Notas a los implementadores

Al asignar un identificador de propiedad, la implementación puede elegir cualquier valor que no esté en uso en el conjunto de propiedades de un identificador de propiedad, siempre que no sea 0 ni 1 o mayor que 0x80000000, todos los cuales son valores reservados. El parámetro *propidNameFirst* establece un valor mínimo para los identificadores de propiedad dentro del conjunto y debe ser mayor que 1 y menor que 0x80000000. Vea la sección Comentarios anterior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IPropertyStorage: implementación de archivos compuestos](ipropertystorage-compound-file-implementation.md)
</dt> <dt>

[IPropertyStorage: implementación del sistema de archivos NTFS](ipropertystorage-ntfs-file-system-implementation.md)
</dt> <dt>

[IPropertyStorage: implementación independiente](ipropertystorage-stand-alone-implementation.md)
</dt> </dl>

 

 