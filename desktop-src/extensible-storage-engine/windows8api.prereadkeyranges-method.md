---
description: 'Más información sobre: Windows8Api. PrereadKeyRanges (método)'
title: Método Windows8Api. PrereadKeyRanges (Microsoft. ISAM. esent. Interop. Windows8)
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
ms.openlocfilehash: 091c1f92512fd9a55bb4acd4d824567acc19fdde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001411"
---
# <a name="windows8apiprereadkeyranges-method"></a>Windows8Api. PrereadKeyRanges, método

Si los registros con los intervalos de claves especificados no están en la caché del búfer, inicie las lecturas asincrónicas para traer los registros a la memoria caché del búfer de la base de datos.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar.

<!-- end list -->

  - TABLEID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Tabla en la que se van a emitir las lecturas preleídas.

<!-- end list -->

  - keysStart  
    Automáticamente \[\]  
    
    Inicio de los intervalos de clave que se van a leer.

<!-- end list -->

  - keyStartLengths  
    Automáticamente \[\]  
    
    Longitud de las claves de inicio que se van a leer como prelectura.

<!-- end list -->

  - keysEnd  
    Automáticamente \[\]  
    
    Final del intervalo de claves que se va a leer.

<!-- end list -->

  - keyEndLengths  
    Automáticamente \[\]  
    
    Longitud de las teclas finales que se van a leer.

<!-- end list -->

  - rangeIndex  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Índice del primer intervalo de claves de la matriz que se va a leer.

<!-- end list -->

  - rangeCount  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Número máximo de intervalos de clave que se van a leer.

<!-- end list -->

  - rangesPreread  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Devuelve el número de claves que se han preleído realmente.

<!-- end list -->

  - columnsPreread  
    Automáticamente \[\]  
    
    Lista de identificadores de columna para las columnas de valor largo que se van a leer como prelectura.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. Windows8. PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)  
    
    Opciones de lectura. Se utiliza para especificar la dirección de la lectura y escritura.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase Windows8Api](./windows8api-class.md)

[Miembros de Windows8Api](./windows8api-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
