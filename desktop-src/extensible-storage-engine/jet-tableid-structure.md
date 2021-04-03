---
description: 'Más información acerca de: estructura de JET_TABLEID'
title: Estructura de JET_TABLEID
TOCTitle: JET_TABLEID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TABLEID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid(v=EXCHG.10)
ms:contentKeyID: 39516503
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLEID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a72713007ace7fb93b3f01ec8e5fc25cbe127298
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083119"
---
# <a name="jet_tableid-structure"></a><span data-ttu-id="56db5-103">Estructura de JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="56db5-103">JET_TABLEID structure</span></span>

<span data-ttu-id="56db5-104">Un JET_TABLEID contiene un identificador para el cursor de base de datos que se va a usar para una llamada a la API de JET.</span><span class="sxs-lookup"><span data-stu-id="56db5-104">A JET_TABLEID contains a handle to the database cursor to use for a call to the JET API.</span></span> <span data-ttu-id="56db5-105">Un cursor solo se puede usar con la sesión que se usó para abrir ese cursor.</span><span class="sxs-lookup"><span data-stu-id="56db5-105">A cursor can only be used with the session that was used to open that cursor.</span></span>

<span data-ttu-id="56db5-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="56db5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="56db5-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="56db5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="56db5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56db5-108">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_TABLEID _
    Implements IEquatable(Of JET_TABLEID), IFormattable
'Usage
Dim instance As JET_TABLEID
```

``` csharp
public struct JET_TABLEID : IEquatable<JET_TABLEID>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="56db5-109">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="56db5-109">Thread safety</span></span>

<span data-ttu-id="56db5-110">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="56db5-110">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="56db5-111">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="56db5-111">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="56db5-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="56db5-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="56db5-113">Referencia</span><span class="sxs-lookup"><span data-stu-id="56db5-113">Reference</span></span>

[<span data-ttu-id="56db5-114">Miembros de JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="56db5-114">JET_TABLEID members</span></span>](./jet-tableid-members.md)

[<span data-ttu-id="56db5-115">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="56db5-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
