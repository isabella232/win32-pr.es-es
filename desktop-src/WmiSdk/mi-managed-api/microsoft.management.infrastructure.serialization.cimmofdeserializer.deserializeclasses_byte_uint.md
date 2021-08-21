---
description: Más información sobre el método CimMofDeserializer.DeserializeClasses (Byte[], UInt32)
title: Método CimMofDeserializer.DeserializeClasses (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@)
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
ms.openlocfilehash: b05a1eca97c650b130170af2c6c03a958b6022017902e39f15156b08038bad08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317416"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32"></a>Método CimMofDeserializer.DeserializeClasses (Byte \[ \] , UInt32)

Deserializa clases CIM basadas en datos serializados.

**Espacio de nombres:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Ensamblado:**  Microsoft.Management.Infrastructure (en Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Sintaxis

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a>Parámetros

  - serializedData  
    Tipo: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]
    
    Búfer que contiene los datos serializados.

<!-- end list -->

  - offset  
    Tipo: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)
    
    Desplazamiento de bytes a la ubicación en la que se comienza a leer los datos. Cuando el método devuelve un resultado, el desplazamiento apuntará al byte siguiente después de las clases deserializadoras.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\>

Interfaz [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) que se puede usar para enumerar las clases CIM.

## <a name="see-also"></a>Consulte también

[CimClass (clase)](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))  
[Espacio de nombres Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
