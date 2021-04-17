---
description: 'Más información acerca de: JetCreateIndex (función)'
title: Función JetCreateIndex
TOCTitle: JetCreateIndex Function
ms:assetid: d164e74a-7719-4587-9059-8fb18b365133
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294099(v=EXCHG.10)
ms:contentKeyID: 32765714
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndexA
- JetCreateIndex
- JetCreateIndexW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0208a5f0adac4ff5128b506123f3b68589cd0d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716166"
---
# <a name="jetcreateindex-function"></a><span data-ttu-id="f0353-103">Función JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="f0353-103">JetCreateIndex Function</span></span>


<span data-ttu-id="f0353-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f0353-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex-function"></a><span data-ttu-id="f0353-105">Función JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="f0353-105">JetCreateIndex Function</span></span>

<span data-ttu-id="f0353-106">La función **JetCreateIndex** le permite crear un índice de datos en una base de datos del motor de almacenamiento extensible (ese), que puede usar para buscar datos específicos rápidamente.</span><span class="sxs-lookup"><span data-stu-id="f0353-106">The **JetCreateIndex** function enables you to create an index of data in an Extensible Storage Engine (ESE) database, which you can use to locate specific data quickly.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          const tchar* szKey,
      __in          unsigned long cbKey,
      __in          unsigned long lDensity
    );
```

### <a name="parameters"></a><span data-ttu-id="f0353-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0353-107">Parameters</span></span>

<span data-ttu-id="f0353-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f0353-108">*sesid*</span></span>

<span data-ttu-id="f0353-109">Contexto de sesión de base de datos que se va a usar para una llamada de API determinada.</span><span class="sxs-lookup"><span data-stu-id="f0353-109">The database session context to use for a particular API call.</span></span>

<span data-ttu-id="f0353-110">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="f0353-110">*tableid*</span></span>

<span data-ttu-id="f0353-111">Tabla para la que se creará un índice.</span><span class="sxs-lookup"><span data-stu-id="f0353-111">The table that an index will be created for.</span></span>

<span data-ttu-id="f0353-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="f0353-112">*szIndexName*</span></span>

<span data-ttu-id="f0353-113">Puntero a una cadena terminada en null que especifica el nombre del índice que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="f0353-113">A pointer to a null-terminated string that specifies the name of the index to be created.</span></span>

<span data-ttu-id="f0353-114">El nombre del índice debe cumplir las siguientes directrices:</span><span class="sxs-lookup"><span data-stu-id="f0353-114">The index name must conform to the following guidelines:</span></span>

  - <span data-ttu-id="f0353-115">Debe contener menos caracteres que JET_cbNameMost, sin incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="f0353-115">It must contain fewer characters than JET_cbNameMost, not including the terminating null character.</span></span>

  - <span data-ttu-id="f0353-116">Solo debe contener caracteres de las categorías siguientes: de 0 a 9, de la a a la Z, de la a a la z y de todos los caracteres de puntuación, excepto " \! "</span><span class="sxs-lookup"><span data-stu-id="f0353-116">It must contain only characters from the following categories: 0 through 9, A through Z, a through z, and all punctuation characters except for "\!"</span></span> <span data-ttu-id="f0353-117">(signo de exclamación), "," (coma), " \[ " (corchete de apertura) y " \] " (corchete de cierre); es decir, los caracteres ASCII 0x20, 0x22 a 0x2d, 0x2f a 0x5a, 0x5c y 0x5d a 0x7F.</span><span class="sxs-lookup"><span data-stu-id="f0353-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, the ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="f0353-118">No debe comenzar con un espacio.</span><span class="sxs-lookup"><span data-stu-id="f0353-118">It must not begin with a space.</span></span>

  - <span data-ttu-id="f0353-119">Debe contener al menos un carácter que no sea un espacio.</span><span class="sxs-lookup"><span data-stu-id="f0353-119">It must contain at least one non-space character.</span></span>

<span data-ttu-id="f0353-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f0353-120">*grbit*</span></span>

<span data-ttu-id="f0353-121">Grupo de bits que contiene las opciones que se van a utilizar para una llamada determinada.</span><span class="sxs-lookup"><span data-stu-id="f0353-121">A group of bits that contains the options to be used for a particular call.</span></span> <span data-ttu-id="f0353-122">Este parámetro puede incluir cero o más de las opciones que se encuentran en la estructura [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="f0353-122">This parameter can include zero or more of the options found in the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

<span data-ttu-id="f0353-123">*szKey*</span><span class="sxs-lookup"><span data-stu-id="f0353-123">*szKey*</span></span>

<span data-ttu-id="f0353-124">Un puntero a una cadena doble terminada en NULL de tokens delimitados por null.</span><span class="sxs-lookup"><span data-stu-id="f0353-124">A pointer to a double null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="f0353-125">Para obtener más información sobre este parámetro, vea la estructura [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="f0353-125">For more information about this parameter, see the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

<span data-ttu-id="f0353-126">*cbKey*</span><span class="sxs-lookup"><span data-stu-id="f0353-126">*cbKey*</span></span>

<span data-ttu-id="f0353-127">La longitud, en bytes, del parámetro *szKey* , incluidos los dos caracteres nulos de terminación.</span><span class="sxs-lookup"><span data-stu-id="f0353-127">The length, in bytes, of the *szKey* parameter, including the two terminating null characters.</span></span>

<span data-ttu-id="f0353-128">*lDensity*</span><span class="sxs-lookup"><span data-stu-id="f0353-128">*lDensity*</span></span>

<span data-ttu-id="f0353-129">Densidad porcentual del árbol B + del índice inicial.</span><span class="sxs-lookup"><span data-stu-id="f0353-129">The percentage density of the initial index B+ tree.</span></span>

<span data-ttu-id="f0353-130">Para obtener más información sobre este parámetro, vea la estructura [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="f0353-130">For more information about this parameter, see the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

### <a name="return-value"></a><span data-ttu-id="f0353-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0353-131">Return Value</span></span>

<span data-ttu-id="f0353-132">Esta función devuelve el tipo de datos [JET_ERR](./jet-err.md) con uno de los códigos de retorno que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f0353-132">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="f0353-133">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f0353-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0353-134">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f0353-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="f0353-135">Significado</span><span class="sxs-lookup"><span data-stu-id="f0353-135">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0353-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f0353-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f0353-137">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f0353-137">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f0353-138">Para obtener una lista de errores adicionales que pueden ser devueltos por la función **JetCreateIndex** , vea [JetCreateIndex2](./jetcreateindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="f0353-138">For a list of additional errors that can be returned by the **JetCreateIndex** function, see [JetCreateIndex2](./jetcreateindex2-function.md).</span></span>

#### <a name="remarks"></a><span data-ttu-id="f0353-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0353-139">Remarks</span></span>

<span data-ttu-id="f0353-140">Llamar a la función **JetCreateIndex** es idéntico a llamar a la función [JetCreateIndex2](./jetcreateindex2-function.md) con una estructura [JET_INDEXCREATE](./jet-indexcreate-structure.md) que contiene la misma configuración que los parámetros de **JetCreateIndex** y un parámetro *cIndexCreate* igual a 1.</span><span class="sxs-lookup"><span data-stu-id="f0353-140">Calling the **JetCreateIndex** function is identical to calling the [JetCreateIndex2](./jetcreateindex2-function.md) function with a [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure containing the same settings as the parameters of **JetCreateIndex**, and a *cIndexCreate* parameter equal to 1.</span></span> <span data-ttu-id="f0353-141">En el caso de los campos de la estructura [JET_INDEXCREATE](./jet-indexcreate-structure.md) que no tienen los parámetros correspondientes en **JetCreateIndex**, se supone un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="f0353-141">For the fields of the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure that do not have corresponding parameters in **JetCreateIndex**, a value of 0 is assumed.</span></span>

<span data-ttu-id="f0353-142">Tenga en cuenta que **JetCreateIndex** se ha reemplazado por [JetCreateIndex2](./jetcreateindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="f0353-142">Note that **JetCreateIndex** has been superseded by [JetCreateIndex2](./jetcreateindex2-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="f0353-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0353-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0353-144">Remoto</span><span class="sxs-lookup"><span data-stu-id="f0353-144">Client</span></span></p></td>
<td><p><span data-ttu-id="f0353-145">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f0353-145">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0353-146">Servidor</span><span class="sxs-lookup"><span data-stu-id="f0353-146">Server</span></span></p></td>
<td><p><span data-ttu-id="f0353-147">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f0353-147">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0353-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0353-148">Header</span></span></p></td>
<td><p><span data-ttu-id="f0353-149">Se declara en esent. h.</span><span class="sxs-lookup"><span data-stu-id="f0353-149">Is declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0353-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0353-150">Library</span></span></p></td>
<td><p><span data-ttu-id="f0353-151">Utiliza ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f0353-151">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0353-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f0353-152">DLL</span></span></p></td>
<td><p><span data-ttu-id="f0353-153">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f0353-153">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0353-154">Unicode</span><span class="sxs-lookup"><span data-stu-id="f0353-154">Unicode</span></span></p></td>
<td><p><span data-ttu-id="f0353-155">Se implementa como <strong>JetCreateIndexW</strong> (Unicode) y <strong>JetCreateIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f0353-155">Is implemented as <strong>JetCreateIndexW</strong> (Unicode) and <strong>JetCreateIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f0353-156">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f0353-156">See Also</span></span>

[<span data-ttu-id="f0353-157">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f0353-157">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f0353-158">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f0353-158">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f0353-159">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f0353-159">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f0353-160">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f0353-160">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f0353-161">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="f0353-161">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="f0353-162">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="f0353-162">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="f0353-163">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="f0353-163">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="f0353-164">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="f0353-164">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
