---
title: GUID de coherencia
description: Los GUID de coherencia son una estrategia de detección que permite a una aplicación detectar actualizaciones parciales.
ms.assetid: 3418667f-4d5a-4a4b-b0f5-7744a21608f7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0a6f0105ebc7732303f74afdebba33883a9d8bc915ef36cbb314858c56e5ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021999"
---
# <a name="consistency-guids"></a>GUID de coherencia

Los GUID de coherencia son una estrategia de detección que permite a una aplicación detectar actualizaciones parciales. Se aplica un GUID de coherencia (IDentifier único global) a cada objeto de un conjunto relacionado. En la implementación, una aplicación de origen genera un nuevo GUID y lo aplica a cada objeto que actualiza en el conjunto de objetos relacionados. A continuación, aplica el nuevo GUID al resto de los objetos del conjunto y finaliza aplicando el nuevo GUID al objeto "maestro". Normalmente, el objeto "maestro" será un contenedor que es el elemento primario de los demás objetos del conjunto.

Algunas consideraciones importantes:

-   Los GUID de coherencia combinados con recuentos de objetos o sumas de comprobación son más eficaces que los GUID de coherencia por sí solos, porque la aplicación que lee los objetos puede no saber cuántos objetos con el GUID deben estar presentes.
-   Las aplicaciones deben generar sus propios GUID (una API de Microsoft Win32, UuidCreate, proporciona esta función) y no usar los GUID generados por el sistema que se encuentran en el atributo **objectGUID de** un objeto. Esto se debe a que un GUID de coherencia debe cambiar cada vez que se actualiza el conjunto de objetos. Los GUID de identidad de objeto que se encuentran **en objectGUID** nunca cambian una vez creado el objeto.
-   Los GUID de coherencia suponen que no se comparte ningún objeto entre los conjuntos, por lo que cada conjunto puede tener un GUID de coherencia único.

 

 




