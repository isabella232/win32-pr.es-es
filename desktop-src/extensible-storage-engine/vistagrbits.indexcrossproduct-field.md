---
description: 'Más información sobre: Campo VistaGrbits.IndexCrossProduct'
title: Campo VistaGrbits.IndexCrossProduct (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: IndexCrossProduct field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits.indexcrossproduct(v=EXCHG.10)
ms:contentKeyID: 55104426
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad3828411177d1c500c1b21b62797f093143ba1ac5b9770d9d6444d5c1a7aa9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471135"
---
# <a name="vistagrbitsindexcrossproduct-field"></a>Campo VistaGrbits.IndexCrossProduct

Si se especifica esta marca para un índice que tiene más de una columna de clave que es una columna con varios valores, se creará una entrada de índice para cada resultado de un producto cruzado de todos los valores de esas columnas de clave. De lo contrario, el índice solo tendría una entrada para cada valor múltiple en la columna de clave más significativa que es una columna con varios valores y cada una de esas entradas de índice usaría el primer valor múltiple de cualquier otra columna de clave que sea de varias columnas con varios valores. Por ejemplo, si especificó esta marca para un índice sobre la columna A que tiene los valores "red" y "blue" y sobre la columna B que tiene los valores "1" y "2", se crearían las siguientes entradas de índice: "red", "1"; "red", "2"; "blue", "1"; "blue", "2". De lo contrario, se crearían las siguientes entradas de índice: "red", "1"; "blue", "1".

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Const IndexCrossProduct As CreateIndexGrbit
'Usage
Dim value As CreateIndexGrbit

value = VistaGrbits.IndexCrossProduct
```

``` csharp
public const CreateIndexGrbit IndexCrossProduct
```

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[VistaGrbits (clase)](./vistagrbits-class.md)

[Miembros de VistaGrbits](./vistagrbits-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
