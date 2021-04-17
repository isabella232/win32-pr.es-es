---
title: Nivel de autenticación
description: El nivel de autenticación controla cuánta seguridad desea un cliente o servidor de su SSP.
ms.assetid: 0bad2bfd-6930-42fc-beb0-bce32440b0b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250661e4a8da42ffd91f37e282a39fbb52b6328a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357763"
---
# <a name="authentication-level"></a>Nivel de autenticación

El nivel de autenticación controla cuánta seguridad desea un cliente o servidor de su SSP. El nivel de autenticación se establece pasando un \_ \_ \_ valor de nivel XXX de autenticación de RPC C adecuado \_ a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) a través del parámetro *dwAuthnLevel* . Los niveles de autenticación del cliente y el servidor se comparan durante el protocolo de enlace y se usa la configuración de protección de seguridad de nivel superior para la conexión.

Los distintos niveles de autenticación se describen a continuación, desde la protección de seguridad de nivel más baja hasta la más alta:

<dl> <dt>

<span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>Ninguno (nivel de autenticación de RPC \_ C \_ \_ \_ ninguno)
</dt> <dd>

No se realiza ninguna autenticación durante la comunicación entre el cliente y el servidor. Se omiten todas las configuraciones de seguridad. Este nivel de autenticación solo se puede establecer si el [nivel de servicio de autenticación](com-authentication-service-constants.md) es RPC \_ C \_ authn \_ ninguno.

</dd> <dt>

<span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Predeterminado (valor predeterminado de nivel de autenticación de RPC \_ C \_ \_ \_ )
</dt> <dd>

COM elige el nivel de autenticación mediante su negociación de la capa de seguridad normal. Nunca elegirá un nivel de autenticación de ninguno.

</dd> <dt>

<span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Connect (conexión de nivel de autenticación de RPC \_ C \_ \_ \_ )
</dt> <dd>

El protocolo de enlace de autenticación normal se produce entre el cliente y el servidor, y se establece una clave de sesión, pero esa clave nunca se utiliza para la comunicación entre el cliente y el servidor. Toda la comunicación después del Protocolo de enlace no es segura.

</dd> <dt>

<span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Llamada (llamada de nivel de autenticación de RPC \_ C \_ \_ \_ )
</dt> <dd>

Solo se firman los encabezados del principio de cada llamada. El resto de los datos intercambiados entre el cliente y el servidor no están firmados ni cifrados. La mayoría de los SSP no admiten este nivel de autenticación y lo promueven de forma silenciosa al paquete.

</dd> <dt>

<span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Paquete (PKT de nivel de autenticación de RPC \_ C \_ \_ \_ )
</dt> <dd>

El encabezado de cada paquete está firmado pero no cifrado. Los paquetes no están firmados ni cifrados.

</dd> <dt>

<span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Integridad de paquetes ( \_ integridad de nivel de autenticación de RPC C \_ \_ \_ \_ )
</dt> <dd>

Cada paquete de datos está firmado en su totalidad, pero no está cifrado. Dado que todos los datos están firmados por el remitente, el destinatario puede estar seguro de que ninguno de los datos se ha alterado durante el tránsito.

</dd> <dt>

<span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Privacidad de paquetes ( \_ privacidad de nivel de autenticación de RPC C \_ \_ \_ \_ )
</dt> <dd>

Cada paquete de datos está firmado y cifrado. Esto ayuda a proteger toda la comunicación entre el cliente y el servidor.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[AuthenticationLevel](authenticationlevel.md)
</dt> <dt>

[LegacyAuthenticationLevel](legacyauthenticationlevel.md)
</dt> </dl>

 

 




