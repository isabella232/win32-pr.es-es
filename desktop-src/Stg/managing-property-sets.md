---
title: Administración de conjuntos de propiedades
description: Un conjunto de propiedades persistente contiene datos relacionados como propiedades.
ms.assetid: 19ff2751-87f3-43d8-9307-ce2dd399f694
keywords:
- Administración de conjuntos de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b6b81c466232d4fd325d53a3cfe67ebb1cbc60c757a6dfe135a021ab7892a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960889"
---
# <a name="managing-property-sets"></a>Administración de conjuntos de propiedades

Un conjunto de propiedades persistente contiene datos relacionados como propiedades. Cada conjunto de propiedades se identifica con un FMTID y un identificador único global (GUID) que permite a las aplicaciones, que acceden al conjunto de propiedades, identificar el conjunto de propiedades. A través de esta identificación, la aplicación interpreta las propiedades que contiene el conjunto.

Por ejemplo, las propiedades de formato de caracteres de un procesador de palabras o los atributos de representación de un elemento de un programa de dibujo son conjuntos de propiedades.

COM define la [**interfaz IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para facilitar la administración de conjuntos de propiedades. Mediante los métodos de esta interfaz, puede crear un nuevo conjunto de propiedades o abrir o eliminar un conjunto de propiedades existente. Además, proporciona un método que crea un enumerador y proporciona un puntero a su [**interfaz IEnumSTATPROPSETSTG.**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) Puede llamar a los métodos de esta interfaz para enumerar estructuras [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) en el objeto, lo que proporcionará información sobre todos los conjuntos de propiedades del objeto.

Al crear o abrir una instancia de [**IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)es similar a abrir un objeto que admita [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), ya que debe especificar el modo de almacenamiento en el que va a abrir la interfaz. Para **IStorage,** incluyen el modo de transacción, el modo de lectura y escritura y el modo de uso compartido.

Al crear un conjunto de propiedades con una llamada a [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), especifique si el conjunto de propiedades va a ser simple o no sencillo. Un conjunto de propiedades simple contiene tipos que se pueden escribir completamente dentro de la secuencia del conjunto de propiedades, que está diseñado para tener un tamaño limitado y no puede ser superior a 256 KB en Windows NT 4.0 y versiones anteriores, o 1 MB en Windows 2000, Windows XP y Windows Server 2003. Sin embargo, cuando necesite almacenar una mayor cantidad de información en el conjunto de propiedades, puede especificar que el conjunto de propiedades no sea simple. Esto le permite usar uno o varios de los tipos que especifican solo un puntero a un objeto de almacenamiento o flujo. Estos tipos son VT \_ STREAM, VT \_ STREAMED OBJECT, VT \_ STORAGE y VT STORED \_ \_ OBJECT.

Los datos almacenados en estas propiedades no se cuentan con el límite de tamaño del conjunto de propiedades de 256 KB en Windows NT 4.0 o versiones anteriores, o el límite de 1 MB en Windows 2000, Windows XP y Windows Server 2003. Sin embargo, se aplican datos sobre la propiedad, como su nombre. Además, si necesita una actualización con transacciones, el conjunto de propiedades debe ser no simple. Por supuesto, hay una determinada penalización de rendimiento para abrir estos tipos, ya que requiere abrir el flujo o el objeto de almacenamiento al que tiene el puntero.

Si la aplicación usa archivos compuestos, puede usar la implementación proporcionada por COM de estas interfaces, que se implementan en el objeto de almacenamiento de archivos compuestos COM.

Cada conjunto de propiedades consta principalmente de un grupo de propiedades conectados lógicamente, como se describe en [Administración de propiedades](managing-properties.md).

Para obtener más información sobre los conjuntos de propiedades en COM, vea:

-   [Implementaciones de conjunto de propiedades en COM](property-set-implementations-in-com.md)
-   [Consideraciones sobre el conjunto de propiedades](property-set-considerations.md)
-   [Consideraciones sobre la implementación de IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)
-   [Almacenar conjuntos de propiedades](storing-property-sets.md)
-   [Características de rendimiento](performance-characteristics.md)
-   [Implementar el conjunto de propiedades Demmary Information](implementing-the-summary-information-property-set.md)

 

 