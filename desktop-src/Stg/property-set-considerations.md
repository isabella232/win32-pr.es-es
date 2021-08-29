---
title: Consideraciones sobre el conjunto de propiedades
description: Se recomienda encarecidamente que los conjuntos de propiedades se queden pequeños porque la secuencia del conjunto de propiedades se lee en la memoria antes de que se pueda leer o escribir una sola propiedad.
ms.assetid: 520db05e-81cd-40ef-af89-471d7194c634
keywords:
- Consideraciones sobre el conjunto de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f1ce6ba761922619c2e52d8a311249bf72ddf7d31ea157c11468f472fd88367
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992396"
---
# <a name="property-set-considerations"></a>Consideraciones sobre el conjunto de propiedades

Se recomienda encarecidamente que los conjuntos de propiedades se queden pequeños porque la secuencia del conjunto de propiedades se lee en la memoria antes de que se pueda leer o escribir una sola propiedad. "pequeño" significa menos de 32 kilobytes de datos. Esto rara vez presenta un problema porque normalmente, las propiedades "en línea" serán elementos pequeños, como cadenas descriptivas, palabras clave, marcas de tiempo, recuentos, nombres de autor, identificadores únicos globales (GUID), identificadores de clase (CLSID), etc.

Para almacenar fragmentos de datos más grandes, o en casos en los que el tamaño total de un conjunto de propiedades relacionadas supera con creces la cantidad recomendada, se recomienda encarecidamente el uso de tipos no simples como **VT \_ STREAM** y **VT \_ STORAGE.** No se almacenan en la secuencia del conjunto de propiedades, por lo que no afectan significativamente a la sobrecarga inicial del primer acceso y escritura de una propiedad. Hay una sobrecarga mínima, ya que la secuencia del conjunto de propiedades contiene el nombre de la propiedad con valores de almacenamiento o secuencia del mismo nivel y esto tarda una pequeña cantidad de tiempo adicional en procesarse.

Para más información, consulte:

-   [Consideraciones sobre la implementación de IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)
-   [Almacenar conjuntos de propiedades](storing-property-sets.md)
-   [Características de rendimiento](performance-characteristics.md)
-   [Implementar el conjunto de propiedades de información de resumen](implementing-the-summary-information-property-set.md)

 

 




