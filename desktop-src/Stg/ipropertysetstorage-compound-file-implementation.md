---
title: IPropertySetStorage-Compound de archivos
description: La implementación de objetos de almacenamiento de archivos compuestos COM incluye una implementación de IPropertyStorage, la interfaz que administra un único conjunto de propiedades persistente e IPropertySetStorage, la interfaz que administra grupos de conjuntos de propiedades persistentes.
ms.assetid: de2cb778-c6eb-4487-996b-87405674f603
keywords:
- IPropertySetStorage Strctd Stg , implementaciones, archivo compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3bc0d423b304b6d456ccddab158a48ba0b6d5f3f310d293c6aed0dedb2a556
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662665"
---
# <a name="ipropertysetstorage-compound-file-implementation"></a>IPropertySetStorage-Compound de archivos

La implementación de objetos de almacenamiento de archivos compuestos [COM](ipropertystorage-compound-file-implementation.md) incluye una implementación de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), la interfaz que administra un único conjunto de propiedades persistente e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), la interfaz que administra grupos de conjuntos de propiedades persistentes.

Para obtener un puntero a la implementación de archivo compuesto de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), especifique el nombre definido por el encabezado para el identificador IID IStorage como parámetro riid o use las funciones \_ [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)  En ambos casos, especifique STGFMT \_ STORAGE como parámetro *stgfmt.* (STGFMT \_ También se puede especificar ANY en el caso de **StgOpenStorageEx).** Además, especifique el nombre definido por el encabezado para el identificador de interfaz (IID) \_ IPropertySetStorage como *parámetro riid.* Ambas funciones suministran un puntero al objeto **IPropertySetStorage** interfaz.

Otra manera de obtener un puntero a la implementación del archivo compuesto es especificar el nombre definido por el encabezado para el identificador IID IStorage como parámetro riid, o usar las funciones \_ [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) o [**StgOpenStorage.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)  Esto suministrará un puntero a la interfaz [**IStorage del**](/windows/desktop/api/Objidl/nn-objidl-istorage) objeto . Si desea tratar con conjuntos de propiedades persistentes, llame a [**IStorage::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para la [**interfaz IPropertySetStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

## <a name="when-to-use-ipropertysetstorage"></a>Cuándo usar IPropertySetStorage

Llame a los métodos [**de IPropertySetStorage para**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) crear, abrir o eliminar conjuntos de propiedades en el almacenamiento del conjunto de propiedades de archivo compuesto actual. También hay un método, [**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), que proporciona un puntero a un enumerador que se puede usar para enumerar los conjuntos de propiedades en el almacenamiento.

## <a name="methods"></a>Métodos

[**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)

Crea un nuevo conjunto de propiedades en el almacenamiento de archivos compuestos actual y, al devolverlo, proporciona un puntero de interfaz a la implementación del archivo compuesto [**IPropertyStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) En esta implementación, los conjuntos de propiedades solo se pueden realizar transacciones si se especifica PROPSETFLAG \_ NONSIMPLE. Este método requiere que el modo de uso compartido especificado en el parámetro *grfMode* sea STGM SHARE EXCLUSIVE y que el modo de acceso sea STGM READ o \_ \_ \_ STGM \_ READWRITE (no se admite el modo STGM \_ WRITE).

[**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)

Abre un conjunto de propiedades existente en el almacenamiento de propiedades actual. En la devolución, proporciona un puntero de interfaz a la implementación de archivo compuesto [**de IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage). Este método requiere que el modo de uso compartido especificado en el parámetro *grfMode* sea STGM SHARE EXCLUSIVE y que el modo de acceso sea STGM READ o \_ \_ \_ STGM \_ READWRITE (no se admite STGM \_ WRITE).

[**IPropertySetStorage::D elete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)

Elimina un conjunto de propiedades en este almacenamiento de propiedades.

[**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)

Crea un objeto que se usa para enumerar [**las estructuras STATPROPSETSTG.**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) Cada **estructura STATPROPSETSTG** proporciona datos sobre un único conjunto de propiedades.

## <a name="remarks"></a>Comentarios

A partir Windows 2000, la implementación de archivo compuesto [**de IPropertySetStorage admite**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) el modo simple. El modo simple se indica especificando la marca STGM SIMPLE para las funciones \_ [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) y [**StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) Si el archivo compuesto se abre en modo simple, la implementación **de IPropertySetStorage** asociada está limitada de la siguiente manera:

-   Solo se pueden crear conjuntos de propiedades simples. Es decir, si se especifica el valor PROPSETFLAG NONSIMPLE en el parámetro \_ *grfFlags* para el método [**IPropertySetStorage::Create,**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) se produce un error.
-   Después de crear un archivo compuesto con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) mediante STGM SIMPLE y consultar la interfaz IPropertySetStorage, solo puede llamar a \_ [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) una vez. [](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) A continuación, debe liberar la [**interfaz IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) antes de llamar de nuevo **al método Create.** Para obtener más información sobre el modo simple, vea [**STGM Constants**](stgm-constants.md).
-   No puede usar el [**método IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) para abrir un conjunto de propiedades después de usar [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) para crear el objeto de almacenamiento. En su lugar, debe [**usar StgOpenStorageEx antes**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) de consultar [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) y llamar al **método Open.**
-   Después de abrir un archivo compuesto con [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) mediante la marca SIMPLE de STGM y consultar la interfaz IPropertySetStorage, puede abrir una propiedad establecida a la vez mediante \_ [**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open). [](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) Además, es posible que no sea posible aumentar el tamaño total del conjunto de propiedades mientras el conjunto de propiedades está abierto.

Los conjuntos de propiedades simples no se pueden realizar transacciones. No puede especificar STGM TRANSACTED en el parámetro grfmode de los métodos Create y Open a menos que también especifique PROPSETFLAG NONSIMPLE en el \_ parámetro  [](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) [](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) \_ *grfFlags.* Tenga en cuenta que los conjuntos de propiedades simples y no simples no están relacionados con los conjuntos de propiedades de modo simple descritos anteriormente. Para obtener más información sobre los conjuntos de propiedades simples y no simples, [vea Storage y Objetos de secuencia para un conjunto de propiedades](storage-vs--stream-for-a-property-set.md).

> [!Note]  
> Los conjuntos de propiedades DocumentSummaryInformation y UserDefined son únicos, ya que pueden tener dos secciones de conjunto de propiedades. Para obtener más información, [vea Los conjuntos de propiedades DocumentSummaryInformation y UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IPropertyStorage: implementación de archivos compuestos](ipropertystorage-compound-file-implementation.md)
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

 

 