---
description: 'Más información sobre: Método Api.JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, SetColumnGrbit, JET_SETINFO)'
title: Método Api.JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, SetColumnGrbit, JET_SETINFO)
TOCTitle: JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, SetColumnGrbit, JET_SETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.SetColumnGrbit,Microsoft.Isam.Esent.Interop.JET_SETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumn(v=EXCHG.10)
ms:contentKeyID: 55100801
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f52c900521d28c82245db53b98ab376dd82faec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360772"
---
# <a name="apijetsetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-setcolumngrbit-jet_setinfo"></a>Método Api.JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, SetColumnGrbit, JET_SETINFO)

La función JetSetColumn modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual. Puede sobrescribir un valor existente, agregar un nuevo valor a una secuencia de valores de una columna con varios valores, quitar un valor de una secuencia de valores de una columna de varios valores o actualizar todo o parte de un valor largo (una columna de tipo [LongText](./jet-coltyp-enumeration.md) o [LongBinary).](./jet-coltyp-enumeration.md)

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function JetSetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    dataOffset As Integer, _
    grbit As SetColumnGrbit, _
    setinfo As JET_SETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim dataOffset As Integer
Dim grbit As SetColumnGrbit
Dim setinfo As JET_SETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumn(sesid, _
    tableid, columnid, data, dataSize, _
    dataOffset, grbit, setinfo)
```

``` csharp
public static JET_wrn JetSetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    int dataOffset,
    SetColumnGrbit grbit,
    JET_SETINFO setinfo
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que realiza la actualización.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor que se actualizará. Se debe preparar una actualización.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Columnid que se establece.

<!-- end list -->

  - datos  
    Tipo: \[\]  
    
    Datos que se van a establecer.

<!-- end list -->

  - dataSize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Tamaño de los datos que se establecerán.

<!-- end list -->

  - dataOffset  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Desplazamiento en el búfer de datos desde el que se establecen los datos.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)  
    
    Opciones de SetColumn.

<!-- end list -->

  - setinfo  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SETINFO](./jet-setinfo-class.md)  
    
    Se usa para especificar itag o desplazamiento de valor largo.

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Valor de advertencia.  

## <a name="remarks"></a>Observaciones

Se trata de una versión solo interna de la API que toma un búfer de datos y un desplazamiento en el búfer.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Sobrecarga de JetSetColumn](./api.jetsetcolumn-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
