---
title: Propiedades del método EAP (Eaptypes. h)
description: Lo usan los suplicantes y los autenticadores para determinar los métodos EAP que se van a usar con un solicitante o autenticador determinados. Las propiedades de método también especifican la configuración de un método.
ms.assetid: 10407b85-5d2c-4c75-9b65-a0d65d4cc7ab
topic_type:
- apiref
api_name:
- eapPropCipherSuiteNegotiation
- eapPropMutualAuth
- eapPropIntegrity
- eapPropReplayProtection
- eapPropConfidentiality
- eapPropKeyDerivation
- eapPropKeyStrength64
- eapPropKeyStrength128
- eapPropKeyStrength256
- eapPropKeyStrength512
- eapPropKeyStrength1024
- eapPropDictionaryAttackResistance
- eapPropFastReconnect
- eapPropCryptoBinding
- eapPropSessionIndependence
- eapPropFragmentation
- eapPropChannelBinding
- eapPropNap
- eapPropStandalone
- eapPropMppeEncryption
- eapPropTunnelMethod
- eapPropSupportsConfig
- eapPropCertifiedMethod
- eapPropmachineAuth
- eapPropUserAuth
- eapPropIdentityPrivacy
- eapPropMethodChaining
- eapPropSharedStateEquivalence
- eapPropReserved
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 844f897456ee21dfa93dfaa5b16b4f218ba5efb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802534"
---
# <a name="eap-method-properties"></a><span data-ttu-id="d4df7-104">Propiedades del método EAP</span><span class="sxs-lookup"><span data-stu-id="d4df7-104">EAP Method Properties</span></span>

<span data-ttu-id="d4df7-105">Lo usan los suplicantes y los autenticadores para determinar los métodos EAP que se van a usar con un solicitante o autenticador determinados.</span><span class="sxs-lookup"><span data-stu-id="d4df7-105">Used by supplicants and authenticators to determine the EAP methods to be used with a given supplicant or authenticator.</span></span> <span data-ttu-id="d4df7-106">Las propiedades de método también especifican la configuración de un método.</span><span class="sxs-lookup"><span data-stu-id="d4df7-106">Method properties also specify the configuration of a method.</span></span>

<span data-ttu-id="d4df7-107">Por ejemplo, el suplicante [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) puede requerir que los métodos tengan determinadas propiedades para su uso con el suplicante [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="d4df7-107">For example, the [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) supplicant may require methods to have certain properties for use with the [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) supplicant.</span></span> <span data-ttu-id="d4df7-108">El material de creación de claves, por ejemplo, es un requisito.</span><span class="sxs-lookup"><span data-stu-id="d4df7-108">Keying material, for example, is a requirement.</span></span>

<span data-ttu-id="d4df7-109">Se enumeran las propiedades que admiten los métodos EAP.</span><span class="sxs-lookup"><span data-stu-id="d4df7-109">The properties supported by EAP methods are listed.</span></span> <span data-ttu-id="d4df7-110">Las propiedades se almacenan como valores de clave del registro.</span><span class="sxs-lookup"><span data-stu-id="d4df7-110">Properties are stored as registry key values.</span></span> <span data-ttu-id="d4df7-111">Para obtener más información, consulte la sección clave del registro de la DLL del método EAP peer del tema [configuración del registro para los métodos EAP.](registry-keys-for-eap-methods.md)</span><span class="sxs-lookup"><span data-stu-id="d4df7-111">For more information, see the EAP Peer Method DLL Registry Key section of the topic [Registry Configuration for EAP Methods.](registry-keys-for-eap-methods.md)</span></span>

<dl> <dt>

<span data-ttu-id="d4df7-112"><span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**</span><span class="sxs-lookup"><span data-stu-id="d4df7-112"><span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d4df7-113">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-114">El método permite negociar el conjunto de cifrado con el fin de cifrar los datos.</span><span class="sxs-lookup"><span data-stu-id="d4df7-114">The method allows the cipher suite to be negotiated for the purpose of data encryption.</span></span> <span data-ttu-id="d4df7-115">Windows Server 2008 admite los siguientes [conjuntos de cifrado](/windows/desktop/SecAuthN/tls-cipher-suites)3DES:</span><span class="sxs-lookup"><span data-stu-id="d4df7-115">Windows Server 2008 supports the following 3DES [cipher suites](/windows/desktop/SecAuthN/tls-cipher-suites):</span></span>

-   <span data-ttu-id="d4df7-116">TLS \_ RSA \_ con \_ 3DES \_ Ede \_ CBC \_ Sha (TLS & SSL 3)</span><span class="sxs-lookup"><span data-stu-id="d4df7-116">TLS\_RSA\_WITH\_3DES\_EDE\_CBC\_SHA (TLS & SSL 3)</span></span>
-   <span data-ttu-id="d4df7-117">TLS \_ DHE \_ DSS \_ con \_ 3DES \_ EDE \_ CBC \_ Sha (TLS & SSL 3)</span><span class="sxs-lookup"><span data-stu-id="d4df7-117">TLS\_DHE\_DSS\_WITH\_3DES\_EDE\_CBC\_SHA (TLS & SSL 3)</span></span>
-   <span data-ttu-id="d4df7-118">SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ con \_ MD5 (SSL 2 Si está habilitado)</span><span class="sxs-lookup"><span data-stu-id="d4df7-118">SSL\_CK\_DES\_192\_EDE3\_CBC\_WITH\_MD5 (SSL 2 if enabled)</span></span>

<span data-ttu-id="d4df7-119">Para obtener más información acerca del Protocolo de seguridad TLS 1,0, consulte [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).</span><span class="sxs-lookup"><span data-stu-id="d4df7-119">For more information about the TLS 1.0 security protocol, see [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-120"><span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**</span><span class="sxs-lookup"><span data-stu-id="d4df7-120"><span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-121">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d4df7-121">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-122">El método proporciona un intercambio, en el que el autenticador autentica al par y viceversa.</span><span class="sxs-lookup"><span data-stu-id="d4df7-122">The method provides an exchange, in which the authenticator authenticates the peer and vice versa.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-123"><span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**</span><span class="sxs-lookup"><span data-stu-id="d4df7-123"><span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-124">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d4df7-124">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-125">El método proporciona la autenticación del origen de datos y la protección contra la modificación no autorizada de la información de los paquetes EAP, incluidas las solicitudes EAP y las respuestas.</span><span class="sxs-lookup"><span data-stu-id="d4df7-125">The method provides data origin authentication and protection against unauthorized modification of information for EAP packets, including EAP requests and responses.</span></span> <span data-ttu-id="d4df7-126">Al efectuar esta declaración, una especificación de método debe especificar los paquetes EAP protegidos y los campos protegidos dentro de los paquetes EAP.</span><span class="sxs-lookup"><span data-stu-id="d4df7-126">When making this claim, a method specification must specify the protected EAP packets and protected fields within EAP packets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-127"><span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**</span><span class="sxs-lookup"><span data-stu-id="d4df7-127"><span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-128">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d4df7-128">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-129">El método puede protegerse frente a la reproducción de un método EAP o de sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="d4df7-129">The method can protect against replay of an EAP method or its messages.</span></span> <span data-ttu-id="d4df7-130">No se pueden reproducir las indicaciones de los resultados correctos y erróneos.</span><span class="sxs-lookup"><span data-stu-id="d4df7-130">Success and failure result indications cannot be replayed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-131"><span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**</span><span class="sxs-lookup"><span data-stu-id="d4df7-131"><span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d4df7-132">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-133">El método puede cifrar los mensajes EAP.</span><span class="sxs-lookup"><span data-stu-id="d4df7-133">The method can encrypt EAP messages.</span></span> <span data-ttu-id="d4df7-134">Se cifran las solicitudes de EAP, las respuestas de EAP, las indicaciones de resultados correctos y las indicaciones de resultados de error.</span><span class="sxs-lookup"><span data-stu-id="d4df7-134">EAP requests, EAP responses, success result indications, and failure result indications are encrypted.</span></span> <span data-ttu-id="d4df7-135">Un método que realiza esta demanda debe admitir Identity Protection.</span><span class="sxs-lookup"><span data-stu-id="d4df7-135">A method making this claim must support identity protection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-136"><span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**</span><span class="sxs-lookup"><span data-stu-id="d4df7-136"><span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-137">0x00000020</span><span class="sxs-lookup"><span data-stu-id="d4df7-137">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-138">El método puede derivar material de creación de claves exportable, como la clave de sesión maestra (MSK) y la clave de sesión maestra extendida (EMSK).</span><span class="sxs-lookup"><span data-stu-id="d4df7-138">The method can derive exportable keying material, such as the Master Session Key (MSK) and the Extended Master Session Key (EMSK).</span></span> <span data-ttu-id="d4df7-139">El MSK solo se usa para la derivación de claves adicionales, no directamente para la protección de la conversación EAP o los datos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="d4df7-139">The MSK is used only for further key derivation, not directly for protection of the EAP conversation or subsequent data.</span></span> <span data-ttu-id="d4df7-140">El uso de EMSK está reservado.</span><span class="sxs-lookup"><span data-stu-id="d4df7-140">Use of the EMSK is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-141"><span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**</span><span class="sxs-lookup"><span data-stu-id="d4df7-141"><span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-142">0x00000040</span><span class="sxs-lookup"><span data-stu-id="d4df7-142">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-143">La longitud de clave mínima admitida por el método EAP es 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d4df7-143">The minimum key length supported by the EAP method is 64 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-144"><span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**</span><span class="sxs-lookup"><span data-stu-id="d4df7-144"><span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-145">0x00000080</span><span class="sxs-lookup"><span data-stu-id="d4df7-145">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-146">La longitud de clave mínima admitida por el método EAP es 128 bits.</span><span class="sxs-lookup"><span data-stu-id="d4df7-146">The minimum key length supported by the EAP method is 128 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-147"><span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**</span><span class="sxs-lookup"><span data-stu-id="d4df7-147"><span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-148">0x00000100</span><span class="sxs-lookup"><span data-stu-id="d4df7-148">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-149">La longitud de clave mínima admitida por el método EAP es 256 bits.</span><span class="sxs-lookup"><span data-stu-id="d4df7-149">The minimum key length supported by the EAP method is 256 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-150"><span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**</span><span class="sxs-lookup"><span data-stu-id="d4df7-150"><span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-151">0x00000200</span><span class="sxs-lookup"><span data-stu-id="d4df7-151">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-152">La longitud de clave mínima admitida por el método EAP es 512 bits.</span><span class="sxs-lookup"><span data-stu-id="d4df7-152">The minimum key length supported by the EAP method is 512 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-153"><span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**</span><span class="sxs-lookup"><span data-stu-id="d4df7-153"><span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-154">0x00000400</span><span class="sxs-lookup"><span data-stu-id="d4df7-154">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-155">La longitud de clave mínima admitida por el método EAP es 1024 bits.</span><span class="sxs-lookup"><span data-stu-id="d4df7-155">The minimum key length supported by the EAP method is 1024 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-156"><span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**</span><span class="sxs-lookup"><span data-stu-id="d4df7-156"><span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-157">0x00000800</span><span class="sxs-lookup"><span data-stu-id="d4df7-157">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-158">El método no permite un ataque sin conexión que tenga un factor de trabajo basado en el número de contraseñas en el Diccionario de un atacante.</span><span class="sxs-lookup"><span data-stu-id="d4df7-158">The method does not allow an offline attack that has a work factor based on the number of passwords in an attacker's dictionary.</span></span> <span data-ttu-id="d4df7-159">En los casos en que se usa la autenticación de contraseña, las contraseñas se seleccionan normalmente a partir de un conjunto pequeño (en comparación con un conjunto de claves de N bits), lo que supone un problema sobre los ataques de diccionario.</span><span class="sxs-lookup"><span data-stu-id="d4df7-159">Where password authentication is used, passwords are commonly selected from a small set (as compared to a set of N-bit keys), which raises a concern about dictionary attacks.</span></span> <span data-ttu-id="d4df7-160">Se puede decir que un método proporciona protección contra ataques de diccionario si, cuando utiliza una contraseña como secreto, el método no permite un ataque sin conexión que tenga un factor de trabajo basado en el número de contraseñas en el Diccionario de un atacante.</span><span class="sxs-lookup"><span data-stu-id="d4df7-160">A method may be said to provide protection against dictionary attacks if, when it uses a password as a secret, the method does not allow an offline attack that has a work factor based on the number of passwords in an attacker's dictionary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-161"><span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**</span><span class="sxs-lookup"><span data-stu-id="d4df7-161"><span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-162">0x00001000</span><span class="sxs-lookup"><span data-stu-id="d4df7-162">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-163">El método tiene la capacidad, en el caso de que se haya establecido previamente una asociación de seguridad, para crear una asociación de seguridad nueva o actualizada de forma más eficaz o en un número menor de recorridos de ida y vuelta.</span><span class="sxs-lookup"><span data-stu-id="d4df7-163">The method has the ability, in the case where a security association has been previously established, to create a new or refreshed security association more efficiently or in a smaller number of round-trips.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-164"><span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**</span><span class="sxs-lookup"><span data-stu-id="d4df7-164"><span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-165">0x00002000</span><span class="sxs-lookup"><span data-stu-id="d4df7-165">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-166">El método muestra al servidor EAP que una sola entidad ha actuado como EAP del mismo nivel para todos los métodos que se ejecutan dentro de un método de túnel.</span><span class="sxs-lookup"><span data-stu-id="d4df7-166">The method demonstrates to the EAP server that a single entity has acted as the EAP peer for all methods executed within a tunnel method.</span></span> <span data-ttu-id="d4df7-167">El enlace también puede implicar que el servidor EAP muestra al sistema del mismo nivel que una sola entidad ha actuado como el servidor EAP para todos los métodos que se ejecutan dentro de un método de túnel.</span><span class="sxs-lookup"><span data-stu-id="d4df7-167">Binding may also imply that the EAP server demonstrates to the peer that a single entity has acted as the EAP server for all methods executed within a tunnel method.</span></span> <span data-ttu-id="d4df7-168">Si se ejecuta correctamente, el enlace sirve para mitigar las vulnerabilidades de tipo "Man in the Middle".</span><span class="sxs-lookup"><span data-stu-id="d4df7-168">If executed correctly, binding serves to mitigate man-in-the-middle vulnerabilities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-169"><span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**</span><span class="sxs-lookup"><span data-stu-id="d4df7-169"><span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-170">0x00004000</span><span class="sxs-lookup"><span data-stu-id="d4df7-170">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-171">El método demuestra que los ataques pasivos (por ejemplo, la captura de la conversación EAP) o los ataques activos (incluido el riesgo de la MSK o EMSK) no ponen en peligro la MSKs o la EMSKs anterior o posterior.</span><span class="sxs-lookup"><span data-stu-id="d4df7-171">The method demonstrates that passive attacks (such as capture of the EAP conversation) or active attacks (including compromise of the MSK or EMSK) do not compromise subsequent or prior MSKs or EMSKs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-172"><span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**</span><span class="sxs-lookup"><span data-stu-id="d4df7-172"><span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-173">0x00008000</span><span class="sxs-lookup"><span data-stu-id="d4df7-173">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-174">El método puede admitir la fragmentación y el reensamblado si los paquetes EAP superan la MTU mínima (unidad de transmisión máxima) de 1020 octetos.</span><span class="sxs-lookup"><span data-stu-id="d4df7-174">The method can support fragmentation and reassembly if EAP packets exceed the minimum MTU (maximum transmission unit) of 1020 octets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-175"><span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**</span><span class="sxs-lookup"><span data-stu-id="d4df7-175"><span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-176">0x00010000</span><span class="sxs-lookup"><span data-stu-id="d4df7-176">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-177">El método puede comunicar propiedades de canal protegidas por integridad, como identificadores de punto de conexión, que se pueden comparar con valores comunicados mediante mecanismos fuera de banda, como la [autenticación, autorización y cuentas](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) o el protocolo de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="d4df7-177">The method can communicate integrity-protected channel properties, such as endpoint identifiers, which can be compared to values communicated using out of band mechanisms - such as an [Authentication, Authorization, and Accounting](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) or the lower layer protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-178"><span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**</span><span class="sxs-lookup"><span data-stu-id="d4df7-178"><span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="d4df7-179">0x00020000</span><span class="sxs-lookup"><span data-stu-id="d4df7-179">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-180">El método es compatible con la protección de acceso a redes (NAP).</span><span class="sxs-lookup"><span data-stu-id="d4df7-180">The method supports Network Access Protection (NAP).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-181"><span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**</span><span class="sxs-lookup"><span data-stu-id="d4df7-181"><span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-182">0x00040000</span><span class="sxs-lookup"><span data-stu-id="d4df7-182">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-183">El método se puede usar en un equipo independiente.</span><span class="sxs-lookup"><span data-stu-id="d4df7-183">The method can be used on a standalone machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-184"><span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**</span><span class="sxs-lookup"><span data-stu-id="d4df7-184"><span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="d4df7-185">0x00080000</span><span class="sxs-lookup"><span data-stu-id="d4df7-185">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-186">El método admite el cifrado [de protocolo MPPE (cifrado punto a punto de Microsoft)](https://go.microsoft.com/fwlink/p/?linkid=83915) .</span><span class="sxs-lookup"><span data-stu-id="d4df7-186">The method supports [Microsoft Point-to-Point Encryption (MPPE) protocol](https://go.microsoft.com/fwlink/p/?linkid=83915) encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-187"><span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**</span><span class="sxs-lookup"><span data-stu-id="d4df7-187"><span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-188">0x00100000</span><span class="sxs-lookup"><span data-stu-id="d4df7-188">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-189">El método admite la tunelización de otros métodos EAP.</span><span class="sxs-lookup"><span data-stu-id="d4df7-189">The method supports tunneling of other EAP methods.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-190"><span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**</span><span class="sxs-lookup"><span data-stu-id="d4df7-190"><span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-191">0x00200000</span><span class="sxs-lookup"><span data-stu-id="d4df7-191">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-192">El método admite las propiedades configurables y tiene una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d4df7-192">The method supports configurable properties, and has a user interface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-193"><span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**</span><span class="sxs-lookup"><span data-stu-id="d4df7-193"><span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-194">0x00400000</span><span class="sxs-lookup"><span data-stu-id="d4df7-194">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-195">El método estaba certificado por el programa de Certificación EAP.</span><span class="sxs-lookup"><span data-stu-id="d4df7-195">The method was certified by the EAP Certification Program.</span></span> <span data-ttu-id="d4df7-196">Este bit solo debe ser enviado por métodos EAP que hayan pasado la certificación.</span><span class="sxs-lookup"><span data-stu-id="d4df7-196">This bit should only be sent by EAP methods that have passed certification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-197"><span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**</span><span class="sxs-lookup"><span data-stu-id="d4df7-197"><span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-198">0x01000000</span><span class="sxs-lookup"><span data-stu-id="d4df7-198">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-199">Windows 7 o posterior: el método se puede usar para autenticar un equipo en una red con las credenciales de los equipos.</span><span class="sxs-lookup"><span data-stu-id="d4df7-199">Windows 7 or later: The method can be used to authenticate a machine on to a network using the machines credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-200"><span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**</span><span class="sxs-lookup"><span data-stu-id="d4df7-200"><span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-201">0x02000000</span><span class="sxs-lookup"><span data-stu-id="d4df7-201">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-202">Windows 7 o posterior: el método se puede usar para autenticar a un usuario en una red con las credenciales de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="d4df7-202">Windows 7 or later: The method can be used to authenticate a user on to a network using the users credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-203"><span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="d4df7-203"><span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-204">0x04000000</span><span class="sxs-lookup"><span data-stu-id="d4df7-204">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-205">Windows 7 o posterior: el método admite el envío de la identidad del usuario en un canal protegido.</span><span class="sxs-lookup"><span data-stu-id="d4df7-205">Windows 7 or later: The method supports sending the user identity in a protected channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-206"><span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**</span><span class="sxs-lookup"><span data-stu-id="d4df7-206"><span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-207">0x08000000</span><span class="sxs-lookup"><span data-stu-id="d4df7-207">0x08000000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-208">Windows 7 o posterior: el método es un método de túnel y admite el encadenamiento de métodos EAP dentro del túnel.</span><span class="sxs-lookup"><span data-stu-id="d4df7-208">Windows 7 or later: The method is a tunnelled method and supports EAP method chaining within the tunnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-209"><span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**</span><span class="sxs-lookup"><span data-stu-id="d4df7-209"><span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-210">0x10000000</span><span class="sxs-lookup"><span data-stu-id="d4df7-210">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-211">Windows 7 o posterior: el método admite la equivalencia de estado compartida tal y como se define en [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).</span><span class="sxs-lookup"><span data-stu-id="d4df7-211">Windows 7 or later: The method supports shared state equivalence as defined in [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4df7-212"><span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**</span><span class="sxs-lookup"><span data-stu-id="d4df7-212"><span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4df7-213">0x80000000</span><span class="sxs-lookup"><span data-stu-id="d4df7-213">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="d4df7-214">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d4df7-214">Reserved.</span></span> <span data-ttu-id="d4df7-215">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d4df7-215">Not used.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4df7-216">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4df7-216">Requirements</span></span>



| <span data-ttu-id="d4df7-217">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4df7-217">Requirement</span></span> | <span data-ttu-id="d4df7-218">Value</span><span class="sxs-lookup"><span data-stu-id="d4df7-218">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4df7-219">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4df7-219">Minimum supported client</span></span><br/> | <span data-ttu-id="d4df7-220">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d4df7-220">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d4df7-221">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4df7-221">Minimum supported server</span></span><br/> | <span data-ttu-id="d4df7-222">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d4df7-222">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4df7-223">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4df7-223">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4df7-224"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4df7-224"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4df7-225">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4df7-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4df7-226">Claves del registro para los métodos EAP</span><span class="sxs-lookup"><span data-stu-id="d4df7-226">Registry Keys for EAP Methods</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="d4df7-227">Constantes de EAPHost comunes</span><span class="sxs-lookup"><span data-stu-id="d4df7-227">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

