---
description: 'Más información acerca de: constructor EsentFatalException (SerializationInfo, StreamingContext)'
title: Constructor EsentFatalException (SerializationInfo, StreamingContext)
TOCTitle: EsentFatalException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFatalException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101554
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2264e3852eb6809f321b9bae162a833e86d7b513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082215"
---
# <a name="esentfatalexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="0080c-103">Constructor EsentFatalException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="0080c-103">EsentFatalException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="0080c-104">Inicializa una nueva instancia de la clase EsentFatalException.</span><span class="sxs-lookup"><span data-stu-id="0080c-104">Initializes a new instance of the EsentFatalException class.</span></span> <span data-ttu-id="0080c-105">Este constructor se utiliza para deserializar una excepción serializada.</span><span class="sxs-lookup"><span data-stu-id="0080c-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="0080c-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0080c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0080c-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0080c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0080c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0080c-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentFatalException(info, context)
```

``` csharp
protected EsentFatalException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="0080c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0080c-109">Parameters</span></span>

  - <span data-ttu-id="0080c-110">info</span><span class="sxs-lookup"><span data-stu-id="0080c-110">info</span></span>  
    <span data-ttu-id="0080c-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="0080c-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="0080c-112">Los datos necesarios para deserializar el objeto.</span><span class="sxs-lookup"><span data-stu-id="0080c-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="0080c-113">context</span><span class="sxs-lookup"><span data-stu-id="0080c-113">context</span></span>  
    <span data-ttu-id="0080c-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="0080c-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="0080c-115">Contexto de la deserialización.</span><span class="sxs-lookup"><span data-stu-id="0080c-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="0080c-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="0080c-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0080c-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="0080c-117">Reference</span></span>

[<span data-ttu-id="0080c-118">Clase EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="0080c-118">EsentFatalException class</span></span>](./esentfatalexception-class.md)

[<span data-ttu-id="0080c-119">Miembros de EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="0080c-119">EsentFatalException members</span></span>](./esentfatalexception-members.md)

[<span data-ttu-id="0080c-120">Sobrecarga EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="0080c-120">EsentFatalException overload</span></span>](./esentfatalexception-constructor.md)

[<span data-ttu-id="0080c-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0080c-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
