---
description: Más información sobre el método Instance.ReleaseHandle
title: Método Instance.ReleaseHandle
TOCTitle: 'ReleaseHandle method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.releasehandle(v=EXCHG.10)
ms:contentKeyID: 55103298
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c3d5b614bdf2b00f7b47b8d9fc2f6c5e2edec2e71960bf0b480024ec65de5540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112574"
---
# <a name="instancereleasehandle-method"></a>Método Instance.ReleaseHandle

Libere el identificador de esta instancia.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Protected Overrides Function ReleaseHandle As Boolean
'Usage
Dim returnValue As Boolean

returnValue = Me.ReleaseHandle()
```

``` csharp
protected override bool ReleaseHandle()
```

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True si se puede liberar el identificador.  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase de instancia](./instance-class.md)

[Miembros de instancia](./instance-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
