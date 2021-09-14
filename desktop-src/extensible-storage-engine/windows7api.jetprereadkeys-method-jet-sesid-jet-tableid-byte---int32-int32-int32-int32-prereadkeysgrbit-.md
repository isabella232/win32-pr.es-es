---
description: 'Más información sobre: Método Windows7Api.JetPrereadKeys (JET_SESID, JET_TABLEID, Byte[][], Int32, Int32, Int32, Int32, Int32, PrereadKeysGrbit)'
title: Método Windows7Api.JetPrereadKeys (JET_SESID, JET_TABLEID, Byte[][], Int32, Int32, Int32, Int32, PrereadKeysGrbit) (Microsoft.Isam.Esent.Interop.Windows7)
TOCTitle: JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte[][], Int32 , Int32, Int32, Int32, PrereadKeysGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7api.jetprereadkeys(v=EXCHG.10)
ms:contentKeyID: 55104374
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a799c890887df730fdad97ad4d08fa500a6dd4b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252633"
---
# <a name="windows7apijetprereadkeys-method-jet_sesid-jet_tableid-byte-int32--int32-int32-int32-prereadkeysgrbit"></a>Método Windows7Api.JetPrereadKeys (JET_SESID, JET_TABLEID, \[ \] \[ \] Byte, Int32, Int32, Int32, Int32, PrereadKeysGrbit)

Si los registros con las claves especificadas no están en la caché del búfer, inicie lecturas asincrónicas para llevar los registros a la caché del búfer de base de datos.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetPrereadKeys ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keys As Byte()(), _
    keyLengths As Integer(), _
    keyIndex As Integer, _
    keyCount As Integer, _
    <OutAttribute> ByRef keysPreread As Integer, _
    grbit As PrereadKeysGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keys As Byte()()
Dim keyLengths As Integer()
Dim keyIndex As Integer
Dim keyCount As Integer
Dim keysPreread As Integer
Dim grbit As PrereadKeysGrbitWindows7Api.JetPrereadKeys(sesid, tableid, _
    keys, keyLengths, keyIndex, keyCount, _
    keysPreread, grbit)
```

``` csharp
public static void JetPrereadKeys(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keys,
    int[] keyLengths,
    int keyIndex,
    int keyCount,
    out int keysPreread,
    PrereadKeysGrbit grbit
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

  - claves  
    Tipo: \[\]  
    
    Claves que se leerán previamente. Las claves deben estar ordenadas.

<!-- end list -->

  - keyLengths  
    Tipo: \[\]  
    
    Longitudes de las claves que se leerán previamente.

<!-- end list -->

  - keyIndex  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Índice de la primera clave de la matriz de claves que se debe leer.

<!-- end list -->

  - keyCount  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Número máximo de claves que se leerán previamente.

<!-- end list -->

  - keysPreread  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Devuelve el número de claves que se leerán previamente.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit](./prereadkeysgrbit-enumeration.md)  
    
    Opciones de lectura previa. Se usa para especificar la dirección de la lectura previa.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase Windows7Api](./windows7api-class.md)

[Miembros de Windows7Api](./windows7api-members.md)

[Sobrecarga de JetPrereadKeys](./windows7api.jetprereadkeys-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)
