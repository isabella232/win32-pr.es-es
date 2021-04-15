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
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass"></a>Método CimMofDeserializer. DeserializeClasses (byte \[ \] , UInt32, IEnumerable \<CimClass\> )

Deserializa clases CIM basadas en datos serializados y una colección de clases CIM primarias.

**Espacio de nombres:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Ensamblado:**  Microsoft. Management. Infrastructure (en Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Sintaxis

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

#### <a name="parameters"></a>Parámetros

  - serializedData  
    Tipo: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]
    
    Búfer que contiene los datos serializados.

<!-- end list -->

  - offset  
    Tipo: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)
    
    Desplazamiento en bytes de la ubicación en la que se va a empezar a leer los datos. Cuando el método devuelve, el desplazamiento apuntará al siguiente byte después de las clases deserializadas.

<!-- end list -->

  - clases  
    Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\>
    
    Una memoria caché opcional de clases CIM principales.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\>

Interfaz [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) que se puede utilizar para enumerar las clases CIM.

## <a name="see-also"></a>Vea también

[Clase CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))  
[Espacio de nombres Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
