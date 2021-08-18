---
title: Estructuras comunes de LA API de EAPHost
description: Obtenga información sobre las estructuras de API de EAPHost comunes. Vea una lista de las estructuras usadas por todas las tecnologías eapHost.
ms.assetid: f6f3b909-1e89-47f8-853c-c0f3f2414817
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4740658f798eadee2a658df1a7f9f8fd44b386c4ac39b52bcf49e75887d2d719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984335"
---
# <a name="common-eaphost-api-structures"></a>Estructuras comunes de LA API de EAPHost

En la tabla siguiente se enumeran las estructuras que son comunes a todas las tecnologías de API de EAPHost.



| Estructura                                                                | Descripción                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ATRIBUTO \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)                                  | Contiene un atributo EAP.                                                                                                                                                                                              |
| [**ATRIBUTOS DE EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes)                                | Contiene una matriz de atributos eap.                                                                                                                                                                                    |
| [**MATRIZ DE \_ CAMPOS DE ENTRADA DE CONFIGURACIÓN DE \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Contiene un conjunto de estructuras DE DATOS DE CAMPO DE ENTRADA DE CONFIGURACIÓN de EAP que contienen colectivamente los datos de campo de entrada del usuario obtenidos de un cuadro de diálogo de configuración de inicio de sesión único (SSO) de EAP. [**\_ \_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) |
| [**DATOS DEL \_ CAMPO DE ENTRADA DE CONFIGURACIÓN \_ \_ DE \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Contiene los datos asociados a un único campo de entrada en un cuadro de diálogo de configuración de inicio de sesión único (SSO) de EAP.                                                                                                              |
| [**ERROR DE EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)                                          | Contiene datos sobre un error que se produjo durante una operación EAPHost.                                                                                                                                                 |
| [**INFORMACIÓN DEL \_ MÉTODO \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info)                             | Contiene datos específicos para un método EAP.                                                                                                                                                                               |
| [**EJEMPLO DE \_ INFORMACIÓN \_ DEL MÉTODO EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_ex)                      | Windows Vista con Service Pack 1 (SP1) o posterior: contiene datos específicos para un método EAP.                                                                                                                             |
| [**MATRIZ DE \_ INFORMACIÓN DEL \_ MÉTODO \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array)                | Contiene información sobre los métodos EAP instalados en el equipo cliente.                                                                                                                                                   |
| [**MATRIZ DE \_ INFORMACIÓN \_ DEL MÉTODO \_ \_ EAP, POR EJEMPLO**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array_ex)         | Windows Vista con SP1 o posterior: contiene información sobre todos los métodos EAP instalados en el equipo cliente.                                                                                                    |
| [**TIPO DE \_ MÉTODO \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type)                             | Contiene datos de tipo, identificación y creación para un método EAP.                                                                                                                                                       |
| [**TIPO DE \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type)                                            | Contiene datos de identificación de tipo y proveedor para un método EAP.                                                                                                                                                         |
| [**EapPacket**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket)                                           | Contiene un paquete de datos opacos enviados durante una sesión de autenticación EAP.                                                                                                                                             |



 

 

 




