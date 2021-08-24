---
description: Más información sobre el método VistaApi.JetOpenTemporaryTable
title: Método VistaApi.JetOpenTemporaryTable (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'JetOpenTemporaryTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetopentemporarytable(v=EXCHG.10)
ms:contentKeyID: 55104291
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4693379f94e7211849c5184a10ec176e6cc916a455d61903aa35110d2cd36eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118484290"
---
# <a name="vistaapijetopentemporarytable-method"></a>Método VistaApi.JetOpenTemporaryTable

Crea una tabla temporal con un único índice. Una tabla temporal almacena y recupera registros como una tabla normal creada mediante JetCreateTableColumnIndex. Sin embargo, las tablas temporales son mucho más rápidas que las tablas normales debido a su naturaleza volátil. También se pueden usar para ordenar y realizar la eliminación de duplicados rápidamente en conjuntos de registros cuando se accede a ellos de una manera puramente secuencial. Vea también [JetOpenTempTable(JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTempTable3(JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEVistaApi.JetOpenTemporaryTable(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - temporarytable  
    Tipo: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)  
    
    Descripción de la tabla temporal que se creará en la entrada. Después de una llamada correcta, la estructura contiene el identificador de la tabla temporal y las identificaciones de columna. Use [JetCloseTable(JET_SESID, JET_TABLEID) para](./api.jetclosetable-method.md) liberar la tabla temporal cuando haya terminado.

## <a name="remarks"></a>Comentarios

Introducido en Windows Vista. Use [JetOpenTempTable3(JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md) para versiones anteriores de Esent.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[VistaApi (clase)](./vistaapi-class.md)

[Miembros de VistaApi](./vistaapi-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
