---
description: 'Más información sobre: API. JetFreeBuffer (método)'
title: Método API. JetFreeBuffer
TOCTitle: 'JetFreeBuffer method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer(System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetfreebuffer(v=EXCHG.10)
ms:contentKeyID: 55100694
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a584caf0f7c59c77e7d3c4a058a03780043e0f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720346"
---
# <a name="apijetfreebuffer-method"></a><span data-ttu-id="d5b98-103">Método API. JetFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d5b98-103">Api.JetFreeBuffer method</span></span>

<span data-ttu-id="d5b98-104">Libera memoria asignada por una llamada del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="d5b98-104">Frees memory that was allocated by a database engine call.</span></span>

<span data-ttu-id="d5b98-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d5b98-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d5b98-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d5b98-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d5b98-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5b98-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetFreeBuffer ( _
    buffer As IntPtr _
)
'Usage
Dim buffer As IntPtrApi.JetFreeBuffer(buffer)
```

``` csharp
public static void JetFreeBuffer(
    IntPtr buffer
)
```

#### <a name="parameters"></a><span data-ttu-id="d5b98-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5b98-108">Parameters</span></span>

  - <span data-ttu-id="d5b98-109">buffer</span><span class="sxs-lookup"><span data-stu-id="d5b98-109">buffer</span></span>  
    <span data-ttu-id="d5b98-110">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="d5b98-110">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="d5b98-111">Búfer asignado por una llamada al motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="d5b98-111">The buffer allocated by a call to the database engine.</span></span> <span data-ttu-id="d5b98-112">[Cero](/dotnet/api/system.intptr.zero) es aceptable y se omitirá.</span><span class="sxs-lookup"><span data-stu-id="d5b98-112">[Zero](/dotnet/api/system.intptr.zero) is acceptable, and will be ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5b98-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5b98-113">Remarks</span></span>

<span data-ttu-id="d5b98-114">Este método es interno porque nunca exponemos la memoria asignada por ESENT a los llamadores.</span><span class="sxs-lookup"><span data-stu-id="d5b98-114">This method is internal because we never expose the memory allocated by ESENT to our callers.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5b98-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5b98-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d5b98-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="d5b98-116">Reference</span></span>

[<span data-ttu-id="d5b98-117">Clase de API</span><span class="sxs-lookup"><span data-stu-id="d5b98-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d5b98-118">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="d5b98-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d5b98-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d5b98-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
