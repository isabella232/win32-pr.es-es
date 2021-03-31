---
description: 'Más información acerca de: constructor EsentStateException (SerializationInfo, StreamingContext)'
title: Constructor EsentStateException (SerializationInfo, StreamingContext)
TOCTitle: EsentStateException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentStateException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102710
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 458efcde030559122085824a99660c3d5d7fc4c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361038"
---
# <a name="esentstateexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="52829-103">Constructor EsentStateException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="52829-103">EsentStateException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="52829-104">Inicializa una nueva instancia de la clase EsentStateException.</span><span class="sxs-lookup"><span data-stu-id="52829-104">Initializes a new instance of the EsentStateException class.</span></span> <span data-ttu-id="52829-105">Este constructor se utiliza para deserializar una excepción serializada.</span><span class="sxs-lookup"><span data-stu-id="52829-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="52829-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="52829-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="52829-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="52829-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="52829-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52829-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentStateException(info, context)
```

``` csharp
protected EsentStateException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="52829-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52829-109">Parameters</span></span>

  - <span data-ttu-id="52829-110">info</span><span class="sxs-lookup"><span data-stu-id="52829-110">info</span></span>  
    <span data-ttu-id="52829-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="52829-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="52829-112">Los datos necesarios para deserializar el objeto.</span><span class="sxs-lookup"><span data-stu-id="52829-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="52829-113">context</span><span class="sxs-lookup"><span data-stu-id="52829-113">context</span></span>  
    <span data-ttu-id="52829-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="52829-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="52829-115">Contexto de la deserialización.</span><span class="sxs-lookup"><span data-stu-id="52829-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="52829-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="52829-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="52829-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="52829-117">Reference</span></span>

[<span data-ttu-id="52829-118">Clase EsentStateException</span><span class="sxs-lookup"><span data-stu-id="52829-118">EsentStateException class</span></span>](./esentstateexception-class.md)

[<span data-ttu-id="52829-119">Miembros de EsentStateException</span><span class="sxs-lookup"><span data-stu-id="52829-119">EsentStateException members</span></span>](./esentstateexception-members.md)

[<span data-ttu-id="52829-120">Sobrecarga EsentStateException</span><span class="sxs-lookup"><span data-stu-id="52829-120">EsentStateException overload</span></span>](./esentstateexception-constructor.md)

[<span data-ttu-id="52829-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="52829-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
