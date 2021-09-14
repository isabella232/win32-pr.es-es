---
description: 'Más información sobre: JET_BKLOGTIME. Método ToDateTime'
title: JET_BKLOGTIME. Método ToDateTime
TOCTitle: 'ToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.ToDateTime
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.todatetime(v=EXCHG.10)
ms:contentKeyID: 39515201
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.ToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.ToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b6470e8486f5ff8c8ec8d1b7eb6678741fccc04f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072535"
---
# <a name="jet_bklogtimetodatetime-method"></a>JET_BKLOGTIME. Método ToDateTime

Genere una representación DateTime de este JET_BKLOGTIME.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Function ToDateTime As Nullable(Of DateTime)
'Usage
Dim instance As JET_BKLOGTIME
Dim returnValue As Nullable(Of DateTime)

returnValue = instance.ToDateTime()
```

``` csharp
public Nullable<DateTime> ToDateTime()
```

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\>  
DateTime que representa el JET_BKLOGTIME. Si el JET_BKLOGTIME es NULL, se devuelve null.  

#### <a name="implements"></a>Implementaciones

[IJET_LOGTIME. ToDateTime()](./ijet-logtime.todatetime-method.md)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_BKLOGTIME estructura](./jet-bklogtime-structure2.md)

[JET_BKLOGTIME miembros](./jet-bklogtime-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
