---
description: Proporciona los métodos que WUA puede usar para recopilar información sobre el token de punto de conexión.
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: Interfaz IUpdateEndpointAuthToken (UpdateEndpointAuth.h)
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
ms.openlocfilehash: 7b5afa1e9039b7f210dfbf71c8bceff4a7b438b413844a7a7e55dec0fd9fea8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855765"
---
# <a name="iupdateendpointauthtoken-interface"></a>Interfaz IUpdateEndpointAuthToken

Proporciona los métodos que WUA puede usar para recopilar información sobre el token de punto de conexión.

## <a name="members"></a>Miembros

La **interfaz IUpdateEndpointAuthToken** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IUpdateEndpointAuthToken** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IUpdateEndpointAuthToken** tiene estos métodos.



| Método                                                                                | Descripción                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**ServiceID**](iupdateendpointauthtoken-serviceid.md)                               | Obtiene el identificador del servicio que se va a autenticar.<br/>                                                          |
| [**SigningKey**](iupdateendpointauthtoken-signingkey.md)                             | Obtiene la clave utilizada para firmar los mensajes salientes entre el equipo cliente y el servidor.<br/>                        |
| [**TokenData**](iupdateendpointauthtoken-tokendata.md)                               | Obtiene los datos XML (enviados a través de la conexión) que representa el token. <br/>                                               |
| [**TokenReferenceAttached**](iupdateendpointauthtoken-tokenreferenceattached.md)     | Obtiene el formato XML de una referencia adjunta al token.<br/>                                                       |
| [**TokenReferenceUnattached**](iupdateendpointauthtoken-tokenreferenceunattached.md) | Obtiene el formato XML de una referencia no separada al token.<br/>                                                     |
| [**TokenType**](iupdateendpointauthtoken-tokentype.md)                               | Obtiene el tipo del token de punto de conexión, como un token WS-Security SAML (Lenguaje de marcado de aserción de seguridad) 1.1. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]<br/>                   |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>                |
| Header<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
