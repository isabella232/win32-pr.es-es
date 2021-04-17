---
description: Recupera el número de objetos de atributo de la colección.
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Propiedad Attributes. Count
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
ms.openlocfilehash: 34a750b34f483342966ed1fcb3831d08b8df8f39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671028"
---
# <a name="attributescount-property"></a>Propiedad Attributes. Count

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography**](/previous-versions/windows/) .\]

La propiedad **Count** recupera el número de objetos de [**atributo**](attribute.md) de la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Attributes.Count As Long
```



## <a name="property-value"></a>Valor de propiedad

Número de objetos de [**atributo**](attribute.md) de la colección. Cada objeto de **atributo** representa un atributo único en la colección.

## <a name="remarks"></a>Observaciones

La propiedad **Count** se puede usar para especificar el último objeto de [**atributo**](attribute.md) de la colección al recuperar un objeto de **atributo** concreto mediante la propiedad [**Attributes. Item**](attributes-item.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 
