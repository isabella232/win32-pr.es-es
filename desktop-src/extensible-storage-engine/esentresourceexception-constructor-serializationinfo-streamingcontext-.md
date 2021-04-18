---
description: 'Más información acerca de: constructor EsentResourceException (SerializationInfo, StreamingContext)'
title: Constructor EsentResourceException (SerializationInfo, StreamingContext)
TOCTitle: EsentResourceException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResourceException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresourceexception.esentresourceexception(v=EXCHG.10)
ms:contentKeyID: 55102649
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResourceException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4f7b52e211d155b92a9917670682af735eedf9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717257"
---
# <a name="esentresourceexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="b70e0-103">Constructor EsentResourceException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="b70e0-103">EsentResourceException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="b70e0-104">Inicializa una nueva instancia de la clase EsentResourceException.</span><span class="sxs-lookup"><span data-stu-id="b70e0-104">Initializes a new instance of the EsentResourceException class.</span></span> <span data-ttu-id="b70e0-105">Este constructor se utiliza para deserializar una excepción serializada.</span><span class="sxs-lookup"><span data-stu-id="b70e0-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="b70e0-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b70e0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b70e0-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b70e0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b70e0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b70e0-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentResourceException(info, context)
```

``` csharp
protected EsentResourceException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="b70e0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b70e0-109">Parameters</span></span>

  - <span data-ttu-id="b70e0-110">info</span><span class="sxs-lookup"><span data-stu-id="b70e0-110">info</span></span>  
    <span data-ttu-id="b70e0-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="b70e0-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="b70e0-112">Los datos necesarios para deserializar el objeto.</span><span class="sxs-lookup"><span data-stu-id="b70e0-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="b70e0-113">context</span><span class="sxs-lookup"><span data-stu-id="b70e0-113">context</span></span>  
    <span data-ttu-id="b70e0-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="b70e0-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="b70e0-115">Contexto de la deserialización.</span><span class="sxs-lookup"><span data-stu-id="b70e0-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="b70e0-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="b70e0-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b70e0-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="b70e0-117">Reference</span></span>

[<span data-ttu-id="b70e0-118">Clase EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="b70e0-118">EsentResourceException class</span></span>](./esentresourceexception-class.md)

[<span data-ttu-id="b70e0-119">Miembros de EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="b70e0-119">EsentResourceException members</span></span>](./esentresourceexception-members.md)

[<span data-ttu-id="b70e0-120">Sobrecarga EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="b70e0-120">EsentResourceException overload</span></span>](./esentresourceexception-constructor.md)

[<span data-ttu-id="b70e0-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b70e0-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
