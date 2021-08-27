---
description: Más información sobre el método Api.JetReadFileInstance
title: Método Api.JetReadFileInstance
TOCTitle: 'JetReadFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_HANDLE,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetreadfileinstance(v=EXCHG.10)
ms:contentKeyID: 55100781
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ea64b78f36ac8dc29df7c98fa3f8c8ade484017d07dbc833b9809c766892b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977905"
---
# <a name="apijetreadfileinstance-method"></a>Método Api.JetReadFileInstance

Recupera el contenido de un archivo abierto con [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64).](./api.jetopenfileinstance-method.md)

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetReadFileInstance ( _
    instance As JET_INSTANCE, _
    file As JET_HANDLE, _
    buffer As Byte(), _
    bufferSize As Integer, _
    <OutAttribute> ByRef bytesRead As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim file As JET_HANDLE
Dim buffer As Byte()
Dim bufferSize As Integer
Dim bytesRead As IntegerApi.JetReadFileInstance(instance, _
    file, buffer, bufferSize, bytesRead)
```

``` csharp
public static void JetReadFileInstance(
    JET_INSTANCE instance,
    JET_HANDLE file,
    byte[] buffer,
    int bufferSize,
    out int bytesRead
)
```

#### <a name="parameters"></a>Parámetros

  - instance  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    La instancia de que se utilizará.

<!-- end list -->

  - archivo  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)  
    
    Archivo del que se leerá.

<!-- end list -->

  - buffer  
    Tipo: \[\]  
    
    Búfer en el que se leerá.

<!-- end list -->

  - bufferSize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Tamaño del búfer.

<!-- end list -->

  - bytesRead  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Devuelve la cantidad de datos leídos en el búfer.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
