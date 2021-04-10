---
description: 'Mensajes de error devueltos por los controladores de protocolo:'
ms.assetid: b5e99ad1-1698-483c-8173-796af33085c4
title: Mensajes de error del controlador de búsqueda (Searchapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 297ea44c367069a5558355cf6fe81cd9db57ee53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153967"
---
# <a name="search-protocol-handler-error-messages"></a>Mensajes de error del controlador de búsqueda

Mensajes de error devueltos por los controladores de protocolo:



| Constante o valor                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRTH_E_ACCESS_DENIED"></span><span id="prth_e_access_denied"></span><dl> <dt>**PRTH \_ E \_ acceso \_ denegado a**</dt> <dt>0x80041205L</dt> </dl>             | Se denegó el acceso. Si esto ocurre durante un rastreo incremental, el archivo se elimina de la cola de direcciones URL del recopilador.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_IS_READ_NONE"></span><span id="prth_e_acl_is_read_none"></span><dl> <dt>**PRTH \_ La \_ ACL de E \_ no es \_ Read \_ None**</dt> <dt>0x80041211L</dt> </dl>  | No se indizará el elemento. Su ACL permite a nadie leer el elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_TOO_BIG"></span><span id="prth_e_acl_too_big"></span><dl> <dt>**PRTH \_ E \_ ACL \_ demasiado \_ grande**</dt> <dt>0x80041212L</dt> </dl>                  | ACL superó 64 KB. La búsqueda no indiza el elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_BAD_REQUEST"></span><span id="prth_e_bad_request"></span><dl> <dt>**PRTH \_ E \_ \_ Solicitud incorrecta**</dt> <dt>0x80041208L</dt> </dl>                   | La solicitud no era válida debido a un error en la dirección URL.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_COMM_ERROR"></span><span id="prth_e_comm_error"></span><dl> <dt>**PRTH \_ E \_ \_**</dt> <dt>0x80041200L</dt> de error de comunicación </dl>                      | Indica un error de comunicación o de servidor. Si hay demasiados errores para un servidor determinado, el recopilador marca el servidor como no disponible.<br/>                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_NOT_REDIRECTED"></span><span id="prth_e_not_redirected"></span><dl> <dt>**PRTH \_ E \_ no \_**</dt> <dt>0x80041207L</dt> Redirigido </dl>          | La dirección URL redirigida no existe.<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_E_OBJ_NOT_FOUND"></span><span id="prth_e_obj_not_found"></span><dl> <dt>**PRTH \_ E \_ \_ no \_ se encontró**</dt> el <dt>0x80041201L</dt> </dl>            | Objeto no encontrado. Indica que el recopilador debe eliminar el documento de la cola si no se encuentra durante un rastreo incremental.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_REQUEST_ERROR"></span><span id="prth_e_request_error"></span><dl> <dt>**PRTH \_ E \_ \_**</dt> <dt>0x80041202L</dt> de error de solicitud </dl>             | No se admiten las opciones usadas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="PRTH_E_SERVER_ERROR"></span><span id="prth_e_server_error"></span><dl> <dt>**PRTH \_ E \_ \_**</dt> <dt>0x80041206L</dt> de errores del servidor </dl>                | Error de comunicación o de servidor. Si hay demasiados errores para un servidor determinado, el recopilador marca el servidor como no disponible.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PRTH_S_NOT_ALL_PARTS"></span><span id="prth_s_not_all_parts"></span><dl> <dt>**PRTH \_ \_No \_ todas las \_ partes**</dt> <dt>0x8004121BL</dt> </dl>            | No se puede tener acceso a las partes de un elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="PRTH_S_NOT_MODIFIED"></span><span id="prth_s_not_modified"></span><dl> <dt>**PRTH \_ S \_ no \_ modificado**</dt> <dt>0x00041203L</dt> </dl>                | El contenido del elemento no ha cambiado. Si este error se produce durante un rastreo incremental, el recopilador omite este elemento porque el elemento no ha cambiado.<br/>                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_S_TRY_IMPERSONATING"></span><span id="prth_s_try_impersonating"></span><dl> <dt>**PRTH \_ S \_ intentar \_ Suplantar**</dt> <dt>0x00041225L</dt> </dl> | Se debe tener acceso al elemento durante la suplantación de un usuario. Se espera que el controlador de protocolo implemente [**IUrlAccessor3:: GetImpersonationSidBlobs**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor3-getimpersonationsidblobs) para que el host del Protocolo de búsqueda pueda recuperar una lista de SID que se usarán para la suplantación y pueda revertir al uso de [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2), suplantando a uno de los usuarios permitidos al abrir el elemento. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]<br/>                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Redistribuible<br/>          | Búsqueda en el escritorio de Windows (WDS) 3,0<br/>                                            |
| Encabezado<br/>                   | <dl> <dt>Searchapi. h</dt> </dl> |



 

 




