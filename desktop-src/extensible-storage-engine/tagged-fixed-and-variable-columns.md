---
description: 'Más información sobre: columnas etiquetadas, fijas y de variable'
title: Columnas etiquetadas, fijas y de variables
TOCTitle: Tagged, Fixed and Variable Columns
ms:assetid: 78a905b8-71a9-4b2e-b9f2-c81bfe3aef8e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269304(v=EXCHG.10)
ms:contentKeyID: 32765595
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 3f27237c5f75874f7320f675affe20f3833084b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497405"
---
# <a name="tagged-fixed-and-variable-columns"></a><span data-ttu-id="1d689-103">Columnas etiquetadas, fijas y de variables</span><span class="sxs-lookup"><span data-stu-id="1d689-103">Tagged, Fixed and Variable Columns</span></span>


<span data-ttu-id="1d689-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1d689-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="tagged-fixed-and-variable-columns"></a><span data-ttu-id="1d689-105">Columnas etiquetadas, fijas y de variables</span><span class="sxs-lookup"><span data-stu-id="1d689-105">Tagged, Fixed and Variable Columns</span></span>

<span data-ttu-id="1d689-106">Las columnas etiquetadas, fijas y de longitud variable son los tipos de columna principales admitidos por ESE.</span><span class="sxs-lookup"><span data-stu-id="1d689-106">Tagged, fixed, and variable-length columns are the primary column types supported by ESE.</span></span> <span data-ttu-id="1d689-107">Las columnas etiquetadas no están presentes en un registro a menos que los datos se almacenen en la columna y pueden ser de longitud fija o variable.</span><span class="sxs-lookup"><span data-stu-id="1d689-107">Tagged columns are not present in a record unless data is stored in the column, and may be fixed or variable length.</span></span> <span data-ttu-id="1d689-108">Las columnas etiquetadas también pueden contener más de un valor en un solo registro.</span><span class="sxs-lookup"><span data-stu-id="1d689-108">Tagged columns can also contain more than one value in a single record.</span></span> <span data-ttu-id="1d689-109">Las columnas fijas ocupan la misma cantidad de espacio en cada fila y requieren 1 bit para representar el valor NULL.</span><span class="sxs-lookup"><span data-stu-id="1d689-109">Fixed columns take the same amount of space in every row, and require 1 bit to represent the NULL value.</span></span> <span data-ttu-id="1d689-110">Las columnas de longitud variable requieren 2 bytes para representar el tamaño y el valor NULL, y ocupan una cantidad variable de espacio en cada registro.</span><span class="sxs-lookup"><span data-stu-id="1d689-110">Variable length columns require 2 bytes to represent the size and NULL value, and occupy a variable amount of space in each record.</span></span> <span data-ttu-id="1d689-111">Para obtener más información sobre las columnas etiquetadas y fijas, vea la opción Jet_bitColumnTagged y Jet_bitColumnFixed en el miembro **grbit** de la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) utilizada en la llamada a [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="1d689-111">For more information on the tagged and fixed columns, see the Jet_bitColumnTagged, and Jet_bitColumnFixed option in the **grbit** member of [JET_COLUMNDEF](./jet-columndef-structure.md) structure used in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span>

<span data-ttu-id="1d689-112">Las columnas de longitud variable se determinan por el tipo de columna que se establece en el parámetro *coltyp* en la llamada a [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="1d689-112">Variable-length columns are determined by the column type that is set in the *coltyp* parameter in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="1d689-113">Los siguientes tipos de columna pueden ser fijos o de longitud variable, dependiendo de si se establece la opción Jet_bitColumnFixed:</span><span class="sxs-lookup"><span data-stu-id="1d689-113">The following column types may be fixed or variable length depending on whether the Jet_bitColumnFixed option is set:</span></span>

  - <span data-ttu-id="1d689-114">JET_coltypBinary</span><span class="sxs-lookup"><span data-stu-id="1d689-114">JET_coltypBinary</span></span>

  - <span data-ttu-id="1d689-115">JET_coltypText</span><span class="sxs-lookup"><span data-stu-id="1d689-115">JET_coltypText</span></span>

  - <span data-ttu-id="1d689-116">JET_coltypLongBinary</span><span class="sxs-lookup"><span data-stu-id="1d689-116">JET_coltypLongBinary</span></span>

  - <span data-ttu-id="1d689-117">JET_coltypLongText</span><span class="sxs-lookup"><span data-stu-id="1d689-117">JET_coltypLongText</span></span>

<span data-ttu-id="1d689-118">En general, los datos del registro se almacenan primero con el intervalo fijo, el intervalo de variables siguiente y el intervalo etiquetado almacenado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="1d689-118">In general, data in the record is stored with the fixed range first, the variable range next, and the tagged range stored last.</span></span> <span data-ttu-id="1d689-119">En el diagrama siguiente se muestra cómo se almacenan los registros en la tabla.</span><span class="sxs-lookup"><span data-stu-id="1d689-119">The following diagram shows how the records are stored in the table.</span></span> <span data-ttu-id="1d689-120">Como se muestra en el diagrama, el intervalo etiquetado puede contener columnas con varios valores.</span><span class="sxs-lookup"><span data-stu-id="1d689-120">As shown in the diagram, the tagged range may contain columns with multiple values.</span></span>

<span data-ttu-id="1d689-121">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span><span class="sxs-lookup"><span data-stu-id="1d689-121">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span></span>
