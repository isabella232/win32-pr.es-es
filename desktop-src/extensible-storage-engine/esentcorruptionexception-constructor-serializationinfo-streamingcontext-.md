---
description: 'Más información acerca de: constructor EsentCorruptionException (SerializationInfo, StreamingContext)'
title: Constructor EsentCorruptionException (SerializationInfo, StreamingContext)
TOCTitle: EsentCorruptionException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentCorruptionException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101038
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a0e80255d86ed6f953e4010541e98b794537f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002995"
---
# <a name="esentcorruptionexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="2263f-103">Constructor EsentCorruptionException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="2263f-103">EsentCorruptionException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="2263f-104">Inicializa una nueva instancia de la clase EsentCorruptionException.</span><span class="sxs-lookup"><span data-stu-id="2263f-104">Initializes a new instance of the EsentCorruptionException class.</span></span> <span data-ttu-id="2263f-105">Este constructor se utiliza para deserializar una excepción serializada.</span><span class="sxs-lookup"><span data-stu-id="2263f-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="2263f-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2263f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2263f-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2263f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2263f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2263f-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentCorruptionException(info, context)
```

``` csharp
protected EsentCorruptionException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="2263f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2263f-109">Parameters</span></span>

  - <span data-ttu-id="2263f-110">info</span><span class="sxs-lookup"><span data-stu-id="2263f-110">info</span></span>  
    <span data-ttu-id="2263f-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="2263f-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="2263f-112">Los datos necesarios para deserializar el objeto.</span><span class="sxs-lookup"><span data-stu-id="2263f-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="2263f-113">context</span><span class="sxs-lookup"><span data-stu-id="2263f-113">context</span></span>  
    <span data-ttu-id="2263f-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="2263f-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="2263f-115">Contexto de la deserialización.</span><span class="sxs-lookup"><span data-stu-id="2263f-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="2263f-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="2263f-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2263f-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="2263f-117">Reference</span></span>

[<span data-ttu-id="2263f-118">Clase EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="2263f-118">EsentCorruptionException class</span></span>](./esentcorruptionexception-class.md)

[<span data-ttu-id="2263f-119">Miembros de EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="2263f-119">EsentCorruptionException members</span></span>](./esentcorruptionexception-members.md)

[<span data-ttu-id="2263f-120">Sobrecarga EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="2263f-120">EsentCorruptionException overload</span></span>](./esentcorruptionexception-constructor.md)

[<span data-ttu-id="2263f-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2263f-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
