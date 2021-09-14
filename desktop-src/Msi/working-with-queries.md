---
description: Dado que el instalador usa una base de datos relacional, hay funciones para realizar consultas Lenguaje de consulta estructurado (SQL) a la base de datos. En el procedimiento siguiente se describe cómo usar SQL para consultar una base de datos.
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: Trabajar con consultas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0be4839c1e97f05d09769d69d62345b0602b789
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071808"
---
# <a name="working-with-queries"></a>Trabajar con consultas

Dado que el instalador usa una base de datos relacional, hay funciones para realizar consultas Lenguaje de consulta estructurado (SQL) a la base de datos. En el procedimiento siguiente se describe cómo usar SQL para consultar una base de datos.

**Para consultar una base de datos con SQL**

1.  Abra el [**objeto View,**](view-object.md) con la instrucción SQL adecuada, llamando a la [**función MsiDatabaseOpenView.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)

    Un [**objeto View**](view-object.md) es la tabla lógica creada mediante la aplicación de una consulta a un conjunto de tablas. SQL consultas deben cumplir la sintaxis [SQL proporcionada](sql-syntax.md) por el instalador. Esta SQL instrucción puede contener marcadores de parámetros que no se especifican hasta que se ejecuta **el objeto** View.

2.  Ejecute el [**objeto View**](view-object.md) mediante una llamada a la [**función MsiViewExecute.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)
3.  Recupere el siguiente registro de un [**objeto View**](view-object.md) llamando a la [**función MsiViewFetch.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch)
4.  Modifique el [**objeto View**](view-object.md) mediante una llamada a la [**función MsiViewModify.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)

    También puede validar los datos [**con MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) pasando las marcas adecuadas. Si **MsiViewModify** devuelve ERROR INVALID DATA desde una solicitud \_ de \_ validación, los datos subyacentes están dañados.

5.  Obtenga información detallada sobre el error en [**el objeto View**](view-object.md) mediante una llamada a la función [**MsiViewGetError.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)
6.  Cierre el [**objeto View**](view-object.md) mediante una llamada a la [**función MsiViewClose.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose)

Para obtener más información, vea [Ejemplos de consultas de base de](examples-of-database-queries-using-sql-and-script.md)datos SQL y Script .

 

 



