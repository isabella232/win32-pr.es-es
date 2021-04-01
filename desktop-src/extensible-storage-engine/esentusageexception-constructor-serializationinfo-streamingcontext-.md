---
description: 'Más información acerca de: constructor EsentUsageException (SerializationInfo, StreamingContext)'
title: Constructor EsentUsageException (SerializationInfo, StreamingContext)
TOCTitle: EsentUsageException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentUsageException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentusageexception.esentusageexception(v=EXCHG.10)
ms:contentKeyID: 55103026
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentUsageException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46100a5f359616b18e5eae0d7b9d9a04b0c2fc25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819139"
---
# <a name="esentusageexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="d0fa4-103">Constructor EsentUsageException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="d0fa4-103">EsentUsageException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="d0fa4-104">Inicializa una nueva instancia de la clase EsentUsageException.</span><span class="sxs-lookup"><span data-stu-id="d0fa4-104">Initializes a new instance of the EsentUsageException class.</span></span> <span data-ttu-id="d0fa4-105">Este constructor se utiliza para deserializar una excepción serializada.</span><span class="sxs-lookup"><span data-stu-id="d0fa4-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="d0fa4-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d0fa4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d0fa4-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d0fa4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d0fa4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0fa4-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentUsageException(info, context)
```

``` csharp
protected EsentUsageException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="d0fa4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0fa4-109">Parameters</span></span>

  - <span data-ttu-id="d0fa4-110">info</span><span class="sxs-lookup"><span data-stu-id="d0fa4-110">info</span></span>  
    <span data-ttu-id="d0fa4-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="d0fa4-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="d0fa4-112">Los datos necesarios para deserializar el objeto.</span><span class="sxs-lookup"><span data-stu-id="d0fa4-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="d0fa4-113">context</span><span class="sxs-lookup"><span data-stu-id="d0fa4-113">context</span></span>  
    <span data-ttu-id="d0fa4-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="d0fa4-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="d0fa4-115">Contexto de la deserialización.</span><span class="sxs-lookup"><span data-stu-id="d0fa4-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0fa4-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0fa4-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d0fa4-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="d0fa4-117">Reference</span></span>

[<span data-ttu-id="d0fa4-118">Clase EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="d0fa4-118">EsentUsageException class</span></span>](./esentusageexception-class.md)

[<span data-ttu-id="d0fa4-119">Miembros de EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="d0fa4-119">EsentUsageException members</span></span>](./esentusageexception-members.md)

[<span data-ttu-id="d0fa4-120">Sobrecarga EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="d0fa4-120">EsentUsageException overload</span></span>](./esentusageexception-constructor.md)

[<span data-ttu-id="d0fa4-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d0fa4-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
