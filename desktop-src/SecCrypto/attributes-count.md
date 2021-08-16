---
description: Recupera el número de objetos Attribute de la colección.
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Propiedad Attributes.Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d7b1f2213fc6de3ec08a9c9b568222f5dd54a6de6f9bdb3adb27e052e8c088e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773510"
---
# <a name="attributescount-property"></a>Propiedad Attributes.Count

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista, Windows XP. En su lugar, use [**la clase CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio [**de nombres System.Security.Cryptography.**](/previous-versions/windows/)\]

La **propiedad Count** recupera el número de objetos [**Attribute**](attribute.md) de la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Attributes.Count As Long
```



## <a name="property-value"></a>Valor de propiedad

Número de objetos [**Attribute**](attribute.md) de la colección. Cada **objeto Attribute** representa un único atributo de la colección.

## <a name="remarks"></a>Comentarios

La **propiedad Count** se puede usar para especificar el último objeto [**Attribute**](attribute.md) de la colección al recuperar un objeto **Attribute** específico mediante la [**propiedad Attributes.Item.**](attributes-item.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 
