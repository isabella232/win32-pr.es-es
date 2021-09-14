---
title: ¿Qué hace que una consulta sea rápida?
description: En este tema se enumeran los métodos de programación preferidos que se usan al consultar un directorio.
ms.assetid: d96f330f-3c57-4edc-9fd2-970f908b54c2
ms.tgt_platform: multiple
keywords:
- ¿Qué hace que un ADSI de consulta rápida?
- consulta ADSI, lo que hace que una consulta sea rápida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883db1e9de7b7b7a1179c814d6f66f774685083e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970368"
---
# <a name="what-makes-a-fast-query"></a>¿Qué hace que una consulta sea rápida?

Tenga en cuenta los siguientes conceptos de mejora del rendimiento al ejecutar una consulta:

-   Si es posible, filtre solo por atributos indexados. Use atributos de índice que espera que generen el menor número de visitas. Para obtener más información y una lista completa de los atributos indizados para Windows, [vea Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema).
-   Busque en **objectCategory en** lugar de **objectClass** porque **objectClass** no es una propiedad indizada.
-   Tenga en cuenta las referencias. Considere la posibilidad de buscar en el catálogo global si los atributos aparecen como GC replicados.
-   Evite buscar texto en el centro y al final de una cadena. Por ejemplo, "cn= \* \* montés" o "cn= \* larouse".
-   Suponga que una búsqueda de subárbol devolverá un conjunto de resultados grande. Use la paginación al realizar búsquedas en subárboles. A continuación, el servidor podrá transmitir un conjunto de resultados grande en fragmentos, lo que reduce los recursos de memoria del lado servidor. Esto reduce eficazmente el uso de la red y reduce la necesidad de enviar fragmentos de datos extremadamente grandes a través de la red.
-   Ajuste el ámbito de las búsquedas correctamente para no recuperar más de lo necesario.
-   Realice una búsqueda compleja en varios atributos, ya que consume menos rendimiento que realizar varias búsquedas. Una búsqueda de un objeto que lee dos atributos es más eficaz que dos búsquedas para el mismo objeto y cada una devuelve un atributo.
-   Para leer el atributo con un gran número de valores, use límites de intervalo para minimizar el tamaño de búsqueda para que pueda leer unos miles de miembros a la vez. Para obtener más información sobre cómo especificar límites de intervalo de atributos, vea [Recuperación del intervalo de atributos.](attribute-range-retrieval.md)
-   Enlazar a un objeto contiene el identificador de enlace durante el resto de la sesión. No enlace ni desenlate para cada llamada. Si usa ADO o OLE DB, no cree muchos objetos de conexión.
-   Lea rootDSE una vez y recuerde su contenido durante el resto de la sesión.

 

 