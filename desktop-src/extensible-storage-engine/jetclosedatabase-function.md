---
description: 'Más información acerca de: JetCloseDatabase (función)'
title: JetCloseDatabase función)
TOCTitle: JetCloseDatabase Function
ms:assetid: e17a05dd-c30b-4e8f-8538-91a65e8052d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294123(v=EXCHG.10)
ms:contentKeyID: 32765737
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9088e0ebc3b4778d6968c999afc238e49fb2f48f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539987"
---
# <a name="jetclosedatabase-function"></a><span data-ttu-id="535d5-103">JetCloseDatabase función)</span><span class="sxs-lookup"><span data-stu-id="535d5-103">JetCloseDatabase Function</span></span>


<span data-ttu-id="535d5-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="535d5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosedatabase-function"></a><span data-ttu-id="535d5-105">JetCloseDatabase función)</span><span class="sxs-lookup"><span data-stu-id="535d5-105">JetCloseDatabase Function</span></span>

<span data-ttu-id="535d5-106">La función **JetCloseDatabase** cierra un archivo de base de datos que se abrió previamente con [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="535d5-106">The **JetCloseDatabase** function closes a database file that was previously opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetCloseDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="535d5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="535d5-107">Parameters</span></span>

<span data-ttu-id="535d5-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="535d5-108">*sesid*</span></span>

<span data-ttu-id="535d5-109">Contexto de sesión de base de datos que se usará para la llamada de API.</span><span class="sxs-lookup"><span data-stu-id="535d5-109">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="535d5-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="535d5-110">*dbid*</span></span>

<span data-ttu-id="535d5-111">Base de datos que se va a cerrar.</span><span class="sxs-lookup"><span data-stu-id="535d5-111">The database to be closed.</span></span>

<span data-ttu-id="535d5-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="535d5-112">*grbit*</span></span>

<span data-ttu-id="535d5-113">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="535d5-113">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="535d5-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="535d5-114">Return Value</span></span>

<span data-ttu-id="535d5-115">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="535d5-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="535d5-116">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="535d5-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="535d5-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="535d5-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="535d5-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="535d5-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="535d5-119">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="535d5-119">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="535d5-120">La base de datos no se ha abierto previamente.</span><span class="sxs-lookup"><span data-stu-id="535d5-120">The database was not previously opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="535d5-121">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="535d5-121">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="535d5-122">El parámetro <em>DBID</em> no era un identificador de base de datos válido.</span><span class="sxs-lookup"><span data-stu-id="535d5-122">The <em>dbid</em> parameter was not a valid database identifier.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="535d5-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="535d5-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="535d5-124">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="535d5-124">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="535d5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="535d5-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="535d5-126"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="535d5-126"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="535d5-127">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="535d5-127">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="535d5-128"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="535d5-128"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="535d5-129">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="535d5-129">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="535d5-130"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="535d5-130"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="535d5-131">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="535d5-131">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="535d5-132"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="535d5-132"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="535d5-133">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="535d5-133">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="535d5-134"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="535d5-134"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="535d5-135">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="535d5-135">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="535d5-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="535d5-136">See Also</span></span>

[<span data-ttu-id="535d5-137">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="535d5-137">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="535d5-138">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="535d5-138">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="535d5-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="535d5-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="535d5-140">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="535d5-140">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="535d5-141">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="535d5-141">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="535d5-142">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="535d5-142">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="535d5-143">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="535d5-143">JetOpenDatabase</span></span>](./jetopendatabase-function.md)
