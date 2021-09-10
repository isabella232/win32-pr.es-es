---
title: Nivel de autenticación
description: El nivel de autenticación controla la cantidad de seguridad que un cliente o servidor desea de su SSP.
ms.assetid: 0bad2bfd-6930-42fc-beb0-bce32440b0b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250661e4a8da42ffd91f37e282a39fbb52b6328a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369759"
---
# <a name="authentication-level"></a>Nivel de autenticación

El nivel de autenticación controla la cantidad de seguridad que un cliente o servidor desea de su SSP. El nivel de autenticación se establece pasando un valor de RPC C AUTHN LEVEL xxx adecuado a \_ \_ \_ \_ [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) a través del *parámetro dwAuthnLevel.* Los niveles de autenticación del cliente y el servidor se comparan durante el protocolo de enlace y la configuración de protección de seguridad de nivel superior se usa para la conexión.

Los distintos niveles de autenticación se describen de la siguiente manera, desde la protección de seguridad de nivel más bajo a la más alta:

<dl> <dt>

<span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>Ninguno (RPC \_ C \_ AUTHN \_ LEVEL \_ NONE)
</dt> <dd>

No se realiza ninguna autenticación durante la comunicación entre el cliente y el servidor. Se omiten todas las opciones de seguridad. Este nivel de autenticación solo se puede establecer si el nivel [de servicio de autenticación](com-authentication-service-constants.md) es RPC \_ C \_ AUTHN \_ NONE.

</dd> <dt>

<span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Valor predeterminado (RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT)
</dt> <dd>

COM elige el nivel de autenticación mediante su negociación normal de negociación de negociación de negociación de seguridad. Nunca elegirá un nivel de autenticación Ninguno.

</dd> <dt>

<span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Conectar (RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT)
</dt> <dd>

El protocolo de enlace de autenticación normal se produce entre el cliente y el servidor, y se establece una clave de sesión, pero esa clave nunca se usa para la comunicación entre el cliente y el servidor. Toda la comunicación después del protocolo de enlace no es segura.

</dd> <dt>

<span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Call (RPC \_ C \_ AUTHN \_ LEVEL \_ CALL)
</dt> <dd>

Solo se firman los encabezados del principio de cada llamada. El resto de los datos intercambiados entre el cliente y el servidor no está firmado ni cifrado. La mayoría de los SSP no admiten este nivel de autenticación y lo promueven silenciosamente a Packet.

</dd> <dt>

<span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Paquete (RPC \_ C \_ AUTHN \_ LEVEL \_ PKT)
</dt> <dd>

El encabezado de cada paquete está firmado, pero no cifrado. Los paquetes no están firmados ni cifrados.

</dd> <dt>

<span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Integridad de paquetes (RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY)
</dt> <dd>

Cada paquete de datos se firma en su totalidad, pero no se cifra. Dado que todos los datos están firmados por el remitente, el destinatario puede estar seguro de que ninguno de los datos se ha alterado durante el tránsito.

</dd> <dt>

<span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Privacidad de paquetes (RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY)
</dt> <dd>

Cada paquete de datos está firmado y cifrado. Esto ayuda a proteger toda la comunicación entre el cliente y el servidor.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[AuthenticationLevel](authenticationlevel.md)
</dt> <dt>

[LegacyAuthenticationLevel](legacyauthenticationlevel.md)
</dt> </dl>

 

 




