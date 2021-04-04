---
title: Preguntas más frecuentes sobre el suplicante de EAPHost
description: En este tema se proporcionan respuestas a preguntas frecuentes acerca de la API de suplicante de EAPHost.
ms.assetid: bf8db711-386e-47c2-be47-4cfd6c4d8d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38e75220b186ef58f2b9f264f8f5fc0550a4119
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "103797625"
---
# <a name="eaphost-supplicant-frequently-asked-questions"></a>Preguntas más frecuentes sobre el suplicante de EAPHost

En este tema se proporcionan respuestas a preguntas frecuentes acerca de la API de suplicante de EAPHost.

### <a name="eaphost-supplicant-frequently-asked-questions"></a>Preguntas más frecuentes sobre el suplicante de EAPHost



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
<td>¿Por qué es necesario llamar a [<strong>EapHostPeerInitialize</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerinitialize) y [<strong>EapHostPeerUninitialize</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeeruninitialize)?</td>
<td>[<strong>EapHostPeerInitialize</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerinitialize) y [<strong>EapHostPeerUninitialize</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeeruninitialize) inicializan y anulan la inicialización del entorno com que se usa para la comunicación entre procesos (IPC) entre un suplicante y EAPHost.</td>
</tr>
<tr class="even">
<td>¿Qué funciones se deben invocar en subprocesos que tienen COM inicializado para [un contenedor uniproceso](/previous-versions/ms810413(v=msdn.10)) (STA)?</td>
<td>[<strong>EapHostPeerInvokeConfigUI</strong>] se debe llamar a (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), [<strong>EapHostPeerInvokeInteractiveUI</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) y [<strong>EapHostAuthenticatorInvokeConfigUI</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodauthenticatorapis/NF-eapmethodauthenticatorapis-eapmethodauthenticatorinvokeconfigui) en subprocesos que tienen com inicializado para Sta. Esto puede lograrse llamando a la API COM [<strong>CoInitialize</strong>] (/Windows/Win32/API/objbase/NF-objbase-CoInitialize); Cuando el suplicante ha finalizado con el subproceso STA [<strong>CoUninitialize</strong>] (/Windows/Win32/API/combaseapi/NF-combaseapi-CoUninitialize) se debe llamar antes de salir.</td>
</tr>
<tr class="odd">
<td>¿Cómo exporta EAPHost el material de creación de claves?</td>
<td>Los métodos EAP de EAPHost exportan las claves de sesión maestra (MSKs) en forma de claves de cifrado punto a punto de Microsoft (MPPE) a los suplicantes. El suplicante puede generar material de clave adicional, como las claves maestras en pares (PMKs), mediante la MSK. Para que los métodos generen otras claves durante la autenticación, los métodos pueden proporcionar esas claves como atributos específicos del proveedor a los suplicantes.</td>
</tr>
<tr class="even">
<td>¿Qué es una clave de sesión maestra extendida (EMSK)?</td>
<td>EMSK es material de creación de claves adicional que exporta el método EAP. EMSK tiene al menos 64 octetos de longitud. EMSK se comparte entre el cliente y el servidor EAP, pero no se comparte con el autenticador ni con ningún otro tercero. Actualmente, EMSK se reserva para uso futuro. Para obtener más información, consulte [requisitos del método de protocolo de autenticación extensible (EAP) para LAN inalámbricas](https://go.microsoft.com/fwlink/p/?linkid=84064).<br/></td>
</tr>
<tr class="odd">
<td>¿Cuándo usa un método o genera un atributo?</td>
<td>Si un método EAP genera atributos o EMSK, el suplicante consumirá atributos. Normalmente, los atributos que utilizan los suplicantes son claves. Los atributos consumidos son <strong>eatPeerId</strong>, <strong>eatServerId</strong>, <strong>eatMethodId</strong>, <strong>eatEMSK</strong>y <strong>eatCredentialsChanged</strong>. Para obtener más información, vea [<strong>EAP_ATTRIBUTE_TYPE</strong>] (/Windows/Desktop/API/eaptypes/ne-eaptypes-eap_attribute_type). Un método EAP puede exportar material de EMSK específico de la aplicación adicional, como:
<ul>
<li>Identificador de sesión</li>
<li>[Protección de acceso a redes](/windows/desktop/NAP/network-access-protection-start-page) (NAP)</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>¿Qué atributos usa [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) ?</td>
<td>El suplicante [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) nativo utilizará los siguientes atributos de autenticación de EAPHost:
<ul>
<li>Notificación de cambio de contraseña</li>
<li>Claves de envío y recepción de cifrado punto a punto de Microsoft (MPPE). VendorId/VendorType = 331/16 y 311/1</li>
</ul>
Las claves MPPE son claves generadas al final de la autenticación correcta, por parte del mismo nivel y del autenticador. Estas claves las usan [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) y el servidor de acceso a la red (NAS) para cifrar y descifrar los paquetes que se envían y reciben.<br/></td>
</tr>
<tr class="odd">
<td>¿Cuál es el propósito de la marca de EAP_PEER_FLAG_GUEST_ACCESS en EAPHost?</td>
<td>Cuando esta marca se establece en [<strong>EAPHostPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession), EAPHost lo interpreta como una solicitud de autorización de invitado y devuelve una respuesta de identidad <strong>nula</strong> que se pasa al solicitante y se devuelve al servidor EAP.</td>
</tr>
<tr class="even">
<td>¿Cómo solicita el solicitante la autenticación del equipo?</td>
<td>La autenticación del equipo se solicita estableciendo la marca [<strong>EAP_FLAG_MACHINE_AUTH</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession).</td>
</tr>
<tr class="odd">
<td>¿Cómo solicita el solicitante la autenticación de usuarios?</td>
<td>La autenticación de usuario se solicita al no establecer la marca [<strong>EAP_FLAG_MACHINE_AUTH</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession).</td>
</tr>
<tr class="even">
<td>¿Cuándo se usa [<strong>EapHostPeerFreeErrorMemory</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerfreeerrormemory) en lugar de la función [<strong>EapHostFreeEapError</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerfreeeaperror)?</td>
<td>La función [<strong>EapHostPeerFreeErrorMemory</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerfreeerrormemory) solo se usa para liberar las estructuras [<strong>EAP_ERROR</strong>] (/Windows/Desktop/API/eaptypes/NS-eaptypes-eap_error) devueltas por las API de configuración de EAPHost. Las API de configuración de EAPHost se definen en EapHostPeerConfigApis. h. En cambio, la función [<strong>EapHostPeerFreeEapError</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerfreeeaperror) se usa para liberar <strong>EAP_ERROR</strong> estructuras devueltas por las API en tiempo de ejecución de EAPHost. Las API en tiempo de ejecución de EAPHost se definen en EapPApis. h. Nunca use la versión en tiempo de ejecución de la API con la versión de configuración de las API; para ello, podría producir resultados inesperados.<br/></td>
</tr>
<tr class="odd">
<td>He implementado mi interfaz de usuario en el mismo subproceso que utilizo para procesar una sesión de autenticación EAP en el suplicante. Después de haber generado un cuadro de diálogo de interfaz de usuario interactiva para obtener credenciales u otros datos de entrada de usuario, se produce un error en la siguiente llamada de EAPHost a un método EAP peer con <strong>ERROR_OBJECT_DISCONNECTED</strong>. ¿Por qué se ha producido esto y cómo lo soluciono?</td>
<td>Aunque las API del lado cliente de EAPHost son todas las API de estilo de C, estas API de C son solo contenedores de las API de COM correspondientes. Las API de estilo C se ejecutan en un entorno COM multiproceso. El código de interfaz de usuario normalmente se ejecuta en el modelo de subprocesos de apartamento. Dado que los dos modelos de subprocesos entran en conflicto entre sí, no ejecute el código de la interfaz de usuario en el mismo subproceso que procesa las autenticaciones de EAP.</td>
</tr>
<tr class="even">
<td>¿Por qué la API [<strong>EapHostPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) toma un puntero de función de devolución de llamada [<em>NotificationHandler</em>] (/Previous-Versions/Windows/Desktop/API) como parámetro?</td>
<td>[<em>NotificationHandler</em>] (/Previous-Versions/Windows/Desktop/API) es el mecanismo por el que se notifica a un suplicante que debe volver a autenticarse. Hay varios escenarios en los que es necesario volver a autenticar el suplicante, incluida la autenticación con [protección de acceso a redes](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</td>
</tr>
<tr class="odd">
<td>¿Cuál es el propósito del parámetro <em>pConnectionId</em> en la API [<strong>EapHostPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession)?</td>
<td><em>pConnectionId</em> es un puntero a un valor GUID definido por el suplicante que se usa para identificar una conexión de red que pertenece al suplicante. Cuando se llama a la función de devolución de llamada [<em>NotificationHandler</em>] (/Previous-Versions/Windows/Desktop/API), este GUID se pasa para identificar la conexión de red que el suplicante usará para las solicitudes de reautenticación.</td>
</tr>
<tr class="even">
<td>Cómo saber si hay un cambio en el estado de cuarentena?</td>
<td>El usuario recibirá una notificación visual de un cambio en el estado de cuarentena solo si hay al menos una interfaz registrada del cliente de cumplimiento de cuarentena de protección de acceso a redes (QEC) en el sistema. Si es así, cuando se intenta la reautenticación, se notificará al usuario de un cambio de estado de cuarentena a través de una ventana emergente.</td>
</tr>
<tr class="odd">
<td>Cómo saber si hay una interfaz registrada de NAP QEC en el sistema?</td>
<td>Abra una ventana con privilegios elevados y ejecute el siguiente comando netsh: &quot; netsh NAP Client show State &quot; . Para obtener más información, vea [comandos Netsh](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</td>
</tr>
<tr class="even">
<td>Si el solicitante vuelve a autenticarse, ¿qué identificador de conexión debe usar el QEC durante la reautenticación?</td>
<td>QEC debe usar el mismo identificador de conexión que se usó para la sesión anterior.</td>
</tr>
<tr class="odd">
<td>Solo hay un método suplicante de EAPHost disponible para mostrar los cuadros de diálogo de la interfaz de usuario, pero los métodos EAP tienen varios tipos de llamadas específicas de la interfaz de usuario. ¿Qué método debe llamar el solicitante cuando obtiene el código de acción <strong>EapHostPeerResponseInvokeUI</strong> , lo que indica que el suplicante debe mostrar un cuadro de diálogo de la interfaz de usuario?</td>
<td>El usuario no requiere ninguna acción porque EAPHost sabe a qué función de método llamar. Por ejemplo, cuando se devuelve el código de acción <strong>EapHostPeerResponseInvokeUI</strong> , el solicitante llama a estas tres funciones en el orden siguiente: [<strong>EapHostPeerGetUIContext</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeergetuicontext), [<strong>EapHostPeerInvokeInteractiveUI</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) y [<strong>EapHostPeerSetUIContext</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeersetuicontext).</td>
</tr>
<tr class="even">
<td>¿Cuál es la diferencia entre un BLOB de credenciales y un BLOB de configuración?</td>
<td>El BLOB de credenciales solo contiene datos de usuario, como el nombre de usuario, la contraseña y el PIN. El BLOB de configuración contiene la configuración que controla el comportamiento del método.</td>
</tr>
<tr class="odd">
<td>¿Puedo habilitar el seguimiento en el lado del cliente de EAPHost?</td>
<td>Sí. Para obtener más información, vea [Habilitar el seguimiento](enabling-tracing.md).</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de API suplicante de EAPHost](eap-host-supplicant-api-reference.md)
</dt> <dt>

[Preguntas frecuentes generales de EAPHost](general-frequently-asked-questions.md)
</dt> <dt>

[Preguntas más frecuentes sobre el método EAPHost](eap-method-frequently-asked-questions.md)
</dt> <dt>

[Preguntas más frecuentes sobre el desarrollo de EAPHost](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

