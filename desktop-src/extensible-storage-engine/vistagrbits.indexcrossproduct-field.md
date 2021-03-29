---
description: 'Más información sobre: VistaGrbits. IndexCrossProduct, campo'
title: Campo VistaGrbits. IndexCrossProduct (Microsoft. ISAM. esent. Interop. vista)
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
ms.openlocfilehash: f1b16f741c63d455d18a887331505080aef62990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003167"
---
# <a name="vistagrbitsindexcrossproduct-field"></a>VistaGrbits. IndexCrossProduct, campo

Si se especifica esta marca para un índice que tiene más de una columna de clave que es una columna con varios valores, se creará una entrada de índice para cada resultado de un producto cruzado de todos los valores de esas columnas de clave. De lo contrario, el índice solo tendrá una entrada para cada valor múltiple de la columna de clave más importante que sea una columna con varios valores y cada una de esas entradas de índice usaría el primer valor entre las demás columnas de clave que son columnas con varios valores. Por ejemplo, si especificó esta marca para un índice sobre la columna A que tiene los valores "rojo" y "azul" y sobre la columna B que tiene los valores "1" y "2", se crearán las siguientes entradas de índice: "rojo", "1"; "rojo", "2"; "Blue", "1"; "Blue", "2". De lo contrario, se crearán las siguientes entradas de índice: "red", "1"; "Blue", "1".

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

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

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase VistaGrbits](./vistagrbits-class.md)

[Miembros de VistaGrbits](./vistagrbits-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
