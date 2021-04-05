---
description: Códigos de error NSP de PNRP
ms.assetid: adf40b1a-c5d6-418d-a012-cf6ba7d4fa24
title: Códigos de error NSP de PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47b02959c921c8e3a468cadfa87dba6fb8d3c29d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909761"
---
# <a name="pnrp-nsp-error-codes"></a>Códigos de error NSP de PNRP

Si la función del proveedor de espacio de nombres (NSP) devuelve un **\_ error de socket**, se debe usar [WSAGetLastError](winsock-nsp-reference-links.md) para obtener más información sobre el error. El NSP de PNRP devuelve los siguientes códigos de error:



| Término                                                                                                                                                                     | Descripción                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>WSA \_ E \_ cancelada<br/>                                                                         | Se cancela una operación.<br/>                                                                               |
| <span id="__WSA_E_NO_MORE"></span><span id="__wsa_e_no_more"></span> WSA \_ E \_ no \_ más<br/>                                                                         | Los resultados de una solicitud resuelta no están listos. Esto puede no ser un error.<br/>                              |
| <span id="_WSA_IO_PENDING_"></span><span id="_wsa_io_pending_"></span>\_e/s de WSA \_ pendientes <br/>                                                                      | No se completó una operación.<br/>                                                                           |
| <span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span>WSA \_ no \_ hay suficiente \_ memoria<br/>                                                      | No hay suficiente memoria para completar una acción especificada.<br/>                                              |
| <span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span>\_operación WSA \_ anulada<br/>                                                       | Se cancela una operación.<br/>                                                                               |
| <span id="WSA_PNRP_CLOUD_DISABLED"></span><span id="wsa_pnrp_cloud_disabled"></span>\_nube PNRP de WSA \_ \_ deshabilitada<br/>                                                | Un nombre de nube especificado está deshabilitado.<br/>                                                                     |
| <span id="WSA_PNRP_CLOUD_NOT_FOUND"></span><span id="wsa_pnrp_cloud_not_found"></span>\_ \_ \_ no \_ se encuentra la nube PNRP de WSA<br/>                                            | Un nombre de nube especificado no está disponible.<br/>                                                                |
| <span id="WSA_PNRP_CLOUD_IS_SEARCH_ONLY"></span><span id="wsa_pnrp_cloud_is_search_only"></span>WSA \_ PNRP \_ Cloud \_ es \_ \_ solo búsqueda<br/>                            | Se ha intentado registrar un nombre en una nube que se ha configurado para resolverse únicamente.<br/>     |
| <span id="WSA_PNRP_CLIENT_INVALID_COMPARTMENT_ID"></span><span id="wsa_pnrp_client_invalid_compartment_id"></span>\_identificador de \_ \_ compartimiento no válido de cliente \_ PNRP WSA \_<br/> | Usar PNRP en un compartimiento fuera del valor predeterminado. PNRP solo funcionará en el compartimiento predeterminado.<br/>     |
| <span id="WSA_PNRP_INVALID_IDENTITY"></span><span id="wsa_pnrp_invalid_identity"></span>\_ \_ identidad incorrecta de PNRP de WSA \_<br/>                                          | No se puede tener acceso a una identidad especificada.<br/>                                                                |
| <span id="WSA_PNRP_TOO_MUCH_LOAD"></span><span id="wsa_pnrp_too_much_load"></span>\_ \_ \_ gran carga de PNRP \_ de WSA<br/>                                                  | No se puede crear un nombre de mismo nivel porque el equipo no tiene los recursos necesarios para procesar la solicitud. <br/> |
| <span id="WSAEFAULT"></span><span id="wsaefault"></span>WSAEFAULT<br/>                                                                                             | No se permite una operación en el estado actual.<br/>                                                        |
| <span id="WSAEINVAL"></span><span id="wsaeinval"></span>WSAEINVAL<br/>                                                                                             | Se ha especificado un parámetro o una combinación de parámetros no válidos.<br/>                                         |
| <span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>WSAENETUNREACH<br/>                                                                              | Se pierde una conexión a la red.<br/>                                                                    |
| <span id="WSAENOTIMPLEMENTED"></span><span id="wsaenotimplemented"></span>WSAENOTIMPLEMENTED<br/>                                                                  | PNRP no implementa una funcionalidad especificada.<br/>                                                   |
| <span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>WSAEOPNOTSUPP<br/>                                                                                 | PNRP no admite una funcionalidad especificada.<br/>                                                     |
| <span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>WSAEWOULDBLOCK<br/>                                                                              | No se completó una operación.<br/>                                                                           |
| <span id="__WSASERVICE_NOT_FOUND"></span><span id="__wsaservice_not_found"></span>\_no \_ se encontró WSASERVICE<br/>                                                     | No se admite un proveedor especificado, un espacio de nombres o un identificador de servicio.<br/>                                       |
| <span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>WSASYSNOTREADY<br/>                                                                              | No se ha iniciado el servicio.<br/>                                                                             |



 

 

 




