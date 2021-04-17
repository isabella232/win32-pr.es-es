---
description: 'Más información acerca de: JET_PFNSTATUS delegado'
title: JET_PFNSTATUS delegado
TOCTitle: JET_PFNSTATUS delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnstatus(v=EXCHG.10)
ms:contentKeyID: 39515654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.BeginInvoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16cc5807d858f964f995b449a0a0eee78659aefd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697455"
---
# <a name="jet_pfnstatus-delegate"></a>JET_PFNSTATUS delegado

Recibe información sobre el progreso de las operaciones de ejecución prolongada, como la desfragmentación, la copia de seguridad o las operaciones de restauración. Durante estas operaciones, el motor de base de datos llama a esta función de devolución de llamada para proporcionar una actualización en el progreso de la operación.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Delegate Function JET_PFNSTATUS ( _
    sesid As JET_SESID, _
    snp As JET_SNP, _
    snt As JET_SNT, _
    data As Object _
) As JET_err
'Usage
Dim instance As New JET_PFNSTATUS(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNSTATUS(
    JET_SESID sesid,
    JET_SNP snp,
    JET_SNT snt,
    Object data
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión con la que se llamó a la operación de larga ejecución.

<!-- end list -->

  - SNP  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SNP](./jet-snp-enumeration.md)  
    
    Tipo de operación.

<!-- end list -->

  - SNT  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SNT](./jet-snt-enumeration.md)  
    
    Estado de la operación.

<!-- end list -->

  - datos  
    Tipo: [System. Object](/dotnet/api/system.object)  
    
    Datos opcionales. Puede ser un [JET_SNPROG](./jet-snprog-class.md).

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
