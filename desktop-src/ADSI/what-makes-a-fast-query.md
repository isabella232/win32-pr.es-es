---
title: Cómo realiza una consulta rápida
description: En este tema se enumeran los métodos de programación preferidos que se usan al consultar un directorio.
ms.assetid: d96f330f-3c57-4edc-9fd2-970f908b54c2
ms.tgt_platform: multiple
keywords:
- Qué hace una consulta rápida ADSI
- consultas ADSI, qué hace una consulta rápida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883db1e9de7b7b7a1179c814d6f66f774685083e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904823"
---
# <a name="what-makes-a-fast-query"></a>¿Qué hace una consulta rápida?

Tenga en cuenta los siguientes conceptos de mejora del rendimiento al ejecutar una consulta:

-   Si es posible, filtre solo por atributos indexados. Use los atributos de índice que espera que generen el menor número de aciertos. Para obtener más información y una lista completa de los atributos indexados para Windows, vea [Active Directory esquema](/windows/desktop/ADSchema/active-directory-schema).
-   Busque en **objectCategory** en lugar de **objectClass** porque **objectClass** no es una propiedad indizada.
-   Tenga en cuenta las referencias. Considere la posibilidad de buscar en el catálogo global si los atributos se muestran como GC replicados.
-   Evite buscar texto en el centro y al final de una cadena. Por ejemplo, "CN = \* Hille \* " o "CN = \* Larouse".
-   Supongamos que una búsqueda de subárbol devolverá un conjunto de resultados grande. Use la paginación al realizar búsquedas de subárbol. A continuación, el servidor podrá transmitir un conjunto de resultados grande en fragmentos, lo que reduce los recursos de memoria del servidor. Esto simplifica el uso de la red y reduce la necesidad de enviar fragmentos de datos extremadamente grandes a través de la red.
-   Considere correctamente el ámbito de las búsquedas para que no recupere más de lo necesario.
-   Realice una búsqueda compleja en varios atributos, ya que el rendimiento es menor que si se realizan varias búsquedas. Una búsqueda de un objeto que lee dos atributos es más eficaz que dos búsquedas para el mismo objeto, cada uno de los cuales devuelve un atributo.
-   Para leer el atributo con un gran número de valores, use límites de intervalo para minimizar el tamaño de búsqueda, de modo que pueda leer algunos miles de miembros a la vez. Para obtener más información sobre cómo especificar los límites de los intervalos de atributo, consulte [recuperación de intervalos de atributos](attribute-range-retrieval.md).
-   Enlazar a un objeto que contiene el identificador de enlace para el resto de la sesión. No enlace y desenlace para cada llamada. Si usa ADO o OLE DB, no cree muchos objetos de conexión.
-   Lea el rootDSE una vez y recuerde su contenido durante el resto de la sesión.

 

 