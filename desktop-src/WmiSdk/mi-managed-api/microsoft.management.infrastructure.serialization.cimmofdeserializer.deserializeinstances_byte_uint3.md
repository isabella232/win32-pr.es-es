---
description: 'Más información sobre: CimMofDeserializer. DeserializeInstances (método) (Byte [], UInt32, IEnumerable <CimClass> , OnClassNeeded, GetIncludedFileContent)'
title: Método CimMofDeserializer. DeserializeInstances (Byte [], UInt32, IEnumerable (CimClass), OnClassNeeded, GetIncludedFileContent) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeInstances method (Byte[], UInt32, IEnumerable(CimClass), OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass},Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
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
ms.openlocfilehash: 081c6d028abdb341d75ff57758c703458fd0b62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720303"
---
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32ienumerablecimclass-onclassneeded-getincludedfilecontent"></a><span data-ttu-id="a9a74-103">Método CimMofDeserializer. DeserializeInstances (byte \[ \] , UInt32, IEnumerable \<CimClass\> , OnClassNeeded, GetIncludedFileContent)</span><span class="sxs-lookup"><span data-stu-id="a9a74-103">CimMofDeserializer.DeserializeInstances method (Byte\[\], UInt32, IEnumerable\<CimClass\>, OnClassNeeded, GetIncludedFileContent)</span></span>

<span data-ttu-id="a9a74-104">Deserializa las instancias CIM basadas en datos serializados, una colección de clases CIM principales y devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="a9a74-104">Deserializes CIM instances based on serialized data, a collection of parent CIM classes, and callbacks.</span></span>

<span data-ttu-id="a9a74-105">**Espacio de nombres:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a9a74-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="a9a74-106">**Ensamblado:**  Microsoft. Management. Infrastructure (en Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="a9a74-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="a9a74-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9a74-107">Syntax</span></span>

``` csharp
public IEnumerable<CimInstance> DeserializeInstances(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> cimClasses,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimInstance^>^ DeserializeInstances(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ cimClasses,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeInstances : 
        serializedData:byte[] *
        offset:uint32 byref *
        cimClasses:IEnumerable<CimClass> *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimInstance>
```

``` vb
Public Function DeserializeInstances (
    serializedData As Byte(),
    ByRef offset As UInteger,
    cimClasses As IEnumerable(Of CimClass),
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
) As IEnumerable(CimInstance)
```

#### <a name="parameters"></a><span data-ttu-id="a9a74-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9a74-108">Parameters</span></span>

  - <span data-ttu-id="a9a74-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="a9a74-109">serializedData</span></span>  
    <span data-ttu-id="a9a74-110">Tipo: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="a9a74-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="a9a74-111">Búfer que contiene los datos serializados.</span><span class="sxs-lookup"><span data-stu-id="a9a74-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="a9a74-112">offset</span><span class="sxs-lookup"><span data-stu-id="a9a74-112">offset</span></span>  
    <span data-ttu-id="a9a74-113">Tipo: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="a9a74-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="a9a74-114">Desplazamiento en bytes de la ubicación en la que se va a empezar a leer los datos.</span><span class="sxs-lookup"><span data-stu-id="a9a74-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="a9a74-115">Cuando el método devuelve, el desplazamiento apuntará al siguiente byte después de las instancias deserializadas.</span><span class="sxs-lookup"><span data-stu-id="a9a74-115">When the method returns, the offset will be pointing to the next byte after the deserialized instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="a9a74-116">cimClasses</span><span class="sxs-lookup"><span data-stu-id="a9a74-116">cimClasses</span></span>  
    <span data-ttu-id="a9a74-117">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="a9a74-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>
    
    <span data-ttu-id="a9a74-118">Una memoria caché opcional de clases CIM principales.</span><span class="sxs-lookup"><span data-stu-id="a9a74-118">An optional cache of parent CIM classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="a9a74-119">onClassNeededCallback</span><span class="sxs-lookup"><span data-stu-id="a9a74-119">onClassNeededCallback</span></span>  
    <span data-ttu-id="a9a74-120">Tipo: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span><span class="sxs-lookup"><span data-stu-id="a9a74-120">Type: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span></span>
    
    <span data-ttu-id="a9a74-121">Función de devolución de llamada que se usa para proporcionar un objeto de clase solicitado durante la deserialización.</span><span class="sxs-lookup"><span data-stu-id="a9a74-121">A callback function used to provide a requested class object during deserialization.</span></span>

<!-- end list -->

  - <span data-ttu-id="a9a74-122">getIncludedFileCallback</span><span class="sxs-lookup"><span data-stu-id="a9a74-122">getIncludedFileCallback</span></span>  
    <span data-ttu-id="a9a74-123">Tipo: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span><span class="sxs-lookup"><span data-stu-id="a9a74-123">Type: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span></span>
    
    <span data-ttu-id="a9a74-124">Función de devolución de llamada que se usa para proporcionar el contenido del búfer de archivos de un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="a9a74-124">A callback function used to provide the file buffer contents of a specified file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a9a74-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9a74-125">Return value</span></span>

<span data-ttu-id="a9a74-126">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="a9a74-126">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span></span>

<span data-ttu-id="a9a74-127">Interfaz [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) que se puede utilizar para enumerar las clases CIM.</span><span class="sxs-lookup"><span data-stu-id="a9a74-127">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="a9a74-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9a74-128">See also</span></span>

<span data-ttu-id="a9a74-129">[Clase CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a9a74-129">[CimInstance class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span></span>  
<span data-ttu-id="a9a74-130">[Espacio de nombres Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a9a74-130">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
