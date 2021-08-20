---
description: Dado que el instalador usa una base de datos relacional, hay funciones para realizar consultas Lenguaje de consulta estructurado (SQL) a la base de datos. En el procedimiento siguiente se describe cómo usar SQL para consultar una base de datos.
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: Trabajar con consultas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b6ea5a2f0b962b195fde531216f4b57fd5834162e31c1e34fc9ff1dd3695df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942130"
---
# <a name="working-with-queries"></a>Trabajar con consultas

Dado que el instalador usa una base de datos relacional, hay funciones para realizar consultas Lenguaje de consulta estructurado (SQL) a la base de datos. En el procedimiento siguiente se describe cómo usar SQL para consultar una base de datos.

**Para consultar una base de datos con SQL**

1.  Abra el [**objeto View,**](view-object.md) con la instrucción SQL adecuada, llamando a la [**función MsiDatabaseOpenView.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)

    Un [**objeto View**](view-object.md) es la tabla lógica creada mediante la aplicación de una consulta a un conjunto de tablas. SQL consultas deben cumplir la sintaxis de SQL [proporcionada](sql-syntax.md) por el instalador. Esta SQL instrucción puede contener marcadores de parámetros que no se especifican hasta que se ejecuta **el objeto** View.

2.  Ejecute el [**objeto View**](view-object.md) llamando a la [**función MsiViewExecute.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)
3.  Recupere el siguiente registro de un [**objeto View**](view-object.md) llamando a la [**función MsiViewFetch.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch)
4.  Modifique el [**objeto View**](view-object.md) mediante una llamada a la [**función MsiViewModify.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)

    También puede validar los datos [**con MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) pasando las marcas adecuadas. Si **MsiViewModify devuelve** ERROR INVALID DATA de una \_ solicitud de \_ validación, los datos subyacentes están dañados.

5.  Obtenga información detallada sobre el error en [**el objeto View**](view-object.md) llamando a la función [**MsiViewGetError.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)
6.  Cierre el [**objeto View**](view-object.md) mediante una llamada a la [**función MsiViewClose.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose)

Para obtener más información, vea [Ejemplos de consultas de base de](examples-of-database-queries-using-sql-and-script.md)datos SQL y Script .

 

 



