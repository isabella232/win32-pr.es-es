---
description: 'Más información sobre: EsentResource. Dispose (método, Boolean)'
title: EsentResource. Dispose (método, Boolean)
TOCTitle: Dispose method (Boolean)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResource.Dispose(System.Boolean)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource.dispose(v=EXCHG.10)
ms:contentKeyID: 55102624
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource.Dispose
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf74291bf4c54ffa1d61c28bf7caff1e8c2b231b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279433"
---
# <a name="esentresourcedispose-method-boolean"></a><span data-ttu-id="19e63-103">EsentResource. Dispose (método, Boolean)</span><span class="sxs-lookup"><span data-stu-id="19e63-103">EsentResource.Dispose method (Boolean)</span></span>

<span data-ttu-id="19e63-104">Lo llama Dispose y el finalizador.</span><span class="sxs-lookup"><span data-stu-id="19e63-104">Called by Dispose and the finalizer.</span></span>

<span data-ttu-id="19e63-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="19e63-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="19e63-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="19e63-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="19e63-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19e63-107">Syntax</span></span>

``` vb
'Declaration
Protected Overridable Sub Dispose ( _
    isDisposing As Boolean _
)
'Usage
Dim isDisposing As Boolean

Me.Dispose(isDisposing)
```

``` csharp
protected virtual void Dispose(
    bool isDisposing
)
```

#### <a name="parameters"></a><span data-ttu-id="19e63-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19e63-108">Parameters</span></span>

  - <span data-ttu-id="19e63-109">isDisposing</span><span class="sxs-lookup"><span data-stu-id="19e63-109">isDisposing</span></span>  
    <span data-ttu-id="19e63-110">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="19e63-110">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
    
    <span data-ttu-id="19e63-111">True si se llama desde Dispose.</span><span class="sxs-lookup"><span data-stu-id="19e63-111">True if called from Dispose.</span></span>

## <a name="see-also"></a><span data-ttu-id="19e63-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="19e63-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="19e63-113">Referencia</span><span class="sxs-lookup"><span data-stu-id="19e63-113">Reference</span></span>

[<span data-ttu-id="19e63-114">Clase EsentResource</span><span class="sxs-lookup"><span data-stu-id="19e63-114">EsentResource class</span></span>](./esentresource-class.md)

[<span data-ttu-id="19e63-115">Miembros de EsentResource</span><span class="sxs-lookup"><span data-stu-id="19e63-115">EsentResource members</span></span>](./esentresource-members.md)

[<span data-ttu-id="19e63-116">Eliminar sobrecarga</span><span class="sxs-lookup"><span data-stu-id="19e63-116">Dispose overload</span></span>](./esentresource.dispose-method.md)

[<span data-ttu-id="19e63-117">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="19e63-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
