---
title: 'IPropertyStorage: implementación del sistema de archivos NTFS'
description: La versión 5,0 de NTFS proporciona una implementación de la interfaz IPropertyStorage para los archivos de un volumen NTFS cuando los archivos no son archivos compuestos.
ms.assetid: d0ffd975-5bc2-4de3-b0c1-c9188541f46a
keywords:
- IPropertyStorage Strctd STG, implementaciones, sistema de archivos NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca359bebbd05e67a034494023d7fc23089396b32
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665837"
---
# <a name="ipropertystorage-ntfs-file-system-implementation"></a>IPropertyStorage: implementación del sistema de archivos NTFS

La versión 5,0 de NTFS proporciona una implementación de la interfaz [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) para los archivos de un volumen NTFS cuando los archivos no son archivos compuestos.

**Para obtener un puntero a la implementación del sistema de archivos NTFS de IPropertySetStorage**

1.  Llame a [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) con la implementación NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).
2.  Llame a [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) mediante la implementación NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).

## <a name="when-to-use"></a>Cuándo usar

Use [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) para administrar propiedades dentro de un único conjunto de propiedades. Sus métodos admiten las propiedades de lectura, escritura y eliminación, así como los nombres de cadena opcionales que se pueden asociar a los identificadores de propiedad. Otro método le permite establecer las horas asociadas al almacenamiento de propiedades y otro permite la asignación de un CLSID, que se usa para asociar otro código, como el código de la interfaz de usuario (IU), con la propiedad establecida. La llamada al método [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) proporciona un puntero a la implementación NTFS de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), que permite enumerar las propiedades del conjunto.

## <a name="remarks"></a>Observaciones

La implementación de NTFS proporciona esencialmente las mismas características que la implementación de archivo compuesto. Para obtener más información, vea [IPropertyStorage: implementación de archivos compuestos](ipropertystorage-compound-file-implementation.md).

Dado que NTFS es un sistema de archivos sólido, un conjunto de propiedades NTFS nunca se quedará en un estado incorrecto. Cuando el contenido de un [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) de NTFS se vacía en el archivo NTFS subyacente, todos o ninguno de los Estados se escriben en el archivo como una operación atómica, incluso si se produce un error durante la operación, como una terminación anómala del proceso. Para lograr un comportamiento similar con la implementación de archivo compuesto, la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) primaria debe estar abierta en modo de transacción.

Este nivel de solidez solo es posible cuando se tiene acceso a un conjunto de propiedades NTFS en un volumen NTFS 5,0. Es posible tener acceso a los conjuntos de propiedades NTFS en versiones anteriores de NTFS (por ejemplo, un equipo que ejecuta en Windows NT o Windows 2000 que tiene acceso a los conjuntos de propiedades en un equipo de servidor de archivos que ejecuta en Windows NT 4,0), pero no se garantiza que estén en un estado correcto en caso de que se produzca un error inesperado.

Aunque la implementación de NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) no admite la transacción, la implementación NTFS de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) lo admite. Es decir, **la \_ transacción STGM** se puede especificar en el parámetro *GrfMode* para los métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) y [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) de **IPropertySetStorage**. Como en la implementación de archivo compuesto, el modo de transacción solo es posible para los almacenamientos de propiedades no simples (especificando **PROPSETFLAG no \_ simple** en el parámetro *grfFlags* ).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[IPropertySetStorage: implementación del sistema de archivos NTFS](ipropertysetstorage-ntfs-file-system-implementation.md)
</dt> </dl>

 

 