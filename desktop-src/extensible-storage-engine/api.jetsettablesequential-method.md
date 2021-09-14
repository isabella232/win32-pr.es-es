---
description: Más información sobre el método Api.JetSetTableSequential
title: Método Api.JetSetTableSequential
TOCTitle: 'JetSetTableSequential method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetTableSequentialGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsettablesequential(v=EXCHG.10)
ms:contentKeyID: 55100810
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 879eca53c4867bb41ee0a231bff9adce39aa58a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969447"
---
# <a name="apijetsettablesequential-method"></a>Método Api.JetSetTableSequential

Notifica al motor de base de datos que la aplicación está analizando todo el índice en el que se encuentra el cursor. Por lo tanto, los métodos que se usan para acceder a los datos de índice se optimizarán para que este escenario sea lo más rápido posible. Consulte también [JetResetTableSequential(JET_SESID, JET_TABLEID, ResetTableSequentialGrbit).](./api.jetresettablesequential-method.md)

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetSetTableSequential ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetTableSequentialGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetTableSequentialGrbitApi.JetSetTableSequential(sesid, _
    tableid, grbit)
```

``` csharp
public static void JetSetTableSequential(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetTableSequentialGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor que tendrá acceso a los datos.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.SetTableSequentialGrbit](./settablesequentialgrbit-enumeration.md)  
    
    Reservado para uso futuro.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
