---
description: 'Más información sobre: JET_PFNDURABLECOMMITCALLBACK delegado'
title: JET_PFNDURABLECOMMITCALLBACK delegado (Microsoft.Isam.Esent.Interop.Windows8)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965636"
---
# <a name="jet_pfndurablecommitcallback-delegate"></a>JET_PFNDURABLECOMMITCALLBACK delegado

Devolución de llamada para JET_paramDurableCommitCallback.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instancia que se usará.

<!-- end list -->

  - pCommitIdSeen  
    Tipo: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Identificador de confirmación que se acaba de vaciar.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallbackGrbit](./durablecommitcallbackgrbit-enumeration.md)  
    
    Reservado actualmente.

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
