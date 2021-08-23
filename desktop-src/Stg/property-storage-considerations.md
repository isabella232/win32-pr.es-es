---
title: Consideraciones Storage propiedades
description: IPropertyStorage ReadMultiple lee tantas propiedades especificadas en la matriz rgpspec como se encuentran en el conjunto de propiedades.
ms.assetid: 7540966f-a3b2-46c9-9e04-b15133a517eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 128c5da70ae08c62660e0177187036fddee6ff27ed1d9971b6f95dea7052ecdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662165"
---
# <a name="property-storage-considerations"></a>Consideraciones Storage propiedades

[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) lee tantas propiedades especificadas en la matriz *rgpspec* como se encuentran en el conjunto de propiedades. Siempre que se lea cualquiera de las propiedades solicitadas, una solicitud para recuperar una propiedad que no existe no es un error. En su lugar, esto debe hacer que VT \_ EMPTY se escriba para esa propiedad en la *matriz rgvar* \[ \] en la devolución. Cuando no existe ninguna de las propiedades solicitadas, el método debe devolver S FALSE y establecer \_ VT EMPTY en cada \_ [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). Si se devuelve cualquier otro error, no se recupera ningún valor de propiedad y el autor de la llamada no tiene que preocuparse de liberarlos.

El *parámetro rgpspec* es una matriz de estructuras [**PROPSPEC,**](/windows/win32/api/propidlbase/ns-propidlbase-propspec) que especifican para cada propiedad su identificador de propiedad o, si se asigna uno, un identificador de cadena. Puede asignar una cadena a un identificador de propiedad llamando a [**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames). Sin embargo, es probable que el uso de identificadores de propiedad sea significativamente más eficaz que el uso de cadenas.

Las propiedades solicitadas por el nombre de cadena (PRSPEC LPWSTR) se asignan sin tener en cuenta las mayúsculas y minúsculas a los identificadores de propiedad (identificadores) tal como se especifican en el conjunto de propiedades actual (y según la configuración regional del sistema \_ actual).

Cuando el tipo de propiedad es VT LPSTR y la propiedad se lee de un conjunto de propiedades ANSI, es decir, la página de códigos del conjunto de propiedades se establece en un valor distinto de Unicode, el valor de la propiedad usa la misma página de códigos que el conjunto de \_ propiedades. Cuando se lee una propiedad LPSTR de VT desde un conjunto de propiedades Unicode, el valor de la propiedad usa la página de códigos ANSI predeterminada actual del sistema, es decir, la página de códigos devuelta desde la \_ **función GetACP.**

[**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), excepto los que son punteros a secuencias y almacenamientos, se denomina **PROPVARIANT simple.** Estos sencillos **PROPVARIANT** reciben datos por valor, por lo que una llamada a [**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) proporciona una copia de los datos que el autor de la llamada posee a continuación. Para crear o actualizar estas propiedades, llame a [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple).

Por el contrario, los tipos variantes VT STREAM, VT STREAMED OBJECT, VT STORAGE y VT STORED OBJECT son propiedades no simples, ya que en lugar de proporcionar un valor, el método recupera un puntero a la interfaz indicada, desde la que se pueden leer los \_ \_ \_ \_ \_ \_ datos. Estos tipos permiten el almacenamiento de grandes cantidades de información a través de una sola propiedad. Hay varios problemas que surgen al usar propiedades no simples.

Para crear estas propiedades, como para las demás propiedades, llame a [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Sin embargo, en lugar de llamar al mismo método para actualizar, es más eficaz llamar primero a [**IPropertyStorage::ReadMultiple para**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) obtener el puntero de interfaz al flujo o almacenamiento y, a continuación, escribir datos mediante los métodos [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) o [**IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage) Una secuencia o almacenamiento abierto a través de una propiedad siempre se abre en modo directo, por lo que no se introduce un nivel adicional de transacción anidada. Sin embargo, puede haber una transacción en el conjunto de propiedades como un todo, en función de cómo se haya abierto o creado a través [**de IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage). Además, las etiquetas de modo de acceso y recurso compartido especificadas cuando se abre o crea el conjunto de propiedades, se pasan a los flujos o almacenamientos basados en propiedades.

De hecho, las duraciones de los punteros de flujo o almacenamiento basados en propiedades, aunque en teoría son independientes de sus punteros [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) asociados, dependen de ellos de forma eficaz. Los datos visibles a través de la secuencia o el almacenamiento están relacionados con la transacción en el objeto de almacenamiento de propiedades desde el que se recuperan, al igual que para un objeto de almacenamiento (compatible con [**IStorage)**](/windows/desktop/api/Objidl/nn-objidl-istorage)con objetos secundarios de flujo y almacenamiento contenidos. Si se anula la transacción en el objeto primario, los punteros [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) e **IStorage** existentes subordinados a ese objeto ya no son accesibles. Dado **que IPropertyStorage** es la única interfaz en el objeto de almacenamiento de propiedades, la duración útil de los punteros **IStream** e **IStorage** contenidos está limitada por la duración de la **interfaz IPropertyStorage.**

La implementación también debe tratar con la situación en la que la misma propiedad con valores de almacenamiento o flujo se solicita varias veces a través de la misma instancia de interfaz [**IPropertyStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) Por ejemplo, en la implementación del archivo compuesto COM, la apertura se realizará correctamente o se producirá un error en función de si la propiedad ya está abierta o no.

Otro problema son varias aperturas en modo de transacción. El resultado depende del nivel de aislamiento que se especificó mediante una llamada a los métodos [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) (el método [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) o [**Create,**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) a través de las marcas STGM) en el momento en que se abrió el almacenamiento de propiedades.

Si la llamada para abrir el conjunto de propiedades especifica acceso de lectura y escritura, las propiedades con valores de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)siempre se abren con acceso de lectura y escritura. A continuación, los datos se pueden escribir a través de estas interfaces, cambiando el valor de la propiedad , que es la manera más eficaz de actualizar estas propiedades. El propio valor de propiedad no tiene un nivel adicional de anidamiento de transacciones, por lo que los cambios se encuentran en el ámbito de la transacción (si existe) en el objeto de almacenamiento de propiedades.

## <a name="storage-and-stream-properties"></a>Storage y propiedades de flujo

Para escribir una secuencia o un objeto de almacenamiento en un conjunto de propiedades, el conjunto de propiedades se debe haber creado como no simple. Para obtener más información sobre los conjuntos de propiedades simples y no simples, vea la sección titulada [Storage y Objetos de secuencia para un conjunto de propiedades.](storage-vs--stream-for-a-property-set.md) Los siguientes tipos de propiedad, como se especifica en el campo *vt* de los elementos de la *matriz rgvar,* son tipos de flujo o almacenamiento: VT \_ STREAM, VT \_ STORAGE, VT \_ STREAMED \_ OBJECT, VT STORED \_ \_ OBJECT.

Para escribir una secuencia o un objeto de almacenamiento como una propiedad en un conjunto de propiedades no simple, llame a [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Aunque también llamaría a este método para actualizar propiedades simples, no es una manera eficaz de actualizar los objetos de flujo y almacenamiento en un conjunto de propiedades. Esto se debe a que la actualización de una de estas propiedades mediante una llamada a **WriteMultiple** crea en el objeto de almacenamiento de propiedades una copia de los datos pasados y los punteros [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) no se conservan más allá de la duración de esta llamada. Normalmente es más eficaz actualizar directamente los objetos de flujo o almacenamiento llamando primero a [**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) para obtener el puntero de interfaz al flujo o almacenamiento y, a continuación, escribir datos a través de los métodos **IStream** o **IStorage.**

Por ejemplo, puede llamar a [**IPropertyStorage::WriteMultiple para**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) escribir un **objeto** de almacenamiento o flujo NULL. A continuación, la implementación creará un objeto vacío en el conjunto de propiedades. A continuación, puede obtener acceso a este objeto llamando a [**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple). Cuando termine de actualizar este objeto, no es necesario escribirlo en el conjunto de propiedades, ya que las actualizaciones se encontraban directamente en el conjunto de propiedades.

Una secuencia o almacenamiento abierto a través de una propiedad siempre se abre en modo directo, por lo que no se introduce un nivel adicional de transacción anidada. Todavía puede haber una transacción en el conjunto de propiedades como un todo. (Por ejemplo, si [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) se obtuvo llamando a [**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) con STGM \_ Marca TRANSACTED establecida en el *parámetro grfmode).* Además, se abre un flujo o almacenamiento basado en propiedades en modo de lectura y escritura, si es posible, dado el modo en el conjunto de propiedades; De lo contrario, se usa el modo de lectura.

Como se mencionó anteriormente, cuando se escribe una secuencia o un objeto de almacenamiento en un conjunto de propiedades con el método [**WriteMultiple,**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) se realiza una copia del objeto. Cuando se realiza una copia de este tipo en un objeto de secuencia, la operación de copia se inicia en la posición de búsqueda actual del origen. La posición de búsqueda no está definida en caso de error, pero si se ejecuta correctamente, se encuentra al final de la secuencia. El puntero de búsqueda no se restaura en su posición original.

Si se ha leído una propiedad de flujo o almacenamiento desde un conjunto de propiedades con [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple), se mantiene abierta y se realiza una llamada posterior a [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) para la misma propiedad, la operación **WriteMultiple** se realizará correctamente. La propiedad de flujo o almacenamiento abierta previamente se coloca en estado revertido (todas las llamadas a ella devolverán el error STG \_ E \_ REVERTED).

Si el [**método WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) devuelve un error al escribir una matriz de propiedades, o incluso propiedades individuales no simples, la cantidad de datos escritos realmente no está definida.

## <a name="reference-properties"></a>Propiedades de referencia

Si una estructura [**PROPVARIANT especificada**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) incluye la marca VT BYREF en su miembro \_ **vt,** la propiedad asociada es una propiedad de referencia. Se desreferencia automáticamente una propiedad de referencia antes de escribir el valor en el conjunto de propiedades. Por ejemplo, si el miembro **vt** de la estructura **PROPVARIANT** especifica un valor de tipo VT BYREF VT I4, el valor real escrito es un \_ tipo VT \| \_ \_ I4. Una llamada subsiguiente al [**método IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) devuelve un valor como VT \_ I4. El uso de propiedades de referencia es similar a llamar [a la función VariantCopyInd.](/windows/win32/api/oleauto/nf-oleauto-variantcopyind) [VariantCopyInd](/windows/win32/api/oleauto/nf-oleauto-variantcopyind) libera la variante de destino y realiza una copia de variantarg de origen, realizando el direccionamiento indirecto necesario si se especifica que el origen es VT \_ BYREF. Esta función es útil cuando se necesita una copia de una variante y para garantizar que no es VT BYREF, por ejemplo, al controlar argumentos en una implementación de \_ [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke).

## <a name="notes-to-callers"></a>Notas a los autores de las llamadas

Se recomienda que los conjuntos de propiedades se creen como Unicode, al no establecer la marca ANSI PROPSETFLAG en el parámetro \_ *grfFlags* de [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). También se recomienda evitar el uso de valores LPSTR de VT y usar \_ valores \_ LPWSTR de VT en su lugar. Cuando la página de códigos del conjunto de propiedades es Unicode, los valores de cadena LPSTR de VT se convierten en Unicode cuando se almacenan y de vuelta a valores de cadena \_ multibyte cuando se recuperan. Cuando la página de códigos del conjunto de propiedades no es Unicode, los nombres de propiedad, las cadenas BSTR de VT y los valores de propiedad no simples se convierten en cadenas multibyte cuando se almacenan y se convierten de nuevo en Unicode cuando se recuperan, todo ello mediante la página de códigos ANSI del sistema \_ actual.

## <a name="notes-to-implementers"></a>Notas a los implementadores

Al asignar un identificador de propiedad, la implementación puede elegir cualquier valor que no esté actualmente en uso en el conjunto de propiedades para un identificador de propiedad, siempre que no sea 0, 1 o mayor que 0x80000000, todos ellos valores reservados. El *parámetro propidNameFirst* establece un valor mínimo para los identificadores de propiedad dentro del conjunto y debe ser mayor que 1 y menor que 0x80000000. Consulte la sección Comentarios anterior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IPropertyStorage-Compound File Implementation](ipropertystorage-compound-file-implementation.md)
</dt> <dt>

[Implementación del sistema de archivos IPropertyStorage-NTFS](ipropertystorage-ntfs-file-system-implementation.md)
</dt> <dt>

[Implementación independiente de IPropertyStorage](ipropertystorage-stand-alone-implementation.md)
</dt> </dl>

 

 