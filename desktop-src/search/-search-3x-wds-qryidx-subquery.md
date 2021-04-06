---
description: Una subconsulta es un archivo de búsqueda guardado ( \* . Search-MS) que puede usar como filtro para una nueva consulta.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Argumento de subconsulta (búsqueda de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f673cf9c2a9867593fd6c8fdac83b5901f531257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000999"
---
# <a name="subquery-argument-windows-search"></a>Argumento de subconsulta (búsqueda de Windows)

Una subconsulta es un archivo de búsqueda guardado ( \* . Search-MS) que puede usar como filtro para una nueva consulta. Los resultados de la subconsulta se usan como origen de la nueva consulta. Por ejemplo, supongamos que tiene varios archivos de búsqueda guardados que restringen una consulta por lista de distribución de correo electrónico: Departamento. Search-MS, teamproject. Search-MS y corporatewide. Search-ms. El uso del `subquery` argumento le permite limitar las búsquedas de correo electrónico a cualquiera de estas búsquedas guardadas.

Este tema se organiza de la siguiente manera:

-   [Ejemplo](#example)
-   [Temas relacionados](#related-topics)

## <a name="example"></a>Ejemplo


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con argumentos de Parameter-Value](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argumentos de identificador de configuración regional](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Argumento de MIGAs de](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Argumento de sintaxis](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argumento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



