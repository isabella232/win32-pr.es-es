---
description: 'Más información acerca de: estructura de JET_SNPROG'
title: Estructura de JET_SNPROG
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 961e9cf264652924cfb1d870fa1a04aabc7fb61a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496954"
---
# <a name="jet_snprog-structure"></a><span data-ttu-id="ab7a1-103">Estructura de JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="ab7a1-103">JET_SNPROG Structure</span></span>


<span data-ttu-id="ab7a1-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ab7a1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snprog-structure"></a><span data-ttu-id="ab7a1-105">Estructura de JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="ab7a1-105">JET_SNPROG Structure</span></span>

<span data-ttu-id="ab7a1-106">La estructura **JET_SNPROG** contiene información sobre el progreso de una operación de ejecución prolongada.</span><span class="sxs-lookup"><span data-stu-id="ab7a1-106">The **JET_SNPROG** structure contains information about the progress of a long-running operation.</span></span> <span data-ttu-id="ab7a1-107">Cuando se llama a la función de devolución de llamada para notificar el estado de la operación y la operación aún está en curso, el último parámetro de la función de devolución de llamada es un puntero a una estructura de **JET_SNPROG** .</span><span class="sxs-lookup"><span data-stu-id="ab7a1-107">When the callback function is called to notify the status of the operation and the operation is still in progress, the last parameter of the callback function is a pointer to a **JET_SNPROG** structure.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a><span data-ttu-id="ab7a1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ab7a1-108">Members</span></span>

<span data-ttu-id="ab7a1-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="ab7a1-109">**cbStruct**</span></span>

<span data-ttu-id="ab7a1-110">Tamaño de la estructura de **JET_SNPROG** , en bytes.</span><span class="sxs-lookup"><span data-stu-id="ab7a1-110">The size of the **JET_SNPROG** structure, in bytes.</span></span> <span data-ttu-id="ab7a1-111">Este valor confirma la presencia de los campos siguientes.</span><span class="sxs-lookup"><span data-stu-id="ab7a1-111">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="ab7a1-112">**cunitDone**</span><span class="sxs-lookup"><span data-stu-id="ab7a1-112">**cunitDone**</span></span>

<span data-ttu-id="ab7a1-113">El número de unidades de trabajo que ya se han completado durante la función de larga ejecución.</span><span class="sxs-lookup"><span data-stu-id="ab7a1-113">The number of work units that are already completed during the long running function.</span></span>

<span data-ttu-id="ab7a1-114">**cunitTotal**</span><span class="sxs-lookup"><span data-stu-id="ab7a1-114">**cunitTotal**</span></span>

<span data-ttu-id="ab7a1-115">El número de unidades de trabajo que se deben completar.</span><span class="sxs-lookup"><span data-stu-id="ab7a1-115">The number of work units that need to be completed.</span></span> <span data-ttu-id="ab7a1-116">Este valor siempre debe ser mayor o igual que **cunitDone**.</span><span class="sxs-lookup"><span data-stu-id="ab7a1-116">This value should always be bigger than or equal to **cunitDone**.</span></span>

### <a name="requirements"></a><span data-ttu-id="ab7a1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab7a1-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab7a1-118"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ab7a1-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ab7a1-119">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ab7a1-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab7a1-120"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ab7a1-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ab7a1-121">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ab7a1-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab7a1-122"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ab7a1-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ab7a1-123">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="ab7a1-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

