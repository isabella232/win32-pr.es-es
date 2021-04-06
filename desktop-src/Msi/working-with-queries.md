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
# <a name="working-with-queries"></a><span data-ttu-id="1dff9-104">Trabajar con consultas</span><span class="sxs-lookup"><span data-stu-id="1dff9-104">Working with Queries</span></span>

<span data-ttu-id="1dff9-105">Dado que el instalador utiliza una base de datos relacional, existen funciones para realizar consultas de Lenguaje de consulta estructurado (SQL) a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1dff9-105">Because the installer uses a relational database, there are functions for making Structured Query Language (SQL) queries to the database.</span></span> <span data-ttu-id="1dff9-106">En el procedimiento siguiente se describe cómo usar SQL para consultar una base de datos.</span><span class="sxs-lookup"><span data-stu-id="1dff9-106">The following procedure describes how to use SQL to query a database.</span></span>

<span data-ttu-id="1dff9-107">**Para consultar una base de datos con SQL**</span><span class="sxs-lookup"><span data-stu-id="1dff9-107">**To query a database with SQL**</span></span>

1.  <span data-ttu-id="1dff9-108">Abra el objeto de [**vista**](view-object.md) con la instrucción SQL adecuada llamando a la función [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .</span><span class="sxs-lookup"><span data-stu-id="1dff9-108">Open the [**View**](view-object.md) object, with the appropriate SQL statement, by calling the [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) function.</span></span>

    <span data-ttu-id="1dff9-109">Un objeto de [**vista**](view-object.md) es la tabla lógica que se crea aplicando una consulta a un conjunto de tablas.</span><span class="sxs-lookup"><span data-stu-id="1dff9-109">A [**View**](view-object.md) object is the logical table created by applying a query to a set of tables.</span></span> <span data-ttu-id="1dff9-110">Las consultas SQL deben adherirse a la [sintaxis SQL](sql-syntax.md) proporcionada por el instalador.</span><span class="sxs-lookup"><span data-stu-id="1dff9-110">SQL queries must adhere to the [SQL syntax](sql-syntax.md) provided by the installer.</span></span> <span data-ttu-id="1dff9-111">Esta instrucción SQL puede contener marcadores de parámetros que no se especifican hasta que se ejecuta el objeto de **vista** .</span><span class="sxs-lookup"><span data-stu-id="1dff9-111">This SQL statement can contain parameter markers that are not specified until the **View** object runs.</span></span>

2.  <span data-ttu-id="1dff9-112">Ejecute el objeto de [**vista**](view-object.md) mediante una llamada a la función [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) .</span><span class="sxs-lookup"><span data-stu-id="1dff9-112">Run the [**View**](view-object.md) object by calling the [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) function.</span></span>
3.  <span data-ttu-id="1dff9-113">Recupere el siguiente registro de un objeto de [**vista**](view-object.md) mediante una llamada a la función [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) .</span><span class="sxs-lookup"><span data-stu-id="1dff9-113">Retrieve the next record from a [**View**](view-object.md) object by calling the [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) function.</span></span>
4.  <span data-ttu-id="1dff9-114">Modifique el objeto de [**vista**](view-object.md) mediante una llamada a la función [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) .</span><span class="sxs-lookup"><span data-stu-id="1dff9-114">Modify the [**View**](view-object.md) object by calling the [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) function.</span></span>

    <span data-ttu-id="1dff9-115">También puede validar los datos con [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) pasando las marcas apropiadas.</span><span class="sxs-lookup"><span data-stu-id="1dff9-115">You can also validate data with [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) by passing the appropriate flags.</span></span> <span data-ttu-id="1dff9-116">Si **MsiViewModify** devuelve \_ un error \_ de datos no válidos de una solicitud de validación, los datos subyacentes están dañados.</span><span class="sxs-lookup"><span data-stu-id="1dff9-116">If **MsiViewModify** returns ERROR\_INVALID\_DATA from a validation request, the underlying data is corrupt.</span></span>

5.  <span data-ttu-id="1dff9-117">Obtenga información detallada del error en el objeto de [**vista**](view-object.md) mediante una llamada a la función [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) .</span><span class="sxs-lookup"><span data-stu-id="1dff9-117">Obtain detailed error information on the [**View**](view-object.md) object by calling the [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) function.</span></span>
6.  <span data-ttu-id="1dff9-118">Cierre el objeto de [**vista**](view-object.md) mediante una llamada a la función [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) .</span><span class="sxs-lookup"><span data-stu-id="1dff9-118">Close the [**View**](view-object.md) object by calling the [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) function.</span></span>

<span data-ttu-id="1dff9-119">Para obtener más información, vea [ejemplos de consultas de base de datos mediante SQL y script](examples-of-database-queries-using-sql-and-script.md).</span><span class="sxs-lookup"><span data-stu-id="1dff9-119">For more information, see [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md).</span></span>

 

 



