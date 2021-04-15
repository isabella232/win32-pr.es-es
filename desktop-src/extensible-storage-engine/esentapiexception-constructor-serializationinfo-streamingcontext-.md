---
description: 'Más información acerca de: constructor EsentApiException (SerializationInfo, StreamingContext)'
title: Constructor EsentApiException (SerializationInfo, StreamingContext)
TOCTitle: EsentApiException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentApiException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101059
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a00204c254378956521a1ae5fe02480dd879c832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498160"
---
# <a name="esentapiexception-constructor-serializationinfo-streamingcontext"></a>Constructor EsentApiException (SerializationInfo, StreamingContext)

Inicializa una nueva instancia de la clase EsentApiException. Este constructor se utiliza para deserializar una excepción serializada.

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

Dim instance As New EsentApiException(info, context)
```

``` csharp
protected EsentApiException(
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

[Clase EsentApiException](./esentapiexception-class.md)

[Miembros de EsentApiException](./esentapiexception-members.md)

[Sobrecarga EsentApiException](./esentapiexception-constructor.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
