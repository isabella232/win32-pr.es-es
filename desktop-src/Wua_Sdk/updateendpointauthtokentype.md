---
description: Define el tipo de tokens que se pueden utilizar para la autenticación con un punto de conexión.
ms.assetid: 2048BD09-056F-47C1-AD2F-998DE6C52EA6
title: Enumeración UpdateEndpointAuthTokenType (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointAuthTokenType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: c978841511b7cfff895a15936a41d169a8500927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714991"
---
# <a name="updateendpointauthtokentype-enumeration"></a>Enumeración UpdateEndpointAuthTokenType

Define el tipo de tokens que se pueden utilizar para la autenticación con un punto de conexión.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagUpdateEndpointAuthTokenType { 
  ueattInvalidTokenType  = 0x0,
  ueattSAML11Token       = 0X1
} UpdateEndpointAuthTokenType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**
</dt> <dd>

No se necesita ningún token de autenticación.

</dd> <dt>

<span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**
</dt> <dd>

El token de autenticación para el punto de conexión es un token WS-Security SAML (Lenguaje de marcado de aserción de seguridad) 1,1.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                              |
| Encabezado<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |



 

 




