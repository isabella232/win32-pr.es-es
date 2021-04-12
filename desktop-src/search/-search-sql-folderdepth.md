---
description: Los predicados de profundidad de carpeta controlan el ámbito de una búsqueda especificando una ruta de acceso y si se realiza un recorrido profundo o superficial.
ms.assetid: 8eadbd42-3538-412e-9bf8-b2355d23437e
title: Predicados de ámbito y directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2418b2149a5bf05bd000460c787b7f967856c5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153961"
---
# <a name="scope-and-directory-predicates"></a>Predicados de ámbito y directorio

Los predicados de profundidad de carpeta controlan el ámbito de una búsqueda especificando una ruta de acceso y si se realiza un recorrido profundo o superficial. A continuación se muestra la sintaxis de los predicados de profundidad de la carpeta:


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



El predicado va seguido de un signo igual. La ruta de acceso se incluye entre comillas simples y debe comenzar por un protocolo y dos puntos (por ejemplo, `file:` , `mapi:` o `csc:` ). El predicado de ámbito realiza un recorrido profundo de la ruta de acceso, incluidas todas las subcarpetas, mientras que el predicado de directorio realiza un recorrido superficial solo de la carpeta especificada. Al igual que otras restricciones de Lenguaje de consulta estructurado (SQL), puede especificar más de una restricción de profundidad de carpeta en una sola consulta.

Para consultar el catálogo local de un equipo remoto, incluya el nombre del equipo delante del catálogo y una ruta de acceso UNC (Convención de nomenclatura universal) en el equipo remoto en la cláusula SCOPE o DIRECTORY.

## <a name="examples"></a>Ejemplos


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



En el primer ejemplo de ámbito se busca en la carpeta C: \\ files \\ Reports y en todas sus subcarpetas. En el ejemplo de directorio solo se buscan en la carpeta raíz los informes C: \\ archivos \\ .

> [!Note]  
> Las barras diagonales inversas del sistema de archivos ( \\ ) se convierten en una barra diagonal de estilo URL (a veces llamadas barras diagonales) (/).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Cláusula FROM](-search-sql-from.md)
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> </dl>

 

 



