---
title: Incluir atributos en el catálogo global
description: El catálogo global de un bosque incluye una réplica parcial de todos los objetos del bosque.
ms.assetid: 185467ed-7bcf-41e9-9862-02412009c437
ms.tgt_platform: multiple
keywords:
- Atributos incluidos en el catálogo global
- Atributos AD, incluidos en el catálogo global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ffbffd39e92456e6de7eccc6127f8a1351a4466
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487514"
---
# <a name="including-attributes-in-the-global-catalog"></a>Incluir atributos en el catálogo global

El catálogo global de un bosque incluye una réplica parcial de todos los objetos del bosque. Para cada objeto, el catálogo global solo incluye un subconjunto de los atributos de cada objeto. El atributo [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) de un objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) se establece en **true** si el atributo se replica en el catálogo global.

Los atributos con las siguientes características son adecuados para el almacenamiento en el catálogo global:

-   El atributo es de interés global, ya sea porque el atributo es necesario para buscar objetos que se pueden producir en cualquier parte del bosque, o porque el acceso de lectura al atributo es valioso incluso cuando no se puede tener acceso al objeto completo. Un ejemplo del primer tipo es el atributo [**Location**](/windows/desktop/ADSchema/a-location) , que se puede utilizar para buscar un objeto [**printQueue**](/windows/desktop/ADSchema/c-printqueue) . Un ejemplo del segundo tipo es [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber), ya que puede llamar a alguien incluso si no puede tener acceso a una réplica completa de su objeto de [**usuario**](/windows/desktop/ADSchema/c-user) .
-   La volatilidad del atributo es muy baja. Esto es importante, porque si una clase de atributo se incluye en el catálogo global, los cambios en todos los valores de esa clase de atributo en todo el bosque de la empresa se replican en todos los servidores de catálogo global de la empresa.
-   El tamaño del valor del atributo es pequeño. "Pequeño" es muy subjetivo: cuando se coloca un atributo en el catálogo global, se debe tener en cuenta el impacto de la replicación del atributo en todos los servidores de catálogo global de la empresa. Cuanto menor sea el atributo, menor será el impacto. Dado que la replicación solo se produce cuando cambia el atributo, el impacto de la replicación también es menor a medida que se reduce la volatilidad, por lo que un atributo grande con una volatilidad muy baja puede tener un impacto general menor que un atributo pequeño con una volatilidad elevada.

Al decidir si colocar o no un atributo en el catálogo global, recuerde que está realizando un aumento de la replicación y un mayor almacenamiento en disco en los servidores de catálogo global para un rendimiento de consulta potencialmente más rápido. Normalmente, se usaría el catálogo global para buscar un objeto de interés, de modo que se puedan leer los atributos seleccionados del objeto. Si los atributos que le interesan se replican en el catálogo global, puede leerlos directamente desde el catálogo global. Como alternativa, para leer los atributos que no se replican en el catálogo global, debe realizar pasos adicionales para recuperarlos. En este caso, después de buscar en el catálogo global para encontrar el objeto de interés, debe leer el nombre distintivo del objeto del catálogo global, usar el DN para enlazar directamente a una réplica completa del objeto, que puede estar en un servidor diferente y, por último, leer los atributos no globales del catálogo de la réplica completa del objeto.

Los atributos consultados y a los que se hace referencia con frecuencia, como el nombre y el número de teléfono de un empleado, son buenos para incluirlos en el catálogo global. Un atributo de referencia poco frecuente, como "driverVersion" para las impresoras, se queda mejor fuera del catálogo global.

 

 