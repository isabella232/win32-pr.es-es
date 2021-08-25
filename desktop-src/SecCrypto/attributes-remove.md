---
description: Quita un objeto Attribute indexado de la colección.
ms.assetid: 6d9423e3-ab24-4973-b0aa-32e38abd607a
title: Método Attributes.Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ea18aab32153c998a0ddbaced65727e1ecb43dc8c54a7e3989aadcb698693970
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879775"
---
# <a name="attributesremove-method"></a>Método Attributes.Remove

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista, Windows XP. En su lugar, use [**la clase CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el [**espacio de nombres System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **método Remove** quita un objeto [**Attribute**](attribute.md) indexado de la colección.

## <a name="syntax"></a>Sintaxis


```VB
Attributes.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ En\]
</dt> <dd>

Índice del objeto [**Attribute**](attribute.md) que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Las aplicaciones que usan este método deben contener código para controlar una excepción que genera este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de criptografía](cryptography-objects.md)
</dt> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 
