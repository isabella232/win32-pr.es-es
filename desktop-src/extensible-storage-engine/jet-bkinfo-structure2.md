---
description: 'Más información acerca de: estructura de JET_BKINFO'
title: Estructura de JET_BKINFO
TOCTitle: JET_BKINFO structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_BKINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bkinfo(v=EXCHG.10)
ms:contentKeyID: 39511166
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKINFO
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKINFO
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c3b0d3178abaa90fe507c06a2a997472492643c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278675"
---
# <a name="jet_bkinfo-structure"></a><span data-ttu-id="f3c8f-103">Estructura de JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="f3c8f-103">JET_BKINFO structure</span></span>

<span data-ttu-id="f3c8f-104">Contiene una colección de datos acerca de un evento de copia de seguridad específico.</span><span class="sxs-lookup"><span data-stu-id="f3c8f-104">Holds a collection of data about a specific backup event.</span></span>

<span data-ttu-id="f3c8f-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f3c8f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f3c8f-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f3c8f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f3c8f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3c8f-107">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_BKINFO _
    Implements IEquatable(Of JET_BKINFO), INullableJetStruct
'Usage
Dim instance As JET_BKINFO
```

``` csharp
[SerializableAttribute]
public struct JET_BKINFO : IEquatable<JET_BKINFO>, 
    INullableJetStruct
```

## <a name="thread-safety"></a><span data-ttu-id="f3c8f-108">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="f3c8f-108">Thread safety</span></span>

<span data-ttu-id="f3c8f-109">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="f3c8f-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f3c8f-110">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="f3c8f-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f3c8f-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3c8f-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f3c8f-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="f3c8f-112">Reference</span></span>

[<span data-ttu-id="f3c8f-113">Miembros de JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="f3c8f-113">JET_BKINFO members</span></span>](./jet-bkinfo-members.md)

[<span data-ttu-id="f3c8f-114">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f3c8f-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
