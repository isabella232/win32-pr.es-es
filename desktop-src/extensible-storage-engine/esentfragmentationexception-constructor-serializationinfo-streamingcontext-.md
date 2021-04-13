---
description: 'Más información acerca de: constructor EsentFragmentationException (SerializationInfo, StreamingContext)'
title: Constructor EsentFragmentationException (SerializationInfo, StreamingContext)
TOCTitle: EsentFragmentationException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFragmentationException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101633
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 251e4beaacb1e895c1da1d501b38cf03f211dd99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361703"
---
# <a name="esentfragmentationexception-constructor-serializationinfo-streamingcontext"></a>Constructor EsentFragmentationException (SerializationInfo, StreamingContext)

Inicializa una nueva instancia de la clase EsentFragmentationException. Este constructor se utiliza para deserializar una excepción serializada.

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

Dim instance As New EsentFragmentationException(info, context)
```

``` csharp
protected EsentFragmentationException(
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

[Clase EsentFragmentationException](./esentfragmentationexception-class.md)

[Miembros de EsentFragmentationException](./esentfragmentationexception-members.md)

[Sobrecarga EsentFragmentationException](./esentfragmentationexception-constructor.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
