---
title: IPropertyStorage-Compound de archivos
description: La implementación COM de la arquitectura structured Storage se denomina archivos compuestos.
ms.assetid: c4b4f313-de58-44f2-8ce1-a07cc187d8ca
keywords:
- IPropertyStorage Strctd Stg , implementaciones, archivo compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3c4fffe98c4bfb896f346f25ce988f75bacf1fbb194b9ec27f50e22095c8cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662615"
---
# <a name="ipropertystorage-compound-file-implementation"></a>IPropertyStorage-Compound de archivos

La implementación COM de la arquitectura structured Storage se denomina [archivos compuestos](istorage-compound-file-implementation.md). Storage objetos implementados en archivos compuestos incluyen una implementación de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), la interfaz que administra un único conjunto de propiedades persistente, e [**IPropertySetStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)la interfaz que administra grupos de conjuntos de propiedades persistentes. Para obtener más información sobre **la interfaz IPropertyStorage,** vea **IPropertyStorage** and [Property Storage Considerations](property-storage-considerations.md).

Para obtener un puntero a la implementación de archivo compuesto de [**IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)llame a [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) para crear un nuevo objeto de archivo compuesto o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) para abrir un objeto de archivo compuesto creado anteriormente. En el caso de **StgCreateStorageEx,** el *parámetro stgfmt* debe establecerse en STGFMT \_ STORAGE. En el caso de **StgOpenStorageEx,** el parámetro *stgfmt* debe establecerse en STGFMT \_ STORAGE o STGFMT \_ ANY. En ambos casos, *el parámetro riid* debe establecerse en IID \_ IPropertySetStorage. Ambas funciones suministran un puntero a la interfaz [**IPropertySetStorage del**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) objeto. Al llamar al [**método Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) o [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) de esa interfaz, se obtiene un puntero a la interfaz **IPropertyStorage,** que puede usar para llamar a cualquiera de sus métodos.

Una manera alternativa de obtener un puntero a la implementación de archivo compuesto de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) consiste en llamar a las funciones [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) y [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) anteriores, o bien especificar un parámetro *riid* de IID IStorage para la función \_ [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) [**o StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) En cualquier caso, se devuelve un puntero a la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) del objeto. Con los conjuntos de propiedades persistentes, llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para la **interfaz IPropertySetStorage** y especifique el nombre definido por el encabezado para el identificador de interfaz (IID) IID \_ IPropertySetStorage.

## <a name="when-to-use"></a>Cuándo usar

Use [**IPropertyStorage para**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) administrar las propiedades dentro de un único conjunto de propiedades. Sus métodos admiten la lectura, escritura y eliminación de propiedades y los nombres de cadena opcionales que se pueden asociar con identificadores de propiedad. Otros métodos admiten las operaciones de confirmación y reversión de almacenamiento estándar. También hay un método que le permite establecer horas asociadas al almacenamiento de propiedades y otro que permite la asignación de un CLSID que se puede usar para asociar otro código, como el código de interfaz de usuario, con el conjunto de propiedades. Llamar al [**método Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) proporciona un puntero a la implementación de archivo compuesto de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), que permite enumerar las propiedades del conjunto.

> [!Note]  
> Si obtiene un puntero a [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) mediante una llamada a [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx,**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) en un almacenamiento de conjunto de propiedades en modo simple, los métodos **IPropertyStorage** cumplen las reglas de los flujos en modo simple. El almacenamiento del conjunto de propiedades es el modo simple si se obtuvo para un archivo que se creó o abrió con la marca \_ STGM SIMPLE. En este caso, no siempre es posible hacer que la secuencia subyacente sea mayor y no es posible reemplazar las propiedades existentes por propiedades más grandes. Para obtener más información, vea [IPropertySetStorage-Compound File Implementation](ipropertysetstorage-compound-file-implementation.md).

 

## <a name="ipropertystorage-and-caching"></a>IPropertyStorage y almacenamiento en caché

La implementación de archivo compuesto de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) almacena en caché los conjuntos de propiedades abiertos en memoria para mejorar el rendimiento. Como resultado, los cambios en un conjunto de propiedades no se escriben en el archivo compuesto hasta que se llama a los métodos [**Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) o **Release** (última referencia).

## <a name="simple-mode-property-sets"></a>Conjuntos de propiedades de modo simple

Un objeto de almacenamiento de propiedades está en modo simple si se crea a partir de un objeto de almacenamiento de conjunto de propiedades en modo simple. Por ejemplo, un objeto de almacenamiento de conjunto de propiedades estaría en modo simple si se hubiera obtenido de la función [**StgOpenStorageEx,**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) con la marca STGM SIMPLE establecida en el \_ *parámetro grfMode.* Tenga en cuenta que el "modo simple" no está relacionado con "conjuntos de propiedades simples". Un conjunto de propiedades es simple si se crea mediante una llamada a [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) con la marca PROPSETFLAG NONSIMPLE establecida en el \_ *parámetro grfFlags.* Para obtener más información sobre los conjuntos de propiedades simples y no simples, [vea Storage y Objetos de secuencia para un conjunto de propiedades.](storage-vs--stream-for-a-property-set.md)

Cuando se crea un objeto de almacenamiento de propiedades de modo simple, no hay ninguna restricción en su uso. Cuando se abre un objeto de almacenamiento de propiedades en modo simple existente, no se puede crecer el objeto de secuencia subyacente que almacena el conjunto de propiedades. Por lo tanto, no siempre es posible modificar este tipo de objeto de almacenamiento de propiedades si el cambio requiere una secuencia más grande.

## <a name="property-set-formats"></a>Formatos de conjunto de propiedades

La implementación de archivo compuesto de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) admite los formatos de serialización del conjunto de propiedades de la versión 0 y la versión 1. El formato de versión 1 se admite en equipos que se ejecutan Windows 2000. Para obtener más información, vea [Serialización del conjunto de propiedades.](version-0-vs--version-1-property-set-serialization.md) Los conjuntos de propiedades se crean en formato de versión 0 y permanecen en ese formato a menos que se soliciten nuevas características. Cuando esto sucede, el formato se actualiza a la versión 1.

Por ejemplo, si se crea un conjunto de propiedades con la marca PROPSETFLAG \_ DEFAULT, su formato es la versión 0. Siempre que los tipos de propiedad que se ajusten al formato de versión 0 se escriban en ese conjunto de propiedades y se lean desde este, el conjunto de propiedades permanece en formato de versión 0. Si se escribe un tipo de propiedad de la versión 1 en el conjunto de propiedades, el conjunto de propiedades se actualiza automáticamente a la versión 1. Posteriormente, las implementaciones que reconocen solo la versión 0 ya no pueden leer ese conjunto de propiedades.

## <a name="ipropertystorage-and-variant-types"></a>Tipos IPropertyStorage y Variant

La implementación de archivo compuesto [**de IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) no admite los tipos variantes VT UNKNOWN o VT DISPATCH en el \_ miembro \_ **vt** de la [**estructura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

En la tabla siguiente se enumeran los tipos de variante que se admiten dentro de safeArray; Es decir, estos valores se pueden combinar con VT \_ ARRAY en el miembro **vt** de la [**estructura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)



Tipos variantes admitidos en SafeArray por la implementación de archivos compuestos de IPropertyStorage

VT \_ I1

VT \_ UI1

VT \_ I2

VT \_ UI2

VT \_ I4

VT \_ UI4

VT \_ INT

VT \_ UINT

VT \_ R4

VT \_ R8

VT \_ CY

VT \_ DATE

VT \_ BSTR

VT \_ BOOL

VT \_ DECIMAL

\_ERROR DE VT

VT \_ VARIANT

 



 

Cuando VT \_ VARIANT se combina con VT \_ ARRAY, safeArray contiene las [**estructuras PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) Sin embargo, los tipos de estos elementos deben tomarse de la lista anterior, no pueden ser VT VARIANT y no pueden incluir los indicadores VT VECTOR, VT ARRAY o \_ \_ VT \_ \_ BYREF.

## <a name="ipropertystorage-methods"></a>Métodos IPropertyStorage

La implementación de archivo compuesto [**de IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) admite los métodos siguientes:

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Lee las propiedades especificadas en la matriz *rgpspec* y proporciona los valores de todas las propiedades válidas en la *matriz rgvar* de PROPVARIANTs. En la implementación de archivos compuestos COM, los identificadores de propiedad duplicados que hacen referencia a tipos de flujo o almacenamiento tienen como resultado varias llamadas a [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) o [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) y el éxito o error de **ReadMultiple** depende de la capacidad de la implementación de almacenamiento subyacente para compartir las operaciones de apertura. Dado que en un archivo compuesto se fuerza STGM \_ SHARE \_ EXCLUSIVE, se producirá un error en varios intentos abiertos. No se admite la apertura del mismo objeto de almacenamiento más de una vez desde el mismo almacenamiento primario. Se debe especificar la marca STGM \_ SHARE \_ EXCLUSIVE.

Además, para garantizar una operación segura para subprocesos si la misma propiedad con valores de flujo o almacenamiento se solicita varias veces a través del mismo puntero [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) en la implementación del archivo compuesto COM, la operación de apertura se realizará correctamente o producirá un error en función de si la propiedad ya está abierta y de si el sistema de archivos subyacente controla varias aperturas de un flujo o almacenamiento. Por lo tanto, la operación **ReadMultiple** en una propiedad con valores de almacenamiento o secuencia siempre produce una llamada a [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)o [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), que pasa el acceso (STGM READWRITE, etc.) y las marcas de recurso compartido \_ (STGM SHARE EXCLUSIVE, etc.) especificadas cuando se abrió o creó el conjunto de propiedades \_ \_ original.

Si se produce un error en el método, los valores escritos en *rgvar* \[ \] no están definidos. Si algunas propiedades con valores de flujo o almacenamiento se abren correctamente, pero se produce un error antes de que se complete la ejecución, deben liberarse antes de que el método vuelva.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Escribe las propiedades especificadas en la matriz *rgpspec* y les asigna las etiquetas PROPVARIANT y los valores especificados \[ \] en *rgvar* [](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \[ \] . A las propiedades que ya existen se les asignan los **valores PROPVARIANT especificados.** Se crean las propiedades que no existen actualmente.

</dd> <dt>

<span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::D eleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)
</dt> <dd>

Elimina las propiedades especificadas en *rgpspec* \[ \] .

</dd> <dt>

<span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)
</dt> <dd>

Lee los nombres de cadena existentes asociados a los ID de propiedad especificados en *la matriz rgpropid.* \[ \]

</dd> <dt>

<span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)
</dt> <dd>

Asigna los nombres de cadena especificados en la *matriz rglpwstrName* a los nombres de propiedad especificados en *la matriz rgpropid.*

</dd> <dt>

<span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::D eletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)
</dt> <dd>

Elimina los nombres de propiedad de las propiedades especificadas en la *matriz rgpropid.* \[ \]

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Establece el **CLSID de** la secuencia del conjunto de propiedades. En la implementación de archivo compuesto, al establecer el CLSID en un conjunto de propiedades no simples (uno que puede contener legalmente propiedades con valores de almacenamiento o de flujo, como se describe en [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)), también se establece el CLSID en el subalmacenamiento subyacente para que se pueda obtener a través de una llamada a [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Para conjuntos de propiedades simples y no simples, vacía la imagen de memoria del conjunto de propiedades en el almacenamiento subyacente. Además, para los conjuntos de propiedades en modo de transacción no simples, este método realiza una confirmación (como en [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)) en el almacenamiento que contiene el conjunto de propiedades.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage::Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Solo para conjuntos de propiedades no simples, llama al [**método Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) del almacenamiento subyacente y vuelve a abrir la secuencia "contents". Para conjuntos de propiedades simples, esta interfaz siempre devuelve S \_ OK. Los conjuntos de propiedades no simples son los que se crearon mediante la marca PROPSETFLAG NONSIMPLE en \_ el [**método IPropertySetStorage::Create.**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) Para obtener más información, [vea Storage y Objetos de secuencia para un conjunto de propiedades.](storage-vs--stream-for-a-property-set.md)

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Construye una instancia de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), cuyos métodos se pueden llamar para enumerar las estructuras [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) que proporcionan información sobre cada una de las propiedades del conjunto. Esta implementación crea una matriz en la que se lee todo el conjunto de propiedades y que se puede compartir cuando se llama a **IEnumSTATPROPSTG::Clone.** Los cambios en el conjunto de propiedades no se reflejan en una instancia **abierta de IEnumSTATPROPSTG.** Para ver estos cambios, se debe construir una nueva instancia de este enumerador.

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Rellena los miembros de una estructura [**STATPROPSETSTG,**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) que contiene datos sobre la propiedad establecida como un todo. En la devolución, proporciona un puntero a la estructura . En el caso de los conjuntos de almacenamiento no simples, esta implementación llama a [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (o [**IStream::Stat)**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)para obtener las horas del almacenamiento o flujo subyacentes. En el caso de los conjuntos de almacenamiento simples, no se mantiene ningún tiempo.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Solo para conjuntos de propiedades no simples, establece las horas admitidas por el almacenamiento subyacente. La implementación de almacenamiento de archivos compuesto admite las tres opciones: modificación, acceso y creación. Esta implementación de [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) llama al método [**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) del almacenamiento subyacente para recuperar estas horas.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> </dl>

 

 