---
description: 'Más información acerca de: JET_PWSTR'
title: JET_PWSTR
TOCTitle: JET_PWSTR
ms:assetid: 6575f0f0-d022-4e70-9f17-c1d884d9e226
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269271(v=EXCHG.10)
ms:contentKeyID: 32765573
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
ms.openlocfilehash: 536ef3bba465f6d152e3483436c1dc1e82277339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697454"
---
# <a name="jet_pwstr"></a><span data-ttu-id="cfc0b-103">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="cfc0b-103">JET_PWSTR</span></span>


<span data-ttu-id="cfc0b-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cfc0b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pwstr"></a><span data-ttu-id="cfc0b-105">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="cfc0b-105">JET_PWSTR</span></span>

<span data-ttu-id="cfc0b-106">El tipo de datos **JET_PWSTR** contiene una cadena **Unicode** terminada en null (char \* ).</span><span class="sxs-lookup"><span data-stu-id="cfc0b-106">The **JET_PWSTR** data type contains a null-terminated **Unicode** string (char \*).</span></span>

<span data-ttu-id="cfc0b-107">**Windows Vista: JET_PWSTR** se incorpora en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cfc0b-107">**Windows Vista:  JET_PWSTR** is introduced in Windows Vista.</span></span>

```cpp
    typedef __nullterminated WCHAR * JET_PWSTR;
```

### <a name="data-types"></a><span data-ttu-id="cfc0b-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="cfc0b-108">Data Types</span></span>

<span data-ttu-id="cfc0b-109">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="cfc0b-109">JET_PWSTR</span></span>

<span data-ttu-id="cfc0b-110">Cadena Unicode terminada en null (char \* ).</span><span class="sxs-lookup"><span data-stu-id="cfc0b-110">Null-terminated, Unicode string (char \*).</span></span>

### <a name="requirements"></a><span data-ttu-id="cfc0b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfc0b-111">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cfc0b-112"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="cfc0b-112"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cfc0b-113">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cfc0b-113">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfc0b-114"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cfc0b-114"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cfc0b-115">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cfc0b-115">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfc0b-116"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="cfc0b-116"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cfc0b-117">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="cfc0b-117">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

