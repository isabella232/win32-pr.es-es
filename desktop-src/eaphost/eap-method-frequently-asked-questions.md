---
title: Preguntas más frecuentes sobre el método EAP
description: Proporciona respuestas a las preguntas de programación más frecuentes sobre la creación de métodos EAP.
ms.assetid: 244e048f-4cc0-4094-a2b9-0f84674a293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fddcc2194f5fe68dc660e40331be1b790b73386
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "105695788"
---
# <a name="eap-method-frequently-asked-questions"></a>Preguntas más frecuentes sobre el método EAP

En este tema se proporcionan respuestas a las preguntas de programación más frecuentes sobre la creación de métodos EAP.

## <a name="eap-method-frequently-asked-questions"></a>Preguntas más frecuentes sobre el método EAP



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
<td>¿Qué son los &quot; datos de configuración &quot; ?</td>
<td>Los datos de &quot; configuración &quot; y los &quot; datos de conexión &quot; son sinónimos.</td>
</tr>
<tr class="even">
<td>¿Qué son los &quot; datos de conexión &quot; ?</td>
<td>&quot;Los datos &quot; de conexión son un BLOB opaco específico del método EAP que contiene información de configuración para el método. El método crea estos datos de conexión cuando se configura inicialmente y nunca se interpreta ni modifica en ningún otro componente que el propio método EAP.</td>
</tr>
<tr class="odd">
<td>¿Qué son &quot; las credenciales &quot; ?</td>
<td>Los términos &quot; credenciales &quot; y &quot; datos de usuario &quot; son sinónimos.</td>
</tr>
<tr class="even">
<td>¿Qué son los &quot; datos de usuario &quot; ?</td>
<td>&quot;Los datos &quot; de usuario son un BLOB opaco específico del método EAP que contiene datos de credenciales de usuario, como un nombre de usuario y una contraseña. Los datos de usuario nunca se interpretan ni modifican en ningún otro componente que el propio método EAP. Los términos &quot; datos &quot; y &quot; credenciales del usuario &quot; son sinónimos.</td>
</tr>
<tr class="odd">
<td>¿Qué es un &quot; atributo EAP &quot; ?</td>
<td>Un &quot; atributo EAP &quot; es una estructura de datos que contiene un tipo predeterminado de datos. Los atributos se utilizan para comunicar información entre los métodos y suplicantes EAP, o entre los métodos EAP y los autenticadores. Las implementaciones del mismo nivel y autenticador de un método EAP pueden intercambiar estos atributos a través de una red.</td>
</tr>
<tr class="even">
<td>¿La API de configuración y la API en tiempo de ejecución aparecen en el mismo archivo DLL de método?</td>
<td>Sí. Asegúrese de especificar la distinción al configurar las entradas del registro para el propio método EAP. La ruta de acceso de configuración y la ruta de acceso del mismo nivel deben ser iguales.</td>
</tr>
<tr class="odd">
<td>¿La API de configuración y la API en tiempo de ejecución aparecen en archivos dll de método independientes?</td>
<td>Sí. Asegúrese de especificar la distinción al configurar las entradas del registro para el propio método EAP. La configuración y las rutas de acceso del mismo nivel deben apuntar a los archivos dll correctos.</td>
</tr>
<tr class="even">
<td>Cómo instalar un método EAP?</td>
<td>Para instalar un método EAP, primero debe implementar [<strong>DllRegisterServer</strong>] (/Windows/Win32/API/olectl/NF-olectl-DllRegisterServer) y [<strong>DllUnregisterServer</strong>] (/Windows/Win32/API/olectl/NF-olectl-DllUnregisterServer) en el propio archivo DLL del método EAP. Después, utilice <strong>regsvr32.exe</strong> para instalar y desinstalar el método. También se deben establecer las claves del registro adecuadas. Para obtener más información, consulte [instalar un método EAP](installing-an-eap-method.md).<br/></td>
</tr>
<tr class="odd">
<td>¿Qué es la compatibilidad con la [protección de acceso a redes](/windows/desktop/NAP/network-access-protection-start-page) (NAP) en banda?</td>
<td>Cuando está habilitada la compatibilidad con NAP en banda, los paquetes NAP se transportan dentro de paquetes de método EAP. Por el contrario, cuando la compatibilidad de NAP fuera de banda está habilitada, el intercambio del [Informe de mantenimiento](https://go.microsoft.com/fwlink/p/?linkid=83917) (SOH) de NAP se produce a través de medios distintos de los paquetes de método interno a EAP y los certificados generados por NAP se usan en la autenticación de método EAP.</td>
</tr>
<tr class="even">
<td>¿Se puede habilitar la compatibilidad con NAP en banda para mi método EAP?</td>
<td>Sí, se puede habilitar la compatibilidad con NAP en banda para el método EAP. Para obtener más información, consulte [habilitación de la compatibilidad con In-Band NAP para métodos EAP](enabling-in-band-nap-support.md).</td>
</tr>
<tr class="odd">
<td>¿Cómo funciona la autenticación flexible de EAP a través de la tunelización segura (EAP-FAST)?</td>
<td>El escenario EAP-FAST funciona de la siguiente manera. <br/>
<ul>
<li>El método procesa un cambio de contraseña en el inicio de sesión único (SSO) que emplea la interfaz de usuario del método.</li>
<li>El método devuelve el atributo [<strong>eatCredentialsChanged</strong>] (/Windows/Desktop/API/eaptypes/ne-eaptypes-eap_attribute_type).</li>
<li>El solicitante indica al usuario que las credenciales han cambiado y solicita al usuario que vuelva a escribir sus credenciales.</li>
<li>El suplicante vuelve a escribir las credenciales del usuario y envía esas credenciales al método.</li>
</ul>
Para obtener más información sobre EAP-FAST, consulte [Autenticación flexible de EAP a través de la tunelización segura](https://go.microsoft.com/fwlink/p/?linkid=84010) (EAP-FAST).</td>
</tr>
<tr class="even">
<td>¿Qué es la clave precompartida (PSK)?</td>
<td>Método de transmisión y recepción de señales digitales en las que la fase de una señal transmitida es distinta para transmitir la información. El campo de entrada [<strong>EAPConfigInputPSK</strong>] (/Windows/Desktop/API/eaptypes/ne-eaptypes-eap_config_input_field_type) contiene la PSK EAP-FAST de usuario.</td>
</tr>
<tr class="odd">
<td>¿Qué es WOW y cómo es importante en EAPHost?</td>
<td>Microsoft Windows-32-bit-on-Windows-64-bit (WOW) es un componente del sistema operativo en Windows de 64 bits que admite la aplicación de la plataforma x86 de 32 bits. Normalmente, un autor de método EAP definiría alguna forma de estructura de C/C++ para encapsular los datos de configuración, los datos de credenciales y los datos interactivos de la interfaz de usuario. Para evitar incompatibilidades en WOW y en otros escenarios, es importante asegurarse de que las estructuras de datos se alineen de forma similar en distintas arquitecturas de procesador (procesadores de 32 bits y de 64 bits). Normalmente, el relleno ficticio se usa para alinear los campos de modo que los datos de configuración, credenciales e interfaz de usuario interactiva sean idénticos en los procesadores 32 y 64 bits.</td>
</tr>
<tr class="even">
<td>¿Qué son &quot; &quot; los códigos de acción y en qué condiciones se devuelven estos códigos de acción?</td>
<td>&quot;Los códigos de acción &quot; permiten a los métodos controlar el flujo de autenticación y son parte de la máquina de Estados. Son los valores devueltos por un método EAP para indicar la acción siguiente que debe tomar EAPHost. Por ejemplo, un código de acción podría indicar a EAPHost que el método EAP tiene un paquete listo para la transmisión. El suplicante se atiene a todos los códigos de acción devueltos por un método EAP, pero nunca emite códigos de acción. Para obtener más información, consulte [códigos de acción de suplicante de EAP del mismo nivel](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).<br/></td>
</tr>
<tr class="odd">
<td>¿Cuándo devuelve un método [<strong>EapPeerMethodResponseActionDiscard</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) y qué significa este código de acción para EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionDiscard</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) es devuelto por un método EAP para indicar a EAPHost que debe descartar el paquete que proporcionó al método. En concreto, el método ha determinado que el paquete no es válido. Después, EAPHost espera el siguiente paquete.</td>
</tr>
<tr class="even">
<td>¿Cuándo devuelve un método [<strong>EapPeerMethodResponseActionSend</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) y qué significa este código de acción para EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionSend</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) es devuelto por un método EAP para indicar a EAPHost que el siguiente paquete recibido por EAPHost debe enviarse al servidor de acceso a la red (NAS).</td>
</tr>
<tr class="odd">
<td>¿Cuándo devuelve un método [<strong>EapPeerMethodResponseActionResult</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) y qué significa este código de acción para EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionResult</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) es devuelto por un método EAP para indicar a EAPHost que la sesión de autenticación ha finalizado y que los resultados de esa sesión están disponibles.</td>
</tr>
<tr class="even">
<td>¿Cuándo devuelve un método [<strong>EapPeerMethodResponseActionInvokeUI</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) y qué significa este código de acción para EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionInvokeUI</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) se devuelve mediante un método EAP para indicar a EAPHost que la entrada del usuario es necesaria para continuar con la autenticación y que se debe mostrar un cuadro de diálogo de interfaz de usuario para obtener esa entrada. Una vez que se han obtenido los datos de entrada del usuario, EAPHost puede volver a llamar al método EAP con los datos de contexto de la interfaz de usuario actualizados.</td>
</tr>
<tr class="odd">
<td>¿Cuándo devuelve un método [<strong>EapPeerMethodResponseActionRespond</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) y qué significa este código de acción para EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionRespond</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) se devuelve mediante un método EAP para indicar a EAPHost que el método EAP tiene atributos disponibles para que EAPHost los use durante la autenticación. EAPHost obtiene los atributos llamando al método [<strong>EapPeerGetResponseAttributes</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeergetresponseattributes) seguido de una llamada al método [<strong>EapPeerSetResponseAttributes</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeersetresponseattributes).</td>
</tr>
<tr class="even">
<td>¿Cuándo devuelve un método [<strong>EapPeerMethodResponseActionNone</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) y qué significa este código de acción para EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionNone</strong>] un método EAP devuelve (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) para indicar a EAPHost que no se requiere ninguna acción en este momento.</td>
</tr>
<tr class="odd">
<td>¿Puedo habilitar el seguimiento en el lado del autenticador?</td>
<td>Sí. Para obtener más información, vea [Habilitar el seguimiento](enabling-tracing.md).</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de API de método del mismo nivel de EAPHost](eap-host-peer-method-api-reference.md)
</dt> <dt>

[Preguntas frecuentes generales de EAPHost](general-frequently-asked-questions.md)
</dt> <dt>

[Preguntas más frecuentes sobre Suplicador de EAPHost](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[Preguntas más frecuentes sobre el desarrollo de EAPHost](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

 

