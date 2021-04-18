---
description: 'Más información sobre: CimMofDeserializer. DeserializeInstances (método) (Byte [], UInt32, OnClassNeeded, GetIncludedFileContent)'
title: CimMofDeserializer. DeserializeInstances (método) (Byte [], UInt32, OnClassNeeded, GetIncludedFileContent) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeInstances method (Byte[], UInt32, OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances(System.Byte[],System.UInt32@,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
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
ms.openlocfilehash: 17a8a84f841f07439b716909fbc8d63232032263
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720436"
---
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32-onclassneeded-getincludedfilecontent"></a><span data-ttu-id="f5fa3-103">Método CimMofDeserializer. DeserializeInstances (byte \[ \] , UInt32, OnClassNeeded, GetIncludedFileContent)</span><span class="sxs-lookup"><span data-stu-id="f5fa3-103">CimMofDeserializer.DeserializeInstances method (Byte\[\], UInt32, OnClassNeeded, GetIncludedFileContent)</span></span>

<span data-ttu-id="f5fa3-104">Deserializa las instancias CIM basadas en datos serializados y devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="f5fa3-104">Deserializes CIM instances based on serialized data, and callbacks.</span></span>

<span data-ttu-id="f5fa3-105">**Espacio de nombres:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5fa3-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="f5fa3-106">**Ensamblado:**  Microsoft. Management. Infrastructure (en Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="f5fa3-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="f5fa3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5fa3-107">Syntax</span></span>

``` csharp
public IEnumerable<CimInstance> DeserializeInstances(
    byte[] serializedData,
    ref uint offset,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimInstance^>^ DeserializeInstances(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeInstances : 
        serializedData:byte[] *
        offset:uint32 byref *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimInstance>
```

``` vb
Public Function DeserializeInstances (
    serializedData As Byte(),
    ByRef offset As UInteger,
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
) As IEnumerable(CimInstance)
```

#### <a name="parameters"></a><span data-ttu-id="f5fa3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5fa3-108">Parameters</span></span>

  - <span data-ttu-id="f5fa3-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="f5fa3-109">serializedData</span></span>  
    <span data-ttu-id="f5fa3-110">Tipo: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="f5fa3-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="f5fa3-111">Búfer que contiene los datos serializados.</span><span class="sxs-lookup"><span data-stu-id="f5fa3-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="f5fa3-112">offset</span><span class="sxs-lookup"><span data-stu-id="f5fa3-112">offset</span></span>  
    <span data-ttu-id="f5fa3-113">Tipo: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="f5fa3-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="f5fa3-114">Desplazamiento en bytes de la ubicación en la que se va a empezar a leer los datos.</span><span class="sxs-lookup"><span data-stu-id="f5fa3-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="f5fa3-115">Cuando el método devuelve, el desplazamiento apuntará al siguiente byte después de las instancias deserializadas.</span><span class="sxs-lookup"><span data-stu-id="f5fa3-115">When the method returns, the offset will be pointing to the next byte after the deserialized instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="f5fa3-116">onClassNeededCallback</span><span class="sxs-lookup"><span data-stu-id="f5fa3-116">onClassNeededCallback</span></span>  
    <span data-ttu-id="f5fa3-117">Tipo: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span><span class="sxs-lookup"><span data-stu-id="f5fa3-117">Type: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span></span>
    
    <span data-ttu-id="f5fa3-118">Función de devolución de llamada que se usa para proporcionar un objeto de clase solicitado durante la deserialización.</span><span class="sxs-lookup"><span data-stu-id="f5fa3-118">A callback function used to provide a requested class object during deserialization.</span></span>

<!-- end list -->

  - <span data-ttu-id="f5fa3-119">getIncludedFileCallback</span><span class="sxs-lookup"><span data-stu-id="f5fa3-119">getIncludedFileCallback</span></span>  
    <span data-ttu-id="f5fa3-120">Tipo: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span><span class="sxs-lookup"><span data-stu-id="f5fa3-120">Type: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span></span>
    
    <span data-ttu-id="f5fa3-121">Función de devolución de llamada que se usa para proporcionar el contenido del búfer de archivos de un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="f5fa3-121">A callback function used to provide the file buffer contents of a specified file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f5fa3-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5fa3-122">Return value</span></span>

<span data-ttu-id="f5fa3-123">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="f5fa3-123">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span></span>

<span data-ttu-id="f5fa3-124">Interfaz [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) que se puede utilizar para enumerar las clases CIM.</span><span class="sxs-lookup"><span data-stu-id="f5fa3-124">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5fa3-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5fa3-125">See also</span></span>

<span data-ttu-id="f5fa3-126">[Clase CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5fa3-126">[CimInstance class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span></span>  
<span data-ttu-id="f5fa3-127">[Espacio de nombres Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5fa3-127">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
