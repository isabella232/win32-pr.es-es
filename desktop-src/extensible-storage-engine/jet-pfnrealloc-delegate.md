---
description: 'Más información acerca de: JET_PFNREALLOC delegado'
title: JET_PFNREALLOC delegado
TOCTitle: JET_PFNREALLOC delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnrealloc(v=EXCHG.10)
ms:contentKeyID: 39515764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aab9fef2d7a449c877f88d2ed77aa19cbb2409d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003079"
---
# <a name="jet_pfnrealloc-delegate"></a><span data-ttu-id="29389-103">JET_PFNREALLOC delegado</span><span class="sxs-lookup"><span data-stu-id="29389-103">JET_PFNREALLOC delegate</span></span>

<span data-ttu-id="29389-104">Devolución de llamada usada por JetEnumerateColumns para asignar memoria para sus búferes de salida.</span><span class="sxs-lookup"><span data-stu-id="29389-104">Callback used by JetEnumerateColumns to allocate memory for its output buffers.</span></span>

<span data-ttu-id="29389-105">Esta API no es conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="29389-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="29389-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="29389-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="29389-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="29389-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="29389-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29389-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Delegate Function JET_PFNREALLOC ( _
    context As IntPtr, _
    memory As IntPtr, _
    requestedSize As UInteger _
) As IntPtr
'Usage
Dim instance As New JET_PFNREALLOC(AddressOf HandlerMethod)
```

``` csharp
[CLSCompliantAttribute(false)]
public delegate IntPtr JET_PFNREALLOC(
    IntPtr context,
    IntPtr memory,
    uint requestedSize
)
```

#### <a name="parameters"></a><span data-ttu-id="29389-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29389-109">Parameters</span></span>

  - <span data-ttu-id="29389-110">context</span><span class="sxs-lookup"><span data-stu-id="29389-110">context</span></span>  
    <span data-ttu-id="29389-111">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="29389-111">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="29389-112">Contexto dado a JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="29389-112">Context given to JetEnumerateColumns.</span></span>

<!-- end list -->

  - <span data-ttu-id="29389-113">memoria</span><span class="sxs-lookup"><span data-stu-id="29389-113">memory</span></span>  
    <span data-ttu-id="29389-114">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="29389-114">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="29389-115">Si es distinto de cero, puntero a un bloque de memoria asignado previamente por esta devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="29389-115">If non-zero, a pointer to a memory block previously allocated by this callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="29389-116">requestedSize</span><span class="sxs-lookup"><span data-stu-id="29389-116">requestedSize</span></span>  
    <span data-ttu-id="29389-117">Tipo: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="29389-117">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="29389-118">Nuevo tamaño del bloque de memoria (en bytes).</span><span class="sxs-lookup"><span data-stu-id="29389-118">The new size of the memory block (in bytes).</span></span> <span data-ttu-id="29389-119">Si es 0 y se especifica un bloque de memoria, el bloque de memoria se liberará.</span><span class="sxs-lookup"><span data-stu-id="29389-119">If this is 0 and a memory block is specified, that memory block will be freed.</span></span>

#### <a name="return-value"></a><span data-ttu-id="29389-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29389-120">Return value</span></span>

<span data-ttu-id="29389-121">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="29389-121">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
<span data-ttu-id="29389-122">Puntero a la memoria recién asignada.</span><span class="sxs-lookup"><span data-stu-id="29389-122">A pointer to newly allocated memory.</span></span> <span data-ttu-id="29389-123">Si no se pudo asignar memoria, se debe devolver [cero](/dotnet/api/system.intptr.zero) .</span><span class="sxs-lookup"><span data-stu-id="29389-123">If memory could not be allocated then [Zero](/dotnet/api/system.intptr.zero) should be returned.</span></span>  

## <a name="see-also"></a><span data-ttu-id="29389-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="29389-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="29389-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="29389-125">Reference</span></span>

[<span data-ttu-id="29389-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="29389-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
