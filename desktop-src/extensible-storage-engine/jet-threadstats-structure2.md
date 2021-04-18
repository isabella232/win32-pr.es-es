---
description: 'Más información acerca de: estructura de JET_THREADSTATS'
title: JET_THREADSTATS estructura (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: JET_THREADSTATS structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats(v=EXCHG.10)
ms:contentKeyID: 39512342
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 764a9276543fbb7a5b1aa2762cc8ed1877c45ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714971"
---
# <a name="jet_threadstats-structure"></a><span data-ttu-id="95c57-103">Estructura de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="95c57-103">JET_THREADSTATS structure</span></span>

<span data-ttu-id="95c57-104">Contiene estadísticas acumuladas sobre el trabajo realizado por el motor de base de datos en el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="95c57-104">Contains cumulative statistics on the work performed by the database engine on the current thread.</span></span> <span data-ttu-id="95c57-105">Esta información se devuelve a través de JetGetThreadStats.</span><span class="sxs-lookup"><span data-stu-id="95c57-105">This information is returned via JetGetThreadStats.</span></span>

<span data-ttu-id="95c57-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="95c57-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="95c57-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="95c57-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="95c57-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95c57-108">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_THREADSTATS _
    Implements IEquatable(Of JET_THREADSTATS)
'Usage
Dim instance As JET_THREADSTATS
```

``` csharp
[SerializableAttribute]
public struct JET_THREADSTATS : IEquatable<JET_THREADSTATS>
```

## <a name="thread-safety"></a><span data-ttu-id="95c57-109">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="95c57-109">Thread safety</span></span>

<span data-ttu-id="95c57-110">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="95c57-110">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="95c57-111">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="95c57-111">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="95c57-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="95c57-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="95c57-113">Referencia</span><span class="sxs-lookup"><span data-stu-id="95c57-113">Reference</span></span>

[<span data-ttu-id="95c57-114">Miembros de JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="95c57-114">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="95c57-115">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="95c57-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
