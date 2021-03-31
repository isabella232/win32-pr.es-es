---
description: 'Más información sobre: API. JetCompact (método)'
title: Método API. JetCompact
TOCTitle: 'JetCompact method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCompact(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS,Microsoft.Isam.Esent.Interop.JET_CONVERT,Microsoft.Isam.Esent.Interop.CompactGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcompact(v=EXCHG.10)
ms:contentKeyID: 55100666
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74d714a1b0fa8d53743945afb3a35cc2015df293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001024"
---
# <a name="apijetcompact-method"></a>Método API. JetCompact

Realiza una copia de una base de datos existente. La copia se compacta con un estado óptimo para su uso. Los datos de los datos copiados se empaquetarán de acuerdo con las medidas elegidas para los índices en la creación de índices. De esta manera, los datos comprimidos se pueden almacenar de la forma más densa posible. Como alternativa, los datos compactos pueden reservar espacio para las inserciones de índice o el crecimiento de registros posteriores.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetCompact ( _
    sesid As JET_SESID, _
    sourceDatabase As String, _
    destinationDatabase As String, _
    statusCallback As JET_PFNSTATUS, _
    ignored As JET_CONVERT, _
    grbit As CompactGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim sourceDatabase As String
Dim destinationDatabase As String
Dim statusCallback As JET_PFNSTATUS
Dim ignored As JET_CONVERT
Dim grbit As CompactGrbitApi.JetCompact(sesid, sourceDatabase, _
    destinationDatabase, statusCallback, _
    ignored, grbit)
```

``` csharp
public static void JetCompact(
    JET_SESID sesid,
    string sourceDatabase,
    string destinationDatabase,
    JET_PFNSTATUS statusCallback,
    JET_CONVERT ignored,
    CompactGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar para la llamada.

<!-- end list -->

  - sourceDatabase  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    La base de datos de origen que se compactará.

<!-- end list -->

  - destinationDatabase  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Nombre que se va a utilizar para la base de datos compactada.

<!-- end list -->

  - statusCallback  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Función de devolución de llamada a la que se puede llamar periódicamente a través de la operación de compactación de base de datos para informar del progreso.

<!-- end list -->

  - no se tiene en cuenta  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_CONVERT](./jet-convert-class.md)  
    
    Este parámetro se omite y debe ser null.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. CompactGrbit](./compactgrbit-enumeration.md)  
    
    Opciones de Compact.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
