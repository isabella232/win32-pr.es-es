---
description: 'Más información sobre: JET_OPENTEMPORARYTABLE.cbKeyMost'
title: JET_OPENTEMPORARYTABLE.cbKeyMost (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55104228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbKeyMost
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 225c801770bb41337ee9f3ae248092c60441cd2e9a059f64897ad19053bfe30b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107704"
---
# <a name="jet_opentemporarytablecbkeymost-property"></a>JET_OPENTEMPORARYTABLE.cbKeyMost, propiedad

Obtiene o establece el tamaño máximo de una clave que representa una fila determinada. El tamaño máximo de la clave se puede establecer para controlar cómo se truncan las claves. El truncamiento de claves es importante porque puede afectar cuando se considera que las filas son distintas. Si este parámetro se establece en 0 o 255, el tamaño máximo de clave y su semántica seguirán siendo idénticos al tamaño máximo de clave admitido por Windows Server 2003. Este parámetro también se puede establecer en un valor mayor como una función del tamaño de página de la base de datos para la [instancia DatabasePageSize](./jet-param-enumeration.md). Vea [KeyMost para](./vistaparam.keymost-field.md) obtener más información.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_OPENTEMPORARYTABLE clase](./jet-opentemporarytable-class.md)

[JET_OPENTEMPORARYTABLE miembros](./jet-opentemporarytable-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
