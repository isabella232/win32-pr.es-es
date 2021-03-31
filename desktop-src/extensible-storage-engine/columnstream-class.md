---
description: 'Más información sobre: clase ColumnStream'
title: Clase ColumnStream
TOCTitle: ColumnStream class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnStream
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream(v=EXCHG.10)
ms:contentKeyID: 55100939
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eea249347acd18ec71f03fcdc82b8a2baa1da9ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277500"
---
# <a name="columnstream-class"></a>Clase ColumnStream

Esta clase proporciona una interfaz de streaming a una columna de valor largo (es decir, una columna de tipo [LongBinary](./jet-coltyp-enumeration.md) o [LongText](./jet-coltyp-enumeration.md)).

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.MarshalByRefObject](/dotnet/api/system.marshalbyrefobject)  
    [System. IO. Stream](/dotnet/api/system.io.stream)  
      Microsoft. ISAM. esent. Interop. ColumnStream  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Class ColumnStream _
    Inherits Stream
'Usage
Dim instance As ColumnStream
```

``` csharp
public class ColumnStream : Stream
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de ColumnStream](./columnstream-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
