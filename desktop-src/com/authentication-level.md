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
# <a name="authentication-level"></a><span data-ttu-id="56a72-103">Nivel de autenticación</span><span class="sxs-lookup"><span data-stu-id="56a72-103">Authentication Level</span></span>

<span data-ttu-id="56a72-104">El nivel de autenticación controla cuánta seguridad desea un cliente o servidor de su SSP.</span><span class="sxs-lookup"><span data-stu-id="56a72-104">The authentication level controls how much security a client or server wants from its SSP.</span></span> <span data-ttu-id="56a72-105">El nivel de autenticación se establece pasando un \_ \_ \_ valor de nivel XXX de autenticación de RPC C adecuado \_ a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) a través del parámetro *dwAuthnLevel* .</span><span class="sxs-lookup"><span data-stu-id="56a72-105">The authentication level is set by passing an appropriate RPC\_C\_AUTHN\_LEVEL\_xxx value to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) through the *dwAuthnLevel* parameter.</span></span> <span data-ttu-id="56a72-106">Los niveles de autenticación del cliente y el servidor se comparan durante el protocolo de enlace y se usa la configuración de protección de seguridad de nivel superior para la conexión.</span><span class="sxs-lookup"><span data-stu-id="56a72-106">The authentication levels from the client and server are compared during the handshake, and the higher level security protection setting is used for the connection.</span></span>

<span data-ttu-id="56a72-107">Los distintos niveles de autenticación se describen a continuación, desde la protección de seguridad de nivel más baja hasta la más alta:</span><span class="sxs-lookup"><span data-stu-id="56a72-107">The different authentication levels are described as follows, from lowest level security protection to highest:</span></span>

<dl> <dt>

<span data-ttu-id="56a72-108"><span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>Ninguno (nivel de autenticación de RPC \_ C \_ \_ \_ ninguno)</span><span class="sxs-lookup"><span data-stu-id="56a72-108"><span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>None (RPC\_C\_AUTHN\_LEVEL\_NONE)</span></span>
</dt> <dd>

<span data-ttu-id="56a72-109">No se realiza ninguna autenticación durante la comunicación entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="56a72-109">No authentication is performed during the communication between client and server.</span></span> <span data-ttu-id="56a72-110">Se omiten todas las configuraciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="56a72-110">All security settings are ignored.</span></span> <span data-ttu-id="56a72-111">Este nivel de autenticación solo se puede establecer si el [nivel de servicio de autenticación](com-authentication-service-constants.md) es RPC \_ C \_ authn \_ ninguno.</span><span class="sxs-lookup"><span data-stu-id="56a72-111">This authentication level can be set only if the [authentication service level](com-authentication-service-constants.md) is RPC\_C\_AUTHN\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="56a72-112"><span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Predeterminado (valor predeterminado de nivel de autenticación de RPC \_ C \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="56a72-112"><span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Default (RPC\_C\_AUTHN\_LEVEL\_DEFAULT)</span></span>
</dt> <dd>

<span data-ttu-id="56a72-113">COM elige el nivel de autenticación mediante su negociación de la capa de seguridad normal.</span><span class="sxs-lookup"><span data-stu-id="56a72-113">COM chooses the authentication level by using its normal security blanket negotiation.</span></span> <span data-ttu-id="56a72-114">Nunca elegirá un nivel de autenticación de ninguno.</span><span class="sxs-lookup"><span data-stu-id="56a72-114">It will never choose an authentication level of None.</span></span>

</dd> <dt>

<span data-ttu-id="56a72-115"><span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Connect (conexión de nivel de autenticación de RPC \_ C \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="56a72-115"><span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Connect (RPC\_C\_AUTHN\_LEVEL\_CONNECT)</span></span>
</dt> <dd>

<span data-ttu-id="56a72-116">El protocolo de enlace de autenticación normal se produce entre el cliente y el servidor, y se establece una clave de sesión, pero esa clave nunca se utiliza para la comunicación entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="56a72-116">The normal authentication handshake occurs between the client and server, and a session key is established but that key is never used for communication between the client and server.</span></span> <span data-ttu-id="56a72-117">Toda la comunicación después del Protocolo de enlace no es segura.</span><span class="sxs-lookup"><span data-stu-id="56a72-117">All communication after the handshake is nonsecure.</span></span>

</dd> <dt>

<span data-ttu-id="56a72-118"><span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Llamada (llamada de nivel de autenticación de RPC \_ C \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="56a72-118"><span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Call (RPC\_C\_AUTHN\_LEVEL\_CALL)</span></span>
</dt> <dd>

<span data-ttu-id="56a72-119">Solo se firman los encabezados del principio de cada llamada.</span><span class="sxs-lookup"><span data-stu-id="56a72-119">Only the headers of the beginning of each call are signed.</span></span> <span data-ttu-id="56a72-120">El resto de los datos intercambiados entre el cliente y el servidor no están firmados ni cifrados.</span><span class="sxs-lookup"><span data-stu-id="56a72-120">The rest of the data exchanged between the client and server is neither signed nor encrypted.</span></span> <span data-ttu-id="56a72-121">La mayoría de los SSP no admiten este nivel de autenticación y lo promueven de forma silenciosa al paquete.</span><span class="sxs-lookup"><span data-stu-id="56a72-121">Most SSPs do not support this authentication level and silently promote it to Packet.</span></span>

</dd> <dt>

<span data-ttu-id="56a72-122"><span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Paquete (PKT de nivel de autenticación de RPC \_ C \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="56a72-122"><span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Packet (RPC\_C\_AUTHN\_LEVEL\_PKT)</span></span>
</dt> <dd>

<span data-ttu-id="56a72-123">El encabezado de cada paquete está firmado pero no cifrado.</span><span class="sxs-lookup"><span data-stu-id="56a72-123">The header of each packet is signed but not encrypted.</span></span> <span data-ttu-id="56a72-124">Los paquetes no están firmados ni cifrados.</span><span class="sxs-lookup"><span data-stu-id="56a72-124">The packets themselves are not signed or encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="56a72-125"><span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Integridad de paquetes ( \_ integridad de nivel de autenticación de RPC C \_ \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="56a72-125"><span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Packet Integrity (RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY)</span></span>
</dt> <dd>

<span data-ttu-id="56a72-126">Cada paquete de datos está firmado en su totalidad, pero no está cifrado.</span><span class="sxs-lookup"><span data-stu-id="56a72-126">Each packet of data is signed in its entirety but is not encrypted.</span></span> <span data-ttu-id="56a72-127">Dado que todos los datos están firmados por el remitente, el destinatario puede estar seguro de que ninguno de los datos se ha alterado durante el tránsito.</span><span class="sxs-lookup"><span data-stu-id="56a72-127">Because all of the data is signed by the sender, the recipient can be certain that none of the data has been tampered with during transit.</span></span>

</dd> <dt>

<span data-ttu-id="56a72-128"><span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Privacidad de paquetes ( \_ privacidad de nivel de autenticación de RPC C \_ \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="56a72-128"><span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Packet Privacy (RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY)</span></span>
</dt> <dd>

<span data-ttu-id="56a72-129">Cada paquete de datos está firmado y cifrado.</span><span class="sxs-lookup"><span data-stu-id="56a72-129">Each data packet is signed and encrypted.</span></span> <span data-ttu-id="56a72-130">Esto ayuda a proteger toda la comunicación entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="56a72-130">This helps protect the entire communication between the client and server.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="56a72-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56a72-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56a72-132">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="56a72-132">AuthenticationLevel</span></span>](authenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="56a72-133">LegacyAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="56a72-133">LegacyAuthenticationLevel</span></span>](legacyauthenticationlevel.md)
</dt> </dl>

 

 




