---
description: 'Más información sobre: método Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, Byte [] [], Int32, Int32, Int32, Int32, PrereadKeysGrbit)'
title: Método Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, Byte [] [], Int32, Int32, Int32, Int32, PrereadKeysGrbit) (Microsoft. ISAM. esent. Interop. Windows7)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275697"
---
# <a name="windows7apijetprereadkeys-method-jet_sesid-jet_tableid-byte-int32--int32-int32-int32-prereadkeysgrbit"></a>Método Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, byte \[ \] \[ \] , Int32, Int32, Int32, Int32, PrereadKeysGrbit)

Si los registros con las claves especificadas no están en la caché del búfer, inicie las lecturas asincrónicas para traer los registros a la memoria caché del búfer de la base de datos.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar.

<!-- end list -->

  - TABLEID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Tabla en la que se van a emitir las lecturas preleídas.

<!-- end list -->

  - claves  
    Automáticamente \[\]  
    
    Claves que se van a leer. Las claves deben estar ordenadas.

<!-- end list -->

  - keyLengths  
    Automáticamente \[\]  
    
    Longitud de las claves que se van a leer.

<!-- end list -->

  - keyIndex  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Índice de la primera clave de la matriz de claves que se va a leer.

<!-- end list -->

  - keyCount  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Número máximo de claves que se van a leer.

<!-- end list -->

  - keysPreread  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Devuelve el número de claves que se va a preleer realmente.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. Windows7. PrereadKeysGrbit](./prereadkeysgrbit-enumeration.md)  
    
    Opciones de lectura. Se utiliza para especificar la dirección de la lectura y escritura.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase Windows7Api](./windows7api-class.md)

[Miembros de Windows7Api](./windows7api-members.md)

[Sobrecarga JetPrereadKeys](./windows7api.jetprereadkeys-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)
