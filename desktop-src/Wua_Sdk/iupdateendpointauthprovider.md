---
description: Contiene los métodos que se usan para negociar el tipo de token que se utiliza para autenticar el extremo de un servicio.
ms.assetid: F6177B24-C166-4BEC-83D6-3AD5B5B3CF08
title: Interfaz IUpdateEndpointAuthProvider (UpdateEndpointAuth. h)
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
ms.openlocfilehash: 071bc23bdf9d67412fef561c71e17fe81485984f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542270"
---
# <a name="iupdateendpointauthprovider-interface"></a>Interfaz IUpdateEndpointAuthProvider

La interfaz **IUpdateEndpointAuthProvider** contiene los métodos que se usan para negociar el tipo de token que se utiliza para autenticar el extremo de un servicio.

## <a name="members"></a>Miembros

La interfaz **IUpdateEndpointAuthProvider** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUpdateEndpointAuthProvider** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IUpdateEndpointAuthProvider** tiene estos métodos.



| Método                                                                                             | Descripción                                                                                    |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)                           | Solicite un token para el extremo del servicio con las credenciales especificadas.<br/>    |
| [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) | Devuelve el tipo de token de autenticación preferido para el extremo del servicio.<br/> |



 

## <a name="remarks"></a>Observaciones

WUA llama al método [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) de esta interfaz para iniciar el proceso de negociación. Cuando se realiza la llamada, se pasa WUA en el identificador de servicio, el tipo de extremo implementado por el servicio y los tipos de token que están disponibles. A continuación, la implementación de esta interfaz devuelve los tipos de token que prefiere usar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]<br/>                   |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]<br/>                |
| Encabezado<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
