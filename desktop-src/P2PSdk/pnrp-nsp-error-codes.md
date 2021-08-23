---
description: Códigos de error de PNRP NSP
ms.assetid: adf40b1a-c5d6-418d-a012-cf6ba7d4fa24
title: Códigos de error de PNRP NSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acee7465a86d56af9b2e07a1ae6948dd1b1a1e9145cee2165b7dd4e90f2a5f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061362"
---
# <a name="pnrp-nsp-error-codes"></a>Códigos de error de PNRP NSP

Si la función Proveedor de espacios de nombres (NSP) devuelve un ERROR DE **\_ SOCKET,** [WSAGetLastError](winsock-nsp-reference-links.md) debe usarse para obtener más información de error. El PNRP NSP devuelve los siguientes códigos de error:



| Término                                                                                                                                                                     | Descripción                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>WSA \_ E \_ CANCELLED<br/>                                                                         | Se cancela una operación.<br/>                                                                               |
| <span id="__WSA_E_NO_MORE"></span><span id="__wsa_e_no_more"></span> WSA \_ E \_ NO \_ MORE<br/>                                                                         | Los resultados de una solicitud resuelta no están listos. Esto puede no ser un error.<br/>                              |
| <span id="_WSA_IO_PENDING_"></span><span id="_wsa_io_pending_"></span> WSA \_ IO \_ PENDING <br/>                                                                      | Una operación no está completa.<br/>                                                                           |
| <span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span>WSA \_ NO TIENE MEMORIA \_ \_ SUFICIENTE<br/>                                                      | No hay suficiente memoria para completar una acción especificada.<br/>                                              |
| <span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span>OPERACIÓN WSA \_ \_ ANULADA<br/>                                                       | Se cancela una operación.<br/>                                                                               |
| <span id="WSA_PNRP_CLOUD_DISABLED"></span><span id="wsa_pnrp_cloud_disabled"></span>WSA \_ PNRP \_ CLOUD \_ DISABLED<br/>                                                | Un nombre de nube especificado está deshabilitado.<br/>                                                                     |
| <span id="WSA_PNRP_CLOUD_NOT_FOUND"></span><span id="wsa_pnrp_cloud_not_found"></span>WSA \_ PNRP \_ CLOUD \_ NOT \_ FOUND<br/>                                            | Un nombre de nube especificado no está disponible.<br/>                                                                |
| <span id="WSA_PNRP_CLOUD_IS_SEARCH_ONLY"></span><span id="wsa_pnrp_cloud_is_search_only"></span>WSA \_ PNRP \_ CLOUD \_ IS \_ SEARCH \_ ONLY<br/>                            | Se ha intentado registrar un nombre en una nube que se ha configurado para resolverse únicamente.<br/>     |
| <span id="WSA_PNRP_CLIENT_INVALID_COMPARTMENT_ID"></span><span id="wsa_pnrp_client_invalid_compartment_id"></span>IDENTIFICADOR DE COMPARTIMIENTO NO VÁLIDO DEL CLIENTE DE WSA \_ PNRP \_ \_ \_ \_<br/> | Usar PNRP en un compartimiento fuera del valor predeterminado. PNRP solo funcionará en el compartimiento predeterminado.<br/>     |
| <span id="WSA_PNRP_INVALID_IDENTITY"></span><span id="wsa_pnrp_invalid_identity"></span>IDENTIDAD NO VÁLIDA DE WSA \_ PNRP \_ \_<br/>                                          | No se puede acceder a una identidad especificada.<br/>                                                                |
| <span id="WSA_PNRP_TOO_MUCH_LOAD"></span><span id="wsa_pnrp_too_much_load"></span>DEMASIADA CARGA \_ DE WSA PNRP \_ \_ \_<br/>                                                  | No se puede crear un nombre del mismo nivel porque el equipo no tiene los recursos para procesar la solicitud. <br/> |
| <span id="WSAEFAULT"></span><span id="wsaefault"></span>WSAEFAULT<br/>                                                                                             | No se permite una operación en el estado actual.<br/>                                                        |
| <span id="WSAEINVAL"></span><span id="wsaeinval"></span>WSAEINVAL<br/>                                                                                             | Se especifica un parámetro no válido o una combinación de parámetros.<br/>                                         |
| <span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>WSAENETUNREACH<br/>                                                                              | Se pierde una conexión a la red.<br/>                                                                    |
| <span id="WSAENOTIMPLEMENTED"></span><span id="wsaenotimplemented"></span>WSAENOTIMPLEMENTED<br/>                                                                  | PNRP no implementa una funcionalidad especificada.<br/>                                                   |
| <span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>WSAEOPNOTSUPP<br/>                                                                                 | PNRP no admite una funcionalidad especificada.<br/>                                                     |
| <span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>WSAEWOULDBLOCK<br/>                                                                              | Una operación no está completa.<br/>                                                                           |
| <span id="__WSASERVICE_NOT_FOUND"></span><span id="__wsaservice_not_found"></span> WSASERVICE \_ NO \_ ENCONTRADO<br/>                                                     | No se admite un proveedor, espacio de nombres o identificador de servicio especificados.<br/>                                       |
| <span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>WSASYSNOTREADY<br/>                                                                              | El servicio no se inicia.<br/>                                                                             |



 

 

 




