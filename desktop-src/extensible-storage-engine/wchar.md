---
description: 'Más información acerca de: WCHAR'
title: WCHAR
TOCTitle: WCHAR
ms:assetid: 922431b3-bf9a-4aba-bc67-dd33d9aeaac0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269344(v=EXCHG.10)
ms:contentKeyID: 32765633
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
ms.openlocfilehash: 1dfa86cbc771059d941027385090dcbd2f401855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705579"
---
# <a name="wchar"></a><span data-ttu-id="abbe7-103">WCHAR</span><span class="sxs-lookup"><span data-stu-id="abbe7-103">WCHAR</span></span>


<span data-ttu-id="abbe7-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="abbe7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="wchar"></a><span data-ttu-id="abbe7-105">WCHAR</span><span class="sxs-lookup"><span data-stu-id="abbe7-105">WCHAR</span></span>

<span data-ttu-id="abbe7-106">El tipo de datos WCHAR contiene un carácter Unicode de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="abbe7-106">The WCHAR data type contains a 16-bit Unicode character.</span></span>

```cpp
    #if !defined(_NATIVE_WCHAR_T_DEFINED)
    typedef unsigned short WCHAR;
    #else
    typedef wchar_t WCHAR;
    #endif
```

### <a name="data-types"></a><span data-ttu-id="abbe7-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="abbe7-107">Data Types</span></span>

<span data-ttu-id="abbe7-108">WCHAR</span><span class="sxs-lookup"><span data-stu-id="abbe7-108">WCHAR</span></span>

<span data-ttu-id="abbe7-109">Carácter Unicode de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="abbe7-109">A 16-bit Unicode character.</span></span>

### <a name="requirements"></a><span data-ttu-id="abbe7-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abbe7-110">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="abbe7-111"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="abbe7-111"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="abbe7-112">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="abbe7-112">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abbe7-113"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="abbe7-113"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="abbe7-114">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="abbe7-114">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abbe7-115"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="abbe7-115"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="abbe7-116">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="abbe7-116">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

