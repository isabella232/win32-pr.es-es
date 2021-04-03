---
title: IPropertyStorage-Compound la implementación de archivos
description: La implementación COM de la arquitectura de almacenamiento estructurado se denomina archivos compuestos.
ms.assetid: c4b4f313-de58-44f2-8ce1-a07cc187d8ca
keywords:
- IPropertyStorage Strctd STG, implementaciones, archivo compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d927b0145077f12e5ba508ca65554ca33633a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904669"
---
# <a name="ipropertystorage-compound-file-implementation"></a>IPropertyStorage-Compound la implementación de archivos

La implementación COM de la arquitectura de almacenamiento estructurado se denomina [archivos compuestos](istorage-compound-file-implementation.md). Los objetos de almacenamiento tal como se implementan en archivos compuestos incluyen una implementación de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), la interfaz que administra un único conjunto de propiedades persistentes y [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), la interfaz que administra grupos de conjuntos de propiedades persistentes. Para obtener más información sobre la interfaz **IPropertyStorage** , consulte consideraciones sobre el [almacenamiento de propiedades](property-storage-considerations.md)y **IPropertyStorage** .

Para obtener un puntero a la implementación de archivo compuesto de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), llame a [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) para crear un nuevo objeto de archivo compuesto o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) para abrir un objeto de archivo compuesto creado previamente. En el caso de **StgCreateStorageEx**, el parámetro *stgfmt* debe establecerse en stgfmt \_ Storage. En el caso de **StgOpenStorageEx**, el parámetro *stgfmt* debe establecerse en stgfmt \_ Storage o stgfmt \_ any. En ambos casos, el parámetro *riid* debe establecerse en IID \_ IPropertySetStorage. Ambas funciones proporcionan un puntero a la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) del objeto. Llamando al método [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) o [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) de la interfaz, obtendrá un puntero a la interfaz **IPropertyStorage** , que puede usar para llamar a cualquiera de sus métodos.

Una manera alternativa de obtener un puntero a la implementación de archivo compuesto de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) es llamar a las funciones anteriores [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) y [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) , o especificar un parámetro *riid* de IID \_ IStorage para la función [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . En cualquier caso, se devuelve un puntero a la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) del objeto. Con conjuntos de propiedades persistentes, llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para la interfaz **IPropertySetStorage** , especificando el nombre definido por el encabezado para el IID del identificador de interfaz (IID) \_ IPropertySetStorage.

## <a name="when-to-use"></a>Cuándo usar

Use [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) para administrar propiedades dentro de un único conjunto de propiedades. Sus métodos permiten leer, escribir y eliminar ambas propiedades y los nombres de cadena opcionales que se pueden asociar a los identificadores de propiedad. Otros métodos admiten las operaciones de almacenamiento estándar commit y Revert. También hay un método que permite establecer las horas asociadas al almacenamiento de propiedades y otro que permite la asignación de un CLSID que se puede utilizar para asociar otro código, como el código de la interfaz de usuario, con el conjunto de propiedades. La llamada al método [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) proporciona un puntero a la implementación de archivo compuesto de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), que permite enumerar las propiedades del conjunto.

> [!Note]  
> Si obtiene un puntero a [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) llamando a [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) en un almacenamiento de conjunto de propiedades de modo simple, los métodos **IPropertyStorage** se adhieren a las reglas de flujos de modo simple. El almacenamiento del conjunto de propiedades es un modo simple si se obtuvo para un archivo que se creó o se abrió con la \_ marca simple STGM. En este caso, no siempre es posible aumentar el flujo subyacente y no es posible reemplazar las propiedades existentes con propiedades más grandes. Para obtener más información, vea [IPropertySetStorage: implementación de archivos compuestos](ipropertysetstorage-compound-file-implementation.md).

 

## <a name="ipropertystorage-and-caching"></a>IPropertyStorage y Caching

La implementación de archivo compuesto de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) almacena en caché los conjuntos de propiedades abiertos en memoria para mejorar el rendimiento. Como resultado, los cambios en un conjunto de propiedades no se escriben en el archivo compuesto hasta que se llama a los métodos [**commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) o **Release** (última referencia).

## <a name="simple-mode-property-sets"></a>Conjuntos de propiedades de modo simple

Un objeto de almacenamiento de propiedades está en modo simple si se crea a partir de un objeto de almacenamiento de conjunto de propiedades de modo simple. Por ejemplo, un objeto de almacenamiento de conjunto de propiedades sería en modo simple si se obtuvo de la función [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) , con la \_ marca simple STGM establecida en el parámetro *grfMode* . Tenga en cuenta que "modo simple" no está relacionado con "conjuntos de propiedades simples". Un conjunto de propiedades es sencillo si se crea llamando a [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) con la marca de PROPSETFLAG no \_ simple establecida en el parámetro *grfFlags* . Para obtener más información sobre los conjuntos de propiedades simples y no simples, vea [almacenamiento y objetos de secuencia para un conjunto de propiedades](storage-vs--stream-for-a-property-set.md).

Cuando se crea un objeto de almacenamiento de propiedades de modo simple, no hay restricciones en su uso. Cuando se abre un objeto de almacenamiento de propiedades de modo simple existente, no se puede incrementar el objeto de secuencia subyacente que almacena el conjunto de propiedades. Por consiguiente, no siempre es posible modificar este tipo de objeto de almacenamiento de propiedades si el cambio requiere una secuencia más grande.

## <a name="property-set-formats"></a>Formatos de conjunto de propiedades

La implementación de archivo compuesto de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) admite los formatos de serialización de la versión 0 y la de la versión 1. El formato de la versión 1 se admite en equipos que ejecutan Windows 2000. Para obtener más información, vea [serialización de conjuntos de propiedades](version-0-vs--version-1-property-set-serialization.md). Los conjuntos de propiedades se crean en el formato de la versión 0 y permanecen en ese formato a menos que se soliciten nuevas características. En ese caso, el formato se actualiza a la versión 1.

Por ejemplo, si se crea un conjunto de propiedades con la \_ marca predeterminada PROPSETFLAG, su formato es la versión 0. Siempre que los tipos de propiedad que se ajustan al formato de la versión 0 se escriben y se leen de ese conjunto de propiedades, el conjunto de propiedades permanece en formato de la versión 0. Si un tipo de propiedad de la versión 1 se escribe en el conjunto de propiedades, el conjunto de propiedades se actualiza automáticamente a la versión 1. Posteriormente, las implementaciones que reconocen solo la versión 0 ya no podrán leer ese conjunto de propiedades.

## <a name="ipropertystorage-and-variant-types"></a>Tipos IPropertyStorage y Variant

La implementación de archivo compuesto de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) no admite los tipos Variant VT \_ Unknown o VT \_ Dispatch en el miembro **VT** de la estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

En la tabla siguiente se enumeran los tipos Variant que se admiten en SafeArray; es decir, estos valores se pueden combinar con \_ la matriz VT en el miembro **VT** de la estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .



Tipos de variante admitidos en SafeArray por implementación de archivo compuesto de IPropertyStorage

VT \_ I1

VT \_ UI1

I2 de VT \_

VT \_ UI2

VT \_ I4

VT \_ UI4

VT \_ int

VT \_ uint

VT \_ R4

VT \_ R8

VT \_ CY

fecha de VT \_

VT \_ BSTR

VT \_ bool

VT \_ decimal

ERROR de VT \_

VT ( \_ variante)

 



 

Cuando \_ se combina VT Variant con una \_ matriz de VT, el propio SafeArray contiene estructuras [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) . Sin embargo, los tipos de estos elementos se deben tomar de la lista anterior, no pueden ser de \_ tipo VT y no pueden incluir los indicadores de VT \_ , \_ matriz VT o VT \_ BYREF.

## <a name="ipropertystorage-methods"></a>Métodos IPropertyStorage

La implementación de archivo compuesto de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) admite los siguientes métodos:

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Lee las propiedades especificadas en la matriz *rgpspec* y proporciona los valores de todas las propiedades válidas en la matriz *rgvar* de PROPVARIANTs. En la implementación de archivo compuesto COM, los identificadores de propiedad duplicados que hacen referencia a los tipos de flujo o de almacenamiento dan como resultado varias llamadas a [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) o [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) y el éxito o el error de **ReadMultiple** depende de la capacidad de la implementación de almacenamiento subyacente para compartir operaciones de apertura. Dado que en un archivo compuesto STGM \_ recurso compartido \_ exclusivo se fuerza, se producirá un error en varios intentos de apertura. No se admite la apertura del mismo objeto de almacenamiento más de una vez desde el mismo almacenamiento primario. \_Se debe especificar la marca de uso compartido STGM \_ .

Además, para asegurarse de que la operación segura para subprocesos se solicita varias veces a través del mismo puntero [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) en la implementación de archivo compuesto com, la operación de apertura se realizará correctamente o producirá un error dependiendo de si la propiedad ya está abierta y si el sistema de archivos subyacente controla varias aperturas de una secuencia o almacenamiento. Por lo tanto, la operación **ReadMultiple** en una propiedad de flujo o de valor de almacenamiento siempre da como resultado una llamada a [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)o [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), que pasa el acceso (STGM \_ ReadWrite, etc.) y las marcas de uso compartido (STGM \_ compartir \_ exclusivo, etc.) que se especifican cuando se abre o se crea el conjunto de propiedades original.

Si se produce un error en el método, los valores escritos en *rgvar* no \[ \] están definidos. Si algunas propiedades de flujo o de valor de almacenamiento se abren correctamente pero se produce un error antes de que se complete la ejecución, se deben liberar antes de que el método devuelva.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Escribe las propiedades especificadas en la matriz *rgpspec* \[ \] , asignándoles las etiquetas y los valores de [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) especificados en *rgvar* \[ \] . A las propiedades que ya existen se les asignan los valores de **PROPVARIANT** especificados. Se crean las propiedades que no existen actualmente.

</dd> <dt>

<span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::D eleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)
</dt> <dd>

Elimina las propiedades especificadas en *rgpspec* \[ \] .

</dd> <dt>

<span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)
</dt> <dd>

Lee los nombres de cadena existentes asociados a los identificadores de propiedad especificados en la matriz *rgpropid* \[ \] .

</dd> <dt>

<span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)
</dt> <dd>

Asigna nombres de cadena especificados en la matriz *rglpwstrName* a los identificadores de propiedad especificados en la matriz *rgpropid* .

</dd> <dt>

<span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::D eletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)
</dt> <dd>

Elimina los nombres de propiedad de las propiedades especificadas en la matriz *rgpropid* \[ \] .

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Establece el **CLSID** de la secuencia del conjunto de propiedades. En la implementación de archivo compuesto, al establecer el CLSID en un conjunto de propiedades no simples (que puede contener legalmente propiedades de almacenamiento o con valores de flujo, como se describe en [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) también se establece el CLSID en el subalmacenamiento subyacente para que se pueda obtener a través de una llamada a [**IStorage:: Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage:: commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

En el caso de conjuntos de propiedades simples y no simples, vacía la imagen de la memoria del conjunto de propiedades en el almacenamiento subyacente. Además, en el caso de conjuntos de propiedades de modo de transacción no simples, este método realiza una confirmación (como en [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)) en el almacenamiento que contiene el conjunto de propiedades.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage:: revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Solo para conjuntos de propiedades no simples, llama al método [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) del almacenamiento subyacente y vuelve a abrir la secuencia ' contents '. En el caso de los conjuntos de propiedades simples, esta interfaz siempre devuelve S \_ correcto. Los conjuntos de propiedades no simples son aquellos que se crearon con la \_ marca PROPSETFLAG nonsimple en el método [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) . Para obtener más información, consulte [almacenamiento y objetos de secuencia para un conjunto de propiedades](storage-vs--stream-for-a-property-set.md) .

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Construye una instancia de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), los métodos de los que se puede llamar para enumerar las estructuras [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) que proporcionan información sobre cada una de las propiedades del conjunto. Esta implementación crea una matriz en la que se lee todo el conjunto de propiedades y que se puede compartir cuando se llama a **IEnumSTATPROPSTG:: Clone** . Los cambios en el conjunto de propiedades no se reflejan en una instancia abierta de **IEnumSTATPROPSTG** . Para ver estos cambios, se debe construir una nueva instancia de este enumerador.

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage:: Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Rellena los miembros de una estructura [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , que contiene datos sobre la propiedad establecida en su totalidad. En la devolución, proporciona un puntero a la estructura. En el caso de los conjuntos de almacenamiento no simples, esta implementación llama a [**IStorage:: Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (o [**IStream:: Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) para obtener las horas de la secuencia o el almacenamiento subyacente. En el caso de los conjuntos de almacenamiento simples, no se mantiene ninguna hora.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Solo para conjuntos de propiedades no simples, establece las horas admitidas por el almacenamiento subyacente. La implementación de almacenamiento de archivos compuesto admite los tres: modificación, acceso y creación. Esta implementación de [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) llama al método [**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) del almacenamiento subyacente para recuperar estas horas.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> </dl>

 

 