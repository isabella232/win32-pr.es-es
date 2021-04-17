---
description: Más información acerca de cómo leer datos de la base de datos
title: Leer datos de la base de datos
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 176cd3189dd1c2701331eff0ef5387827da19b94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687678"
---
# <a name="reading-data-from-the-database"></a><span data-ttu-id="30843-103">Leer datos de la base de datos</span><span class="sxs-lookup"><span data-stu-id="30843-103">Reading Data from the Database</span></span>


<span data-ttu-id="30843-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="30843-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="reading-data-from-the-database"></a><span data-ttu-id="30843-105">Leer datos de la base de datos</span><span class="sxs-lookup"><span data-stu-id="30843-105">Reading Data from the Database</span></span>

<span data-ttu-id="30843-106">La lectura de datos de la base de datos debe realizarse dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="30843-106">Reading data from the database should be performed within a transaction.</span></span>

<span data-ttu-id="30843-107">En el procedimiento siguiente se muestra cómo realizar una operación de lectura simple en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="30843-107">The following procedure shows how to perform a simple read operation in the database.</span></span>

### <a name="to-read-data-from-a-database"></a><span data-ttu-id="30843-108">Para leer datos de una base de datos</span><span class="sxs-lookup"><span data-stu-id="30843-108">To read data from a database</span></span>

1.  <span data-ttu-id="30843-109">Llame a [JetBeginTransaction](./jetbegintransaction-function.md) o [JETBEGINTRANSACTION2](./jetbegintransaction2-function.md) con el identificador de sesión para iniciar la transacción.</span><span class="sxs-lookup"><span data-stu-id="30843-109">Call [JetBeginTransaction](./jetbegintransaction-function.md) or [JetBeginTransaction2](./jetbegintransaction2-function.md) with the session ID to start the transaction.</span></span>

2.  <span data-ttu-id="30843-110">Mueva el cursor al registro deseado llamando a [JetMove](./jetmove-function.md) con JET_MoveFirst en el parámetro *cRow* .</span><span class="sxs-lookup"><span data-stu-id="30843-110">Move the cursor to the desired record by calling [JetMove](./jetmove-function.md) with JET_MoveFirst in the *cRow* parameter.</span></span> <span data-ttu-id="30843-111">Para obtener más información acerca de cómo se mueve el cursor, vea el tema [indexación en la tabla](./indexing-in-the-table.md) .</span><span class="sxs-lookup"><span data-stu-id="30843-111">For more information on how to move the cursor, see the [Indexing in the Table](./indexing-in-the-table.md) topic.</span></span>

3.  <span data-ttu-id="30843-112">Llame a [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) en el registro actual con JET_ColInfo especificado en el parámetro *InfoLevel* para recuperar el ID. de columna de la columna.</span><span class="sxs-lookup"><span data-stu-id="30843-112">Call [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) on the current record with JET_ColInfo specified in the *InfoLevel* parameter to retrieve the column ID for the column.</span></span> <span data-ttu-id="30843-113">El ID. de columna se devuelve en la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="30843-113">The column ID is returned in the [JET_COLUMNDEF](./jet-columndef-structure.md) structure.</span></span>

4.  <span data-ttu-id="30843-114">Lea los datos de la columna mediante una llamada a [JetRetrieveColumn](./jetretrievecolumn-function.md) con el identificador de columna recuperado en el paso 3 en el parámetro columnid.</span><span class="sxs-lookup"><span data-stu-id="30843-114">Read the data from the column by calling [JetRetrieveColumn](./jetretrievecolumn-function.md) with the column ID retrieved in step 3 in the columnid parameter.</span></span> <span data-ttu-id="30843-115">El parámetro *pvData* contiene el tipo de datos especificado en la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) recuperada en el paso 3.</span><span class="sxs-lookup"><span data-stu-id="30843-115">The *pvData* parameter contains the type of data specified in the [JET_COLUMNDEF](./jet-columndef-structure.md) structure retrieved in step 3.</span></span>

5.  <span data-ttu-id="30843-116">Llame a [JetCommitTransaction](./jetcommittransaction-function.md) para confirmar la transacción en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="30843-116">Call [JetCommitTransaction](./jetcommittransaction-function.md) to commit the transaction to the database.</span></span>
