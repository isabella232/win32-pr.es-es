---
description: 'Más información acerca de: método Instance.Init (JET_RSTINFO, InitGrbit)'
title: Método Instance.Init (JET_RSTINFO, InitGrbit)
TOCTitle: Init method (JET_RSTINFO, InitGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.Init(Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.init(v=EXCHG.10)
ms:contentKeyID: 55103274
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Init
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1945b0119053a2759b57b8781b86cf682b3a364c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705821"
---
# <a name="instanceinit-method-jet_rstinfo-initgrbit"></a>Método Instance.Init (JET_RSTINFO, InitGrbit)

Inicialice el JET_INSTANCE. Esta API requiere al menos la versión de vista de ESENT.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Sub Init ( _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
)
'Usage
Dim instance As Instance
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit

instance.Init(recoveryOptions, grbit)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public void Init(
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - recoveryOptions  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)  
    
    Parámetros de recuperación adicionales para volver a asignar las bases de datos durante la recuperación, ubicación en la que detener la recuperación o en el estado de recuperación.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)  
    
    Opciones de inicialización.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de instancia](./instance-class.md)

[Miembros de instancia](./instance-members.md)

[Sobrecarga init](./instance.init-method2.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
