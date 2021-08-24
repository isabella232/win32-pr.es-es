---
description: Más información sobre el método Windows8Api.PrereadKeyRanges
title: Método Windows8Api.PrereadKeyRanges (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: 'PrereadKeyRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.prereadkeyranges(v=EXCHG.10)
ms:contentKeyID: 55104465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02328ddc47daec4fbd98f88222dd7519053ed92aa64d2a0048782340d626b03c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452695"
---
# <a name="windows8apiprereadkeyranges-method"></a>Método Windows8Api.PrereadKeyRanges

Si los registros con los intervalos de claves especificados no están en la caché del búfer, inicie lecturas asincrónicas para llevar los registros a la caché del búfer de base de datos.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub PrereadKeyRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keysStart As Byte()(), _
    keyStartLengths As Integer(), _
    keysEnd As Byte()(), _
    keyEndLengths As Integer(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keysStart As Byte()()
Dim keyStartLengths As Integer()
Dim keysEnd As Byte()()
Dim keyEndLengths As Integer()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbitWindows8Api.PrereadKeyRanges(sesid, tableid, _
    keysStart, keyStartLengths, keysEnd, _
    keyEndLengths, rangeIndex, rangeCount, _
    rangesPreread, columnsPreread, grbit)
```

``` csharp
public static void PrereadKeyRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keysStart,
    int[] keyStartLengths,
    byte[][] keysEnd,
    int[] keyEndLengths,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Tabla con la que se emitirán los preleciones.

<!-- end list -->

  - keysStart  
    Tipo: \[\]  
    
    Inicio de los intervalos de claves que se van a leer previamente.

<!-- end list -->

  - keyStartLengths  
    Tipo: \[\]  
    
    Longitudes de las claves de inicio que se leerán previamente.

<!-- end list -->

  - keysEnd  
    Tipo: \[\]  
    
    Final del intervalo de claves que se va a leer previamente.

<!-- end list -->

  - keyEndLengths  
    Tipo: \[\]  
    
    Longitudes de las claves finales que se leerán previamente.

<!-- end list -->

  - rangeIndex  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Índice del primer intervalo de claves de la matriz que se va a leer.

<!-- end list -->

  - rangeCount  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Número máximo de intervalos de claves que se van a leer previamente.

<!-- end list -->

  - rangesPreread  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Devuelve el número de claves que realmente se han leído previamente.

<!-- end list -->

  - columnsPreread  
    Tipo: \[\]  
    
    Lista de identificadores de columna para las columnas de valor largo que se deben leer previamente.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)  
    
    Opciones de lectura previa. Se usa para especificar la dirección de la lectura previa.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase Windows8Api](./windows8api-class.md)

[Miembros de Windows8Api](./windows8api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
