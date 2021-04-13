---
description: 'Más información acerca de: constructor EsentOperationException (SerializationInfo, StreamingContext)'
title: Constructor EsentOperationException (SerializationInfo, StreamingContext)
TOCTitle: EsentOperationException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentOperationException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102312
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ee281a47ae8e24ff51ffe5c3d6a4ef4f4b1873e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276474"
---
# <a name="esentoperationexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="34467-103">Constructor EsentOperationException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="34467-103">EsentOperationException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="34467-104">Inicializa una nueva instancia de la clase EsentOperationException.</span><span class="sxs-lookup"><span data-stu-id="34467-104">Initializes a new instance of the EsentOperationException class.</span></span> <span data-ttu-id="34467-105">Este constructor se utiliza para deserializar una excepción serializada.</span><span class="sxs-lookup"><span data-stu-id="34467-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="34467-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="34467-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="34467-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="34467-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="34467-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34467-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentOperationException(info, context)
```

``` csharp
protected EsentOperationException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="34467-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34467-109">Parameters</span></span>

  - <span data-ttu-id="34467-110">info</span><span class="sxs-lookup"><span data-stu-id="34467-110">info</span></span>  
    <span data-ttu-id="34467-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="34467-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="34467-112">Los datos necesarios para deserializar el objeto.</span><span class="sxs-lookup"><span data-stu-id="34467-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="34467-113">context</span><span class="sxs-lookup"><span data-stu-id="34467-113">context</span></span>  
    <span data-ttu-id="34467-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="34467-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="34467-115">Contexto de la deserialización.</span><span class="sxs-lookup"><span data-stu-id="34467-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="34467-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="34467-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="34467-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="34467-117">Reference</span></span>

[<span data-ttu-id="34467-118">Clase EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="34467-118">EsentOperationException class</span></span>](./esentoperationexception-class.md)

[<span data-ttu-id="34467-119">Miembros de EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="34467-119">EsentOperationException members</span></span>](./esentoperationexception-members.md)

[<span data-ttu-id="34467-120">Sobrecarga EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="34467-120">EsentOperationException overload</span></span>](./esentoperationexception-constructor.md)

[<span data-ttu-id="34467-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="34467-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
