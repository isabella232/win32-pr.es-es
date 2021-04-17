---
description: 'Más información sobre: enumeración StopServiceGrbit'
title: Enumeración StopServiceGrbit (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: StopServiceGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.stopservicegrbit(v=EXCHG.10)
ms:contentKeyID: 55104330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 54e54576dfb1023ec4e3bc55ddd198a77f0ddf25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696608"
---
# <a name="stopservicegrbit-enumeration"></a><span data-ttu-id="1ff10-103">Enumeración StopServiceGrbit</span><span class="sxs-lookup"><span data-stu-id="1ff10-103">StopServiceGrbit enumeration</span></span>

<span data-ttu-id="1ff10-104">Opciones de [JetStopServiceInstance2 (JET_INSTANCE, StopServiceGrbit)](./windows8api.jetstopserviceinstance2-method.md).</span><span class="sxs-lookup"><span data-stu-id="1ff10-104">Options for [JetStopServiceInstance2(JET_INSTANCE, StopServiceGrbit)](./windows8api.jetstopserviceinstance2-method.md).</span></span>

<span data-ttu-id="1ff10-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="1ff10-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="1ff10-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1ff10-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="1ff10-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1ff10-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff10-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ff10-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration StopServiceGrbit
'Usage
Dim instance As StopServiceGrbit
```

``` csharp
[FlagsAttribute]
public enum StopServiceGrbit
```

## <a name="members"></a><span data-ttu-id="1ff10-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1ff10-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="1ff10-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="1ff10-110">Member name</span></span></th>
<th><span data-ttu-id="1ff10-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ff10-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1ff10-112">Todo</span><span class="sxs-lookup"><span data-stu-id="1ff10-112">All</span></span></td>
<td><span data-ttu-id="1ff10-113">Detiene todos los servicios de ESE para la instancia especificada.</span><span class="sxs-lookup"><span data-stu-id="1ff10-113">Stops all ESE services for the specified instance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="1ff10-114">BackgroundUserTasks</span><span class="sxs-lookup"><span data-stu-id="1ff10-114">BackgroundUserTasks</span></span></td>
<td><span data-ttu-id="1ff10-115">Detiene las tareas de mantenimiento de fondo específico del cliente reiniciables (B + desfragmentación de árbol).</span><span class="sxs-lookup"><span data-stu-id="1ff10-115">Stops restartable client specificed background maintenance tasks (B+ Tree Defrag).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1ff10-116">QuiesceCaches</span><span class="sxs-lookup"><span data-stu-id="1ff10-116">QuiesceCaches</span></span></td>
<td><span data-ttu-id="1ff10-117">Quiesces todas las cachés desfasadas en el disco.</span><span class="sxs-lookup"><span data-stu-id="1ff10-117">Quiesces all dirty caches to disk.</span></span> <span data-ttu-id="1ff10-118">Asincrónica</span><span class="sxs-lookup"><span data-stu-id="1ff10-118">Asynchronous.</span></span> <span data-ttu-id="1ff10-119">La inactividad se cancela si se llama al bit de reanudación posteriormente.</span><span class="sxs-lookup"><span data-stu-id="1ff10-119">Quiescing is cancelled if the Resume bit is called subsequently.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="1ff10-120">Reanudar</span><span class="sxs-lookup"><span data-stu-id="1ff10-120">Resume</span></span></td>
<td><span data-ttu-id="1ff10-121">Reanuda las operaciones de StopService emitidas previamente, es decir, &quot; reinicia el servicio &quot; .</span><span class="sxs-lookup"><span data-stu-id="1ff10-121">Resumes previously issued StopService operations, i.e. &quot;restarts service&quot;.</span></span> <span data-ttu-id="1ff10-122">Se puede combinar con los grbits anteriores para reanudar servicios específicos o con 0X0 reanuda todos los servicios detenidos anteriores.</span><span class="sxs-lookup"><span data-stu-id="1ff10-122">Can be combined with above grbits to Resume specific services, or with 0x0 Resumes all previous stopped services.</span></span>
<p><span data-ttu-id="1ff10-123">ADVERTENCIA: este bit solo se puede usar para reanudar JET_bitStopServiceBackground y JET_bitStopServiceQuiesceCaches, si ha realizado una JET_bitStopServiceAll o JET_bitStopServiceAPI, se producirá un error al intentar usar JET_bitStopServiceResume.</span><span class="sxs-lookup"><span data-stu-id="1ff10-123">Warning: This bit can only be used to resume JET_bitStopServiceBackground and JET_bitStopServiceQuiesceCaches, if you did a JET_bitStopServiceAll or JET_bitStopServiceAPI, attempting to use JET_bitStopServiceResume will fail.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="1ff10-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ff10-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1ff10-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="1ff10-125">Reference</span></span>

[<span data-ttu-id="1ff10-126">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="1ff10-126">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
