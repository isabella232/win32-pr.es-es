---
description: Más información sobre el método Api.JetCompact
title: Método Api.JetCompact
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072652"
---
# <a name="apijetcompact-method"></a>Método Api.JetCompact

Realiza una copia de una base de datos existente. La copia se compacta a un estado óptimo para su uso. Los datos de los datos copiados se empaquetarán según las medidas elegidas para los índices en la creación del índice. De esta manera, los datos compactados se pueden almacenar lo más densamente posible. Como alternativa, los datos compactados pueden reservar espacio para las posteriores inserciones de índices o crecimiento de registros.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará para la llamada.

<!-- end list -->

  - sourceDatabase  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Base de datos de origen que se compactará.

<!-- end list -->

  - destinationDatabase  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Nombre que se usará para la base de datos compactada.

<!-- end list -->

  - statusCallback  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Función de devolución de llamada a la que se puede llamar periódicamente a través de la operación compacta de base de datos para informar del progreso.

<!-- end list -->

  - no se tiene en cuenta  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_CONVERT](./jet-convert-class.md)  
    
    Este parámetro se omite y debe ser NULL.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.CompactGrbit](./compactgrbit-enumeration.md)  
    
    Opciones compactas.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
