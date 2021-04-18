---
title: Administrar conjuntos de propiedades
description: Un conjunto de propiedades persistentes contiene datos relacionados como propiedades.
ms.assetid: 19ff2751-87f3-43d8-9307-ce2dd399f694
keywords:
- Administrar conjuntos de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3f9862d3074a5221bf1d5d975754486a562f87
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665834"
---
# <a name="managing-property-sets"></a>Administrar conjuntos de propiedades

Un conjunto de propiedades persistentes contiene datos relacionados como propiedades. Cada conjunto de propiedades se identifica con un FMTID y un identificador único global (GUID) que permite a las aplicaciones, que tienen acceso al conjunto de propiedades, identificar el conjunto de propiedades. A través de esta identificación, la aplicación interpreta las propiedades que contiene el conjunto.

Por ejemplo, las propiedades de formato de caracteres de un procesador de textos o los atributos de representación de un elemento en un programa de dibujo son conjuntos de propiedades.

COM define la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para facilitar la administración de conjuntos de propiedades. A través de los métodos de esta interfaz, puede crear un nuevo conjunto de propiedades, o bien abrir o eliminar un conjunto de propiedades existente. Además, proporciona un método que crea un enumerador y proporciona un puntero a su interfaz [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Puede llamar a los métodos de esta interfaz para enumerar las estructuras [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) en el objeto, que proporcionará información sobre todos los conjuntos de propiedades en el objeto.

Al crear o abrir una instancia de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), es similar a abrir un objeto que admita [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), ya que es necesario especificar el modo de almacenamiento en el que se abre la interfaz. En el caso de **IStorage**, incluyen el modo de transacción, el modo de lectura y escritura y el modo de uso compartido.

Cuando cree un conjunto de propiedades con una llamada a [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), especifique si el conjunto de propiedades debe ser simple o no simple. Un conjunto de propiedades simple contiene tipos que se pueden escribir completamente en el flujo del conjunto de propiedades, cuyo tamaño debe ser limitado y no puede ser superior a 256 KB en Windows NT 4,0 y versiones anteriores, o 1 MB en Windows 2000, Windows XP y Windows Server 2003. Sin embargo, si necesita almacenar una cantidad mayor de información en el conjunto de propiedades, puede especificar que el conjunto de propiedades no sea simple. Esto le permite usar uno o varios de los tipos que especifican solo un puntero a un objeto de almacenamiento o de secuencia. Estos tipos son el \_ flujo VT, el \_ objeto VT Streamed, el \_ almacenamiento VT y el \_ objeto almacenado VT \_ .

Los datos almacenados en estas propiedades no se cuentan con el límite de tamaño del conjunto de propiedades de 256 KB en Windows NT 4,0 o versiones anteriores, o con el límite de 1 MB en Windows 2000, Windows XP y Windows Server 2003. Sin embargo, se aplican los datos sobre la propiedad, como su nombre. Además, si necesita una actualización de transacción, el conjunto de propiedades debe ser no simple. Por supuesto, hay una penalización de rendimiento determinada para abrir estos tipos, ya que requiere abrir el flujo o el objeto de almacenamiento en el que se tiene el puntero.

Si su aplicación usa archivos compuestos, puede usar la implementación proporcionada por COM de estas interfaces, que se implementan en el objeto de almacenamiento de archivo compuesto COM.

Cada conjunto de propiedades se compone principalmente de un grupo de propiedades conectado lógicamente, como se describe en [Administración de propiedades](managing-properties.md).

Para obtener más información acerca de los conjuntos de propiedades en COM, vea:

-   [Implementaciones de conjuntos de propiedades en COM](property-set-implementations-in-com.md)
-   [Consideraciones sobre los conjuntos de propiedades](property-set-considerations.md)
-   [Consideraciones de implementación de IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)
-   [Almacenar conjuntos de propiedades](storing-property-sets.md)
-   [Características de rendimiento](performance-characteristics.md)
-   [Implementar el conjunto de propiedades de información de Resumen](implementing-the-summary-information-property-set.md)

 

 