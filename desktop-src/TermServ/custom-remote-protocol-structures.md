---
title: Protocolo de escritorio remoto de proveedores de servicios
description: La API de protocolo remoto personalizado admite las estructuras siguientes.
ms.assetid: 45d17758-4554-42aa-aeb9-c8d4e7fc6bb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a626db328ede3bac9422a9a47ebe55f05953a22d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073359"
---
# <a name="remote-desktop-protocol-provider-structures"></a>Protocolo de escritorio remoto de proveedores de servicios

La API de protocolo remoto personalizado admite las estructuras siguientes.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**DATOS DE COMPATIBILIDAD DE TSMF \_ \_ \_ EN**](tsmf-support-data-in.md)
</dt> <dd>

Contiene información sobre los formatos multimedia.

</dd> <dt>

[**SALIDA DE DATOS \_ DE COMPATIBILIDAD \_ CON TSMF \_**](tsmf-support-data-out.md)
</dt> <dd>

Contiene información sobre los formatos multimedia.

</dd> <dt>

[**COMPATIBILIDAD DE TSMF \_ \_ CON NODEDATA \_ EN**](tsmf-support-nodedata-in.md)
</dt> <dd>

Se usa dentro de la [**estructura SUPPORT DATA \_ \_ \_ IN de TSMF**](tsmf-support-data-in.md) para contener información sobre los formatos multimedia admitidos.

</dd> <dt>

[**TSMF \_ ADMITE \_ NODEDATA \_ OUT**](tsmf-support-nodedata-out.md)
</dt> <dd>

Se usa dentro de la [**estructura \_ TSMF SUPPORT DATA \_ \_ OUT**](tsmf-support-data-out.md) para contener información sobre los formatos multimedia admitidos.

</dd> <dt>

[**CONFIGURACIÓN DE CONEXIÓN DE WRDS \_ \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings)
</dt> <dd>

Contiene información de configuración de conexión para una sesión remota.

</dd> <dt>

[**CONFIGURACIÓN DE CONEXIÓN DE WRDS \_ \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings_1)
</dt> <dd>

Contiene información de configuración de conexión para una sesión remota.

</dd> <dt>

[**INFORMACIÓN DE ZONA HORARIA DINÁMICA DE \_ \_ \_ \_ WRDS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information)
</dt> <dd>

Contiene información de zona horaria dinámica.

</dd> <dt>

[**CONFIGURACIÓN DEL AGENTE \_ DE ESCUCHA DE WRDS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings)
</dt> <dd>

Contiene información de configuración del agente de escucha para una sesión remota.

</dd> <dt>

[**CONFIGURACIÓN DEL AGENTE DE ESCUCHA DE WRDS \_ \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings_1)
</dt> <dd>

Contiene la configuración del agente de escucha para una sesión remota.

</dd> <dt>

[**CONFIGURACIÓN DE \_ WRDS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings)
</dt> <dd>

Contiene información de configuración relacionada con la directiva para una sesión remota.

</dd> <dt>

[**CONFIGURACIÓN DE WRDS \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings_1)
</dt> <dd>

Contiene la configuración relacionada con directivas para una sesión remota.

</dd> <dt>

[**\_WTS ESTADÍSTICAS DE \_ CACHÉ**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_cache_stats)
</dt> <dd>

Contiene estadísticas de caché de protocolos.

</dd> <dt>

[**\_WTS VISUALIZACIÓN \_ DE IOCTL**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_display_ioctl)
</dt> <dd>

Contiene información sobre la presentación del cliente.

</dd> <dt>

[**\_WTS DATOS DE \_ CLIENTE**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_client_data)
</dt> <dd>

Contiene información sobre la conexión de cliente.

</dd> <dt>

[**\_WTS FUNCIONALIDADES \_ DE LICENCIA**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_license_capabilities)
</dt> <dd>

Contiene información sobre las funcionalidades de licencia del cliente.

</dd> <dt>

[**\_WTS DATOS DE \_ DIRECTIVA**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_policy_data)
</dt> <dd>

Contiene información de directiva que el servicio Servicios de Escritorio remoto pasa al protocolo.

</dd> <dt>

[**\_WTS VALOR DE \_ PROPIEDAD**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_property_value)
</dt> <dd>

Contiene información sobre un valor de propiedad que se recuperará del protocolo.

</dd> <dt>

[**\_WTS CACHÉ DE \_ PROTOCOLOS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_cache)
</dt> <dd>

Contiene el número de lecturas y aciertos de caché.

</dd> <dt>

[**\_WTS CONTADORES \_ DE PROTOCOLO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_counters)
</dt> <dd>

Contiene contadores de rendimiento de protocolo.

</dd> <dt>

[**\_WTS ESTADO \_ DEL PROTOCOLO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_status)
</dt> <dd>

Contiene información sobre el estado del protocolo.

</dd> <dt>

[**\_WTS ESTADO DEL \_ SERVICIO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_service_state)
</dt> <dd>

Contiene información sobre los cambios en el estado del Servicios de Escritorio remoto servicio.

</dd> <dt>

[**\_WTS ID. \_ DE SESIÓN**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_session_id)
</dt> <dd>

Contiene un **GUID que** identifica de forma única una sesión.

</dd> <dt>

[**\_WTS SMALL \_ RECT**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_small_rect)
</dt> <dd>

Contiene coordenadas de ventana de cliente.

</dd> <dt>

[**\_WTS SOCKADDR**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_sockaddr)
</dt> <dd>

Contiene una dirección de socket.

</dd> <dt>

[**\_WTS SYSTEMTIME**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_systemtime)
</dt> <dd>

Especifica información de fecha y hora para las transiciones entre el horario estándar y el horario de verano.

</dd> <dt>

[**\_WTS INFORMACIÓN \_ DE ZONA \_ HORARIA**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_time_zone_information)
</dt> <dd>

Contiene información de zona horaria del cliente.

</dd> <dt>

[**\_WTS \_CREDENCIAL DE USUARIO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_credential)
</dt> <dd>

Contiene información de credenciales para un usuario.

</dd> <dt>

[**\_WTS DATOS DE \_ USUARIO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_data)
</dt> <dd>

Contiene los valores de propiedad de cliente seleccionados.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[referencia Protocolo de escritorio remoto proveedor de servicios](custom-remote-protocol-reference.md)
</dt> <dt>

[Protocolo de escritorio remoto provider enumerations](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Protocolo de escritorio remoto interfaces de proveedor de servicios](custom-remote-protocol-interfaces.md)
</dt> <dt>

[Protocolo de escritorio remoto de proveedor de servicios](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




