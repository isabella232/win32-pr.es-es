---
description: 'Más información acerca de: estructura de JET_SPACEHINTS'
title: Estructura de JET_SPACEHINTS
TOCTitle: JET_SPACEHINTS Structure
ms:assetid: 23328993-93c9-4a23-892b-e6a9f434d1d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269205(v=EXCHG.10)
ms:contentKeyID: 32765508
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf786d1f47b5eaae3f9540c8635853020f9b0521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720308"
---
# <a name="jet_spacehints-structure"></a><span data-ttu-id="70905-103">Estructura de JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="70905-103">JET_SPACEHINTS Structure</span></span>


<span data-ttu-id="70905-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="70905-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_spacehints-structure"></a><span data-ttu-id="70905-105">Estructura de JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="70905-105">JET_SPACEHINTS Structure</span></span>

<span data-ttu-id="70905-106">La estructura **JET_SPACEHINTS** contiene información sobre los patrones de asignación de espacio cuando un árbol b crece a través de las divisiones Append o Hotpoint.</span><span class="sxs-lookup"><span data-stu-id="70905-106">The **JET_SPACEHINTS** structure contains information about space allocation patterns when a b-tree grows through append or hotpoint splits.</span></span> <span data-ttu-id="70905-107">Anexar divisiones se producen cuando los registros se agregan al final de un árbol b y se producen divisiones de Hotpoint cuando se agregan varios registros al mismo punto de inserción virtual (por ejemplo, al agregar ' Marie ', ' Mark ', ' Martin' ', ' Mary ' a la mitad de un árbol b que está ordenado alfabéticamente).</span><span class="sxs-lookup"><span data-stu-id="70905-107">Append splits happen when records are added to the end of a b-tree and hotpoint splits happen when multiple records are added to the same virtual insertion point (for example, adding 'Marie', 'Mark', 'Martin', 'Mary' to the middle of a b-tree that is sorted alphabetically).</span></span>

<span data-ttu-id="70905-108">**Windows 7:** La estructura de **JET_SPACEHINTS** se presenta en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="70905-108">**Windows 7:** The **JET_SPACEHINTS** structure is introduced in Windows 7.</span></span>

```cpp
    typedef struct tagJET_SPACEHINTS {
      unsigned long cbStruct;
      unsigned long ulInitialDensity;
      unsigned long cbInitial;
      JET_GRBIT grbit;
      unsigned long ulMaintDensity;
      unsigned long ulGrowth;
      unsigned long cbMinExtent;
      unsigned long cbMaxExtent;
    } JET_SPACEHINTS;
```

### <a name="members"></a><span data-ttu-id="70905-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="70905-109">Members</span></span>

<span data-ttu-id="70905-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="70905-110">**cbStruct**</span></span>

<span data-ttu-id="70905-111">Tamaño, en bytes, de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="70905-111">The size, in bytes, of this structure.</span></span> <span data-ttu-id="70905-112">Establezca este miembro en sizeof (JET_SPACEHINTS).</span><span class="sxs-lookup"><span data-stu-id="70905-112">Set this member to sizeof( JET_SPACEHINTS ).</span></span>

<span data-ttu-id="70905-113">**ulInitialDensity**</span><span class="sxs-lookup"><span data-stu-id="70905-113">**ulInitialDensity**</span></span>

<span data-ttu-id="70905-114">El diseño de densidad en (anexar).</span><span class="sxs-lookup"><span data-stu-id="70905-114">The density at (append) layout.</span></span>

<span data-ttu-id="70905-115">**cbInitial**</span><span class="sxs-lookup"><span data-stu-id="70905-115">**cbInitial**</span></span>

<span data-ttu-id="70905-116">Tamaño inicial (en bytes) del objeto que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="70905-116">The initial size (in bytes) of the object being created.</span></span> <span data-ttu-id="70905-117">Debe ser un múltiplo del tamaño de página de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="70905-117">This must be a multiple of the database page size.</span></span>

<span data-ttu-id="70905-118">**grbit**</span><span class="sxs-lookup"><span data-stu-id="70905-118">**grbit**</span></span>

<span data-ttu-id="70905-119">Grupo de bits que contiene las opciones que se van a usar para esta estructura, que incluyen cero o más de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="70905-119">A group of bits that contain the options to be used for this structure, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70905-120">Value</span><span class="sxs-lookup"><span data-stu-id="70905-120">Value</span></span></p></th>
<th><p><span data-ttu-id="70905-121">Significado</span><span class="sxs-lookup"><span data-stu-id="70905-121">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70905-122">JET_bitSpaceHintsUtilizeParentSpace</span><span class="sxs-lookup"><span data-stu-id="70905-122">JET_bitSpaceHintsUtilizeParentSpace</span></span><br />
<span data-ttu-id="70905-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="70905-123">0x00000001</span></span></p></td>
<td><p><span data-ttu-id="70905-124">Cambia la Directiva de asignación interna para obtener el espacio heirarchically del elemento primario inmediato de un árbol b.</span><span class="sxs-lookup"><span data-stu-id="70905-124">Changes the internal allocation policy to get space heirarchically from the immediate parent of a b-tree.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70905-125">JET_bitCreateHintAppendSequential</span><span class="sxs-lookup"><span data-stu-id="70905-125">JET_bitCreateHintAppendSequential</span></span><br />
<span data-ttu-id="70905-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="70905-126">0x00000002</span></span></p></td>
<td><p><span data-ttu-id="70905-127">Habilita el comportamiento de anexar División para aumentar según la dinámica de crecimiento de la tabla (establecida por cbMinExtent, ulGrowth, cbMaxExtent).</span><span class="sxs-lookup"><span data-stu-id="70905-127">Enables append split behavior to grow according to the growth dynamics of the table (set by cbMinExtent, ulGrowth, cbMaxExtent).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70905-128">JET_bitCreateHintHotpointSequential</span><span class="sxs-lookup"><span data-stu-id="70905-128">JET_bitCreateHintHotpointSequential</span></span><br />
<span data-ttu-id="70905-129">0x00000004</span><span class="sxs-lookup"><span data-stu-id="70905-129">0x00000004</span></span></p></td>
<td><p><span data-ttu-id="70905-130">Permite que el comportamiento de división Hotpoint crezca según la dinámica de crecimiento de la tabla (establecida por cbMinExtent, ulGrowth, cbMaxExtent).</span><span class="sxs-lookup"><span data-stu-id="70905-130">Enables hotpoint split behavior to grow according to the growth dynamics of the table (set by cbMinExtent, ulGrowth, cbMaxExtent).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70905-131">JET_bitRetrieveHintTableScanForward</span><span class="sxs-lookup"><span data-stu-id="70905-131">JET_bitRetrieveHintTableScanForward</span></span><br />
<span data-ttu-id="70905-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="70905-132">0x00000010</span></span></p></td>
<td><p><span data-ttu-id="70905-133">Si se establece, el cliente indica que el examen secuencial hacia delante es el patrón de uso predominante de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="70905-133">If set, the client indicates that forward sequential scan is the predominant usage pattern of this table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70905-134">JET_bitRetrieveHintTableScanBackward</span><span class="sxs-lookup"><span data-stu-id="70905-134">JET_bitRetrieveHintTableScanBackward</span></span><br />
<span data-ttu-id="70905-135">0x00000020</span><span class="sxs-lookup"><span data-stu-id="70905-135">0x00000020</span></span></p></td>
<td><p><span data-ttu-id="70905-136">Si se establece, el cliente indica que el examen secuencial hacia atrás es el patrón de uso predominante de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="70905-136">If set, the client indicates that backward sequential scan is the predominant usage pattern of this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70905-137">JET_bitDeleteHintTableSequential</span><span class="sxs-lookup"><span data-stu-id="70905-137">JET_bitDeleteHintTableSequential</span></span><br />
<span data-ttu-id="70905-138">0x00000100</span><span class="sxs-lookup"><span data-stu-id="70905-138">0x00000100</span></span></p></td>
<td><p><span data-ttu-id="70905-139">Si se establece, la aplicación espera que esta tabla se limpie en orden secuencial, de la clave más baja a la más alta.</span><span class="sxs-lookup"><span data-stu-id="70905-139">If set, the application expects this table to be cleaned up in sequential order, from lowest key to highest key.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="70905-140">**ulMaintDensity**</span><span class="sxs-lookup"><span data-stu-id="70905-140">**ulMaintDensity**</span></span>

<span data-ttu-id="70905-141">densidad a mulMaintDensity</span><span class="sxs-lookup"><span data-stu-id="70905-141">density to mulMaintDensity</span></span>

<span data-ttu-id="70905-142">Densidad que se debe mantener en.</span><span class="sxs-lookup"><span data-stu-id="70905-142">Density to maintain at.</span></span> <span data-ttu-id="70905-143">Si las sugerencias de espacio especifican JET_bitRetrieveHintTableScanForward o JET_bitRetrieveHintTableScanBackward, la desfragmentación de la tabla se desencadenará cuando el espacio usado en la tabla caiga por debajo de este umbral.</span><span class="sxs-lookup"><span data-stu-id="70905-143">If the space hints specify JET_bitRetrieveHintTableScanForward or JET_bitRetrieveHintTableScanBackward, table defragmentation will be triggered when the used space in the table drops below this threshold.</span></span> <span data-ttu-id="70905-144">La desfragmentación de tablas se puede deshabilitar estableciendo este miembro en cero.</span><span class="sxs-lookup"><span data-stu-id="70905-144">Table defragmentation can be disabled by setting this member to zero.</span></span> <span data-ttu-id="70905-145">Si se establece este miembro en 100, la desfragmentación de la tabla se ejecutará en cuanto se libere una página.</span><span class="sxs-lookup"><span data-stu-id="70905-145">Setting this member to 100 will cause table defragmentation to run as soon as a page is freed.</span></span>

<span data-ttu-id="70905-146">**ulGrowth**</span><span class="sxs-lookup"><span data-stu-id="70905-146">**ulGrowth**</span></span>

<span data-ttu-id="70905-147">Porcentaje de crecimiento del último crecimiento o tamaño inicial, redondeado al tamaño de asignación de JET nativo más cercano.</span><span class="sxs-lookup"><span data-stu-id="70905-147">The percent growth from the last growth or initial size, rounded to nearest native JET allocation size.</span></span>

<span data-ttu-id="70905-148">**cbMinExtent demasiado pequeño**</span><span class="sxs-lookup"><span data-stu-id="70905-148">**cbMinExtent too small**</span></span>

<span data-ttu-id="70905-149">Esto invalida ulGrowth si es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="70905-149">This overrides ulGrowth if too small.</span></span>

<span data-ttu-id="70905-150">**cbMaxExtent**</span><span class="sxs-lookup"><span data-stu-id="70905-150">**cbMaxExtent**</span></span>

<span data-ttu-id="70905-151">Valor máximo para el crecimiento en bytes.</span><span class="sxs-lookup"><span data-stu-id="70905-151">The maximum value for growth in bytes.</span></span> <span data-ttu-id="70905-152">Este ulGrowth de mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="70905-152">This caps ulGrowth.</span></span>

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a><span data-ttu-id="70905-153">Cuando un árbol b crece a través de las divisiones Append o Hotpoint (en lugar de las inserciones de registros aleatorios), la cantidad de espacio en la que crecerá la tabla se calcula de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="70905-153">When a b-tree grows through append or hotpoint splits (as opposed to random record insertions), the amount of space the table will grow by is calculated as follows:</span></span>

1.  <span data-ttu-id="70905-154">En el momento de su creación, asignamos el árbol b cbInitial, siempre.</span><span class="sxs-lookup"><span data-stu-id="70905-154">At creation, we give the b-tree cbInitial, always.</span></span>

2.  <span data-ttu-id="70905-155">Durante la primera asignación de un área determinada, asignaremos: cbInitial \* ulGrowth/100 (redondeado al tamaño de página de la base de BD) o cbMinExtent si es mayor.</span><span class="sxs-lookup"><span data-stu-id="70905-155">During the first allocation of a given area, we will allocate: cbInitial \* ulGrowth / 100 (rounded to the DB's page size), or cbMinExtent if larger.</span></span>

3.  <span data-ttu-id="70905-156">Durante la siguiente asignación, cbLastAlloc \* ulGrowth/100 (redondeado al tamaño de página de la base de BD) o cbMinExtent si es mayor.</span><span class="sxs-lookup"><span data-stu-id="70905-156">During the next allocation, cbLastAlloc \* ulGrowth / 100 (rounded to the page size of the DB), or cbMinExtent if larger.</span></span>

4.  <span data-ttu-id="70905-157">En alguna asignación (que podría ser la primera asignación), el tamaño calculado superará el cbMaxExtent y tendrá el tamaño de crecimiento a partir de entonces.</span><span class="sxs-lookup"><span data-stu-id="70905-157">At some allocation (which could be the first allocation), the calculated size will exceed cbMaxExtent, and that will be the growth size thereafter.</span></span>

### <a name="requirements"></a><span data-ttu-id="70905-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70905-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70905-159"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="70905-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="70905-160">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="70905-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70905-161"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="70905-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="70905-162">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="70905-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70905-163"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="70905-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="70905-164">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="70905-164">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="70905-165">Consulte también</span><span class="sxs-lookup"><span data-stu-id="70905-165">See Also</span></span>

[<span data-ttu-id="70905-166">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="70905-166">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="70905-167">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="70905-167">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)
