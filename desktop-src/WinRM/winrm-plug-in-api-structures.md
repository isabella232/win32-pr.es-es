---
title: Estructuras de la API del complemento de WinRM
description: Estructuras de la API del complemento de WinRM
ms.assetid: 745619bc-c7b3-48fa-8212-cb1b5b9ed4db
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685bcf87ef8c634db367db62b3ec1472b50e3b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357423"
---
# <a name="winrm-plug-in-api-structures"></a>Estructuras de la API del complemento de WinRM

En la tabla siguiente se proporciona información general sobre las estructuras de la interfaz de programación de aplicaciones (API) de complementos de Administración remota de Windows (WinRM).



| Estructura                                                        | Descripción                                                                              |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**cuota de WSMAN \_ AUTHZ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_authz_quota)                 | Define la información de cuota por usuario.                                           |
| [**\_detalles del certificado WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_certificate_details) | Representa los campos en el certificado de cliente.                                     |
| [**\_conjunto de \_ argumentos del comando WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_command_arg_set)        | Representa el conjunto de argumentos que se pasan a la línea de comandos.                  |
| [**\_filtro WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_filter)                            | Define el filtrado utilizado para una operación.                                             |
| [**\_fragmento WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_fragment)                        | Define la información de fragmento para una operación.                                       |
| [**información de la \_ operación WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_operation_info)           | Representa un punto de conexión de recurso específico para el que el complemento debe realizar la solicitud. |
| [**\_solicitud de complemento WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request)           | Contiene información sobre la solicitud y se pasa a cada operación de complemento.       |
| [**detalles del remitente de WSMAN \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_sender_details)           | Especifica los detalles del cliente para cada solicitud de entrada.                                      |



 

 

 




