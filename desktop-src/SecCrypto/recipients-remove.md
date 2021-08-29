---
description: Quita un objeto Certificate de una colección Recipients.
ms.assetid: bb75f6d0-4bab-40dd-9d0c-f0431da9c5f3
title: Método Recipients.Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0da608dcafc8fc0c2341a053679dee0f8d2715c34dcbfb28e84bee02aa658093
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900765"
---
# <a name="recipientsremove-method"></a>Método Recipients.Remove

\[El **método Remove** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **método Remove** quita un objeto [**Certificate**](certificate.md) de una [**colección Recipients.**](recipients.md)

## <a name="syntax"></a>Sintaxis


```VB
Recipients.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ En\]
</dt> <dd>

Índice del objeto [**Certificate que**](certificate.md) se va a quitar de la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> <dt>

[**Recipients**](recipients.md)
</dt> </dl>

 

 
