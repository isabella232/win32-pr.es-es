---
description: 'Más información acerca de: constructor EsentFatalException (SerializationInfo, StreamingContext)'
title: Constructor EsentFatalException (SerializationInfo, StreamingContext)
TOCTitle: EsentFatalException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFatalException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101554
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2264e3852eb6809f321b9bae162a833e86d7b513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082215"
---
# <a name="esentfatalexception-constructor-serializationinfo-streamingcontext"></a>Constructor EsentFatalException (SerializationInfo, StreamingContext)

Inicializa una nueva instancia de la clase EsentFatalException. Este constructor se utiliza para deserializar una excepción serializada.

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

Dim instance As New EsentFatalException(info, context)
```

``` csharp
protected EsentFatalException(
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

[Clase EsentFatalException](./esentfatalexception-class.md)

[Miembros de EsentFatalException](./esentfatalexception-members.md)

[Sobrecarga EsentFatalException](./esentfatalexception-constructor.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
