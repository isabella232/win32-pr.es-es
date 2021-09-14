---
description: 'Más información sobre: Constructor EsentIOException (String, JET_err)'
title: EsentIOException constructor (String, JET_err)
TOCTitle: EsentIOException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentIOException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentioexception.esentioexception(v=EXCHG.10)
ms:contentKeyID: 55102030
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentIOException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 087f22d7836ff41ac97b65c15be1b51dfac84a8b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966140"
---
# <a name="esentioexception-constructor-string-jet_err"></a>EsentIOException constructor (String, JET_err)

Inicializa una nueva instancia de la clase EsentIOException.

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

Dim instance As New EsentIOException(description, _
    err)
```

``` csharp
protected EsentIOException(
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

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase EsentIOException](./esentioexception-class.md)

[Miembros de EsentIOException](./esentioexception-members.md)

[Sobrecarga de EsentIOException](./esentioexception-constructor.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
