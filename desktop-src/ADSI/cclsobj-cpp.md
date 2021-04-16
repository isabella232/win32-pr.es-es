---
title: CCLSOBJ. CPP
description: En el componente de proveedor de ejemplo, las funciones del objeto de clase de esquema se encuentran en cclsobj. cpp.
ms.assetid: e8cdef8e-c031-49e0-9496-871064aec8bd
ms.tgt_platform: multiple
keywords:
- CSampleDSClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23c198413819627ce1fcb5a605bd8e45faae0ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656193"
---
# <a name="cclsobjcpp"></a>CCLSOBJ. CPP

En el componente de proveedor de ejemplo, las funciones del objeto de clase de esquema se encuentran en cclsobj. cpp.

La clase **CSampleDSClass** se define en este archivo. **CSampleDSClass** se define con métodos y propiedades que se enumeran en la tabla siguiente.



| Método                      | Descripción                                                                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSClass**          | Constructor estándar.                                                                                                                                                                                      |
| **~ CSampleDSClass**         | Destructor estándar.                                                                                                                                                                                       |
| **CreateClass**             | Cree un objeto de clase de esquema ADs. Definiciones de atributos de búsqueda mediante una llamada a **SampleDSGetClassDefinition**.                                                                                                 |
| **CreateClass**             | Cree un objeto de clase de esquema, según las definiciones de atributo, estableciendo los atributos conocidos, como los enumerados en [**IADsClass:: MandatoryAttributes**](iadsclass-property-methods.md).                     |
| **AllocateClassObject**     | Cree un objeto de clase de esquema y cargue sus datos de tipo.                                                                                                                                                       |
| **QueryInterface**          | Devuelve el puntero de interfaz solicitado, si está disponible.                                                                                                                                                      |
| Métodos IADs estándar.      | Métodos de interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) estándar incluidos en este archivo.                                                                                                                                     |
| Métodos estándar de IADsClass. | Métodos de interfaz [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) estándar incluidos en este archivo.                                                                                                                           |
| **CreatePropertyList**      | Cree una lista de propiedades asociadas a esta clase de esquema mediante una llamada a **CreatePropertyEntry**.                                                                                                          |
| **CreatePropertyEntry**     | Cree un objeto de propiedad en esta clase de esquema.                                                                                                                                                           |
| **FreePropertyEntry**       | Libere la entrada realizada en **CreatePropertyEntry**.                                                                                                                                                            |
| **MakeVariantFromPropList** | Cree una matriz de variantes a partir de la lista de propiedades creada por **CreatePropertyList**. Se puede usar en la implementación de [**IADsClass:: MandatoryAttributes**](iadsclass-property-methods.md) y así sucesivamente. |



 

 

 




