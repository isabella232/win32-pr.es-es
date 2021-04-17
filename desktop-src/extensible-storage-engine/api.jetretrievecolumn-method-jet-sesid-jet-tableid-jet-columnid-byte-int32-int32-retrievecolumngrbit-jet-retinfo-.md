---
description: 'Más información sobre: método API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)'
title: Método API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
TOCTitle: JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100790
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d417e188c72914f871df4b46dede204f6633a8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696304"
---
# <a name="apijetretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-retrievecolumngrbit-jet_retinfo"></a>Método API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)

Recupera un valor de una sola columna del registro actual. El registro es el registro asociado a la entrada de índice en la posición actual del cursor. Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia del cursor. Esta función también puede recuperar los datos de columna de una entrada de índice que hace referencia al registro actual. Además de recuperar el valor de la columna real, JetRetrieveColumn también se puede usar para recuperar el tamaño de una columna, antes de recuperar los propios datos de la columna para que se pueda ajustar el tamaño adecuado de los búferes de la aplicación.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function JetRetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumn(sesid, _
    tableid, columnid, data, dataSize, _
    actualDataSize, grbit, retinfo)
```

``` csharp
public static JET_wrn JetRetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar.

<!-- end list -->

  - TABLEID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor del que se va a recuperar la columna.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Columnid que se va a recuperar.

<!-- end list -->

  - datos  
    Automáticamente \[\]  
    
    Búfer de datos que se va a recuperar en.

<!-- end list -->

  - dataSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Tamaño del búfer de datos.

<!-- end list -->

  - actualDataSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Devuelve el tamaño real del búfer de datos.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)  
    
    Recupera opciones de columna.

<!-- end list -->

  - retinfo  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_RETINFO](./jet-retinfo-class.md)  
    
    Si pretinfo se da como NULL, la función se comporta como si se hubiera proporcionado un valor de itagSequence de 1 y una ibLongValue de 0 (cero). Esto hace que la recuperación de columnas recupere el primer valor de una columna con varios valores y que recupere datos largos en el desplazamiento 0 (cero).

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Código de advertencia de ESENT.  

## <a name="remarks"></a>Observaciones

Las funciones RetrieveColumnAs proporcionan funciones de recuperación específicas del tipo de información.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Sobrecarga JetRetrieveColumn](./api.jetretrievecolumn-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
