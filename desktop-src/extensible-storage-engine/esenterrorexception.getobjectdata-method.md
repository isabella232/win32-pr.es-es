---
description: 'Más información sobre: Método EsentErrorException.GetObjectData'
title: Método EsentErrorException.GetObjectData
TOCTitle: 'GetObjectData method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.getobjectdata(v=EXCHG.10)
ms:contentKeyID: 55101432
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ff4588429d5b45690763c3f4eefd3553f88f480
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476668"
---
# <a name="esenterrorexceptiongetobjectdata-method"></a>Método EsentErrorException.GetObjectData

Cuando se invalida en una clase derivada, establece [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) con información sobre la excepción.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Overrides Sub GetObjectData ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim instance As EsentErrorException
Dim info As SerializationInfo
Dim context As StreamingContext

instance.GetObjectData(info, context)
```

``` csharp
public override void GetObjectData(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a>Parámetros

  - info  
    Tipo: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)  
    
    [SerializationInfo que](/dotnet/api/system.runtime.serialization.serializationinfo) contiene los datos del objeto serializado sobre la excepción que se está iniciando.

<!-- end list -->

  - context  
    Tipo: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)  
    
    [StreamingContext que](/dotnet/api/system.runtime.serialization.streamingcontext) contiene información contextual sobre el origen o el destino.

#### <a name="implements"></a>Implementaciones

[ISerializable.GetObjectData(SerializationInfo, StreamingContext)](/dotnet/api/system.runtime.serialization.iserializable.getobjectdata#System_Runtime_Serialization_ISerializable_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  
[_Exception.GetObjectData(SerializationInfo, StreamingContext)](/dotnet/api/system.runtime.interopservices._exception.getobjectdata#System_Runtime_InteropServices__Exception_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  

## <a name="exceptions"></a>Excepciones


| Excepción | Condición | 
|-----------|-----------|
| <a href="/dotnet/api/system.argumentnullexception">ArgumentNullException</a> | <p>El parámetro info es una referencia null (Nothing en Visual Basic).</p> | 



## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase EsentErrorException](./esenterrorexception-class.md)

[Miembros de EsentErrorException](./esenterrorexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
