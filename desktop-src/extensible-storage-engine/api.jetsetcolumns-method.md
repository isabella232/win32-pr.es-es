---
description: Más información sobre el método Api.JetSetColumns
title: Método Api.JetSetColumns
TOCTitle: 'JetSetColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_SETCOLUMN[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumns(v=EXCHG.10)
ms:contentKeyID: 55100800
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a0d84c982fe3a3e7834210741f5bd20cc52615197756653c743f5cd67d0b59dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118084934"
---
# <a name="apijetsetcolumns-method"></a>Método Api.JetSetColumns

Permite a una aplicación establecer varios valores de columna en una sola operación. Se usa una [matriz](./jet-setcolumn-class.md) JET_SETCOLUMN estructura para describir el conjunto de valores de columna que se va a establecer y para describir los búferes de entrada para cada valor de columna que se va a establecer.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Shared Function JetSetColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    setcolumns As JET_SETCOLUMN(), _
    numColumns As Integer _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim setcolumns As JET_SETCOLUMN()
Dim numColumns As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumns(sesid, _
    tableid, setcolumns, numColumns)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public static JET_wrn JetSetColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_SETCOLUMN[] setcolumns,
    int numColumns
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor en el que se establecen las columnas.

<!-- end list -->

  - setcolumns  
    Tipo: \[\]  
    
    Matriz de [estructuras JET_SETCOLUMN](./jet-setcolumn-class.md) que describen los datos que se establecerán.

<!-- end list -->

  - numColumns  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Número de entradas del parámetro setcolumns.

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Una advertencia. Si el último conjunto de columnas tiene una advertencia, esta advertencia se devolverá desde el propio JetSetColumns.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
