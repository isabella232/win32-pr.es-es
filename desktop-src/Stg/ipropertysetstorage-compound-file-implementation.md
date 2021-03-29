---
title: IPropertySetStorage-Compound la implementación de archivos
description: La implementación del objeto de almacenamiento de archivo compuesto COM incluye una implementación de IPropertyStorage, la interfaz que administra un único conjunto de propiedades persistentes y IPropertySetStorage, la interfaz que administra los grupos de conjuntos de propiedades persistentes.
ms.assetid: de2cb778-c6eb-4487-996b-87405674f603
keywords:
- IPropertySetStorage Strctd STG, implementaciones, archivo compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9053a7cf6bf1ae7e4230b15eb0117c428acb08da
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792963"
---
# <a name="ipropertysetstorage-compound-file-implementation"></a>IPropertySetStorage-Compound la implementación de archivos

La [implementación del objeto de almacenamiento de archivo compuesto com](ipropertystorage-compound-file-implementation.md) incluye una implementación de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), la interfaz que administra un único conjunto de propiedades persistentes y [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), la interfaz que administra los grupos de conjuntos de propiedades persistentes.

Para obtener un puntero a la implementación de archivo compuesto de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), especifique el nombre definido por el encabezado para el identificador de IID de identificador \_ como parámetro *riid* , o bien use las funciones [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . En ambos casos, especifique \_ el almacenamiento de STGFMT como el parámetro *STGFMT* . (STGFMT \_ También se puede especificar ANY en el caso de **StgOpenStorageEx**). Además, especifique el nombre definido por el encabezado para el IID del identificador de interfaz (IID) \_ IPropertySetStorage como parámetro *riid* . Ambas funciones proporcionan un puntero a la interfaz **IPropertySetStorage** del objeto.

Otra manera de obtener un puntero a la implementación de archivos compuestos es especificar el nombre definido por el encabezado para el identificador de IID de identificador \_ como parámetro *riid* , o para usar las funciones [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) o [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) . Esto proporcionará un puntero a la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) de objetos. Cuando desee trabajar con conjuntos de propiedades persistentes, llame a [**IStorage:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) .

## <a name="when-to-use-ipropertysetstorage"></a>Cuándo usar IPropertySetStorage

Llame a los métodos de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para crear, abrir o eliminar conjuntos de propiedades en el almacenamiento del conjunto de propiedades de archivo compuesto actual. También hay un método, [**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), que proporciona un puntero a un enumerador que se puede usar para enumerar los conjuntos de propiedades en el almacenamiento.

## <a name="methods"></a>Métodos

[**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)

Crea un nuevo conjunto de propiedades en el almacenamiento de archivos compuesto actual y, en la devolución, proporciona un puntero de interfaz a la implementación de archivo compuesto [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . En esta implementación, los conjuntos de propiedades se pueden transaccionar solo si \_ se especifica PROPSETFLAG nonsimple. Este método requiere que el modo de uso compartido especificado en el parámetro *grfMode* sea STGM \_ compartido \_ exclusivo y que el modo de acceso sea STGM \_ Read o STGM \_ ReadWrite ( \_ no se admite el modo de escritura STGM).

[**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)

Abre un conjunto de propiedades existente en el almacenamiento de propiedades actual. En la devolución, proporciona un puntero de interfaz a la implementación de archivo compuesto de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage). Este método requiere que el modo de uso compartido especificado en el parámetro *grfMode* sea STGM \_ compartido \_ exclusivo y que el modo de acceso sea STGM \_ Read o STGM \_ ReadWrite ( \_ no se admite la escritura en STGM).

[**IPropertySetStorage::D iminar**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)

Elimina un conjunto de propiedades en este almacenamiento de propiedades.

[**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)

Crea un objeto que se usa para enumerar las estructuras [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Cada estructura **STATPROPSETSTG** proporciona datos sobre un conjunto de propiedades único.

## <a name="remarks"></a>Observaciones

A partir de Windows 2000, la implementación de archivo compuesto de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) admite el modo simple. El modo simple se indica especificando la \_ marca de STGM simple para las funciones [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) y [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . Si el archivo compuesto se abre en modo simple, la implementación de **IPropertySetStorage** asociada se limita de la siguiente manera:

-   Solo se pueden crear conjuntos de propiedades simples. Es decir, si se especifica el \_ valor NONSIMPLE PROPSETFLAG en el parámetro *grfFlags* para el método [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) se produce un error.
-   Después de crear un archivo compuesto con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) mediante STGM \_ simple y consultar la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) , solo puede llamar una vez a [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) . Después, debe liberar la interfaz [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) antes de volver a llamar al método **Create** . Para obtener más información sobre el modo simple, vea [**constantes STGM**](stgm-constants.md).
-   No se puede usar el método [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) para abrir un conjunto de propiedades después de usar [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) para crear el objeto de almacenamiento. En su lugar, debe usar [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) antes de consultar [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) y llamar al método **Open** .
-   Después de abrir un archivo compuesto con [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) mediante la \_ marca simple STGM y la consulta de la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) , puede abrir un conjunto de propiedades a la vez mediante [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open). Además, es posible que no sea posible que el tamaño total del conjunto de propiedades aumente mientras el conjunto de propiedades esté abierto.

No se pueden realizar transacciones en conjuntos de propiedades simples. No se puede especificar STGM \_ TRANSaccionado en el parámetro *grfmode* de los métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) y [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , a menos que también se especifique PROPSETFLAG \_ nonsimple en el parámetro *grfFlags* . Tenga en cuenta que los conjuntos de propiedades simples y no simples no están relacionados con los conjuntos de propiedades de modo simple descritos anteriormente. Para obtener más información sobre los conjuntos de propiedades simples y no simples, vea [almacenamiento y objetos de secuencia para un conjunto de propiedades](storage-vs--stream-for-a-property-set.md).

> [!Note]  
> Los conjuntos de propiedades DocumentSummaryInformation y UserDefined son únicos en que pueden tener dos secciones set de propiedad. Para obtener más información, vea [los conjuntos de propiedades DocumentSummaryInformation y UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IPropertyStorage: implementación de archivos compuestos](ipropertystorage-compound-file-implementation.md)
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

 

 