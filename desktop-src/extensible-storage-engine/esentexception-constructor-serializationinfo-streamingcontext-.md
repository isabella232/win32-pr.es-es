---
description: 'Más información sobre: Constructor esentException (SerializationInfo, StreamingContext)'
title: Constructor EsentException (SerializationInfo, StreamingContext) (Microsoft.Isam.Esent)
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
ms.openlocfilehash: f190f4a77d13cb4bc1e8a123dd1ec0f0b07498f2821a07d93a00372ecfaf32cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118778997"
---
# <a name="esentexception-constructor-serializationinfo-streamingcontext"></a>EsentException constructor (SerializationInfo, StreamingContext)

Inicializa una nueva instancia de la clase EsentException. Este constructor se usa para deserializar una excepción serializada.

**Espacio de nombres:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

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

#### <a name="parameters"></a>Parámetros

  - info  
    Tipo: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)  
    
    Datos necesarios para deserializar el objeto.

<!-- end list -->

  - context  
    Tipo: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)  
    
    Contexto de la deserialización.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase EsentException](./esentexception-class.md)

[Miembros de EsentException](./esentexception-members.md)

[Sobrecarga de EsentException](./esentexception-constructor.md)

[Espacio de nombres Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)
