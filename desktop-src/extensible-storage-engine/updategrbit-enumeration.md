---
description: 'Más información sobre: enumeración UpdateGrbit'
title: Enumeración UpdateGrbit (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: UpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.updategrbit(v=EXCHG.10)
ms:contentKeyID: 39514938
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e27809ef16fb00fd538e4c37826d10fefa3b396c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542414"
---
# <a name="updategrbit-enumeration"></a>Enumeración UpdateGrbit

Opciones para [JetUpdate2 (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, UpdateGrbit)](./server2003api.jetupdate2-method.md).

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration UpdateGrbit
'Usage
Dim instance As UpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum UpdateGrbit
```

## <a name="members"></a>Miembros

<table>
<thead>
<tr class="header">
<th></th>
<th>Nombre del miembro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>None</td>
<td>Opciones predeterminadas.</td>
</tr>
<tr class="even">
<td></td>
<td>CheckESE97Compatibility</td>
<td><strong>Obsoleto.</strong> Esta marca hace que la actualización devuelva un error si la actualización no hubiera sido posible en la versión de Windows 2000 de ESE, que aplicó un número máximo menor de instancias de columna multivalor en cada registro que en versiones posteriores de ESE. Esto solo es importante para las aplicaciones que desean replicar datos entre aplicaciones hospedadas en Windows 2000 y aplicaciones hospedadas en Windows 2003 o versiones posteriores de ESE. No debe ser necesario para la mayoría de las aplicaciones.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
