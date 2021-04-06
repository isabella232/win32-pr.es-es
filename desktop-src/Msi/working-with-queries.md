---
description: Dado que el instalador utiliza una base de datos relacional, existen funciones para realizar consultas de Lenguaje de consulta estructurado (SQL) a la base de datos. En el procedimiento siguiente se describe cómo usar SQL para consultar una base de datos.
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: Trabajar con consultas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0be4839c1e97f05d09769d69d62345b0602b789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002190"
---
# <a name="working-with-queries"></a>Trabajar con consultas

Dado que el instalador utiliza una base de datos relacional, existen funciones para realizar consultas de Lenguaje de consulta estructurado (SQL) a la base de datos. En el procedimiento siguiente se describe cómo usar SQL para consultar una base de datos.

**Para consultar una base de datos con SQL**

1.  Abra el objeto de [**vista**](view-object.md) con la instrucción SQL adecuada llamando a la función [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .

    Un objeto de [**vista**](view-object.md) es la tabla lógica que se crea aplicando una consulta a un conjunto de tablas. Las consultas SQL deben adherirse a la [sintaxis SQL](sql-syntax.md) proporcionada por el instalador. Esta instrucción SQL puede contener marcadores de parámetros que no se especifican hasta que se ejecuta el objeto de **vista** .

2.  Ejecute el objeto de [**vista**](view-object.md) mediante una llamada a la función [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) .
3.  Recupere el siguiente registro de un objeto de [**vista**](view-object.md) mediante una llamada a la función [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) .
4.  Modifique el objeto de [**vista**](view-object.md) mediante una llamada a la función [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) .

    También puede validar los datos con [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) pasando las marcas apropiadas. Si **MsiViewModify** devuelve \_ un error \_ de datos no válidos de una solicitud de validación, los datos subyacentes están dañados.

5.  Obtenga información detallada del error en el objeto de [**vista**](view-object.md) mediante una llamada a la función [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) .
6.  Cierre el objeto de [**vista**](view-object.md) mediante una llamada a la función [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) .

Para obtener más información, vea [ejemplos de consultas de base de datos mediante SQL y script](examples-of-database-queries-using-sql-and-script.md).

 

 



