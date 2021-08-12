---
description: Más información sobre el método Api.JetDefragment
title: Método Api.JetDefragment
TOCTitle: 'JetDefragment method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment(v=EXCHG.10)
ms:contentKeyID: 55100679
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9761782e2c6522752d6a05f69005a4db6844542c700cbc5c942ea80d96bf4c2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272659"
---
# <a name="apijetdefragment-method"></a>Método Api.JetDefragment

Inicia y detiene las tareas de desfragmentación de base de datos que mejoran la organización de datos dentro de una base de datos.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function JetDefragment ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment(sesid, _
    dbid, tableName, passes, seconds, _
    grbit)
```

``` csharp
public static JET_wrn JetDefragment(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará para la llamada.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de datos que se va a desfragmentar.

<!-- end list -->

  - tableName  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Parámetro sin usar. La desfragmentación se realiza para toda la base de datos descrita por el identificador de base de datos especificado.

<!-- end list -->

  - Pasa  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Al iniciar una tarea de desfragmentación en línea, este parámetro establece el número máximo de pases de desfragmentación. Al detener una tarea de desfragmentación en línea, este parámetro se establece en el número de pases realizados.

<!-- end list -->

  - segundos  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Al iniciar una tarea de desfragmentación en línea, este parámetro establece el tiempo máximo para la desfragmentación. Al detener una tarea de desfragmentación en línea, este búfer de salida se establece en el período de tiempo utilizado para la desfragmentación.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.DefragGrbit](./defraggrbit-enumeration.md)  
    
    Opciones de desfragmentación.

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Un código de advertencia.  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
