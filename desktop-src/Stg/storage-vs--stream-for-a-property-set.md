---
title: Storage y objetos de secuencia para un conjunto de propiedades
description: El programador especifica si un conjunto de propiedades se almacena en un almacenamiento o una secuencia cuando se crea el conjunto de propiedades.
ms.assetid: d0ca649a-d405-4c34-af02-9c2ca8b2790e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e63ff148a72342da4cf5a6d8e1d59feab5c9b5b6fcbdf8a413069413cdb1e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661845"
---
# <a name="storage-and-stream-objects-for-a-property-set"></a>Storage y objetos de secuencia para un conjunto de propiedades

El programador especifica si un conjunto de propiedades se almacena en un almacenamiento o una secuencia cuando se crea el conjunto de propiedades. El valor de enumeración PROPSETFLAG NONSIMPLE, pasado en el parámetro \_ *grfFlags* al método [**IPropertySetStorage::Create,**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) indica esto. El valor donde se almacena el conjunto de propiedades proporciona controles de aplicación adecuados para interoperar completamente a través de la [**interfaz IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) con el conjunto de propiedades COM.

Si se establece la marca PROPSETFLAG NONSIMPLE, el conjunto de propiedades se almacena en un objeto de almacenamiento y los valores de propiedad no simples se pueden \_ escribir en él. Los valores no simples incluyen valores con **un VARTYPE** de VT \_ STORAGE, VT \_ STREAM, VT \_ STORED OBJECT u VT STREAMED \_ \_ \_ OBJECT. Para obtener más información sobre **los valores VARTYPE** y cómo usarlos, vea la [**estructura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

Si no se establece la marca PROPSETFLAG NONSIMPLE, solo se pueden escribir valores simples \_ en el conjunto de propiedades.

En el objeto de almacenamiento de un conjunto de propiedades no simples, se crea una secuencia denominada Contents. Se trata de la secuencia principal del conjunto de propiedades y contiene todos los valores de propiedad simples. Los valores de propiedad no simples (flujos y almacenamientos) se almacenan en el objeto de almacenamiento principal del conjunto de propiedades como substreams y storages. Es decir, estos valores no simples se almacenan como elementos del mismo nivel en la secuencia Contenido. La implementación determina el nombre de los flujos y almacenamientos relacionados y se almacena en el flujo Contenido de forma similar a la forma en que se almacena una propiedad de cadena simple.

 

 