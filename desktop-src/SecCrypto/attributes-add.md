---
description: Agrega un objeto Attribute a la colección.
ms.assetid: dc2fe542-7168-4ffa-a10d-b2c051c4d42c
title: Método Attributes.Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5639a4bed96dcf4cef315b4550cd2982778d6ecc68024364f06eb377cbd8b0d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773520"
---
# <a name="attributesadd-method"></a>Método Attributes.Add

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista, Windows XP. En su lugar, use [**la clase CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el [**espacio de nombres System.Security.Cryptography.**](/previous-versions/windows/)\]

El **método Add** agrega un objeto [**Attribute**](attribute.md) a la colección.

## <a name="syntax"></a>Sintaxis


```VB
Attributes.Add( _
  ByVal Attribute _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Atributo* \[ En\]
</dt> <dd>

Objeto [**Attribute**](attribute.md) que se va a agregar al final de la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor. Una aplicación que usa este método debe contener código para controlar una excepción que genera este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de criptografía](cryptography-objects.md)
</dt> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 
