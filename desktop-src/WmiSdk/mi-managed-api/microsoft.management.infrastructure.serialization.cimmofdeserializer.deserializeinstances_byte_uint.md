---
description: 'Más información sobre: CimMofDeserializer. DeserializeInstances (método) (Byte [], UInt32)'
title: CimMofDeserializer. DeserializeInstances (método) (Byte [], UInt32) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeInstances method (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances(System.Byte[],System.UInt32@)
ms.date: 11/14/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 90cc4f9d88afa9f4ec566ff4733995bce8160eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539774"
---
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32"></a><span data-ttu-id="c6747-103">Método CimMofDeserializer. DeserializeInstances (byte \[ \] , UInt32)</span><span class="sxs-lookup"><span data-stu-id="c6747-103">CimMofDeserializer.DeserializeInstances method (Byte\[\], UInt32)</span></span>

<span data-ttu-id="c6747-104">Deserializa las instancias CIM basadas en datos serializados.</span><span class="sxs-lookup"><span data-stu-id="c6747-104">Deserializes CIM instances based on serialized data.</span></span>

<span data-ttu-id="c6747-105">**Espacio de nombres:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6747-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="c6747-106">**Ensamblado:**  Microsoft. Management. Infrastructure (en Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="c6747-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="c6747-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6747-107">Syntax</span></span>

``` csharp
public IEnumerable<CimInstance> DeserializeInstances(
    byte[] serializedData,
    ref uint offset
)
```

``` c++
public:
IEnumerable<CimInstance^>^ DeserializeInstances(
    array<unsigned char>^ serializedData,
    unsigned int% offset
)
```

``` fsharp
member DeserializeInstances : 
        serializedData:byte[] *
        offset:uint32 byref -> IEnumerable<CimInstance>
```

``` vb
Public Function DeserializeInstances (
    serializedData As Byte(),
    ByRef offset As UInteger
) As IEnumerable(CimInstance)
```

#### <a name="parameters"></a><span data-ttu-id="c6747-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6747-108">Parameters</span></span>

  - <span data-ttu-id="c6747-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="c6747-109">serializedData</span></span>  
    <span data-ttu-id="c6747-110">Tipo: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="c6747-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="c6747-111">Búfer que contiene los datos serializados.</span><span class="sxs-lookup"><span data-stu-id="c6747-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="c6747-112">offset</span><span class="sxs-lookup"><span data-stu-id="c6747-112">offset</span></span>  
    <span data-ttu-id="c6747-113">Tipo: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="c6747-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="c6747-114">Desplazamiento en bytes de la ubicación en la que se va a empezar a leer los datos.</span><span class="sxs-lookup"><span data-stu-id="c6747-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="c6747-115">Cuando el método devuelve, el desplazamiento apuntará al siguiente byte después de las instancias deserializadas.</span><span class="sxs-lookup"><span data-stu-id="c6747-115">When the method returns, the offset will be pointing to the next byte after the deserialized instances.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c6747-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6747-116">Return value</span></span>

<span data-ttu-id="c6747-117">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="c6747-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span></span>

<span data-ttu-id="c6747-118">Interfaz [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) que se puede utilizar para enumerar las clases CIM.</span><span class="sxs-lookup"><span data-stu-id="c6747-118">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6747-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6747-119">See also</span></span>

<span data-ttu-id="c6747-120">[Clase CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6747-120">[CimInstance class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span></span>  
<span data-ttu-id="c6747-121">[Espacio de nombres Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6747-121">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
