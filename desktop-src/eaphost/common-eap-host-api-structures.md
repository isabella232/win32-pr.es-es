---
title: Estructuras comunes de API de EAPHost
description: Obtenga información sobre las estructuras de API de EAPHost comunes. Vea una lista de estructuras utilizadas por todas las tecnologías de EAPHost.
ms.assetid: f6f3b909-1e89-47f8-853c-c0f3f2414817
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b44a94aae1f18336dae8c11a1dc0217dc7c8d08
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793941"
---
# <a name="common-eaphost-api-structures"></a>Estructuras comunes de API de EAPHost

En la tabla siguiente se enumeran las estructuras que son comunes a todas las tecnologías de API de EAPHost.



| Estructura                                                                | Descripción                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_atributo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)                                  | Contiene un atributo EAP.                                                                                                                                                                                              |
| [**\_atributos EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes)                                | Contiene una matriz de atributos EAP.                                                                                                                                                                                    |
| [**\_matriz de \_ campos de entrada de configuración de EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Contiene un conjunto de estructuras de datos de campo de entrada de configuración de EAP que contienen colectivamente los datos de campo de entrada del usuario obtenidos de un cuadro de diálogo de configuración de inicio de sesión único (SSO) de EAP. [**\_ \_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) |
| [**\_datos de \_ campo de entrada de configuración de EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Contiene los datos asociados a un único campo de entrada en un cuadro de diálogo de configuración de inicio de sesión único (SSO) de EAP.                                                                                                              |
| [**ERROR de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)                                          | Contiene datos sobre un error que se produjo durante una operación de EAPHost.                                                                                                                                                 |
| [**\_información del método EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info)                             | Contiene datos específicos para un método EAP.                                                                                                                                                                               |
| [**\_información del método EAP \_ \_ ex**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_ex)                      | Windows Vista con Service Pack 1 (SP1) o posterior: contiene datos específicos para un método EAP.                                                                                                                             |
| [**\_matriz de \_ información del método EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array)                | Contiene información sobre los métodos EAP instalados en el equipo cliente.                                                                                                                                                   |
| [**\_matriz de información de método EAP \_ \_ \_ ex**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array_ex)         | Windows Vista con SP1 o posterior: contiene información sobre todos los métodos EAP instalados en el equipo cliente.                                                                                                    |
| [**\_tipo de método EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type)                             | Contiene datos de tipo, identificación y autor para un método EAP.                                                                                                                                                       |
| [**tipo de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type)                                            | Contiene datos de identificación de tipo y proveedor para un método EAP.                                                                                                                                                         |
| [**EapPacket**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket)                                           | Contiene un paquete de datos opacos enviados durante una sesión de autenticación EAP.                                                                                                                                             |



 

 

 




