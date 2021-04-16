---
description: 'Más información acerca de: estructura de JET_RETRIEVECOLUMN'
title: Estructura de JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN Structure
ms:assetid: 8e23bed5-5279-4733-b787-a073a0e8d5a5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269334(v=EXCHG.10)
ms:contentKeyID: 32765623
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
ms.openlocfilehash: 688728e74d81055922f9e7e748dea1f30faa3548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705757"
---
# <a name="jet_retrievecolumn-structure"></a><span data-ttu-id="24d02-103">Estructura de JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="24d02-103">JET_RETRIEVECOLUMN Structure</span></span>


<span data-ttu-id="24d02-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="24d02-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_retrievecolumn-structure"></a><span data-ttu-id="24d02-105">Estructura de JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="24d02-105">JET_RETRIEVECOLUMN Structure</span></span>

<span data-ttu-id="24d02-106">La estructura **JET_RETRIEVECOLUMN** contiene los parámetros de entrada y salida de [JetRetrieveColumns](./jetretrievecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="24d02-106">The **JET_RETRIEVECOLUMN** structure contains input and output parameters for [JetRetrieveColumns](./jetretrievecolumns-function.md).</span></span> <span data-ttu-id="24d02-107">Los campos de la estructura describen qué valor de columna se va a recuperar, cómo se recupera y dónde se guardan los resultados.</span><span class="sxs-lookup"><span data-stu-id="24d02-107">Fields in the structure describe what column value to retrieve, how to retrieve it, and where to save results.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      void* pvData;
      unsigned long cbData;
      unsigned long cbActual;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
      JET_ERR err;
    } JET_RETRIEVECOLUMN;
```

### <a name="members"></a><span data-ttu-id="24d02-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="24d02-108">Members</span></span>

<span data-ttu-id="24d02-109">**columnid**</span><span class="sxs-lookup"><span data-stu-id="24d02-109">**columnid**</span></span>

<span data-ttu-id="24d02-110">Identificador de columna para la columna que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="24d02-110">The column identifier for the column to retrieve.</span></span>

<span data-ttu-id="24d02-111">**pvData**</span><span class="sxs-lookup"><span data-stu-id="24d02-111">**pvData**</span></span>

<span data-ttu-id="24d02-112">Un puntero para empezar a almacenar los datos que se recuperan del valor de la columna.</span><span class="sxs-lookup"><span data-stu-id="24d02-112">A pointer to begin storing data that is retrieved from the column value.</span></span>

<span data-ttu-id="24d02-113">**cbData**</span><span class="sxs-lookup"><span data-stu-id="24d02-113">**cbData**</span></span>

<span data-ttu-id="24d02-114">Tamaño de la asignación a partir de **pvData**, en bytes.</span><span class="sxs-lookup"><span data-stu-id="24d02-114">The size of allocation beginning at **pvData**, in bytes.</span></span> <span data-ttu-id="24d02-115">La operación de recuperación de columna no almacenará más datos en **pvData** que **cbData**.</span><span class="sxs-lookup"><span data-stu-id="24d02-115">The retrieve column operation will not store more data at **pvData** than **cbData**.</span></span>

<span data-ttu-id="24d02-116">**cbActual**</span><span class="sxs-lookup"><span data-stu-id="24d02-116">**cbActual**</span></span>

<span data-ttu-id="24d02-117">Tamaño, en bytes, de los datos recuperados por una operación de recuperación de columna.</span><span class="sxs-lookup"><span data-stu-id="24d02-117">The size, in bytes, of data that is retrieved by a retrieve column operation.</span></span>

<span data-ttu-id="24d02-118">**grbit**</span><span class="sxs-lookup"><span data-stu-id="24d02-118">**grbit**</span></span>

<span data-ttu-id="24d02-119">Grupo de bits que contiene las opciones para la recuperación de columnas, que incluyen cero o más de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="24d02-119">A group of bits that contain the options for column retrieval, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="24d02-120">Value</span><span class="sxs-lookup"><span data-stu-id="24d02-120">Value</span></span></p></th>
<th><p><span data-ttu-id="24d02-121">Significado</span><span class="sxs-lookup"><span data-stu-id="24d02-121">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24d02-122">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="24d02-122">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="24d02-123">Recupera el valor modificado en lugar del valor original.</span><span class="sxs-lookup"><span data-stu-id="24d02-123">Retrieves the modified value instead of the original value.</span></span> <span data-ttu-id="24d02-124">Si el valor no se ha modificado, se recupera el valor original.</span><span class="sxs-lookup"><span data-stu-id="24d02-124">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="24d02-125">De esta manera, se puede recuperar un valor que todavía no se ha insertado o actualizado cuando se inserta o actualiza un registro.</span><span class="sxs-lookup"><span data-stu-id="24d02-125">In this way, a value that has not yet been inserted or updated can be retrieved when a record is inserted or updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24d02-126">JET_bitRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="24d02-126">JET_bitRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="24d02-127">Recupera los valores de columna del índice sin tener acceso al registro, si es posible.</span><span class="sxs-lookup"><span data-stu-id="24d02-127">Retrieves column values from the index without accessing the record, if possible.</span></span> <span data-ttu-id="24d02-128">De esta manera, se puede evitar la carga innecesaria de registros cuando los datos necesarios están disponibles en las propias entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="24d02-128">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span> <span data-ttu-id="24d02-129">En los casos en los que no se puede recuperar el valor de la columna original del índice debido a las transformaciones irreversibles o al truncamiento de los datos, se obtendrá acceso al registro y se recuperarán los datos de la forma habitual.</span><span class="sxs-lookup"><span data-stu-id="24d02-129">In cases where the original column value cannot be retrieved from the index, because of irreversible transformations or data truncation, the record will be accessed and the data retrieved as normal.</span></span> <span data-ttu-id="24d02-130">Se trata de una opción de rendimiento y solo se debe especificar cuando es probable que se pueda recuperar el valor de la columna del índice.</span><span class="sxs-lookup"><span data-stu-id="24d02-130">This is a performance option and should only be specified when it is likely that the column value can be retrieved from the index.</span></span> <span data-ttu-id="24d02-131">Esta opción no se debe especificar si el índice actual es el índice clúster, ya que las entradas de índice para el índice agrupado, o principal, son los propios registros.</span><span class="sxs-lookup"><span data-stu-id="24d02-131">This option should not be specified if the current index is the clustered index, since the index entries for the clustered, or primary, index are the records themselves.</span></span> <span data-ttu-id="24d02-132">No se puede establecer este bit si también se establece JET_bitRetrieveFromPrimaryBookmark.</span><span class="sxs-lookup"><span data-stu-id="24d02-132">This bit cannot be set if JET_bitRetrieveFromPrimaryBookmark is also set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24d02-133">JET_bitRetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="24d02-133">JET_bitRetrieveFromPrimaryBookmark</span></span></p></td>
<td><p><span data-ttu-id="24d02-134">Recupera los valores de columna del marcador de índice y puede diferir del valor de índice cuando una columna aparece en el índice principal y en el índice actual.</span><span class="sxs-lookup"><span data-stu-id="24d02-134">Retrieves column values from the index bookmark, and can differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="24d02-135">Esta opción no se debe especificar si el índice actual es el índice clúster o principal.</span><span class="sxs-lookup"><span data-stu-id="24d02-135">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="24d02-136">No se puede establecer este bit si también se establece JET_bitRetrieveFromIndex.</span><span class="sxs-lookup"><span data-stu-id="24d02-136">This bit cannot be set if JET_bitRetrieveFromIndex is also set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24d02-137">JET_bitRetrieveTag</span><span class="sxs-lookup"><span data-stu-id="24d02-137">JET_bitRetrieveTag</span></span></p></td>
<td><p><span data-ttu-id="24d02-138">Recupera el número de secuencia de un valor de columna de varios valores en pretinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="24d02-138">Retrieves the sequence number of a multi-valued column value in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="24d02-139">A menudo, el campo itagSequence se usa como entrada para recuperar valores de columna con varios valores de un registro.</span><span class="sxs-lookup"><span data-stu-id="24d02-139">The itagSequence field is often used an input for retrieving multi-valued column values from a record.</span></span> <span data-ttu-id="24d02-140">Sin embargo, cuando se recuperan valores de un índice, también es posible asociar la entrada de índice con un número de secuencia determinado y recuperar también este número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="24d02-140">However, when retrieving values from an index, it is also possible to associate the index entry with a particular sequence number and retrieve this sequence number as well.</span></span> <span data-ttu-id="24d02-141">Recuperar el número de secuencia puede ser una operación costosa y solo debe realizarse si es necesario.</span><span class="sxs-lookup"><span data-stu-id="24d02-141">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24d02-142">JET_ bitRetrieveNull</span><span class="sxs-lookup"><span data-stu-id="24d02-142">JET_ bitRetrieveNull</span></span></p></td>
<td><p><span data-ttu-id="24d02-143">Recupera los valores NULL de la columna con varios valores.</span><span class="sxs-lookup"><span data-stu-id="24d02-143">Retrieves multi-valued column NULL values.</span></span> <span data-ttu-id="24d02-144">Si no se especifica esta opción, se omitirán automáticamente los valores NULL de las columnas con varios valores.</span><span class="sxs-lookup"><span data-stu-id="24d02-144">If this option is not specified, multi-valued column NULL values will automatically be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24d02-145">JET_bitRetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="24d02-145">JET_bitRetrieveIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="24d02-146">Hace que se devuelva un valor NULL cuando el número de secuencia solicitado es 1 y no hay valores establecidos para la columna en el registro.</span><span class="sxs-lookup"><span data-stu-id="24d02-146">Causes a NULL value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span> <span data-ttu-id="24d02-147">Esta opción solo afecta a las columnas con varios valores.</span><span class="sxs-lookup"><span data-stu-id="24d02-147">This option affects only multi-valued columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24d02-148">JET_bitRetrieveLongId</span><span class="sxs-lookup"><span data-stu-id="24d02-148">JET_bitRetrieveLongId</span></span></p></td>
<td><p><span data-ttu-id="24d02-149">Esta marca solo es para uso interno y no está pensada para usarse en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="24d02-149">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24d02-150">JET_bitRetrieveLongValueRefCount</span><span class="sxs-lookup"><span data-stu-id="24d02-150">JET_bitRetrieveLongValueRefCount</span></span></p></td>
<td><p><span data-ttu-id="24d02-151">Esta marca solo es para uso interno y no está pensada para usarse en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="24d02-151">This flag is for internal use only and is not intended to be used in your application.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="24d02-152">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="24d02-152">**ibLongValue**</span></span>

<span data-ttu-id="24d02-153">Desplazamiento al primer byte que se va a recuperar de una columna de tipo [JET_coltypLongBinary](./jet-coltyp.md) o [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="24d02-153">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md) or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="24d02-154">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="24d02-154">**itagSequence**</span></span>

<span data-ttu-id="24d02-155">Número de secuencia de los valores contenidos en una columna con varios valores.</span><span class="sxs-lookup"><span data-stu-id="24d02-155">The sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="24d02-156">**itagSequence** aquí en el **JET_RETRIEVECOLUMN** puede ser 0.</span><span class="sxs-lookup"><span data-stu-id="24d02-156">**itagSequence** here in the **JET_RETRIEVECOLUMN** can be 0.</span></span> <span data-ttu-id="24d02-157">Si el valor de **itagSequence** es 0, se devuelve el número de instancias de una columna con varios valores en lugar de datos de columna.</span><span class="sxs-lookup"><span data-stu-id="24d02-157">If the **itagSequence** is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span> <span data-ttu-id="24d02-158">No se puede usar un valor de **itagSequence** de 0 en llamadas a [JetRetrieveColumn](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="24d02-158">An **itagSequence** value of 0 cannot be used in calls to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

<span data-ttu-id="24d02-159">**columnidNextTagged**</span><span class="sxs-lookup"><span data-stu-id="24d02-159">**columnidNextTagged**</span></span>

<span data-ttu-id="24d02-160">El **columnid** de la columna etiquetada, con varios valores o disperso cuando se recuperan todas las columnas etiquetadas pasando 0 como **columnid** a [JetRetrieveColumn](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="24d02-160">The **columnid** of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the **columnid** to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

<span data-ttu-id="24d02-161">**ERR**</span><span class="sxs-lookup"><span data-stu-id="24d02-161">**err**</span></span>

<span data-ttu-id="24d02-162">Códigos de error y advertencias devueltos por la recuperación de la columna.</span><span class="sxs-lookup"><span data-stu-id="24d02-162">Error codes and warnings returned from the retrieval of the column.</span></span>

### <a name="requirements"></a><span data-ttu-id="24d02-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24d02-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24d02-164"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="24d02-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="24d02-165">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="24d02-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24d02-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="24d02-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="24d02-167">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="24d02-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24d02-168"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="24d02-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="24d02-169">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="24d02-169">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="24d02-170">Consulte también</span><span class="sxs-lookup"><span data-stu-id="24d02-170">See Also</span></span>

[<span data-ttu-id="24d02-171">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="24d02-171">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="24d02-172">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="24d02-172">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="24d02-173">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="24d02-173">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="24d02-174">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="24d02-174">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="24d02-175">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="24d02-175">JET_RETRIEVECOLUMN</span></span>]()  
[<span data-ttu-id="24d02-176">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="24d02-176">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="24d02-177">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="24d02-177">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
