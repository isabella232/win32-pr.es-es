---
description: 'Más información acerca de: columnas'
title: Columnas
TOCTitle: Columns
ms:assetid: bc16ca4c-e3c9-43db-ac16-284d7cc0926d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294073(v=EXCHG.10)
ms:contentKeyID: 32765688
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 86f7d2bbb3925434ddbfff52e987b6e408af9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155053"
---
# <a name="columns"></a><span data-ttu-id="33179-103">Columnas</span><span class="sxs-lookup"><span data-stu-id="33179-103">Columns</span></span>


<span data-ttu-id="33179-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="33179-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="columns"></a><span data-ttu-id="33179-105">Columnas</span><span class="sxs-lookup"><span data-stu-id="33179-105">Columns</span></span>

<span data-ttu-id="33179-106">Una tabla se puede crear con un conjunto inicial de columnas mediante una llamada a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o sin un conjunto inicial de columnas llamando a [JetCreateTable](./jetcreatetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="33179-106">A table can be created either with an initial set of columns by calling [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) or without an initial set of columns by calling [JetCreateTable](./jetcreatetable-function.md).</span></span> <span data-ttu-id="33179-107">Las tablas de ESE pueden contener hasta 127 columnas de longitud fija, 128 columnas de longitud variable y 64.993 columnas etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="33179-107">Tables in ESE can contain up to 127 fixed-length columns, 128 variable-length columns, and 64,993 tagged columns.</span></span> <span data-ttu-id="33179-108">Las columnas se identifican por su nombre e identificador y se pueden agregar dinámicamente a la tabla con [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="33179-108">Columns are identified by their name and ID and can be dynamically added to the table with [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="33179-109">Las columnas se crean con un tipo de datos específico y un conjunto opcional de atributos, por ejemplo, si la columna tiene una longitud fija o si puede ser NULL o no.</span><span class="sxs-lookup"><span data-stu-id="33179-109">Columns are created with a specific data type and an optional set of attributes, such as whether the column is fixed-length or whether it can be NULL or not.</span></span>

<span data-ttu-id="33179-110">El tipo de una columna determina los datos que se pueden almacenar en la columna y muchas de las propiedades de la columna, incluido su orden de indexación.</span><span class="sxs-lookup"><span data-stu-id="33179-110">The type of a column determines the data that may be stored in the column and many of the properties of the column, including its order for indexing.</span></span> <span data-ttu-id="33179-111">ESE es compatible con una amplia gama de tipos de columna, con un tamaño de entre 1 y 2 GB (2146483647 caracteres ASCII o 1073741823 caracteres Unicode).</span><span class="sxs-lookup"><span data-stu-id="33179-111">ESE supports a wide range of column types, ranging in size from 1 bit to 2 GB (2146483647 ASCII characters or 1073741823 Unicode characters).</span></span> <span data-ttu-id="33179-112">Para obtener una lista completa de los tipos de datos de columna admitidos por ESE, vea el tema [JET_COLTYP](./jet-coltyp.md) .</span><span class="sxs-lookup"><span data-stu-id="33179-112">For a complete list of the column data types supported by ESE, see the [JET_COLTYP](./jet-coltyp.md) topic.</span></span> <span data-ttu-id="33179-113">En los temas siguientes se tratan algunos de los tipos de columnas admitidos por ESE:</span><span class="sxs-lookup"><span data-stu-id="33179-113">The topics below discuss a few of the columns types supported by ESE:</span></span>

  - [<span data-ttu-id="33179-114">Columnas etiquetadas, fijas y de variables</span><span class="sxs-lookup"><span data-stu-id="33179-114">Tagged, Fixed and Variable Columns</span></span>](./tagged-fixed-and-variable-columns.md)

  - [<span data-ttu-id="33179-115">Columnas de versión, incremento automático y custodia</span><span class="sxs-lookup"><span data-stu-id="33179-115">Version, Auto-Increment and Escrow Columns</span></span>](./version-auto-increment-and-escrow-columns.md)

  - [<span data-ttu-id="33179-116">Columnas de valor largo</span><span class="sxs-lookup"><span data-stu-id="33179-116">Long Value Columns</span></span>](./long-value-columns.md)

  - [<span data-ttu-id="33179-117">Columnas dispersas con varios valores</span><span class="sxs-lookup"><span data-stu-id="33179-117">Multi-Valued Sparse Columns</span></span>](./multi-valued-sparse-columns.md)

  - [<span data-ttu-id="33179-118">Columnas definidas por el usuario</span><span class="sxs-lookup"><span data-stu-id="33179-118">User Defined Columns</span></span>](./user-defined-columns.md)

  - [<span data-ttu-id="33179-119">Usar columnas en una tabla</span><span class="sxs-lookup"><span data-stu-id="33179-119">Using Columns in a Table</span></span>](./using-columns-in-a-table.md)
