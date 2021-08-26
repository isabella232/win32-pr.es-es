---
description: Contiene los métodos usados para negociar qué tipo de token se usa para autenticar el punto de conexión de un servicio.
ms.assetid: F6177B24-C166-4BEC-83D6-3AD5B5B3CF08
title: Interfaz IUpdateEndpointAuthProvider (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 3cbc51ab0f1192e20612829532b907e3644a7da3f99fdedd8e3dbd45a780c54d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994575"
---
# <a name="iupdateendpointauthprovider-interface"></a>IUpdateEndpointAuthProvider (interfaz)

La **interfaz IUpdateEndpointAuthProvider** contiene los métodos usados para negociar qué tipo de token se usa para autenticar el punto de conexión de un servicio.

## <a name="members"></a>Miembros

La **interfaz IUpdateEndpointAuthProvider** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IUpdateEndpointAuthProvider** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IUpdateEndpointAuthProvider** tiene estos métodos.



| Método                                                                                             | Descripción                                                                                    |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)                           | Solicite un token para el punto de conexión del servicio con las credenciales especificadas.<br/>    |
| [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) | Devuelve el tipo preferido de token de autenticación para el punto de conexión del servicio.<br/> |



 

## <a name="remarks"></a>Comentarios

WUA llama al [**método GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) de esta interfaz para iniciar el proceso de negociación. Cuando se realiza la llamada, WUA pasa el identificador de servicio, el tipo de punto de conexión implementado por el servicio y los tipos de token que están disponibles. A continuación, la implementación de esta interfaz devuelve los tipos de token que prefiere usar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio SP3 \[\]<br/>                   |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>                |
| Header<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
