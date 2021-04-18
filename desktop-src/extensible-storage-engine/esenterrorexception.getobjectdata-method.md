---
description: 'Más información sobre: EsentErrorException. GetObjectData (método)'
title: EsentErrorException. GetObjectData (método)
TOCTitle: 'GetObjectData method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.getobjectdata(v=EXCHG.10)
ms:contentKeyID: 55101432
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86d951828da0f8bb8eb3ada13bb67b02e801709e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707391"
---
# <a name="esenterrorexceptiongetobjectdata-method"></a><span data-ttu-id="75a82-103">EsentErrorException. GetObjectData (método)</span><span class="sxs-lookup"><span data-stu-id="75a82-103">EsentErrorException.GetObjectData method</span></span>

<span data-ttu-id="75a82-104">Cuando se reemplaza en una clase derivada, establece [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) con información sobre la excepción.</span><span class="sxs-lookup"><span data-stu-id="75a82-104">When overridden in a derived class, sets the [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) with information about the exception.</span></span>

<span data-ttu-id="75a82-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="75a82-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="75a82-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="75a82-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="75a82-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75a82-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Sub GetObjectData ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim instance As EsentErrorException
Dim info As SerializationInfo
Dim context As StreamingContext

instance.GetObjectData(info, context)
```

``` csharp
public override void GetObjectData(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="75a82-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75a82-108">Parameters</span></span>

  - <span data-ttu-id="75a82-109">info</span><span class="sxs-lookup"><span data-stu-id="75a82-109">info</span></span>  
    <span data-ttu-id="75a82-110">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="75a82-110">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="75a82-111">[SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) que contiene los datos serializados del objeto sobre la excepción que se va a producir.</span><span class="sxs-lookup"><span data-stu-id="75a82-111">The [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) that holds the serialized object data about the exception being thrown.</span></span>

<!-- end list -->

  - <span data-ttu-id="75a82-112">context</span><span class="sxs-lookup"><span data-stu-id="75a82-112">context</span></span>  
    <span data-ttu-id="75a82-113">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="75a82-113">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="75a82-114">[StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext) que contiene información contextual sobre el origen o el destino.</span><span class="sxs-lookup"><span data-stu-id="75a82-114">The [StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext) that contains contextual information about the source or destination.</span></span>

#### <a name="implements"></a><span data-ttu-id="75a82-115">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="75a82-115">Implements</span></span>

[<span data-ttu-id="75a82-116">ISerializable. GetObjectData (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="75a82-116">ISerializable.GetObjectData(SerializationInfo, StreamingContext)</span></span>](/dotnet/api/system.runtime.serialization.iserializable.getobjectdata#System_Runtime_Serialization_ISerializable_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  
[<span data-ttu-id="75a82-117">_Exception. GetObjectData (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="75a82-117">_Exception.GetObjectData(SerializationInfo, StreamingContext)</span></span>](/dotnet/api/system.runtime.interopservices._exception.getobjectdata#System_Runtime_InteropServices__Exception_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  

## <a name="exceptions"></a><span data-ttu-id="75a82-118">Excepciones</span><span class="sxs-lookup"><span data-stu-id="75a82-118">Exceptions</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="75a82-119">Excepción</span><span class="sxs-lookup"><span data-stu-id="75a82-119">Exception</span></span></th>
<th><span data-ttu-id="75a82-120">Condición</span><span class="sxs-lookup"><span data-stu-id="75a82-120">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="75a82-121"><a href="/dotnet/api/system.argumentnullexception">ArgumentNullException</a></span><span class="sxs-lookup"><span data-stu-id="75a82-121"><a href="/dotnet/api/system.argumentnullexception">ArgumentNullException</a></span></span></td>
<td><p><span data-ttu-id="75a82-122">El parámetro info es una referencia null (Nothing en Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="75a82-122">The info parameter is a null reference (Nothing in Visual Basic).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="75a82-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="75a82-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="75a82-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="75a82-124">Reference</span></span>

[<span data-ttu-id="75a82-125">Clase EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="75a82-125">EsentErrorException class</span></span>](./esenterrorexception-class.md)

[<span data-ttu-id="75a82-126">Miembros de EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="75a82-126">EsentErrorException members</span></span>](./esenterrorexception-members.md)

[<span data-ttu-id="75a82-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="75a82-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
