---
title: 'IPropertySetStorage: implementación del sistema de archivos NTFS'
description: NTFS versión 5,0 proporciona una implementación de IPropertySetStorage para los archivos de un volumen NTFS cuando los mismos archivos no son archivos compuestos.
ms.assetid: cd7290bb-bb4e-4dea-9bf6-2e1fdd0ebae8
keywords:
- IPropertySetStorage Strctd STG, implementaciones, sistema de archivos NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0d647b9cb804376a9efeb687b1524585ee938d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665830"
---
# <a name="ipropertysetstorage-ntfs-file-system-implementation"></a>IPropertySetStorage: implementación del sistema de archivos NTFS

NTFS versión 5,0 proporciona una implementación de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para los archivos de un volumen NTFS cuando los mismos archivos no son archivos compuestos. La implementación de NTFS es equivalente a la [implementación de archivo compuesto](ipropertysetstorage-compound-file-implementation.md). Para obtener más información sobre las excepciones, vea la sección Comentarios.

**Para obtener un puntero a la implementación de NTFS de IPropertySetStorage**

1.  Llame a [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) y especifique el **\_ archivo STGFMT** en el parámetro *grfFlags* para crear un nuevo archivo.
2.  Llame a [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) y especifique el **\_ archivo STGFMT** o **STGFMT \_ cualquier** valor de enumeración en el parámetro *grfFlags* para abrir un archivo existente.

Sin embargo, no se puede obtener la implementación NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para un archivo compuesto. Al abrir un archivo compuesto con [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage), si se especifica el valor de enumeración del **\_ archivo STGFMT** , se produce un error.

Además, no se pueden realizar transacciones en los conjuntos de propiedades simples. Es decir, no puede especificar **STGM \_ transaccionado** en el parámetro *Grfmode* de los métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) y [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) a menos que también especifique **PROPSETFLAG \_ nonsimple** en el parámetro *grfFlags* . El propio objeto de almacenamiento del conjunto de propiedades no admite el procesamiento de transacciones.

## <a name="when-to-use"></a>Cuándo usar

Llame a los métodos de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para crear, abrir o eliminar conjuntos de propiedades en el almacenamiento del conjunto de propiedades NTFS actual. También hay un método, [**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), que proporciona un puntero a un enumerador que se puede usar para enumerar los conjuntos de propiedades en el almacenamiento.

## <a name="compatibility"></a>Compatibilidad

Las implementaciones de NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) y [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) están disponibles a partir de Windows 2000. Las versiones anteriores no pueden tener acceso a estos conjuntos de propiedades.

La implementación de NTFS almacena conjuntos de propiedades en secuencias alternativas de un archivo NTFS. Los flujos alternativos se deben copiar cuando se copia el archivo principal.

> [!Caution]  
> No todos los sistemas de archivos admiten tales flujos. Si un archivo NTFS con conjuntos de propiedades se copia en un volumen FAT, solo se copian los datos del archivo; se pierde el conjunto de propiedades. En este caso, la función [**CopyFile**](/windows/desktop/api/winbase/nf-winbase-copyfile) no devuelve un error.

 

> [!Caution]  
> Si el equipo que realiza la copia de archivos no es un equipo que se ejecuta en Windows 2000 o posterior, es posible que se pierdan los conjuntos de propiedades. Por ejemplo, si un equipo que ejecuta el sistema operativo Windows 95 copia un archivo NTFS, el conjunto de propiedades se pierde aunque el archivo de destino esté también en un volumen NTFS.

 

## <a name="methods"></a>Métodos

La implementación del sistema de archivos NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) admite los siguientes métodos.

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

Crea un nuevo conjunto de propiedades en el almacenamiento de archivos NTFS actual y, en la devolución, proporciona un puntero de interfaz a la implementación de archivos NTFS de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . El modo de uso compartido especificado en el parámetro *grfmode* debe ser **STGM \_ share \_ Exclusive**.

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

Abre un conjunto de propiedades existente en el almacenamiento de propiedades actual. En la devolución, proporciona un puntero de interfaz a la implementación de archivos NTFS de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage). El modo de uso compartido especificado en el parámetro *grfmode* debe ser **STGM \_ share \_ Exclusive**.

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D iminar**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

Elimina una propiedad establecida en el almacenamiento de propiedades actual.

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

Crea un objeto que se usa para enumerar las estructuras [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Cada estructura **STATPROPSETSTG** proporciona datos sobre un conjunto de propiedades único.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las implementaciones de NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) y [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) almacenan los conjuntos de propiedades en un archivo sin que ello afecte al contenido de ese archivo. Por ejemplo, si crea un conjunto de propiedades en un archivo HTML denominado Default.htm, ese archivo se mostrará correctamente en un explorador Web. Es decir, los cambios en un archivo mediante estas dos interfaces no se detectan al obtener acceso a un archivo con la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

La implementación de NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) proporciona una implementación segura cuando se usa para escribir conjuntos de propiedades en un archivo en un volumen NTFS de la versión 5,0. La implementación no puede dañar estos conjuntos de propiedades incluso en caso de que se produzca un error del sistema. Por ejemplo, si se produce un error en la alimentación de un sistema durante una llamada a [**IPropertyStorage:: commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) mientras el conjunto de propiedades se vacía en el disco, el conjunto de propiedades nunca se deja en un estado intermedio. La versión anterior del conjunto de propiedades permanece o se guardan todas las actualizaciones.

La implementación de NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) difiere de la implementación de archivo compuesto de las siguientes maneras:

-   Una estructura [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) obtenida de la interfaz [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) contiene un miembro **CLSID** cuyo valor siempre es cero (**CLSID \_ null**). Con la implementación de archivo compuesto, se devuelve el miembro **CLSID** correcto para los conjuntos de propiedades no simples (consulte [almacenamiento y objetos de secuencia para un conjunto de propiedades](storage-vs--stream-for-a-property-set.md)).
-   Al obtener una implementación NTFS del puntero de la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) con la función [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) , el parámetro *grfmode* debe seguir las mismas reglas que para la implementación de archivo compuesto.

    Además, no se pueden usar las marcas siguientes:

    **STGM \_ SIMPLE**, **STGM \_ transacción**, **STGM \_ Convert**, **STGM \_ Priority** y **STGM \_ DELETEONRELEASE**.

-   Cuando las funciones [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) obtienen una interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) de NTFS, los modos de uso compartido se aplican principalmente a otras instancias de esa interfaz y no a las instancias de que abren el archivo. Por ejemplo, si se abre una interfaz **IPropertySetStorage** de NTFS mediante una llamada a la función **StgOpenStorageEx** , con el parámetro *grfmode* establecido en **STGM \_ ReadWrite \| STGM \_ share en \_ exclusiva**, es posible abrir el archivo con la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

    Estas instancias simultáneas de apertura de esta interfaz están sujetas a las siguientes restricciones: el parámetro *dwShareMode* de la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) debe especificar la marca de **\_ \_ lectura del recurso compartido de archivos** y el parámetro *dwAccess* no debe especificar la marca de **eliminación** . Además, las funciones [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) y [**MoveFile**](/windows/desktop/api/winbase/nf-winbase-movefile) no deben llamarse en un archivo para el que estén abiertas estas interfaces de conjunto de propiedades, ya que estas funciones requieren acceso de **eliminación** al archivo.

-   Si un método [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) de NTFS se abre como de solo lectura y el archivo no tiene ningún conjunto de propiedades, el objeto devuelto no conservará realmente el archivo. Por consiguiente, otras aperturas de ese archivo se realizarán correctamente, incluso si el modo de uso compartido de la operación de apertura original lo rechazaría.

    Ejemplo Si un [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) de NTFS se abre en el modo **STGM \_ Read \| STGM \_ share \_ Exclusive** y el archivo no tiene ningún conjunto de propiedades, se puede abrir simultáneamente el archivo **STGM \_ ReadWrite \| STGM \_ share \_**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IPropertyStorage: implementación del sistema de archivos NTFS](ipropertystorage-ntfs-file-system-implementation.md)
</dt> <dt>

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage:: EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[**Constantes de PROPSETFLAG**](propsetflag-constants.md)
</dt> <dt>

[**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> </dl>

 

 