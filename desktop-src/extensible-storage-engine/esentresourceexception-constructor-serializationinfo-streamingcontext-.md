---
description: 'Más información acerca de: constructor EsentResourceException (SerializationInfo, StreamingContext)'
title: Constructor EsentResourceException (SerializationInfo, StreamingContext)
TOCTitle: EsentResourceException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResourceException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresourceexception.esentresourceexception(v=EXCHG.10)
ms:contentKeyID: 55102649
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResourceException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4f7b52e211d155b92a9917670682af735eedf9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717257"
---
# <a name="esentresourceexception-constructor-serializationinfo-streamingcontext"></a>Constructor EsentResourceException (SerializationInfo, StreamingContext)

Inicializa una nueva instancia de la clase EsentResourceException. Este constructor se utiliza para deserializar una excepción serializada.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

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

Dim instance As New EsentResourceException(info, context)
```

``` csharp
protected EsentResourceException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a>Parámetros

  - info  
    Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)  
    
    Los datos necesarios para deserializar el objeto.

<!-- end list -->

  - context  
    Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)  
    
    Contexto de la deserialización.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase EsentResourceException](./esentresourceexception-class.md)

[Miembros de EsentResourceException](./esentresourceexception-members.md)

[Sobrecarga EsentResourceException](./esentresourceexception-constructor.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
