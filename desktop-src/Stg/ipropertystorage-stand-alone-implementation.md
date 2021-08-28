---
title: Implementación independiente de IPropertyStorage
description: La implementación independiente proporcionada por el sistema de IPropertySetStorage incluye una implementación de IPropertyStorage, la interfaz que lee y escribe propiedades en un almacenamiento de conjunto de propiedades.
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- Implementación independiente de IPropertyStorage
- IPropertyStorage Strctd Stg, implementaciones, independientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 200d7f328670b8945807b7db7f742feabe58ad32847e3c56aa98a34278a71fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662555"
---
# <a name="ipropertystorage-stand-alone-implementation"></a>Implementación independiente de IPropertyStorage

La implementación independiente proporcionada por el sistema de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) incluye una implementación de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), la interfaz que lee y escribe propiedades en un almacenamiento de conjunto de propiedades. La **interfaz IPropertySetStorage** crea y abre conjuntos de propiedades en un almacenamiento. Las [**interfaces IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) e [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) también se proporcionan en la implementación independiente.

Para obtener un puntero a la implementación independiente de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), llame a la función [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) para crear un nuevo conjunto de propiedades o [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) para obtener el puntero de interfaz en un conjunto de propiedades existente (o llame a los métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) o [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) de la implementación [**independiente de IPropertySetStorage).**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

La implementación independiente de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) crea conjuntos de propiedades en cualquier objeto de almacenamiento o flujo, no solo en flujos y almacenamientos de archivos compuestos. La implementación independiente no depende de archivos compuestos y se puede usar con cualquier implementación de almacenamientos estructurados. Para obtener más información sobre la implementación de archivos compuestos de esta interfaz, vea [IPropertyStorage-Compound File Implementation](ipropertystorage-compound-file-implementation.md).

## <a name="when-to-use"></a>Cuándo usar

Use [**IPropertyStorage para**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) administrar propiedades dentro de un único conjunto de propiedades. Sus métodos admiten la lectura, escritura y eliminación de propiedades y los nombres de cadena opcionales que se pueden asociar a los IDs de propiedad. Otros métodos admiten las operaciones de confirmación y reversión de almacenamiento estándar. También hay un método que establece las horas asociadas al almacenamiento de propiedades y otro que permite usar la asignación de un CLSID para asociar otro código, como el código de interfaz de usuario, con el conjunto de propiedades. El [**método Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) proporciona un puntero a la implementación independiente de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), que enumera las propiedades del conjunto.

## <a name="version-0-and-version-1-property-set-formats"></a>Formatos de conjunto de propiedades de la versión 0 y la versión 1

La implementación independiente de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) admite tanto la versión 0 como los formatos de serialización del conjunto de propiedades de la versión 1. Para obtener más información, vea [Serialización de conjunto de propiedades.](version-0-vs--version-1-property-set-serialization.md) Los conjuntos de propiedades se crean en formato de versión 0 y permanecen en ese formato a menos que se soliciten nuevas características. En ese momento, el formato se actualiza a la versión 1.

Por ejemplo, si se crea un conjunto de propiedades con la marca PROPSETFLAG \_ DEFAULT, su formato es la versión 0. Siempre que los tipos de propiedad que se ajusten al formato de la versión 0 se escriban en ese conjunto de propiedades y se lean desde este, el conjunto de propiedades permanece en formato de versión 0. Si se escribe un tipo de propiedad de la versión 1 en el conjunto de propiedades, el conjunto de propiedades se actualiza automáticamente a la versión 1. Posteriormente, las implementaciones que solo entiendan la versión 0 ya no podrán leer ese conjunto de propiedades.

## <a name="ipropertystorage-and-variant-types"></a>IPropertyStorage y tipos variant

La implementación independiente de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) no admite los tipos variantes VT UNKNOWN o VT DISPATCH en el \_ miembro vt de la estructura \_ [**PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 

Los siguientes tipos de variantes se admiten dentro de safeArray; Es decir, estos valores se pueden combinar con VT \_ ARRAY en el miembro **vt** de la [**estructura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)



Tipos variantes admitidos en SafeArray por la implementación de archivos compuestos [ **de IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)

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

FECHA \_ DE VT

VT \_ BSTR

VT \_ BOOL

VT \_ DECIMAL

\_ERROR DE VT

VT \_ VARIANT

 



 

Cuando VT \_ VARIANT se combina con VT \_ ARRAY, safeArray contiene las [**estructuras PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) Sin embargo, los tipos de estos elementos deben tomarse de la lista anterior, no pueden ser VT VARIANT y no pueden incluir los indicadores VT VECTOR, VT ARRAY o \_ \_ VT \_ \_ BYREF.

## <a name="ipropertystorage-methods"></a>Métodos IPropertyStorage

La implementación independiente de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) admite los métodos siguientes:

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Lee las propiedades especificadas en la matriz *rgpspec* y proporciona los valores de todas las propiedades válidas en la *matriz rgvar* de [**elementos PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

En la implementación independiente proporcionada por el sistema, los identificadores de propiedad duplicados que hacen referencia a los tipos de flujo o almacenamiento tienen como resultado varias llamadas a [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) o [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) y el éxito o error de [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) depende de la capacidad de la implementación de almacenamiento subyacente para compartir almacenamientos abiertos.

Además, para garantizar una operación segura para subprocesos si la misma propiedad con valores de flujo o almacenamiento se solicita varias veces a través del mismo puntero [**IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) la apertura se realizará correctamente o producirá un error en función de si la propiedad ya está abierta o no y de si el sistema de archivos subyacente controla varias aperturas de una secuencia o almacenamiento. Por lo tanto, la operación [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) en una propiedad con valores de flujo o almacenamiento siempre produce una llamada a [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)o [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), pasando el acceso (STGM READWRITE, por ejemplo) y los valores de recurso compartido (STGM SHARE EXCLUSIVE, por ejemplo) especificados cuando el conjunto de propiedades se abrió o creó \_ \_ \_ originalmente.

Si se produce un error en el método , los valores escritos en *rgvar* \[ \] no están definidos. Si algunas propiedades con valores de flujo o almacenamiento se abren correctamente pero se produce un error antes de que se complete la ejecución, estas propiedades se deben liberar antes de que el método vuelva.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Escribe las propiedades especificadas en la matriz *rgpspec* y les asigna las etiquetas PROPVARIANT y los valores \[ \] especificados en *rgvar* [](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \[ \] . A las propiedades que ya existen se les asignan los valores **PROPVARIANT** especificados y se crean las propiedades que no existen actualmente.

</dd> <dt>

<span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::D eleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)
</dt> <dd>

Elimina las propiedades especificadas en *rgpspec* \[ \] .

</dd> <dt>

<span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)
</dt> <dd>

Lee los nombres de cadena existentes asociados a los IDs de propiedad especificados en *la matriz rgpropid.* \[ \]

</dd> <dt>

<span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)
</dt> <dd>

Asigna los nombres de cadena especificados en la *matriz rglpwstrName* a los IDs de propiedad especificados en *la matriz rgpropid.*

</dd> <dt>

<span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::D eletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)
</dt> <dd>

Elimina los nombres de cadena de los iD de propiedad especificados en la *matriz rgpropid* escribiendo **NULL** en el nombre de propiedad.

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Establece el **CLSID de** la secuencia del conjunto de propiedades. En la implementación independiente, al establecer el CLSID en un conjunto de propiedades no simples (uno que puede contener propiedades con valores de almacenamiento o flujo, como se describe en [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)), también se establece el CLSID en el subalmacenamiento subyacente para que se pueda obtener a través de una llamada a [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Para conjuntos de propiedades simples y no simples, vacía la imagen de memoria en el subsistema de disco. Además, para los conjuntos de propiedades en modo de transacción no simples, este método llama a [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) en el conjunto de propiedades.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage::Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Solo para conjuntos de propiedades no simples, llama al [**método Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) del almacenamiento subyacente y vuelve a abrir la secuencia "contents". Para conjuntos de propiedades simples, solo devuelve E \_ OK.

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Crea un objeto enumerador que implementa [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), cuyos métodos se pueden llamar para enumerar las estructuras [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) que proporcionan información sobre cada una de las propiedades del conjunto.

Esta implementación crea una matriz en la que se lee todo el conjunto de propiedades y que se puede compartir cuando se llama a [**IEnumSTATPROPSTG::Clone.**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Rellena los miembros de una [**estructura STATPROPSETSTG,**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) que contiene información sobre el conjunto de propiedades en su conjunto. En la devolución, proporciona un puntero a la estructura .

En el caso de los conjuntos de almacenamiento no simples, esta implementación llama a [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (o [**IStream::Stat)**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)para obtener la información del almacenamiento o flujo subyacentes.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Solo para conjuntos de propiedades no simples, establece las horas admitidas por el almacenamiento subyacente. Esta implementación de [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) llama al método [**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) del almacenamiento subyacente para modificar las horas. Admite las horas admitidas por el método subyacente, que pueden ser la hora de modificación, la hora de acceso o la hora de creación.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Implementación independiente de IPropertySetStorage](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 