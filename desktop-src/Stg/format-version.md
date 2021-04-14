---
title: Versión de formato
description: El valor de la versión de formato es un tipo de datos de WORD que se usa para indicar la versión de formato de esta secuencia.
ms.assetid: 38362a45-4f49-4a85-aabe-452ff32c2812
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503019a3bfe3224e4137ac3bfd43fadbe1e15a3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533279"
---
# <a name="format-version"></a>Versión de formato

El valor de la versión de formato es un tipo de datos de **Word** que se usa para indicar la versión de formato de esta secuencia. Puede ser cero o uno. El indicador de versión de formato debe comprobarse cuando se lee el conjunto de propiedades. Si no es cero o uno, la secuencia se escribió en una especificación diferente y no se puede leer mediante el código desarrollado según esta especificación.

Los conjuntos de propiedades con la versión de formato 1 son equivalentes a la versión 0, con las siguientes adiciones:

-   **Nombres de propiedad que distinguen mayúsculas de minúsculas**. Los nombres de propiedad se almacenan en la propiedad de diccionario reservada, [identificador de propiedad 0](/windows/desktop/Stg/reserved-property-identifiers). En los conjuntos de propiedades de la versión 1, estos nombres pueden distinguir entre mayúsculas y minúsculas. La distinción entre mayúsculas y minúsculas viene determinada por la propiedad comportamiento reservado, ID. de [propiedad 0x80000003](/windows/desktop/Stg/reserved-property-identifiers).
-   **Nombres de propiedad largos**. Los conjuntos de propiedades de la versión 1, a diferencia de los conjuntos de propiedades de la versión 0, no se limitan en la longitud de los nombres de propiedad. Consulte [ID. de propiedad 0](/windows/desktop/Stg/reserved-property-identifiers) para obtener más información sobre los nombres de propiedad.
-   **Tipos de propiedad**. Los conjuntos de propiedades de la versión 1 pueden contener todos los tipos de propiedades que se pueden mantener en un conjunto de propiedades de la versión 0 más tipos adicionales. Vea la estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) para obtener más información sobre estos tipos.

 

 