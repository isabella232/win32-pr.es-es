---
description: 'Más información sobre: enumeración JET_InstanceMiscInfo datos'
title: JET_InstanceMiscInfo enumeración (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: JET_InstanceMiscInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_instancemiscinfo(v=EXCHG.10)
ms:contentKeyID: 39516547
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo
- Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo.LogSignature
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo.LogSignature
- Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: acf008b1a349ab2ddfe735dab45214cb19a71fe9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964304"
---
# <a name="jet_instancemiscinfo-enumeration"></a>JET_InstanceMiscInfo enumeración

Niveles de información [para JetGetInstanceMiscInfo(JET_INSTANCE, JET_SIGNATURE, JET_InstanceMiscInfo).](./vistaapi.jetgetinstancemiscinfo-method.md)

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration JET_InstanceMiscInfo
'Usage
Dim instance As JET_InstanceMiscInfo
```

``` csharp
[FlagsAttribute]
public enum JET_InstanceMiscInfo
```

## <a name="members"></a>Members

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
<td>LogSignature</td>
<td>Obtenga la firma del registro de transacciones asociado a esta secuencia.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
