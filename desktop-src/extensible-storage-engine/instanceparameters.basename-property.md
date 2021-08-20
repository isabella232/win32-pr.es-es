---
description: 'Más información sobre: Propiedad InstanceParameters.BaseName'
title: Propiedad InstanceParameters.BaseName
TOCTitle: 'BaseName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.BaseName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.basename(v=EXCHG.10)
ms:contentKeyID: 55103315
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.BaseName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.BaseName
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_BaseName
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_BaseName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe441036dbd4ae4b6c861e17e73596ef194cd05f2ad7fa46eb5c8fd8f5d8dbcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112468"
---
# <a name="instanceparametersbasename-property"></a>Propiedad InstanceParameters.BaseName

Obtiene o establece el prefijo de tres letras utilizado para muchos de los archivos usados por el motor de base de datos. Por ejemplo, el archivo de punto de comprobación se denomina EDB. CHK de forma predeterminada porque EDB es el nombre base predeterminado.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property BaseName As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.BaseName

instance.BaseName = value
```

``` csharp
public string BaseName { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System.String](/dotnet/api/system.string)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase InstanceParameters](./instanceparameters-class.md)

[Miembros InstanceParameters](./instanceparameters-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
