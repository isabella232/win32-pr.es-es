---
title: MPTHREAT_CATEGORY enumeración (MpClient.h)
description: Posibles categorías de amenazas.
ms.assetid: 478ED59E-5D3C-43B3-A89D-44A649EDD086
keywords:
- MPTHREAT_CATEGORY enumeración heredada de Windows environment
- PMPTHREAT_CATEGORY puntero de enumeración heredado Windows de entorno
topic_type:
- apiref
api_name:
- MPTHREAT_CATEGORY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a149ef6ce6ebadacbac6f0dd35247d793ca7000
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568720"
---
# <a name="mpthreat_category-enumeration"></a>Enumeración MPTHREAT \_ CATEGORY

Posibles categorías de amenazas.

## <a name="syntax"></a>Sintaxis

```C++
typedef enum tagMPTHREAT_CATEGORY {
  MP_THREAT_CATEGORY_INVALID                    = 0,
  MP_THREAT_CATEGORY_ADWARE                     = 1,
  MP_THREAT_CATEGORY_SPYWARE                    = 2,
  MP_THREAT_CATEGORY_PASSWORDSTEALER            = 3,
  MP_THREAT_CATEGORY_TROJANDOWNLOADER           = 4,
  MP_THREAT_CATEGORY_WORM                       = 5,
  MP_THREAT_CATEGORY_BACKDOOR                   = 6,
  MP_THREAT_CATEGORY_REMOTEACCESSTROJAN         = 7,
  MP_THREAT_CATEGORY_TROJAN                     = 8,
  MP_THREAT_CATEGORY_EMAILFLOODER               = 9,
  MP_THREAT_CATEGORY_KEYLOGGER                  = 10,
  MP_THREAT_CATEGORY_DIALER                     = 11,
  MP_THREAT_CATEGORY_MONITORINGSOFTWARE         = 12,
  MP_THREAT_CATEGORY_BROWSERMODIFIER            = 13,
  MP_THREAT_CATEGORY_COOKIE                     = 14,
  MP_THREAT_CATEGORY_BROWSERPLUGIN              = 15,
  MP_THREAT_CATEGORY_AOLEXPLOIT                 = 16,
  MP_THREAT_CATEGORY_NUKER                      = 17,
  MP_THREAT_CATEGORY_SECURITYDISABLER           = 18,
  MP_THREAT_CATEGORY_JOKEPROGRAM                = 19,
  MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL      = 20,
  MP_THREAT_CATEGORY_SOFTWAREBUNDLER            = 21,
  MP_THREAT_CATEGORY_STEALTHNOTIFIER            = 22,
  MP_THREAT_CATEGORY_SETTINGSMODIFIER           = 23,
  MP_THREAT_CATEGORY_TOOLBAR                    = 24,
  MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE      = 25,
  MP_THREAT_CATEGORY_TROJANFTP                  = 26,
  MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE  = 27,
  MP_THREAT_CATEGORY_ICQEXPLOIT                 = 28,
  MP_THREAT_CATEGORY_TROJANTELNET               = 29,
  MP_THREAT_CATEGORY_EXPLOIT                    = 30,
  MP_THREAT_CATEGORY_FILESHARINGPROGRAM         = 31,
  MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL      = 32,
  MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE    = 33,
  MP_THREAT_CATEGORY_TOOL                       = 34,
  MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE     = 36,
  MP_THREAT_CATEGORY_TROJAN_DROPPER             = 37,
  MP_THREAT_CATEGORY_TROJAN_MASSMAILER          = 38,
  MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE  = 39,
  MP_THREAT_CATEGORY_TROJAN_PROXYSERVER         = 40,
  MP_THREAT_CATEGORY_VIRUS                      = 42,
  MP_THREAT_CATEGORY_KNOWN                      = 43,
  MP_THREAT_CATEGORY_UNKNOWN                    = 44,
  MP_THREAT_CATEGORY_SPP                        = 45,
  MP_THREAT_CATEGORY_BEHAVIOR                   = 46,
  MP_THREAT_CATEGORY_VULNERABILTIY              = 47,
  MP_THREAT_CATEGORY_POLICY                     = 48
} MPTHREAT_CATEGORY, *PMPTHREAT_CATEGORY;
```

## <a name="constants"></a>Constantes

Categoría de amenazas | Descripción
-|-
<span id="MP_THREAT_CATEGORY_INVALID"></span><span id="mp_threat_category_invalid"></span>**MP \_ CATEGORÍA \_ DE AMENAZA NO \_ VÁLIDA** | La categoría de amenazas no existe o se ha escrito incorrectamente.
<span id="MP_THREAT_CATEGORY_ADWARE"></span><span id="mp_threat_category_adware"></span>**MP \_ THREAT \_ CATEGORY \_ ADWARE** | Aplicación potencialmente no deseada que muestra anuncios.
<span id="MP_THREAT_CATEGORY_SPYWARE"></span><span id="mp_threat_category_spyware"></span>**MP \_ SPYWARE DE \_ CATEGORÍA \_ DE AMENAZAS** | Malware que transmite información sobre el dispositivo o el usuario, sin el consentimiento ni el conocimiento del usuario.
<span id="MP_THREAT_CATEGORY_PASSWORDSTEALER"></span><span id="mp_threat_category_passwordstealer"></span>**MP \_ CONTRASEÑAS \_ DE CATEGORÍA DE \_ AMENAZASTEALER** | Una aplicación que recopila o transmite una contraseña a un atacante.
<span id="MP_THREAT_CATEGORY_TROJANDOWNLOADER"></span><span id="mp_threat_category_trojandownloader"></span>**CATEGORÍA \_ DE AMENAZAS DE MP \_ \_ TROJANDOWNLOADER** | Un troyano que descarga malware o aplicaciones potencialmente no deseadas en un dispositivo infectado.
<span id="MP_THREAT_CATEGORY_WORM"></span><span id="mp_threat_category_worm"></span>**MP \_ THREAT \_ CATEGORY \_ WORM** | Software malintencionado auto propagado que puede distribuirse automáticamente a través de conexiones de red.
<span id="MP_THREAT_CATEGORY_BACKDOOR"></span><span id="mp_threat_category_backdoor"></span>**PUERTA TRASERA \_ DE CATEGORÍA DE AMENAZAS DE \_ \_ MP** | Malware que proporciona un medio para omitir los protocolos de autenticación y seguridad normales en un dispositivo.
<span id="MP_THREAT_CATEGORY_REMOTEACCESSTROJAN"></span><span id="mp_threat_category_remoteaccesstrojan"></span>**MP \_ CATEGORÍA \_ DE AMENAZAS \_ REMOTEACCESSTROJAN** | Un troyano que proporciona acceso remoto a un equipo.
<span id="MP_THREAT_CATEGORY_TROJAN"></span><span id="mp_threat_category_trojan"></span>**CATEGORÍA \_ DE AMENAZAS DE MP DE \_ \_ TROJAN** | Software malintencionado que se oculta como software legítimo.
<span id="MP_THREAT_CATEGORY_EMAILFLOODER"></span><span id="mp_threat_category_emailflooder"></span>**MP \_ THREAT \_ CATEGORY \_ EMAILFLOODER** | Malware que envía un gran volumen de correo electrónico a un destino.
<span id="MP_THREAT_CATEGORY_KEYLOGGER"></span><span id="mp_threat_category_keylogger"></span>**MP \_ CATEGORÍA \_ DE \_ AMENAZAS: CATEGORÍA DE AMENAZAS** | Malware que registra las pulsaciones de teclas del usuario, lo que podría robar contraseñas y otros datos confidenciales.
<span id="MP_THREAT_CATEGORY_DIALER"></span><span id="mp_threat_category_dialer"></span>**MP \_ MARCADOR \_ DE CATEGORÍA DE \_ AMENAZAS** | Malware que realiza llamadas telefónicas no autorizadas, a menudo a tarifas premium.
<span id="MP_THREAT_CATEGORY_MONITORINGSOFTWARE"></span><span id="mp_threat_category_monitoringsoftware"></span>**MP \_ SUPERVISIÓN \_ DE CATEGORÍA DE \_ AMENAZASSOFTWARE** | Una aplicación potencialmente no deseada que supervisa la actividad del usuario, como lo que el usuario tipos en el teclado o las vistas de su pantalla.
<span id="MP_THREAT_CATEGORY_BROWSERMODIFIER"></span><span id="mp_threat_category_browsermodifier"></span>**MP \_ CATEGORÍA \_ DE \_ AMENAZAS BROWSERMODIFIER** | Aplicación potencialmente no deseada que cambia la configuración del explorador web sin el consentimiento del usuario.
<span id="MP_THREAT_CATEGORY_COOKIE"></span><span id="mp_threat_category_cookie"></span>**MP \_ COOKIE \_ DE CATEGORÍA DE \_ AMENAZAS** | Datos que un servidor web envía a un explorador, lo que le permite guardar información sobre el usuario, como la configuración de la aplicación web, en visitas repetidas.
<span id="MP_THREAT_CATEGORY_BROWSERPLUGIN"></span><span id="mp_threat_category_browserplugin"></span>**MP \_ CATEGORÍA \_ DE AMENAZAS \_ BROWSERPLUGIN** | Software que permite que un explorador web estándar muestre y ejecute tipos específicos de contenido, como archivos multimedia, imágenes animadas y formularios interactivos.
<span id="MP_THREAT_CATEGORY_AOLEXPLOIT"></span><span id="mp_threat_category_aolexploit"></span>**MP \_ CATEGORÍA \_ DE \_ AMENAZAS AOLEXPLOIT** | Malware que ataque a los usuarios del servicio de Internet AOL, a menudo mediante la recuperación de contraseñas o la modificación de la configuración.
<span id="MP_THREAT_CATEGORY_NUKER"></span><span id="mp_threat_category_nuker"></span>**MP \_ CATEGORÍA \_ DE \_ AMENAZAS NUKER** | Malware diseñado para bloquear un dispositivo o hacer que sea menos estable.
<span id="MP_THREAT_CATEGORY_SECURITYDISABLER"></span><span id="mp_threat_category_securitydisabler"></span>**MP \_ CATEGORÍA \_ DE \_ AMENAZAS SECURITYDISABLER** | Malware que deshabilita la configuración de seguridad o los productos.
<span id="MP_THREAT_CATEGORY_JOKEPROGRAM"></span><span id="mp_threat_category_jokeprogram"></span>**MP \_ THREAT \_ CATEGORY \_ SUSPROGRAMA** | Una aplicación diseñada para entretener o dañar a un usuario, sin dañar realmente el dispositivo.
<span id="MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL"></span><span id="mp_threat_category_hostileactivexcontrol"></span>**MP \_ CATEGORÍA \_ DE \_ AMENAZAS HOSTILEACTIVEXCONTROL** | Control ActiveX diseñado por un atacante para dañar un dispositivo. Un ActiveX control es un tipo de complemento de explorador específico de Internet Explorer.
<span id="MP_THREAT_CATEGORY_SOFTWAREBUNDLER"></span><span id="mp_threat_category_softwarebundler"></span>**MP \_ CATEGORÍA \_ DE \_ AMENAZAS SOFTWAREBUNDLER** | Software que instala otras aplicaciones potencialmente no deseadas, como spyware o spyware. El contrato de licencia del software de unión puede requerir estos otros componentes para funcionar.
<span id="MP_THREAT_CATEGORY_STEALTHNOTIFIER"></span><span id="mp_threat_category_stealthnotifier"></span>**MP \_ THREAT \_ CATEGORY \_ STEALTHNOTIFIER** | Malware que se conecta a un servidor remoto a través de una conexión descontrolada para notificar a un atacante que el malware se ha instalado.
<span id="MP_THREAT_CATEGORY_SETTINGSMODIFIER"></span><span id="mp_threat_category_settingsmodifier"></span>**MP \_ CONFIGURACIÓN \_ DE CATEGORÍA DE \_ AMENAZASMODIFIER** | Una aplicación potencialmente no deseada que cambia la configuración de un usuario sin el conocimiento o consentimiento del usuario.
<span id="MP_THREAT_CATEGORY_TOOLBAR"></span><span id="mp_threat_category_toolbar"></span>**MP \_ BARRA DE \_ HERRAMIENTAS DE CATEGORÍA DE \_ AMENAZAS** | Una aplicación potencialmente no deseada (PUA) que instala una barra de herramientas en el explorador web del usuario; a menudo se agrupan con PUA adicionales, como por ejemplo, pubis.
<span id="MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE"></span><span id="mp_threat_category_remotecontrolsoftware"></span>**MP \_ CATEGORÍA \_ DE AMENAZAS \_ REMOTECONTROLSOFTWARE** | Una aplicación potencialmente no deseada que proporciona acceso remoto a un dispositivo.
<span id="MP_THREAT_CATEGORY_TROJANFTP"></span><span id="mp_threat_category_trojanftp"></span>**MP \_ CATEGORÍA \_ DE AMENAZAS DE \_ TROJANFTP** | Un troyano que usa un servidor FTP para permitir que un atacante cargue o descargue archivos desde un dispositivo.
<span id="MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE"></span><span id="mp_threat_category_potentialunwantedsoftware"></span>**MP \_ THREAT \_ CATEGORY \_ POTENTIALUNWANTEDSOFTWARE** | También se conoce como *aplicación potencialmente no deseada* o *PUA*; software que puede comportarse de una manera muy intrusiva, que es posible que el usuario no haya esperado o haya dado su consentimiento completo.
<span id="MP_THREAT_CATEGORY_ICQEXPLOIT"></span><span id="mp_threat_category_icqexploit"></span>**MP \_ CATEGORÍA \_ DE \_ AMENAZAS ICQEXPLOIT** | Un troyano que ataca el servicio de mensajería ICQ, a menudo mediante la recuperación de contraseñas o la alteración de la configuración.
<span id="MP_THREAT_CATEGORY_TROJANTELNET"></span><span id="mp_threat_category_trojantelnet"></span>**MP \_ CATEGORÍA \_ DE AMENAZAS DE \_ TROJANTELNET** | Un troyano que instala un servidor telnet en el equipo de un usuario sin el conocimiento o consentimiento del usuario.
<span id="MP_THREAT_CATEGORY_EXPLOIT"></span><span id="mp_threat_category_exploit"></span>**MP \_ VULNERABILIDAD DE \_ SEGURIDAD DE CATEGORÍA DE \_ AMENAZAS** | Código malintencionado que aprovecha una vulnerabilidad en un dispositivo o sistema.
<span id="MP_THREAT_CATEGORY_FILESHARINGPROGRAM"></span><span id="mp_threat_category_filesharingprogram"></span>**MP \_ ARCHIVOS \_ DE CATEGORÍA DE \_ AMENAZASHARINGPROGRAM** | Una aplicación potencialmente no deseada que abre un dispositivo para compartir los archivos del dispositivo punto a punto.
<span id="MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL"></span><span id="mp_threat_category_malware_creation_tool"></span>**MP \_ THREAT \_ CATEGORY MALWARE CREATION \_ \_ \_ TOOL** | Una aplicación que puede generar automáticamente archivos malintencionados.
<span id="MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE"></span><span id="mp_threat_category_remote_control_software"></span>**MP \_ SOFTWARE DE \_ CONTROL REMOTO DE CATEGORÍA DE \_ \_ \_ AMENAZAS** | Una aplicación potencialmente no deseada que permite el acceso remoto a un dispositivo.
<span id="MP_THREAT_CATEGORY_TOOL"></span><span id="mp_threat_category_tool"></span>**MP \_ HERRAMIENTA \_ DE CATEGORÍA DE \_ AMENAZAS** | Una utilidad que ayuda a un atacante a realizar acciones malintencionadas en un dispositivo.
<span id="MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE"></span><span id="mp_threat_category_trojan_denialofservice"></span>**MP \_ CATEGORÍA \_ DE AMENAZAS \_ \_ DENIALOFSERVICE DE TROYANO** | Un troyano diseñado para enviar un gran volumen de solicitudes de red a un destino como parte de un ataque por denegación de servicio (DoS).
<span id="MP_THREAT_CATEGORY_TROJAN_DROPPER"></span><span id="mp_threat_category_trojan_dropper"></span>**MP \_ DROPPER \_ DE TROYANO DE CATEGORÍA DE \_ \_ AMENAZAS** | Un troyano que descarga e instala malware o aplicaciones potencialmente no deseadas en un destino.
<span id="MP_THREAT_CATEGORY_TROJAN_MASSMAILER"></span><span id="mp_threat_category_trojan_massmailer"></span>**MP \_ \_ \_ MASSMAILER DE \_ MASSMAILER DE LA** CATEGORÍA DE AMENAZAS | Un troyano que envía un gran volumen de correo electrónico a un destino, diseñado para sobrecargar la bandeja de entrada del destino.
<span id="MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE"></span><span id="mp_threat_category_trojan_monitoringsoftware"></span>**MP \_ THREAT \_ CATEGORY \_ TROJAN \_ MONITORINGSOFTWARE** | Un troyano que supervisa la actividad del usuario, como lo que el usuario tipos en el teclado o las vistas en su pantalla.
<span id="MP_THREAT_CATEGORY_TROJAN_PROXYSERVER"></span><span id="mp_threat_category_trojan_proxyserver"></span>**MP \_ CATEGORÍA DE \_ AMENAZAS \_ PROXY DE \_ TROYANOSERVER** | Un servidor proxy instalado por un troyano, que proporciona lo que parece ser una conexión a Internet ininterrumpida al tiempo que permite el acceso no autorizado al dispositivo infectado.
<span id="MP_THREAT_CATEGORY_VIRUS"></span><span id="mp_threat_category_virus"></span>**MP \_ VIRUS DE \_ CATEGORÍA \_ DE AMENAZAS** | Malware que se replica, normalmente mediante lafisificación de otros archivos en el sistema, lo que permite la ejecución del código de malware y su propagación cuando se activan esos archivos.
<span id="MP_THREAT_CATEGORY_KNOWN"></span><span id="mp_threat_category_known"></span>**MP \_ CATEGORÍA \_ DE AMENAZA \_ CONOCIDA** | Una amenaza de malware no especificada.
<span id="MP_THREAT_CATEGORY_UNKNOWN"></span><span id="mp_threat_category_unknown"></span>**MP \_ CATEGORÍA \_ DE AMENAZA \_ DESCONOCIDA** | Una amenaza de malware no especificada que aún no se ha definido.
<span id="MP_THREAT_CATEGORY_SPP"></span><span id="mp_threat_category_spp"></span>**MP \_ SPP \_ DE CATEGORÍA \_ DE AMENAZAS** | Tecnología antisecuidad que requiere que cada instalación de un Windows producto se active con Microsoft.
<span id="MP_THREAT_CATEGORY_BEHAVIOR"></span><span id="mp_threat_category_behavior"></span>**MP \_ COMPORTAMIENTO DE \_ CATEGORÍA \_ DE AMENAZAS** | Tipo de detección basada en acciones de archivo que a menudo están asociadas a actividades malintencionadas.
<span id="MP_THREAT_CATEGORY_VULNERABILTIY"></span><span id="mp_threat_category_vulnerabiltiy"></span>**MP \_ CATEGORÍA \_ DE \_ AMENAZAS VULNERABILTIY** | Cualquier debilidad, proceso administrativo o actividad que haga que un dispositivo sea susceptible a ser aprovechado por una amenaza.
<span id="MP_THREAT_CATEGORY_POLICY"></span><span id="mp_threat_category_policy"></span>**MP \_ DIRECTIVA \_ DE CATEGORÍA DE \_ AMENAZAS** | Conjunto de reglas definidas por un administrador que controlan las características de dispositivos móviles y de escritorio, como las actualizaciones de software.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Cliente mínimo compatible | Windows 8 (solo aplicaciones de escritorio) |
| Servidor mínimo compatible | Windows Server 2012 (solo aplicaciones de escritorio) |
| Encabezado | MpClient.h |
