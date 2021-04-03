---
description: 'Más información acerca de: JET_PFNDURABLECOMMITCALLBACK delegado'
title: JET_PFNDURABLECOMMITCALLBACK delegado (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: JET_PFNDURABLECOMMITCALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_pfndurablecommitcallback(v=EXCHG.10)
ms:contentKeyID: 55104327
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.Invoke
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK..ctor
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.BeginInvoke
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9ff2f613138103be56db3fe7084202965a949cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913565"
---
# <a name="jet_pfndurablecommitcallback-delegate"></a>JET_PFNDURABLECOMMITCALLBACK delegado

Devolución de llamada para JET_paramDurableCommitCallback.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Delegate Function JET_PFNDURABLECOMMITCALLBACK ( _
    instance As JET_INSTANCE, _
    pCommitIdSeen As JET_COMMIT_ID, _
    grbit As DurableCommitCallbackGrbit _
) As JET_err
'Usage
Dim instance As New JET_PFNDURABLECOMMITCALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNDURABLECOMMITCALLBACK(
    JET_INSTANCE instance,
    JET_COMMIT_ID pCommitIdSeen,
    DurableCommitCallbackGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - instance  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instancia de que se va a usar.

<!-- end list -->

  - pCommitIdSeen  
    Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    El ID. de confirmación que acaba de vaciarse.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. Windows8. DurableCommitCallbackGrbit](./durablecommitcallbackgrbit-enumeration.md)  
    
    Reservado actualmente.

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
