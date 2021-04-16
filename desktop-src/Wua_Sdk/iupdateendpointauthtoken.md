---
description: Proporciona los métodos que WUA puede usar para recopilar información sobre el token del extremo.
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: Interfaz IUpdateEndpointAuthToken (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a5902b3c91b3ab12b311121bd7dcd8c415a68d6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497608"
---
# <a name="iupdateendpointauthtoken-interface"></a>Interfaz IUpdateEndpointAuthToken

Proporciona los métodos que WUA puede usar para recopilar información sobre el token del extremo.

## <a name="members"></a>Miembros

La interfaz **IUpdateEndpointAuthToken** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUpdateEndpointAuthToken** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IUpdateEndpointAuthToken** tiene estos métodos.



| Método                                                                                | Descripción                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**ServiceID**](iupdateendpointauthtoken-serviceid.md)                               | Obtiene el identificador del servicio que se va a autenticar.<br/>                                                          |
| [**SigningKey**](iupdateendpointauthtoken-signingkey.md)                             | Obtiene la clave utilizada para firmar los mensajes salientes entre el equipo cliente y el sercvice.<br/>                        |
| [**TokenData**](iupdateendpointauthtoken-tokendata.md)                               | Obtiene los datos XML (enviados a través de la conexión) que representa el token. <br/>                                               |
| [**TokenReferenceAttached**](iupdateendpointauthtoken-tokenreferenceattached.md)     | Obtiene el formato XML de una referencia adjunta al token.<br/>                                                       |
| [**TokenReferenceUnattached**](iupdateendpointauthtoken-tokenreferenceunattached.md) | Obtiene el formato XML de una referencia no adjunta al token.<br/>                                                     |
| [**TokenType**](iupdateendpointauthtoken-tokentype.md)                               | Obtiene el tipo del token del punto de conexión, como un token WS-Security SAML (Lenguaje de marcado de aserción de seguridad) 1,1. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]<br/>                   |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]<br/>                |
| Encabezado<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
