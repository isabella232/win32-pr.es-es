---
title: Estructuras de proveedor de Protocolo de escritorio remoto
description: La API de protocolo remoto personalizada admite las siguientes estructuras.
ms.assetid: 45d17758-4554-42aa-aeb9-c8d4e7fc6bb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a626db328ede3bac9422a9a47ebe55f05953a22d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676105"
---
# <a name="remote-desktop-protocol-provider-structures"></a>Estructuras de proveedor de Protocolo de escritorio remoto

La API de protocolo remoto personalizada admite las siguientes estructuras.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**TSMF \_ admiten \_ datos \_ en**](tsmf-support-data-in.md)
</dt> <dd>

Contiene información acerca de los formatos de medios.

</dd> <dt>

[**TSMF \_ admiten \_ datos de \_ salida**](tsmf-support-data-out.md)
</dt> <dd>

Contiene información acerca de los formatos de medios.

</dd> <dt>

[**TSMF \_ admite \_ NODEDATA \_ en**](tsmf-support-nodedata-in.md)
</dt> <dd>

Se utiliza dentro de los [**\_ \_ datos \_ de soporte de TSMF en**](tsmf-support-data-in.md) la estructura para contener información acerca de los formatos multimedia admitidos.

</dd> <dt>

[**\_compatibilidad con TSMF \_ NODEDATA \_ out**](tsmf-support-nodedata-out.md)
</dt> <dd>

Se usa dentro de la estructura de salida de datos de soporte de TSMF para contener información acerca de los formatos multimedia admitidos. [**\_ \_ \_**](tsmf-support-data-out.md)

</dd> <dt>

[**\_configuración de conexión de Wrds \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings)
</dt> <dd>

Contiene información de configuración de conexión para una sesión remota.

</dd> <dt>

[**Configuración de conexión de WRDS \_ \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings_1)
</dt> <dd>

Contiene información de configuración de conexión para una sesión remota.

</dd> <dt>

[**WRDS \_ \_ información de \_ zona \_ horaria dinámica**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information)
</dt> <dd>

Contiene información de zona horaria dinámica.

</dd> <dt>

[**\_configuración del agente de escucha de Wrds \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings)
</dt> <dd>

Contiene información de configuración del agente de escucha para una sesión remota.

</dd> <dt>

[**Configuración del agente de escucha de WRDS \_ \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings_1)
</dt> <dd>

Contiene la configuración del agente de escucha para una sesión remota.

</dd> <dt>

[**configuración de WRDS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings)
</dt> <dd>

Contiene información de configuración relacionada con la Directiva para una sesión remota.

</dd> <dt>

[**Configuración de WRDS \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings_1)
</dt> <dd>

Contiene la configuración relacionada con la Directiva para una sesión remota.

</dd> <dt>

[**\_estadísticas de caché de WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_cache_stats)
</dt> <dd>

Contiene estadísticas de caché del protocolo.

</dd> <dt>

[**\_Ver \_ ioctl de WTS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_display_ioctl)
</dt> <dd>

Contiene información acerca de la presentación del cliente.

</dd> <dt>

[**\_datos de cliente de WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_client_data)
</dt> <dd>

Contiene información acerca de la conexión de cliente.

</dd> <dt>

[**\_funcionalidades de licencia de WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_license_capabilities)
</dt> <dd>

Contiene información sobre las capacidades de licencia del cliente.

</dd> <dt>

[**\_datos de directiva de WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_policy_data)
</dt> <dd>

Contiene información de directiva que pasa el servicio Servicios de Escritorio remoto al Protocolo.

</dd> <dt>

[**\_valor de propiedad de WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_property_value)
</dt> <dd>

Contiene información sobre un valor de propiedad que se va a recuperar del protocolo.

</dd> <dt>

[**\_caché del protocolo WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_cache)
</dt> <dd>

Contiene el número de lecturas de caché y aciertos de caché.

</dd> <dt>

[**\_contadores del protocolo WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_counters)
</dt> <dd>

Contiene contadores de rendimiento del protocolo.

</dd> <dt>

[**\_Estado del Protocolo de WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_status)
</dt> <dd>

Contiene información sobre el estado del protocolo.

</dd> <dt>

[**\_Estado del servicio de WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_service_state)
</dt> <dd>

Contiene información sobre los cambios en el estado del servicio Servicios de Escritorio remoto.

</dd> <dt>

[**\_ID. de sesión de WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_session_id)
</dt> <dd>

Contiene un **GUID** que identifica de forma única una sesión.

</dd> <dt>

[**\_rectángulo pequeño de WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_small_rect)
</dt> <dd>

Contiene las coordenadas de la ventana de cliente.

</dd> <dt>

[**SOCKADDR de WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_sockaddr)
</dt> <dd>

Contiene una dirección de socket.

</dd> <dt>

[**SYSTEMTIME de WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_systemtime)
</dt> <dd>

Especifica la información de fecha y hora para las transiciones entre la hora estándar y el horario de verano.

</dd> <dt>

[**\_información de \_ zona \_ horaria de WTS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_time_zone_information)
</dt> <dd>

Contiene información de zona horaria del cliente.

</dd> <dt>

[**\_credencial de usuario de WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_credential)
</dt> <dd>

Contiene información de credenciales para un usuario.

</dd> <dt>

[**\_datos de usuario de WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_data)
</dt> <dd>

Contiene los valores de propiedad Select Client.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del proveedor de Protocolo de escritorio remoto](custom-remote-protocol-reference.md)
</dt> <dt>

[Enumeraciones de proveedor de Protocolo de escritorio remoto](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Interfaces de proveedor de Protocolo de escritorio remoto](custom-remote-protocol-interfaces.md)
</dt> <dt>

[Uniones de proveedor de Protocolo de escritorio remoto](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




