---
description: 'Más información sobre: Constructor EsentStateException (String, JET_err)'
title: EsentStateException constructor (String, JET_err)
TOCTitle: EsentStateException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentStateException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102995
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 99a5e381eb05b634f8eb76b18a9ba5bd477abaf5f796834635793538394bf11b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118490601"
---
# <a name="esentstateexception-constructor-string-jet_err"></a>EsentStateException constructor (String, JET_err)

Inicializa una nueva instancia de la clase EsentStateException.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentStateException(description, _
    err)
```

``` csharp
protected EsentStateException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a>Parámetros

  - description  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Descripción del error.

<!-- end list -->

  - err  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)  
    
    Código de error de la excepción.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase EsentStateException](./esentstateexception-class.md)

[Miembros de EsentStateException](./esentstateexception-members.md)

[Sobrecarga de EsentStateException](./esentstateexception-constructor.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
