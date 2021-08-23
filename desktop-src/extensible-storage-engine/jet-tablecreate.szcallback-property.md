---
description: 'Más información sobre: JET_TABLECREATE.szCallback'
title: JET_TABLECREATE.szCallback, propiedad
TOCTitle: 'szCallback property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate.szcallback(v=EXCHG.10)
ms:contentKeyID: 55103969
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.set_szCallback
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.get_szCallback
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 414abc99547a07f46902a355efcb42ce01cd6bde24c84d3a0ca309b008ef02c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729065"
---
# <a name="jet_tablecreateszcallback-property"></a>JET_TABLECREATE.szCallback, propiedad

Obtiene o establece una función de devolución de llamada que se va a usar para la tabla. Tiene el formato "module \! functionName" y supone código no administrado. Consulte **JetRegisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)** para obtener una alternativa.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property szCallback As String
    Get
    Set
'Usage
Dim instance As JET_TABLECREATE
Dim value As String

value = instance.szCallback

instance.szCallback = value
```

``` csharp
public string szCallback { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System.String](/dotnet/api/system.string)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_TABLECREATE clase](./jet-tablecreate-class.md)

[JET_TABLECREATE miembros](./jet-tablecreate-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
