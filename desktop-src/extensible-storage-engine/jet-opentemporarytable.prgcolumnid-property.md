---
description: 'Más información acerca de: propiedad JET_OPENTEMPORARYTABLE. prgcolumnid'
title: Propiedad JET_OPENTEMPORARYTABLE. prgcolumnid (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'prgcolumnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.prgcolumnid(v=EXCHG.10)
ms:contentKeyID: 55104133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_prgcolumnid
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_prgcolumnid
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd6516e01d08de32f7962a48d2caca69ddbf0427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002898"
---
# <a name="jet_opentemporarytableprgcolumnid-property"></a>Propiedad JET_OPENTEMPORARYTABLE. prgcolumnid

Obtiene o establece el búfer de salida que recibe la matriz de identificadores de columna generados durante la creación de la tabla temporal. Los identificadores de columna de esta matriz se corresponden exactamente con la matriz de entrada de definiciones de columna. Como resultado, el tamaño de este búfer debe corresponder al tamaño de [prgcolumndef](./jet-opentemporarytable.prgcolumndef-property.md).

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property prgcolumnid As JET_COLUMNID()
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_COLUMNID()

value = instance.prgcolumnid

instance.prgcolumnid = value
```

``` csharp
public JET_COLUMNID[] prgcolumnid { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Automáticamente \[\]  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_OPENTEMPORARYTABLE (clase)](./jet-opentemporarytable-class.md)

[Miembros de JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
