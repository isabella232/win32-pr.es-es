---
title: Implementación del sistema de archivos IPropertySetStorage-NTFS
description: Ntfs versión 5.0 proporciona una implementación de IPropertySetStorage para los archivos de un volumen NTFS cuando los propios archivos no son archivos compuestos.
ms.assetid: cd7290bb-bb4e-4dea-9bf6-2e1fdd0ebae8
keywords:
- IPropertySetStorage Strctd Stg , implementaciones, sistema de archivos NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0794e2905cd9e8bd06804decb756b3f1f639c75e837b2d5f3181bb73939717f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683045"
---
# <a name="ipropertysetstorage-ntfs-file-system-implementation"></a>Implementación del sistema de archivos IPropertySetStorage-NTFS

Ntfs versión 5.0 proporciona una implementación de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para los archivos de un volumen NTFS cuando los propios archivos no son archivos compuestos. La implementación de NTFS es equivalente a la [implementación de archivo compuesto](ipropertysetstorage-compound-file-implementation.md). Para obtener más información sobre las excepciones, vea Comentarios.

**Para obtener un puntero a la implementación NTFS de IPropertySetStorage**

1.  Llame [**a StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) y especifique **STGFMT \_ FILE** en el *parámetro grfFlags* para crear un nuevo archivo.
2.  Llame [**a StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) y especifique el valor de enumeración **STGFMT \_ FILE** o **STGFMT \_ ANY** en el *parámetro grfFlags* para abrir un archivo existente.

Sin embargo, no puede obtener la implementación NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para un archivo compuesto. Al abrir un archivo compuesto con [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage), la especificación del valor de enumeración **STGFMT \_ FILE** produce un error.

Además, los conjuntos de propiedades simples no se pueden realizar transacciones. Es decir, no puede especificar **STGM \_ TRANSACTED** en el parámetro *grfmode* de los métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) y [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) a menos que también especifique **PROPSETFLAG \_ NONSIMPLE** en el *parámetro grfFlags.* El propio objeto de almacenamiento del conjunto de propiedades no admite el procesamiento de transacciones.

## <a name="when-to-use"></a>Cuándo usar

Llame a [**los métodos IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para crear, abrir o eliminar conjuntos de propiedades en el almacenamiento del conjunto de propiedades NTFS actual. También hay un método, [**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), que proporciona un puntero a un enumerador que se puede usar para enumerar los conjuntos de propiedades en el almacenamiento.

## <a name="compatibility"></a>Compatibilidad

Las implementaciones NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) [**e IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) están disponibles a partir Windows 2000. Las versiones anteriores no pueden tener acceso a estos conjuntos de propiedades.

La implementación de NTFS almacena conjuntos de propiedades en secuencias alternativas de un archivo NTFS. Las secuencias alternativas se deben copiar cuando se copia el archivo principal.

> [!Caution]  
> No todos los sistemas de archivos admiten tales secuencias. Si un archivo NTFS con conjuntos de propiedades se copia en un volumen FAT, solo se copian los datos del archivo; se pierde el conjunto de propiedades. En [**este caso,**](/windows/desktop/api/winbase/nf-winbase-copyfile) la función CopyFile no devuelve un error.

 

> [!Caution]  
> Si el equipo que realiza la copia de archivos no es un equipo que se ejecuta en Windows 2000 o posterior, es posible que se pierdan los conjuntos de propiedades. Por ejemplo, si un equipo que se ejecuta en un sistema operativo Windows 95 copia un archivo NTFS, el conjunto de propiedades se pierde incluso si el archivo de destino también está en un volumen NTFS.

 

## <a name="methods"></a>Métodos

La implementación del sistema de archivos NTFS [**de IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) admite los métodos siguientes.

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

Crea un nuevo conjunto de propiedades en el almacenamiento de archivos NTFS actual y, al devolverlo, proporciona un puntero de interfaz a la implementación del archivo NTFS [**IPropertyStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) El modo de uso compartido especificado en *el parámetro grfmode* debe ser **STGM SHARE \_ \_ EXCLUSIVE.**

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

Abre un conjunto de propiedades existente en el almacenamiento de propiedades actual. En la devolución, proporciona un puntero de interfaz a la implementación del archivo NTFS [**de IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage). El modo de uso compartido especificado en *el parámetro grfmode* debe ser **STGM SHARE \_ \_ EXCLUSIVE.**

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D elete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

Elimina un conjunto de propiedades en el almacenamiento de propiedades actual.

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

Crea un objeto que se usa para enumerar las [**estructuras STATPROPSETSTG.**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) Cada **estructura STATPROPSETSTG** proporciona datos sobre un único conjunto de propiedades.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las implementaciones NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) [**e IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) almacenan conjuntos de propiedades en un archivo sin afectar al contenido de ese archivo. Por ejemplo, si crea un conjunto de propiedades en un archivo HTML denominado Default.htm, ese archivo todavía se muestra correctamente en un explorador web. Es decir, los cambios realizados en un archivo que usa estas dos interfaces son indetectables al acceder a un archivo con la [**función CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

La implementación NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) proporciona una implementación segura cuando se usa para escribir conjuntos de propiedades en un archivo en un volumen NTFS versión 5.0. La implementación de no puede dañar estos conjuntos de propiedades ni siquiera en caso de error del sistema. Por ejemplo, si se produce un error en la alimentación de un sistema durante una llamada a [**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) mientras el conjunto de propiedades se vacía en el disco, el conjunto de propiedades nunca se deja en un estado intermedio. La versión anterior del conjunto de propiedades permanece o se guardan todas las actualizaciones.

La implementación NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) difiere de la implementación de archivos compuestos de las maneras siguientes:

-   Una [**estructura STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) obtenida de la interfaz [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) contiene un **miembro clsid** cuyo valor siempre es cero (**CLSID \_ NULL**). Con la implementación de archivo compuesto, se devuelve el miembro **clsid** correcto para conjuntos de propiedades no simples (vea Storage y Objetos de secuencia para [un](storage-vs--stream-for-a-property-set.md)conjunto de propiedades).
-   Al obtener una implementación NTFS del puntero de interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) mediante las funciones [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**StgOpenStorageEx,**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) el parámetro *grfmode* debe seguir las mismas reglas que para la implementación de archivos compuestos.

    Además, es posible que no se utilicen las marcas siguientes:

    **STGM \_ SIMPLE,** **STGM \_ TRANSACTED,** **STGM \_ CONVERT,** **STGM \_ PRIORITY** y **STGM \_ DELETEONRELEASE**.

-   Cuando las funciones [**StgCreateStorageEx o StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) obtienen una interfaz NTFS [**IPropertySetStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) los modos de uso compartido se aplican principalmente a otras instancias de esa interfaz y no a las instancias de abrir el propio archivo. [](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) Por ejemplo, si se abre una interfaz NTFS **IPropertySetStorage** llamando a la función **StgOpenStorageEx,** con el parámetro *grfmode* establecido en **STGM \_ READWRITE \| STGM \_ SHARE \_ EXCLUSIVE,** es posible abrir el archivo con la función [**CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

    Estas instancias simultáneas de abrir esta interfaz están sujetas a las siguientes restricciones: el parámetro *dwShareMode* de la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) debe especificar la marca READ de **FILE \_ SHARE \_** y el parámetro *dwAccess* no debe especificar la **marca DELETE.** Además, [**no se debe**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) llamar a las funciones DeleteFile y [**MoveFile**](/windows/desktop/api/winbase/nf-winbase-movefile) en un archivo para el que estén abiertas estas interfaces de conjunto de propiedades, ya que estas funciones requieren **acceso DELETE** al archivo.

-   Si un método NTFS [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) se abre como de solo lectura y el archivo no tiene actualmente ningún conjunto de propiedades, el objeto devuelto no mantendrá abierto realmente el archivo. Por lo tanto, otras aperturas de ese archivo se realizará correctamente, incluso si el modo de uso compartido de la operación de apertura original lo rechazaría.

    Ejemplo; Si se abre un objeto NTFS [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) en el modo **STGM \_ READ \| STGM \_ SHARE \_ EXCLUSIVE** y el archivo no tiene ningún conjunto de propiedades, será posible abrir simultáneamente el archivo **STGM \_ READWRITE \| STGM SHARE \_ \_ EXCLUSIVE**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Implementación del sistema de archivos IPropertyStorage-NTFS](ipropertystorage-ntfs-file-system-implementation.md)
</dt> <dt>

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage::EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[**Constantes PROPSETFLAG**](propsetflag-constants.md)
</dt> <dt>

[**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> </dl>

 

 