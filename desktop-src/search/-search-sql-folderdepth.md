---
description: Los predicados de profundidad de carpeta controlan el ámbito de una búsqueda especificando una ruta de acceso y si se debe realizar un recorrido profundo o superficial.
ms.assetid: 8eadbd42-3538-412e-9bf8-b2355d23437e
title: Predicados SCOPE y DIRECTORY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f221ba4048f1ab7f5096321cc00aed209acb5ca3e5616e6e6a4fbbc516dfc28b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462474"
---
# <a name="scope-and-directory-predicates"></a>Predicados SCOPE y DIRECTORY

Los predicados de profundidad de carpeta controlan el ámbito de una búsqueda especificando una ruta de acceso y si se debe realizar un recorrido profundo o superficial. A continuación se muestra la sintaxis de los predicados de profundidad de carpeta:


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



El predicado va seguido de un signo igual. La ruta de acceso se delimita entre comillas simples y debe comenzar con un protocolo y dos puntos (por ejemplo, `file:` `mapi:` , o `csc:` ). El predicado SCOPE realiza un recorrido profundo de la ruta de acceso, incluidas todas las subcarpetas, mientras que el predicado DIRECTORY realiza un recorrido superficial de solo la carpeta especificada. Al igual que Lenguaje de consulta estructurado restricciones de SQL , puede especificar más de una restricción de profundidad de carpeta en una sola consulta.

Para consultar el catálogo local de un equipo remoto, incluya el nombre del equipo antes del catálogo y una ruta de acceso de convención de nomenclatura universal (UNC) en el equipo remoto en la cláusula SCOPE o DIRECTORY.

## <a name="examples"></a>Ejemplos


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



El primer ejemplo scope busca en la carpeta C: \\ Files Reports y en todas sus \\ subcarpetas. En el ejemplo DE DIRECTORIO solo se busca la carpeta raíz C: \\ Informes \\ de archivos.

> [!Note]  
> Las barras diagonales inversas del sistema de archivos ( ) se convierten en una barra diagonal de estilo URL (a veces denominadas \\ barras diagonales) (/).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[FROM (Cláusula)](-search-sql-from.md)
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> </dl>

 

 



