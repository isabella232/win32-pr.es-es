---
description: Quita todos los objetos Certificate de una colección Recipients.
ms.assetid: 456fcfbc-4388-40f4-ab58-04508ee2141b
title: Método Recipients.Clear
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c956aacd7b61243fbaeb26ed1a29ed0fee4522d83d8b4ef3ac25b3b1921b42a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900812"
---
# <a name="recipientsclear-method"></a>Método Recipients.Clear

\[El **método Clear** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **método Clear** quita todos los objetos [**Certificate**](certificate.md) de una [**colección Recipients.**](recipients.md)

## <a name="syntax"></a>Sintaxis


```VB
Recipients.Clear()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor. Una aplicación que usa este método debe contener código para controlar una excepción que genera este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> <dt>

[**Recipients**](recipients.md)
</dt> </dl>

 

 
