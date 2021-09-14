---
description: 'Más información sobre: Constructor EsentObsoleteException (String, JET_err)'
title: EsentObsoleteException constructor (String, JET_err)
TOCTitle: EsentObsoleteException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentObsoleteException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102363
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 435a3db75cb09a47bccc311733b90fae30563c86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966036"
---
# <a name="esentobsoleteexception-constructor-string-jet_err"></a>EsentObsoleteException constructor (String, JET_err)

Inicializa una nueva instancia de la clase EsentObsoleteException.

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

Dim instance As New EsentObsoleteException(description, _
    err)
```

``` csharp
protected EsentObsoleteException(
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

[Clase EsentObsoleteException](./esentobsoleteexception-class.md)

[Miembros de EsentObsoleteException](./esentobsoleteexception-members.md)

[Sobrecarga de EsentObsoleteException](./esentobsoleteexception-constructor.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
