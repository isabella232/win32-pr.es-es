---
description: 'Más información sobre: Server2003Grbits. ForwardOnly, campo'
title: Campo Server2003Grbits. ForwardOnly (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: ForwardOnly field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.forwardonly(v=EXCHG.10)
ms:contentKeyID: 55104214
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec4427628e8d6bfee427fa91c15ed6aee3887314
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155004"
---
# <a name="server2003grbitsforwardonly-field"></a><span data-ttu-id="d747b-103">Server2003Grbits. ForwardOnly, campo</span><span class="sxs-lookup"><span data-stu-id="d747b-103">Server2003Grbits.ForwardOnly field</span></span>

<span data-ttu-id="d747b-104">Esta opción solicita que la tabla temporal se cree solo si el administrador de tablas temporales puede usar la implementación optimizada para los resultados intermedios de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d747b-104">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="d747b-105">Si alguna característica de la tabla temporal impidiera el uso de esta optimización, la operación producirá un error con JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="d747b-105">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="d747b-106">Un efecto secundario de esta opción es permitir que la tabla temporal contenga registros con claves de índice duplicadas.</span><span class="sxs-lookup"><span data-stu-id="d747b-106">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="d747b-107">Consulte [Unique](./temptablegrbit-enumeration.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="d747b-107">See [Unique](./temptablegrbit-enumeration.md) for more information.</span></span>

<span data-ttu-id="d747b-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d747b-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="d747b-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d747b-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d747b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d747b-110">Syntax</span></span>

``` vb
'Declaration
Public Const ForwardOnly As TempTableGrbit
'Usage
Dim value As TempTableGrbit

value = Server2003Grbits.ForwardOnly
```

``` csharp
public const TempTableGrbit ForwardOnly
```

## <a name="see-also"></a><span data-ttu-id="d747b-111">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d747b-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d747b-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="d747b-112">Reference</span></span>

[<span data-ttu-id="d747b-113">Clase Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="d747b-113">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="d747b-114">Miembros de Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="d747b-114">Server2003Grbits members</span></span>](./server2003grbits-members.md)

[<span data-ttu-id="d747b-115">Espacio de nombres Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="d747b-115">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
