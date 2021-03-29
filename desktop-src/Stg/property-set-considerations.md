---
title: Consideraciones sobre los conjuntos de propiedades
description: Se recomienda encarecidamente que los conjuntos de propiedades se mantengan reducidos porque la secuencia del conjunto de propiedades se lee en la memoria antes de que se pueda leer o escribir una sola propiedad.
ms.assetid: 520db05e-81cd-40ef-af89-471d7194c634
keywords:
- Consideraciones sobre los conjuntos de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfd89140092b13d113122ffe1c1a2b576e654c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780095"
---
# <a name="property-set-considerations"></a>Consideraciones sobre los conjuntos de propiedades

Se recomienda encarecidamente que los conjuntos de propiedades se mantengan reducidos porque la secuencia del conjunto de propiedades se lee en la memoria antes de que se pueda leer o escribir una sola propiedad. "pequeño" significa menos de 32 kilobytes de datos. Esto no suele presentar un problema, ya que, por lo general, las propiedades "en línea" serán elementos pequeños como cadenas descriptivas, palabras clave, marcas de tiempo, recuentos, nombres de autor, identificadores únicos globales (GUID), identificadores de clase (CLSID), etc.

Para almacenar grandes fragmentos de datos, o en los casos en los que el tamaño total de un conjunto de propiedades relacionadas supere la cantidad recomendada, se recomienda encarecidamente el uso de tipos no simples como el **\_ almacenamiento** **VT \_ Stream** y VT. No se almacenan en el flujo del conjunto de propiedades, por lo que no afectan de forma significativa a la sobrecarga inicial del primer acceso y la escritura de una propiedad. Hay una sobrecarga mínima, ya que la secuencia del conjunto de propiedades contiene el nombre de la propiedad del flujo o del valor de almacenamiento del mismo nivel, lo que tarda en procesarse una pequeña cantidad de tiempo.

Para más información, consulte:

-   [Consideraciones de implementación de IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)
-   [Almacenar conjuntos de propiedades](storing-property-sets.md)
-   [Características de rendimiento](performance-characteristics.md)
-   [Implementar el conjunto de propiedades de información de Resumen](implementing-the-summary-information-property-set.md)

 

 




