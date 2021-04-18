---
description: 'Más información acerca de: estructura de JET_SIGNATURE'
title: Estructura de JET_SIGNATURE
TOCTitle: JET_SIGNATURE structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SIGNATURE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature(v=EXCHG.10)
ms:contentKeyID: 39511048
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f5c8ce12b23194aea2a45c273e0207f88faad6f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705755"
---
# <a name="jet_signature-structure"></a><span data-ttu-id="4d938-103">Estructura de JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="4d938-103">JET_SIGNATURE structure</span></span>

<span data-ttu-id="4d938-104">La estructura JET_SIGNATURE contiene información que identifica de forma única una secuencia de archivo o de base de datos.</span><span class="sxs-lookup"><span data-stu-id="4d938-104">The JET_SIGNATURE structure contains information that uniquely identifies a database or logfile sequence.</span></span>

<span data-ttu-id="4d938-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4d938-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4d938-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4d938-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4d938-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d938-107">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_SIGNATURE _
    Implements IEquatable(Of JET_SIGNATURE)
'Usage
Dim instance As JET_SIGNATURE
```

``` csharp
[SerializableAttribute]
public struct JET_SIGNATURE : IEquatable<JET_SIGNATURE>
```

## <a name="thread-safety"></a><span data-ttu-id="4d938-108">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="4d938-108">Thread safety</span></span>

<span data-ttu-id="4d938-109">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="4d938-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4d938-110">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="4d938-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4d938-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d938-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4d938-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="4d938-112">Reference</span></span>

[<span data-ttu-id="4d938-113">Miembros de JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="4d938-113">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="4d938-114">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4d938-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
