---
description: 'Más información sobre: constructor EsentException (String)'
title: Constructor EsentException (String) (Microsoft. ISAM. esent)
TOCTitle: EsentException constructor (String)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100720
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 22a93625b7becbe083a42fbd6fcc71ad801173ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707246"
---
# <a name="esentexception-constructor-string"></a>Constructor EsentException (String)

Inicializa una nueva instancia de la clase EsentException con un mensaje de error especificado.

**Espacio de nombres:**  [Microsoft. ISAM. esent](./microsoft.isam.esent-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Protected Sub New ( _
    message As String _
)
'Usage
Dim message As String

Dim instance As New EsentException(message)
```

``` csharp
protected EsentException(
    string message
)
```

#### <a name="parameters"></a>Parámetros

  - message  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Mensaje que describe el error.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase EsentException](./esentexception-class.md)

[Miembros de EsentException](./esentexception-members.md)

[Sobrecarga EsentException](./esentexception-constructor.md)

[Espacio de nombres Microsoft. ISAM. esent](./microsoft.isam.esent-namespace.md)
