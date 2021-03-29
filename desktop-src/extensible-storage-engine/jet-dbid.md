---
description: 'Más información acerca de: JET_DBID'
title: JET_DBID
TOCTitle: JET_DBID
ms:assetid: 516acb79-aa75-4609-81b6-3b2e4e0c95af
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269248(v=EXCHG.10)
ms:contentKeyID: 32765550
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
ms.openlocfilehash: fe3a8ccd813ececcb42388c7d577f78e9055d5b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809680"
---
# <a name="jet_dbid"></a><span data-ttu-id="268b5-103">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="268b5-103">JET_DBID</span></span>


<span data-ttu-id="268b5-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="268b5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbid"></a><span data-ttu-id="268b5-105">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="268b5-105">JET_DBID</span></span>

<span data-ttu-id="268b5-106">El tipo de datos **JET_DBID** contiene el identificador de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="268b5-106">The **JET_DBID** data type contains the handle to the database.</span></span> <span data-ttu-id="268b5-107">Un identificador de base de datos se utiliza para administrar el esquema de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="268b5-107">A database handle is used to manage the schema of a database.</span></span> <span data-ttu-id="268b5-108">También se puede usar para administrar las tablas dentro de esa base de datos.</span><span class="sxs-lookup"><span data-stu-id="268b5-108">It can also be used to manage the tables inside of that database.</span></span>

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a><span data-ttu-id="268b5-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="268b5-109">Data Types</span></span>

<span data-ttu-id="268b5-110">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="268b5-110">JET_DBID</span></span>

<span data-ttu-id="268b5-111">Identificador de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="268b5-111">Handle to the database.</span></span>

<span data-ttu-id="268b5-112">Un valor de JET_dbidNil indica que el identificador no es válido.</span><span class="sxs-lookup"><span data-stu-id="268b5-112">A value of JET_dbidNil indicates that the handle is invalid.</span></span>

### <a name="remarks"></a><span data-ttu-id="268b5-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="268b5-113">Remarks</span></span>

<span data-ttu-id="268b5-114">Un identificador de base de datos se crea mediante una llamada a [JetCreateDatabase](./jetcreatedatabase-function.md) o [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="268b5-114">A database handle is created by means of a call to [JetCreateDatabase](./jetcreatedatabase-function.md) or [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

<span data-ttu-id="268b5-115">Un identificador de base de datos se puede cerrar explícitamente con [JetCloseDatabase](./jetclosedatabase-function.md) o cerrarse implícitamente mediante [JetEndSession](./jetendsession-function.md) o [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="268b5-115">A database handle can be explicitly closed by [JetCloseDatabase](./jetclosedatabase-function.md) or implicitly closed by [JetEndSession](./jetendsession-function.md) or [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="268b5-116">Un identificador de base de datos solo se puede usar dentro de la sesión en la que se creó.</span><span class="sxs-lookup"><span data-stu-id="268b5-116">A database handle can be used only within the session in which it was created.</span></span> <span data-ttu-id="268b5-117">La existencia de un identificador de base de datos corresponde al abierto lógico de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="268b5-117">The existence of a database handle corresponds to the logical open of a database.</span></span> <span data-ttu-id="268b5-118">Una apertura lógica es diferente de la abierta física de una base de datos, que se produce cuando se adjunta una base de datos al sistema.</span><span class="sxs-lookup"><span data-stu-id="268b5-118">A logical open is different from the physical open of a database, which happens when a database is attached to the system.</span></span>

### <a name="requirements"></a><span data-ttu-id="268b5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="268b5-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="268b5-120"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="268b5-120"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="268b5-121">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="268b5-121">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="268b5-122"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="268b5-122"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="268b5-123">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="268b5-123">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="268b5-124"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="268b5-124"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="268b5-125">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="268b5-125">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="268b5-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="268b5-126">See Also</span></span>

[<span data-ttu-id="268b5-127">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="268b5-127">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="268b5-128">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="268b5-128">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="268b5-129">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="268b5-129">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="268b5-130">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="268b5-130">JetEndSession</span></span>](./jetendsession-function.md)
