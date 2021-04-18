---
description: 'Más información sobre: VistaApi. JetGetThreadStats (método)'
title: Método VistaApi. JetGetThreadStats (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetGetThreadStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetthreadstats(v=EXCHG.10)
ms:contentKeyID: 55104192
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 92572fd538f0c6c2643e7b40a07ac168ae6980d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705997"
---
# <a name="vistaapijetgetthreadstats-method"></a><span data-ttu-id="f92fa-103">VistaApi. JetGetThreadStats, método</span><span class="sxs-lookup"><span data-stu-id="f92fa-103">VistaApi.JetGetThreadStats method</span></span>

<span data-ttu-id="f92fa-104">Recupera información de rendimiento del motor de base de datos para el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="f92fa-104">Retrieves performance information from the database engine for the current thread.</span></span> <span data-ttu-id="f92fa-105">Se pueden usar varias llamadas para recopilar estadísticas que reflejen la actividad del motor de base de datos en este subproceso entre esas llamadas.</span><span class="sxs-lookup"><span data-stu-id="f92fa-105">Multiple calls can be used to collect statistics that reflect the activity of the database engine on this thread between those calls.</span></span>

<span data-ttu-id="f92fa-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f92fa-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="f92fa-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f92fa-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f92fa-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f92fa-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetThreadStats ( _
    <OutAttribute> ByRef threadstats As JET_THREADSTATS _
)
'Usage
Dim threadstats As JET_THREADSTATSVistaApi.JetGetThreadStats(threadstats)
```

``` csharp
public static void JetGetThreadStats(
    out JET_THREADSTATS threadstats
)
```

#### <a name="parameters"></a><span data-ttu-id="f92fa-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f92fa-109">Parameters</span></span>

  - <span data-ttu-id="f92fa-110">threadstats</span><span class="sxs-lookup"><span data-stu-id="f92fa-110">threadstats</span></span>  
    <span data-ttu-id="f92fa-111">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="f92fa-111">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="f92fa-112">Devuelve los datos de las estadísticas del subproceso.</span><span class="sxs-lookup"><span data-stu-id="f92fa-112">Returns the thread statistics data.</span></span>

## <a name="see-also"></a><span data-ttu-id="f92fa-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="f92fa-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f92fa-114">Referencia</span><span class="sxs-lookup"><span data-stu-id="f92fa-114">Reference</span></span>

[<span data-ttu-id="f92fa-115">Clase VistaApi</span><span class="sxs-lookup"><span data-stu-id="f92fa-115">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="f92fa-116">Miembros de VistaApi</span><span class="sxs-lookup"><span data-stu-id="f92fa-116">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="f92fa-117">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="f92fa-117">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
