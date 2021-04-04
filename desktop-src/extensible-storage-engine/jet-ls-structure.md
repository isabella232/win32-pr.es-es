---
description: 'Más información acerca de: estructura de JET_LS'
title: Estructura de JET_LS
TOCTitle: JET_LS structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_LS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls(v=EXCHG.10)
ms:contentKeyID: 39510760
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d32c1a6815cfa7552fed0d8f1a01376ae0eacaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277875"
---
# <a name="jet_ls-structure"></a><span data-ttu-id="c8571-103">Estructura de JET_LS</span><span class="sxs-lookup"><span data-stu-id="c8571-103">JET_LS structure</span></span>

<span data-ttu-id="c8571-104">Almacenamiento local para un controlador ESENT.</span><span class="sxs-lookup"><span data-stu-id="c8571-104">Local storage for an ESENT handle.</span></span> <span data-ttu-id="c8571-105">Usado por [JetGetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md) y [JetSetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).</span><span class="sxs-lookup"><span data-stu-id="c8571-105">Used by [JetGetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md) and [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).</span></span>

<span data-ttu-id="c8571-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c8571-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c8571-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c8571-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c8571-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8571-108">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_LS _
    Implements IEquatable(Of JET_LS), IFormattable
'Usage
Dim instance As JET_LS
```

``` csharp
public struct JET_LS : IEquatable<JET_LS>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="c8571-109">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="c8571-109">Thread safety</span></span>

<span data-ttu-id="c8571-110">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c8571-110">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c8571-111">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c8571-111">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8571-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8571-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c8571-113">Referencia</span><span class="sxs-lookup"><span data-stu-id="c8571-113">Reference</span></span>

[<span data-ttu-id="c8571-114">Miembros de JET_LS</span><span class="sxs-lookup"><span data-stu-id="c8571-114">JET_LS members</span></span>](./jet-ls-members.md)

[<span data-ttu-id="c8571-115">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c8571-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
