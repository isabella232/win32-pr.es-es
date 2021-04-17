---
title: Preguntas frecuentes generales
description: Lea las respuestas a las preguntas más frecuentes sobre las API de EAPHost, como "¿Cuál es la duración de una autenticación?".
ms.assetid: 4025e8da-8cb1-477b-86bb-7756d9636224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb0dd9b3b997d8682c3cab1ba91afc3ee2db7ba
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "105714501"
---
# <a name="general-frequently-asked-questions"></a>Preguntas frecuentes generales

En el siguiente tema se proporcionan respuestas a las preguntas más frecuentes sobre las API de EAPHost.

### <a name="general-frequently-asked-questions"></a>Preguntas frecuentes generales



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pregunta</th>
<th>Respuesta</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>¿Qué es un suplicante?</td>
<td>El suplicante es la entidad que se va a autenticar mediante EAPHost. Los suplicantes típicos son los clientes de [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) , 802,3 clientes y el servicio de enrutamiento y acceso remoto (RRAS), los clientes de punto a punto (PPP).</td>
</tr>
<tr class="even">
<td>¿Qué es un elemento del mismo nivel?</td>
<td>El elemento del mismo nivel es el lado cliente de una autenticación EAP.</td>
</tr>
<tr class="odd">
<td>¿Cómo difiere un elemento del mismo nivel de un suplicante?</td>
<td>El solicitante transporta los paquetes, mientras que un elemento del mismo nivel no lo hace. Sin embargo, los términos del mismo nivel, el suplicante y el cliente son principalmente sinónimos.</td>
</tr>
<tr class="even">
<td>¿Qué es un autenticador?</td>
<td>El autenticador es el punto de acceso inalámbrico, el servidor de acceso a la red (NAS) o el dispositivo de acceso a la red (NAD) que autentica al solicitante. El autenticador también se conoce como servidor EAP.</td>
</tr>
<tr class="odd">
<td>¿Cuál es la duración de una autenticación?</td>
<td>La duración de una sesión de autenticación única en el lado cliente es todo lo que se produce entre las funciones [<strong>EapHostPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) y [<strong>EapHostPeerEndSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerendsession) a las que se llama. La vigencia en el lado del autenticador es todo lo que se produce entre las funciones [<strong>EapPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerbeginsession) y [<strong>EapPeerEndSession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerendsession).</td>
</tr>
<tr class="even">
<td>¿Qué es un BLOB? ¿Por qué se puede convertir un BLOB de configuración (binario) en XML?</td>
<td>Un BLOB es un objeto binario grande. XML tiene varias ventajas con respecto a un BLOB de configuración binaria. Los datos de configuración que se almacenan en XML son legibles para el usuario, editables y multiplataforma.</td>
</tr>
<tr class="odd">
<td>¿Cuándo se vuelve a convertir un BLOB XML almacenado en un BLOB binario?</td>
<td>Es posible almacenar un BLOB binario o XML, pero siempre debe volver a convertir el BLOB XML en un BLOB binario antes de usarlo con las API de tiempo de ejecución; las API de tiempo de ejecución no pueden aceptar un directorio XML.</td>
</tr>
<tr class="even">
<td>¿Qué son los métodos nativos?</td>
<td>Los métodos EAP nativos usan la nueva API de EAPHost.</td>
</tr>
<tr class="odd">
<td>¿Qué son los métodos heredados?</td>
<td>Los métodos EAP heredados se definen en la [Referencia del Protocolo de autenticación extensible](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference). Los métodos EAP heredados están disponibles para su uso en Windows Vista y Windows Server 2008. Es posible que estos métodos no estén disponibles para su uso en versiones posteriores del sistema operativo.</td>
</tr>
<tr class="even">
<td>¿Cuál es la diferencia entre los métodos heredados y nativos?</td>
<td>Las API nativas son más sencillas y tienen menos características. Todos los nuevos métodos EAP deben escribirse con la API de EAPHost.</td>
</tr>
<tr class="odd">
<td>¿Qué es la &quot; Directiva de grupo &quot; ?</td>
<td>Para obtener una descripción de la Directiva de grupo, vea [Directiva de grupo colección](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</td>
</tr>
<tr class="even">
<td>¿Pueden las funciones de EAPHost invalidar la Directiva de configuración especificada por la Directiva de grupo?</td>
<td>No, nunca. Si se usa la Directiva de grupo, la configuración de directiva de grupo siempre invalidará las opciones de configuración de EAPHost.</td>
</tr>
<tr class="odd">
<td>¿Qué es el inicio de sesión único (SSO)?</td>
<td>[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) es un mecanismo de autenticación de nivel 2. En función de la configuración de SSO, SSO permite a los usuarios autenticarse en la red mediante la autenticación de [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) antes o inmediatamente después de iniciar sesión en Windows. SSO puede configurarse para usar credenciales de Windows para la autenticación de red (en cuyo caso los usuarios escriben sus credenciales una sola vez) o usan credenciales diferentes para la autenticación de Windows y de red. Para obtener más información, consulte [SSO y PLAP](understanding-sso-and-plap.md).<br/></td>
</tr>
<tr class="even">
<td>Qué es el proveedor de acceso previo al inicio de sesión (PLAP)</td>
<td>Para obtener más información, consulte [SSO y PLAP](understanding-sso-and-plap.md).</td>
</tr>
<tr class="odd">
<td>¿Qué es el protocolo de autenticación extensible protegido (PEAP)?</td>
<td>Para obtener más información, vea [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) y [acerca del Protocolo de autenticación extensible](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol).</td>
</tr>
<tr class="even">
<td>¿Cómo se trata PEAP con la reanudación de la sesión y la reautenticación?</td>
<td>La reanudación de la sesión y la reautenticación suele producirse durante la itinerancia en una red inalámbrica. La API de protección de datos de Windows (DPAPI) proporciona una manera de proteger y enlazar datos a un usuario y, opcionalmente, la sesión de inicio de sesión. El autor de la llamada proporciona a [<strong>CryptProtectMemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptprotectmemory) un búfer sin cifrar y DPAPI cifrará la memoria en su lugar. Más adelante, el autor de la llamada puede pasar el búfer cifrado a [<strong>CryptUnprotectMemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptunprotectmemory) y DPAPI descifrará la memoria, una vez más. Para obtener más información, consulte la [extensión de aplicación interna TLS (TSL/IA)](https://go.microsoft.com/fwlink/p/?linkid=84011) y [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).<br/></td>
</tr>
<tr class="odd">
<td>¿Qué es la seguridad de nivel de EAP-Transport (EAP-TLS)?</td>
<td>EAP-TLS es un protocolo cliente-servidor en el que se suelen usar perfiles de certificado distintos para el cliente y el servidor. Para obtener más información, consulte [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).<br/></td>
</tr>
<tr class="even">
<td>Cómo implementar un cambio de contraseña con la API de autoridad de seguridad local (LSA)?</td>
<td>Use la función [<strong>LsaCallAuthenticationPackage</strong>] (/Windows/Desktop/API/ntsecapi/NF-ntsecapi-lsacallauthenticationpackage) para implementar un cambio de contraseña.</td>
</tr>
<tr class="odd">
<td>¿Por qué deseo habilitar el seguimiento en EAPHost?</td>
<td>Los registros de seguimiento contienen información de depuración (disponible solo en inglés) que puede ayudar a los desarrolladores y asociados de Microsoft a encontrar las causas raíz de cualquier problema experimentado con el proceso de autenticación. Para obtener más información, vea [Habilitar el seguimiento](enabling-tracing.md).<br/></td>
</tr>
<tr class="even">
<td>¿Por qué encuentro el código de error, NTE_BAD_KEY_STATE (0x8009000BL) cuando uso la API de [Criptografía](/windows/desktop/SecCrypto/cryptography-portal) para iniciar sesión en el intercambio de EAP-TLS?</td>
<td>En Winerror. h NTE_BAD_KEY_STATE (0x8009000BL) se define como una &quot; clave no válida para su uso en el estado especificado &quot; . Este error se devuelve normalmente en los escenarios siguientes.
<ul>
<li>Al intentar exportar un BLOB de clave privada no exportable</li>
<li>Cuando se intenta generar de forma incorrecta un identificador hash de función pseudoaleatorios (PRF) mediante [<strong>CryptCreateHash</strong>] (/Windows/Desktop/API/wincrypt/NF-wincrypt-cryptcreatehash)</li>
</ul>
Para obtener más información, consulte [Finalizar mensajes en el protocolo TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</td>
</tr>
<tr class="odd">
<td>¿Qué es una función pseudoaleatorios (PRF)?</td>
<td>Una función que toma una clave, una etiqueta y una inicialización como entrada y, a continuación, genera una salida de longitud arbitraria. Para obtener más información, consulte [Finalizar mensajes en el protocolo TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).<br/></td>
</tr>
<tr class="even">
<td>¿Cómo se enlaza EAPHost a adaptadores de red?</td>
<td>EAPHost permite que varios suplicantes operen simultáneamente, y cada suplicante puede enlazar a varios adaptadores de red. Los suplicantes de EAPHost proporcionan enlaces a los niveles de red y controlan el proceso de autenticación. Los suplicantes contienen la configuración de autenticación. Los suplicantes también guardan el estado y proporcionan una seguridad de conexión posterior. Dado que EAPHost no se enlaza directamente a ningún mecanismo de red, es posible la extensibilidad del suplicante.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Preguntas más frecuentes sobre Suplicador de EAPHost](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[Preguntas más frecuentes sobre el método EAPHost](eap-method-frequently-asked-questions.md)
</dt> <dt>

[Preguntas más frecuentes sobre el desarrollo de EAPHost](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

