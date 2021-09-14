---
description: 'Más información sobre: estructura JET_TABLEID datos'
title: JET_TABLEID estructura
TOCTitle: JET_TABLEID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TABLEID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid(v=EXCHG.10)
ms:contentKeyID: 39516503
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLEID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a72713007ace7fb93b3f01ec8e5fc25cbe127298
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269743"
---
# <a name="jet_tableid-structure"></a>JET_TABLEID estructura

Un JET_TABLEID contiene un identificador para el cursor de base de datos que se usará para una llamada a la API jet. Un cursor solo se puede usar con la sesión que se usó para abrir ese cursor.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Structure JET_TABLEID _
    Implements IEquatable(Of JET_TABLEID), IFormattable
'Usage
Dim instance As JET_TABLEID
```

``` csharp
public struct JET_TABLEID : IEquatable<JET_TABLEID>, 
    IFormattable
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_TABLEID miembros](./jet-tableid-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
