---
description: 'Más información acerca de: estructura de JET_SETSYSPARAM'
title: Estructura de JET_SETSYSPARAM
TOCTitle: JET_SETSYSPARAM Structure
ms:assetid: 3c0fdd28-99bd-4026-b64b-6859ef9dc91b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269230(v=EXCHG.10)
ms:contentKeyID: 32765532
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
ms.openlocfilehash: 0e88795bb3ee966bf2ad7fa50cc7d2180d7264bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360197"
---
# <a name="jet_setsysparam-structure"></a><span data-ttu-id="5f254-103">Estructura de JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="5f254-103">JET_SETSYSPARAM Structure</span></span>


<span data-ttu-id="5f254-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5f254-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setsysparam-structure"></a><span data-ttu-id="5f254-105">Estructura de JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="5f254-105">JET_SETSYSPARAM Structure</span></span>

<span data-ttu-id="5f254-106">Una matriz de estructuras **JET_SETSYSPARAM** indica un conjunto específico de parámetros globales del sistema que se establecen como argumento cuando se usa la función [JetEnableMultiInstance](./jetenablemultiinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="5f254-106">An array of **JET_SETSYSPARAM** structures indicate a specific set of global system parameters that are set as an argument when using the [JetEnableMultiInstance](./jetenablemultiinstance-function.md) function.</span></span>

<span data-ttu-id="5f254-107">**Windows XP:** Esta estructura se ha introducido en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5f254-107">**Windows XP:** This structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct {
      unsigned long paramid;
      JET_API_PTR lParam;
      const tchar* sz;
      JET_ERR err;
    } JET_SETSYSPARAM;
```

### <a name="members"></a><span data-ttu-id="5f254-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5f254-108">Members</span></span>

<span data-ttu-id="5f254-109">**paramid**</span><span class="sxs-lookup"><span data-stu-id="5f254-109">**paramid**</span></span>

<span data-ttu-id="5f254-110">IDENTIFICADOR del parámetro del sistema que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="5f254-110">The ID of the system parameter that will be set.</span></span>

<span data-ttu-id="5f254-111">Consulte [parámetros del sistema del motor de almacenamiento extensible](./extensible-storage-engine-system-parameters.md) para obtener una lista completa de parámetros del sistema y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="5f254-111">See [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="5f254-112">**lParam**</span><span class="sxs-lookup"><span data-stu-id="5f254-112">**lParam**</span></span>

<span data-ttu-id="5f254-113">Valor opcional que se va a establecer para el parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo entero.</span><span class="sxs-lookup"><span data-stu-id="5f254-113">The optional value to be set for the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="5f254-114">**SZ**</span><span class="sxs-lookup"><span data-stu-id="5f254-114">**sz**</span></span>

<span data-ttu-id="5f254-115">Valor opcional que se va a establecer para el parámetro del sistema seleccionado si ese parámetro del sistema es de un tipo de cadena.</span><span class="sxs-lookup"><span data-stu-id="5f254-115">The optional value to be set for the selected system parameter if that system parameter is of a string type.</span></span>

<span data-ttu-id="5f254-116">**ERR**</span><span class="sxs-lookup"><span data-stu-id="5f254-116">**err**</span></span>

<span data-ttu-id="5f254-117">El error resultante de la llamada a [JetSetSystemParameter](./jetsetsystemparameter-function.md) con los parámetros especificados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5f254-117">The error resulting from the call to [JetSetSystemParameter](./jetsetsystemparameter-function.md) with the previously specified parameters.</span></span>

### <a name="requirements"></a><span data-ttu-id="5f254-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f254-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f254-119"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5f254-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5f254-120">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5f254-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f254-121"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5f254-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5f254-122">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5f254-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f254-123"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5f254-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5f254-124">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="5f254-124">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f254-125"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5f254-125"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5f254-126">Se implementa como <strong>JET_ SETSYSPARAM_W</strong> (Unicode) y <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="5f254-126">Implemented as <strong>JET_ SETSYSPARAM_W</strong> (Unicode) and <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="5f254-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5f254-127">See Also</span></span>

[<span data-ttu-id="5f254-128">Parámetros del sistema del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="5f254-128">Extensible Storage Engine System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)  
[<span data-ttu-id="5f254-129">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="5f254-129">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="5f254-130">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5f254-130">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5f254-131">JetEnableMultiInstance</span><span class="sxs-lookup"><span data-stu-id="5f254-131">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="5f254-132">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="5f254-132">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
