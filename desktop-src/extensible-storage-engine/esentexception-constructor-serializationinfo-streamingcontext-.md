---
description: 'Más información acerca de: constructor EsentException (SerializationInfo, StreamingContext)'
title: Constructor EsentException (SerializationInfo, StreamingContext) (Microsoft. ISAM. esent)
TOCTitle: EsentException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100719
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bdcfe5c3b37746f50926850b45763f9d70de893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707474"
---
# <a name="esentexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="49743-103">Constructor EsentException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="49743-103">EsentException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="49743-104">Inicializa una nueva instancia de la clase EsentException.</span><span class="sxs-lookup"><span data-stu-id="49743-104">Initializes a new instance of the EsentException class.</span></span> <span data-ttu-id="49743-105">Este constructor se utiliza para deserializar una excepción serializada.</span><span class="sxs-lookup"><span data-stu-id="49743-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="49743-106">**Espacio de nombres:**  [Microsoft. ISAM. esent](./microsoft.isam.esent-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="49743-106">**Namespace:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)</span></span>  
<span data-ttu-id="49743-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="49743-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="49743-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49743-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentException(info, context)
```

``` csharp
protected EsentException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="49743-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49743-109">Parameters</span></span>

  - <span data-ttu-id="49743-110">info</span><span class="sxs-lookup"><span data-stu-id="49743-110">info</span></span>  
    <span data-ttu-id="49743-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="49743-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="49743-112">Los datos necesarios para deserializar el objeto.</span><span class="sxs-lookup"><span data-stu-id="49743-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="49743-113">context</span><span class="sxs-lookup"><span data-stu-id="49743-113">context</span></span>  
    <span data-ttu-id="49743-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="49743-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="49743-115">Contexto de la deserialización.</span><span class="sxs-lookup"><span data-stu-id="49743-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="49743-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="49743-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="49743-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="49743-117">Reference</span></span>

[<span data-ttu-id="49743-118">Clase EsentException</span><span class="sxs-lookup"><span data-stu-id="49743-118">EsentException class</span></span>](./esentexception-class.md)

[<span data-ttu-id="49743-119">Miembros de EsentException</span><span class="sxs-lookup"><span data-stu-id="49743-119">EsentException members</span></span>](./esentexception-members.md)

[<span data-ttu-id="49743-120">Sobrecarga EsentException</span><span class="sxs-lookup"><span data-stu-id="49743-120">EsentException overload</span></span>](./esentexception-constructor.md)

[<span data-ttu-id="49743-121">Espacio de nombres Microsoft. ISAM. esent</span><span class="sxs-lookup"><span data-stu-id="49743-121">Microsoft.Isam.Esent namespace</span></span>](./microsoft.isam.esent-namespace.md)
