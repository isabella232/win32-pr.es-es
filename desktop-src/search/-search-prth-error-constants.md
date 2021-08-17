---
description: 'Mensajes de error devueltos por controladores de protocolo:'
ms.assetid: b5e99ad1-1698-483c-8173-796af33085c4
title: Mensajes de error del controlador de protocolo de búsqueda (Searchapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4473e3e235641e5b4bb5d86313b4154cd00ec029fe96d42d8964dab51f33780f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969734"
---
# <a name="search-protocol-handler-error-messages"></a>Mensajes de error del controlador de protocolo de búsqueda

Mensajes de error devueltos por controladores de protocolo:



| Constante o valor                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRTH_E_ACCESS_DENIED"></span><span id="prth_e_access_denied"></span><dl> <dt>**PRTH \_ ACCESO \_ \_ DENEGADO E**</dt> <dt>0x80041205L</dt> </dl>             | Se denegó el acceso. Si esto ocurre durante un rastreo incremental, el archivo se elimina de la cola de direcciones URL del recopilador.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_IS_READ_NONE"></span><span id="prth_e_acl_is_read_none"></span><dl> <dt>**PRTH \_ E \_ ACL IS READ \_ \_ \_ NONE**</dt> <dt>0x80041211L</dt> </dl>  | El elemento no se indexará. Su ACL no permite que nadie lea el elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_TOO_BIG"></span><span id="prth_e_acl_too_big"></span><dl> <dt>**PRTH \_ E \_ ACL \_ TOO \_ BIG**</dt> <dt>0x80041212L</dt> </dl>                  | La ACL superó los 64 KB. La búsqueda no indexa el elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_BAD_REQUEST"></span><span id="prth_e_bad_request"></span><dl> <dt>**PRTH \_ E \_ BAD \_ REQUEST**</dt> <dt>0x80041208L</dt> </dl>                   | La solicitud no era válida debido a un error en la dirección URL.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_COMM_ERROR"></span><span id="prth_e_comm_error"></span><dl> <dt>**PRTH \_ E \_ COMM \_ ERROR**</dt> <dt>0x80041200L</dt> </dl>                      | Indica un error de comunicación o de servidor. Si hay demasiados errores para un servidor determinado, el recopilador marca el servidor como no disponible.<br/>                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_NOT_REDIRECTED"></span><span id="prth_e_not_redirected"></span><dl> <dt>**PRTH \_ E \_ NOT \_ REDIRECTED**</dt> <dt>0x80041207L</dt> </dl>          | La dirección URL redirigida no existe.<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_E_OBJ_NOT_FOUND"></span><span id="prth_e_obj_not_found"></span><dl> <dt>**PRTH \_ E \_ OBJ \_ NOT \_ FOUND**</dt> <dt>0x80041201L</dt> </dl>            | Objeto no encontrado. Indica que el recopilador debe eliminar el documento de la cola si no se encuentra durante un rastreo incremental.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_REQUEST_ERROR"></span><span id="prth_e_request_error"></span><dl> <dt>**PRTH \_ E \_ REQUEST \_ ERROR**</dt> <dt>0x80041202L</dt> </dl>             | No se admiten las opciones usadas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="PRTH_E_SERVER_ERROR"></span><span id="prth_e_server_error"></span><dl> <dt>**PRTH \_ ERROR \_ DEL \_ SERVIDOR**</dt> <dt>E 0x80041206L</dt> </dl>                | Error de comunicación o de servidor. Si hay demasiados errores para un servidor determinado, el recopilador marca el servidor como no disponible.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PRTH_S_NOT_ALL_PARTS"></span><span id="prth_s_not_all_parts"></span><dl> <dt>**PRTH \_ S \_ NOT \_ ALL \_ PARTS**</dt> <dt>0x8004121BL</dt> </dl>            | No se puede acceder a partes de un elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="PRTH_S_NOT_MODIFIED"></span><span id="prth_s_not_modified"></span><dl> <dt>**PRTH \_ S \_ NO \_ MODIFICADO**</dt> <dt>0x00041203L</dt> </dl>                | El contenido del elemento no ha cambiado. Si este error se produce durante un rastreo incremental, el recopilador omite este elemento porque el elemento no ha cambiado.<br/>                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_S_TRY_IMPERSONATING"></span><span id="prth_s_try_impersonating"></span><dl> <dt>**PRTH \_ S \_ TRY \_ IMPERSONATING**</dt> <dt>0x00041225L</dt> </dl> | Se debe tener acceso al elemento al suplantar a un usuario. Se espera que el controlador de protocolo implemente [**IUrlAccessor3::GetImpersonationSidBlobs**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor3-getimpersonationsidblobs) para que el host del protocolo de búsqueda pueda recuperar una lista de SID que se usarán para la suplantación y pueda revertir al uso de [**IUrlAccessor2,**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2)suplantando a uno de los usuarios permitidos al abrir el elemento. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo Windows de \[ escritorio de Vista\]<br/>                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>                                            |
| Header<br/>                   | <dl> <dt>Searchapi.h</dt> </dl> |



 

 




