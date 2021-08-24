---
description: 'Más información sobre: JET_INDEXCREATE.szKey'
title: JET_INDEXCREATE.szKey, propiedad
TOCTitle: 'szKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.szkey(v=EXCHG.10)
ms:contentKeyID: 55103656
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 905bc6e72704121617a2fcc2b9b368bee9014f897ce157f473e3f9ced5a92c72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720575"
---
# <a name="jet_indexcreateszkey-property"></a>JET_INDEXCREATE.szKey, propiedad

Obtiene o establece la descripción de la clave de índice. Se trata de una cadena doble terminada en NULL de tokens delimitados por null. Cada token tiene el formato \[ direction-specifier \] \[ column-name , donde \] direction-specification es "+" o "-". Por ejemplo, un szKey de "+abc 0-def 0+ghi 0" se indexará sobre las tres columnas \\ \\ \\ "abc" (en orden ascendente), "def" (en orden descendente) y "ghi" (en orden ascendente).

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property szKey As String
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As String

value = instance.szKey

instance.szKey = value
```

``` csharp
public string szKey { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System.String](/dotnet/api/system.string)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_INDEXCREATE clase](./jet-indexcreate-class.md)

[JET_INDEXCREATE miembros](./jet-indexcreate-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
