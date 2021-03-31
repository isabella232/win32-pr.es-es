---
description: 'Más información acerca de: EsentErrorException. error (propiedad)'
title: EsentErrorException. error (propiedad)
TOCTitle: 'Error property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentErrorException.Error
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.error(v=EXCHG.10)
ms:contentKeyID: 55101646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.Error
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException.get_Error
- Microsoft.Isam.Esent.Interop.EsentErrorException.Error
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e777886ed95ea72a02626f7eb91724123a495f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279062"
---
# <a name="esenterrorexceptionerror-property"></a>EsentErrorException. error (propiedad)

Obtiene el error de esent subyacente para esta excepción.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public ReadOnly Property Error As JET_err
    Get
'Usage
Dim instance As EsentErrorException
Dim value As JET_err

value = instance.Error
```

``` csharp
public JET_err Error { get; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase EsentErrorException](./esenterrorexception-class.md)

[Miembros de EsentErrorException](./esenterrorexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
