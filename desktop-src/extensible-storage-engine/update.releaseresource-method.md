---
description: 'Más información sobre: método Update. ReleaseResource'
title: Método Update. ReleaseResource
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104200
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update.ReleaseResource
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72a17022ff91f278b6a5ac4f84fc7e2d70bb04bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696586"
---
# <a name="updatereleaseresource-method"></a><span data-ttu-id="36a86-103">Método Update. ReleaseResource</span><span class="sxs-lookup"><span data-stu-id="36a86-103">Update.ReleaseResource method</span></span>

<span data-ttu-id="36a86-104">Se llama cuando la transacción se desecha mientras está activa.</span><span class="sxs-lookup"><span data-stu-id="36a86-104">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="36a86-105">Esto debería revertir la transacción.</span><span class="sxs-lookup"><span data-stu-id="36a86-105">This should rollback the transaction.</span></span>

<span data-ttu-id="36a86-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="36a86-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="36a86-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="36a86-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="36a86-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36a86-108">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="see-also"></a><span data-ttu-id="36a86-109">Consulte también</span><span class="sxs-lookup"><span data-stu-id="36a86-109">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="36a86-110">Referencia</span><span class="sxs-lookup"><span data-stu-id="36a86-110">Reference</span></span>

[<span data-ttu-id="36a86-111">Update (clase)</span><span class="sxs-lookup"><span data-stu-id="36a86-111">Update class</span></span>](./update-class.md)

[<span data-ttu-id="36a86-112">Actualizar miembros</span><span class="sxs-lookup"><span data-stu-id="36a86-112">Update members</span></span>](./update-members.md)

[<span data-ttu-id="36a86-113">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="36a86-113">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
