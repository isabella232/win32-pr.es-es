---
description: 'Más información acerca de: estructura de JET_SESID'
title: Estructura de JET_SESID
TOCTitle: JET_SESID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SESID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid(v=EXCHG.10)
ms:contentKeyID: 39516065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SESID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f547425f40b4336213ef69abe4bba07ee1baa513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686629"
---
# <a name="jet_sesid-structure"></a><span data-ttu-id="1c43b-103">Estructura de JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1c43b-103">JET_SESID structure</span></span>

<span data-ttu-id="1c43b-104">Un JET_SESID contiene un identificador de la sesión que se va a usar para las llamadas a JET API-.</span><span class="sxs-lookup"><span data-stu-id="1c43b-104">A JET_SESID contains a handle to the session to use for calls to the JET APIr-.</span></span>

<span data-ttu-id="1c43b-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1c43b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1c43b-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1c43b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1c43b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c43b-107">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_SESID _
    Implements IEquatable(Of JET_SESID), IFormattable
'Usage
Dim instance As JET_SESID
```

``` csharp
public struct JET_SESID : IEquatable<JET_SESID>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="1c43b-108">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="1c43b-108">Thread safety</span></span>

<span data-ttu-id="1c43b-109">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="1c43b-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1c43b-110">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="1c43b-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c43b-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c43b-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1c43b-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="1c43b-112">Reference</span></span>

[<span data-ttu-id="1c43b-113">Miembros de JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1c43b-113">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="1c43b-114">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1c43b-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
