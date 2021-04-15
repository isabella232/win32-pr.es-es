---
description: 'Más información sobre: CimMofDeserializer. DeserializeClasses (método) (Byte [], UInt32, IEnumerable <CimClass> )'
title: Método CimMofDeserializer. DeserializeClasses (Byte [], UInt32, IEnumerable (CimClass)) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32, IEnumerable(CimClass)) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass})
ms.date: 11/13/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: edcdb84e9c3a3fe7a070263385c9ee6551341152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720710"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass"></a><span data-ttu-id="10f78-103">Método CimMofDeserializer. DeserializeClasses (byte \[ \] , UInt32, IEnumerable \<CimClass\> )</span><span class="sxs-lookup"><span data-stu-id="10f78-103">CimMofDeserializer.DeserializeClasses method (Byte\[\], UInt32, IEnumerable\<CimClass\>)</span></span>

<span data-ttu-id="10f78-104">Deserializa clases CIM basadas en datos serializados y una colección de clases CIM primarias.</span><span class="sxs-lookup"><span data-stu-id="10f78-104">Deserializes CIM classes based on serialized data, and a collection of parent CIM classes.</span></span>

<span data-ttu-id="10f78-105">**Espacio de nombres:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10f78-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="10f78-106">**Ensamblado:**  Microsoft. Management. Infrastructure (en Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="10f78-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="10f78-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10f78-107">Syntax</span></span>

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> classes
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ classes
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref *
        classes:IEnumerable<CimClass> -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger,
    classes As IEnumerable(Of CimClass)
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a><span data-ttu-id="10f78-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10f78-108">Parameters</span></span>

  - <span data-ttu-id="10f78-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="10f78-109">serializedData</span></span>  
    <span data-ttu-id="10f78-110">Tipo: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="10f78-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="10f78-111">Búfer que contiene los datos serializados.</span><span class="sxs-lookup"><span data-stu-id="10f78-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="10f78-112">offset</span><span class="sxs-lookup"><span data-stu-id="10f78-112">offset</span></span>  
    <span data-ttu-id="10f78-113">Tipo: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="10f78-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="10f78-114">Desplazamiento en bytes de la ubicación en la que se va a empezar a leer los datos.</span><span class="sxs-lookup"><span data-stu-id="10f78-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="10f78-115">Cuando el método devuelve, el desplazamiento apuntará al siguiente byte después de las clases deserializadas.</span><span class="sxs-lookup"><span data-stu-id="10f78-115">When the method returns, the offset will be pointing to the next byte after the deserialized classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="10f78-116">clases</span><span class="sxs-lookup"><span data-stu-id="10f78-116">classes</span></span>  
    <span data-ttu-id="10f78-117">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="10f78-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>
    
    <span data-ttu-id="10f78-118">Una memoria caché opcional de clases CIM principales.</span><span class="sxs-lookup"><span data-stu-id="10f78-118">An optional cache of parent CIM classes.</span></span>

#### <a name="return-value"></a><span data-ttu-id="10f78-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10f78-119">Return value</span></span>

<span data-ttu-id="10f78-120">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="10f78-120">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>

<span data-ttu-id="10f78-121">Interfaz [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) que se puede utilizar para enumerar las clases CIM.</span><span class="sxs-lookup"><span data-stu-id="10f78-121">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="10f78-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="10f78-122">See also</span></span>

<span data-ttu-id="10f78-123">[Clase CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10f78-123">[CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>  
<span data-ttu-id="10f78-124">[Espacio de nombres Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10f78-124">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
