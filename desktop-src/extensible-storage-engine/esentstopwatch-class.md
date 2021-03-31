---
description: 'Más información sobre: clase EsentStopwatch'
title: Clase EsentStopwatch
TOCTitle: EsentStopwatch class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentStopwatch
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch(v=EXCHG.10)
ms:contentKeyID: 55102933
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStopwatch
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStopwatch
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1250b10763aca6155ef7ac12bc64adbb95ac77a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912701"
---
# <a name="esentstopwatch-class"></a><span data-ttu-id="43f07-103">Clase EsentStopwatch</span><span class="sxs-lookup"><span data-stu-id="43f07-103">EsentStopwatch class</span></span>

<span data-ttu-id="43f07-104">Proporciona un conjunto de métodos y propiedades que puede usar para medir las estadísticas de trabajo ESENT de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="43f07-104">Provides a set of methods and properties that you can use to measure ESENT work statistics for a thread.</span></span> <span data-ttu-id="43f07-105">Si la versión actual de ESENT no es compatible con [JetGetThreadStats (JET_THREADSTATS)](./vistaapi.jetgetthreadstats-method.md) , todas las estadísticas de esent serán 0.</span><span class="sxs-lookup"><span data-stu-id="43f07-105">If the current version of ESENT doesn't support [JetGetThreadStats(JET_THREADSTATS)](./vistaapi.jetgetthreadstats-method.md) then all ESENT statistics will be 0.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="43f07-106">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="43f07-106">Inheritance hierarchy</span></span>

[<span data-ttu-id="43f07-107">System.Object</span><span class="sxs-lookup"><span data-stu-id="43f07-107">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="43f07-108">Microsoft. ISAM. esent. Interop. EsentStopwatch</span><span class="sxs-lookup"><span data-stu-id="43f07-108">Microsoft.Isam.Esent.Interop.EsentStopwatch</span></span>  

<span data-ttu-id="43f07-109">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="43f07-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="43f07-110">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="43f07-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="43f07-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43f07-111">Syntax</span></span>

``` vb
'Declaration
Public Class EsentStopwatch
'Usage
Dim instance As EsentStopwatch
```

``` csharp
public class EsentStopwatch
```

## <a name="thread-safety"></a><span data-ttu-id="43f07-112">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="43f07-112">Thread safety</span></span>

<span data-ttu-id="43f07-113">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="43f07-113">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="43f07-114">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="43f07-114">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="43f07-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="43f07-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="43f07-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="43f07-116">Reference</span></span>

[<span data-ttu-id="43f07-117">Miembros de EsentStopwatch</span><span class="sxs-lookup"><span data-stu-id="43f07-117">EsentStopwatch members</span></span>](./esentstopwatch-members.md)

[<span data-ttu-id="43f07-118">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="43f07-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
