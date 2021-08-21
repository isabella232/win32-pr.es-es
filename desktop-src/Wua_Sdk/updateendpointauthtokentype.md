---
description: Define el tipo de tokens que se pueden usar para la autenticación con un punto de conexión.
ms.assetid: 2048BD09-056F-47C1-AD2F-998DE6C52EA6
title: Enumeración UpdateEndpointAuthTokenType (UpdateEndpointAuth.h)
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
ms.openlocfilehash: b9e3efbff48097dcede12d5c8d3117171ef622f20a3bf017b12c6d3ce13a1c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814717"
---
# <a name="updateendpointauthtokentype-enumeration"></a>Enumeración UpdateEndpointAuthTokenType

Define el tipo de tokens que se pueden usar para la autenticación con un punto de conexión.

## <a name="syntax"></a>Syntax


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

El token de autenticación para el punto de conexión es WS-Security saml (Lenguaje de marcado de aserción de seguridad) 1.1.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                              |
| Header<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |



 

 




