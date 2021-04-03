---
title: GUID de coherencia
description: Los GUID de coherencia son una estrategia de detección que permite a una aplicación detectar actualizaciones parciales.
ms.assetid: 3418667f-4d5a-4a4b-b0f5-7744a21608f7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcfb25d0f04a459217811a2ff0393fac47e3206
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075016"
---
# <a name="consistency-guids"></a>GUID de coherencia

Los GUID de coherencia son una estrategia de detección que permite a una aplicación detectar actualizaciones parciales. Se aplica un GUID de coherencia (identificador único global) a cada objeto de un conjunto relacionado. En la implementación, una aplicación de origen genera un nuevo GUID y lo aplica a cada objeto que actualiza en el conjunto de objetos relacionados. A continuación, aplica el nuevo GUID al resto de los objetos del conjunto y finaliza aplicando el nuevo GUID al objeto "Master". Normalmente, el objeto "Master" será un contenedor que sea el primario de los demás objetos del conjunto.

Algunas consideraciones importantes:

-   Los GUID de coherencia combinados con recuentos de objetos o sumas de comprobación son más efectivos que los GUID de coherencia solos, ya que es posible que la aplicación que lee los objetos no sepa Cuántos objetos tienen el GUID debe estar presente.
-   Las aplicaciones deben generar sus propios GUID (una API de Microsoft Win32, UuidCreate, proporciona esta función) y no usar los GUID generados por el sistema que se encuentran en el atributo **objectGUID** de un objeto. Esto se debe a que un GUID de coherencia debe cambiar cada vez que se actualiza el conjunto de objetos. Los GUID de identidad de objeto encontrados en **objectGUID** nunca cambian una vez creado el objeto.
-   Los GUID de coherencia suponen que ningún objeto se comparte entre conjuntos, por lo que cada conjunto puede tener un GUID de coherencia único.

 

 




