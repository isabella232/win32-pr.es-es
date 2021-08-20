---
description: 'Más información sobre: Constructor EsentObsoleteException (SerializationInfo, StreamingContext)'
title: EsentObsoleteException constructor (SerializationInfo, StreamingContext)
TOCTitle: EsentObsoleteException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentObsoleteException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102167
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b114078e25cd394caa294dac5604502a4a2f783945914a44423b1c8681c105a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119040113"
---
# <a name="esentobsoleteexception-constructor-serializationinfo-streamingcontext"></a>EsentObsoleteException constructor (SerializationInfo, StreamingContext)

Inicializa una nueva instancia de la clase EsentObsoleteException. Este constructor se usa para deserializar una excepción serializada.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
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

Dim instance As New EsentObsoleteException(info, context)
```

``` csharp
protected EsentObsoleteException(
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

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase EsentObsoleteException](./esentobsoleteexception-class.md)

[Miembros de EsentObsoleteException](./esentobsoleteexception-members.md)

[Sobrecarga de EsentObsoleteException](./esentobsoleteexception-constructor.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
