---
description: Más información acerca de cómo agregar tablas a la base de datos
title: Agregar tablas a la base de datos
TOCTitle: Adding Tables to the Database
ms:assetid: 176d4fea-c856-441b-bd58-165b37c35095
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269195(v=EXCHG.10)
ms:contentKeyID: 32765498
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 67569f8efc164cc7156f346b6754f13b296d3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000879"
---
# <a name="adding-tables-to-the-database"></a><span data-ttu-id="7ee5a-103">Agregar tablas a la base de datos</span><span class="sxs-lookup"><span data-stu-id="7ee5a-103">Adding Tables to the Database</span></span>


<span data-ttu-id="7ee5a-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7ee5a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="adding-tables-to-the-database"></a><span data-ttu-id="7ee5a-105">Agregar tablas a la base de datos</span><span class="sxs-lookup"><span data-stu-id="7ee5a-105">Adding Tables to the Database</span></span>

<span data-ttu-id="7ee5a-106">Las tablas son una colección heterogénea de registros que agrupan de forma física y lógica los datos en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="7ee5a-106">Tables are a heterogeneous collection of records that physically and logically group the data in the database.</span></span> <span data-ttu-id="7ee5a-107">Las tablas se identifican de forma exclusiva por su nombre.</span><span class="sxs-lookup"><span data-stu-id="7ee5a-107">Tables are uniquely identified by their name.</span></span> <span data-ttu-id="7ee5a-108">El identificador de tabla ([JET_TABLEID](./jet-tableid.md)) es un identificador de un cursor que se utiliza para actualizar y navegar por las tablas.</span><span class="sxs-lookup"><span data-stu-id="7ee5a-108">The table ID ([JET_TABLEID](./jet-tableid.md)) is a handle to a cursor that is used to update and navigate tables.</span></span> <span data-ttu-id="7ee5a-109">Puede abrir varios [JET_TABLEID](./jet-tableid.md) en la misma tabla.</span><span class="sxs-lookup"><span data-stu-id="7ee5a-109">You may open multiple [JET_TABLEID](./jet-tableid.md) on the same table.</span></span>

<span data-ttu-id="7ee5a-110">Se abre una tabla existente en la llamada a [JetOpenTable](./jetopentable-function.md)y se crea una nueva tabla sin filas ni columnas con [JetCreateTable](./jetcreatetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="7ee5a-110">An existing table is opened in the call to [JetOpenTable](./jetopentable-function.md), and a new table is created without rows or columns with [JetCreateTable](./jetcreatetable-function.md).</span></span> <span data-ttu-id="7ee5a-111">Para crear de forma atómica una tabla con un conjunto inicial de columnas e índices, llame a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="7ee5a-111">To atomically create a table with an initial set of columns and indices, call [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) or [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span></span> <span data-ttu-id="7ee5a-112">El tamaño inicial de la tabla se proporciona en el parámetro *lPages* de [JetCreateTable](./jetcreatetable-function.md) o en el miembro **ulPages** de la estructura [JET_TABLECREATE](./jet-tablecreate-structure.md) en la llamada a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="7ee5a-112">The initial size of the table is given in the *lPages* parameter in [JetCreateTable](./jetcreatetable-function.md) or the **ulPages** member of the [JET_TABLECREATE](./jet-tablecreate-structure.md) structure in the call to [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="7ee5a-113">Las tablas aumentan automáticamente cuando se agregan datos a la tabla.</span><span class="sxs-lookup"><span data-stu-id="7ee5a-113">Tables grow automatically when data is added to the table.</span></span> <span data-ttu-id="7ee5a-114">El crecimiento es proporcional al tamaño inicial de la tabla.</span><span class="sxs-lookup"><span data-stu-id="7ee5a-114">The growth is proportional to the initial size of the table.</span></span> <span data-ttu-id="7ee5a-115">Se pueden agregar columnas a la tabla en cualquier momento con [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="7ee5a-115">Columns may be added to the table at any time with [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="7ee5a-116">Cuando la aplicación ya no necesita tener acceso a la tabla, el cursor se puede cerrar con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="7ee5a-116">When the application no longer needs to access the table, the cursor can be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="7ee5a-117">La tabla se puede eliminar mediante una llamada a [JetDeleteTable](./jetdeletetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="7ee5a-117">The table may be deleted via a call to [JetDeleteTable](./jetdeletetable-function.md).</span></span>

<span data-ttu-id="7ee5a-118">Las operaciones de tabla deben realizarse en el contexto de una transacción.</span><span class="sxs-lookup"><span data-stu-id="7ee5a-118">Table operations should be performed within the context of a transaction.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ee5a-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7ee5a-119">See Also</span></span>

[<span data-ttu-id="7ee5a-120">Transactions</span><span class="sxs-lookup"><span data-stu-id="7ee5a-120">Transactions</span></span>](./transactions.md)
