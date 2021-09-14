---
description: 'Más información sobre: Método EsentResource.Dispose (booleano)'
title: Método EsentResource.Dispose (booleano)
TOCTitle: Dispose method (Boolean)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResource.Dispose(System.Boolean)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource.dispose(v=EXCHG.10)
ms:contentKeyID: 55102624
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource.Dispose
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf74291bf4c54ffa1d61c28bf7caff1e8c2b231b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358840"
---
# <a name="esentresourcedispose-method-boolean"></a>Método EsentResource.Dispose (booleano)

Lo llaman Dispose y el finalizador.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Protected Overridable Sub Dispose ( _
    isDisposing As Boolean _
)
'Usage
Dim isDisposing As Boolean

Me.Dispose(isDisposing)
```

``` csharp
protected virtual void Dispose(
    bool isDisposing
)
```

#### <a name="parameters"></a>Parámetros

  - isDisposing  
    Tipo: [System.Boolean](/dotnet/api/system.boolean)  
    
    True si se llama desde Dispose.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase EsentResource](./esentresource-class.md)

[Miembros de EsentResource](./esentresource-members.md)

[Sobrecarga de Dispose](./esentresource.dispose-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
