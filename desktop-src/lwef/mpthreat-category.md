---
title: Enumeración MPTHREAT_CATEGORY (MpClient. h)
description: Posibles categorías de amenaza.
ms.assetid: 478ED59E-5D3C-43B3-A89D-44A649EDD086
keywords:
- MPTHREAT_CATEGORY enumeración características de entorno heredado de Windows
- PMPTHREAT_CATEGORY el puntero de enumeración características de entorno heredado de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714563"
---
# <a name="mpthreat_category-enumeration"></a>\_Enumeración de categoría MPTHREAT

Posibles categorías de amenaza.

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
<span id="MP_THREAT_CATEGORY_INVALID"></span><span id="mp_threat_category_invalid"></span>**Módulo de administración \_ Categoría de amenaza \_ \_ no válida** | La categoría de amenaza no existe o se ha escrito incorrectamente.
<span id="MP_THREAT_CATEGORY_ADWARE"></span><span id="mp_threat_category_adware"></span>**Módulo de administración \_ \_ \_ adware categoría de amenazas** | Una aplicación potencialmente no deseada que muestra los anuncios.
<span id="MP_THREAT_CATEGORY_SPYWARE"></span><span id="mp_threat_category_spyware"></span>**Módulo de administración \_ \_ \_ spyware de categoría de amenazas** | Malware que transmite información sobre el dispositivo o el usuario, sin el consentimiento o el conocimiento del usuario.
<span id="MP_THREAT_CATEGORY_PASSWORDSTEALER"></span><span id="mp_threat_category_passwordstealer"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ PASSWORDSTEALER** | Aplicación que recopila o transmite una contraseña a un atacante.
<span id="MP_THREAT_CATEGORY_TROJANDOWNLOADER"></span><span id="mp_threat_category_trojandownloader"></span>**Categoría de amenazas de MP \_ \_ \_ TROJANDOWNLOADER** | Un troyano que descarga malware o aplicaciones potencialmente no deseadas en un dispositivo infectado.
<span id="MP_THREAT_CATEGORY_WORM"></span><span id="mp_threat_category_worm"></span>**Módulo de administración \_ \_ \_ gusano de categoría de amenazas** | Software malintencionado de autopropagación que se puede distribuir automáticamente a través de conexiones de red.
<span id="MP_THREAT_CATEGORY_BACKDOOR"></span><span id="mp_threat_category_backdoor"></span>**\_ \_ puerta trasera de categoría de amenazas MP \_** | Malware que proporciona un medio para omitir los protocolos de seguridad y autenticación normales en un dispositivo.
<span id="MP_THREAT_CATEGORY_REMOTEACCESSTROJAN"></span><span id="mp_threat_category_remoteaccesstrojan"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ REMOTEACCESSTROJAN** | Un troyano que proporciona acceso remoto a un equipo.
<span id="MP_THREAT_CATEGORY_TROJAN"></span><span id="mp_threat_category_trojan"></span>**\_troyano de \_ categoría de amenazas MP \_** | Software malintencionado que se camufla como software legítimo.
<span id="MP_THREAT_CATEGORY_EMAILFLOODER"></span><span id="mp_threat_category_emailflooder"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ EMAILFLOODER** | Malware envía un gran volumen de correo electrónico a un destino.
<span id="MP_THREAT_CATEGORY_KEYLOGGER"></span><span id="mp_threat_category_keylogger"></span>**Módulo de administración \_ \_ \_ registradores** de la categoría de amenazas | Malware que registra las pulsaciones de teclas del usuario, pudiendo robar contraseñas y otros datos confidenciales.
<span id="MP_THREAT_CATEGORY_DIALER"></span><span id="mp_threat_category_dialer"></span>**Módulo de administración \_ \_ \_ marca de categoría de amenazas** | Malware que realiza llamadas telefónicas no autorizadas, a menudo a tarifas premium.
<span id="MP_THREAT_CATEGORY_MONITORINGSOFTWARE"></span><span id="mp_threat_category_monitoringsoftware"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ MONITORINGSOFTWARE** | Aplicación potencialmente no deseada que supervisa la actividad de los usuarios, por ejemplo, lo que el usuario escribe en su pantalla.
<span id="MP_THREAT_CATEGORY_BROWSERMODIFIER"></span><span id="mp_threat_category_browsermodifier"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ BROWSERMODIFIER** | Una aplicación potencialmente no deseada que cambia la configuración del explorador Web sin el consentimiento del usuario.
<span id="MP_THREAT_CATEGORY_COOKIE"></span><span id="mp_threat_category_cookie"></span>**Módulo de administración \_ \_ \_ cookie de categoría de amenaza** | Datos que un servidor Web envía a un explorador, lo que le permite guardar información sobre el usuario, como la configuración de la aplicación Web, en visitas repetidas.
<span id="MP_THREAT_CATEGORY_BROWSERPLUGIN"></span><span id="mp_threat_category_browserplugin"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ BROWSERPLUGIN** | Software que permite a un explorador Web estándar Mostrar y ejecutar tipos de contenido específicos, como archivos multimedia, imágenes animadas y formularios interactivos.
<span id="MP_THREAT_CATEGORY_AOLEXPLOIT"></span><span id="mp_threat_category_aolexploit"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ AOLEXPLOIT** | Malware que ataca a los usuarios del servicio de Internet de AOL, a menudo mediante la recuperación de contraseñas o la modificación de la configuración.
<span id="MP_THREAT_CATEGORY_NUKER"></span><span id="mp_threat_category_nuker"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ NUKER** | Malware diseñado para bloquear un dispositivo o hacer que sea menos estable.
<span id="MP_THREAT_CATEGORY_SECURITYDISABLER"></span><span id="mp_threat_category_securitydisabler"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ SECURITYDISABLER** | Malware que deshabilita la configuración de seguridad o los productos.
<span id="MP_THREAT_CATEGORY_JOKEPROGRAM"></span><span id="mp_threat_category_jokeprogram"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ JOKEPROGRAM** | Aplicación diseñada para amuse o SCARE a un usuario, sin dañar realmente el dispositivo.
<span id="MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL"></span><span id="mp_threat_category_hostileactivexcontrol"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ HOSTILEACTIVEXCONTROL** | Control ActiveX diseñado por un atacante para dañar un dispositivo. Un control ActiveX es un tipo de complemento de explorador específico de Internet Explorer.
<span id="MP_THREAT_CATEGORY_SOFTWAREBUNDLER"></span><span id="mp_threat_category_softwarebundler"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ SOFTWAREBUNDLER** | Software que instala otras aplicaciones potencialmente no deseadas, como adware o spyware. El contrato de licencia del software de agrupación puede requerir estos otros componentes para que funcione.
<span id="MP_THREAT_CATEGORY_STEALTHNOTIFIER"></span><span id="mp_threat_category_stealthnotifier"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ STEALTHNOTIFIER** | Malware que se conecta a un servidor remoto a través de una conexión oculta para notificar a un atacante que el malware se ha instalado.
<span id="MP_THREAT_CATEGORY_SETTINGSMODIFIER"></span><span id="mp_threat_category_settingsmodifier"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ SETTINGSMODIFIER** | Una aplicación potencialmente no deseada que cambia la configuración de un usuario sin el conocimiento o consentimiento del usuario.
<span id="MP_THREAT_CATEGORY_TOOLBAR"></span><span id="mp_threat_category_toolbar"></span>**Módulo de administración \_ \_barra de \_ herramientas categoría de amenaza** | Una aplicación potencialmente no deseada (PUA) que instala una barra de herramientas en el explorador Web del usuario. a menudo se incluye PUA adicionales, como adware.
<span id="MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE"></span><span id="mp_threat_category_remotecontrolsoftware"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ REMOTECONTROLSOFTWARE** | Una aplicación potencialmente no deseada que proporciona acceso remoto a un dispositivo.
<span id="MP_THREAT_CATEGORY_TROJANFTP"></span><span id="mp_threat_category_trojanftp"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ TROJANFTP** | Un troyano que usa un servidor FTP para permitir a un atacante cargar o descargar archivos desde un dispositivo.
<span id="MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE"></span><span id="mp_threat_category_potentialunwantedsoftware"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ POTENTIALUNWANTEDSOFTWARE** | También se conoce como *aplicación potencialmente no deseada* o *PUA*; software que puede comportarse de forma excesivamente intrusiva, que es posible que el usuario no haya esperado o que haya dado su consentimiento por completo.
<span id="MP_THREAT_CATEGORY_ICQEXPLOIT"></span><span id="mp_threat_category_icqexploit"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ ICQEXPLOIT** | Un troyano que ataca el servicio de mensajería de ICQ, a menudo mediante la recuperación de contraseñas o la manipulación de la configuración.
<span id="MP_THREAT_CATEGORY_TROJANTELNET"></span><span id="mp_threat_category_trojantelnet"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ TROJANTELNET** | Un troyano que instala un servidor Telnet en el equipo de un usuario sin el conocimiento o consentimiento del usuario.
<span id="MP_THREAT_CATEGORY_EXPLOIT"></span><span id="mp_threat_category_exploit"></span>**Módulo de administración \_ \_ \_ vulnerabilidad** en la categoría de amenazas | Código malintencionado que aprovecha una vulnerabilidad en un dispositivo o sistema.
<span id="MP_THREAT_CATEGORY_FILESHARINGPROGRAM"></span><span id="mp_threat_category_filesharingprogram"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ FILESHARINGPROGRAM** | Una aplicación potencialmente no deseada que abre un dispositivo al uso compartido punto a punto de los archivos del dispositivo.
<span id="MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL"></span><span id="mp_threat_category_malware_creation_tool"></span>**Módulo de administración \_ \_herramienta de \_ \_ creación \_ de malware de categoría de amenazas** | Aplicación que puede generar archivos malintencionados automáticamente.
<span id="MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE"></span><span id="mp_threat_category_remote_control_software"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ \_ \_ software de control remoto** | Una aplicación potencialmente no deseada que permite el acceso remoto a un dispositivo.
<span id="MP_THREAT_CATEGORY_TOOL"></span><span id="mp_threat_category_tool"></span>**Módulo de administración \_ \_ \_ herramienta categoría de amenazas** | Utilidad que ayuda a un atacante a realizar acciones malintencionadas en un dispositivo.
<span id="MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE"></span><span id="mp_threat_category_trojan_denialofservice"></span>**Módulo de administración \_ troyano de categoría de amenaza \_ \_ \_ DENIALOFSERVICE** | Un troyano diseñado para enviar un gran volumen de solicitudes de red a un destino como parte de un ataque por denegación de servicio (DoS).
<span id="MP_THREAT_CATEGORY_TROJAN_DROPPER"></span><span id="mp_threat_category_trojan_dropper"></span>**Módulo de administración \_ \_ \_ \_ instalador troyano** de la categoría de amenazas | Un troyano que descarga e instala malware o aplicaciones potencialmente no deseadas en un destino.
<span id="MP_THREAT_CATEGORY_TROJAN_MASSMAILER"></span><span id="mp_threat_category_trojan_massmailer"></span>**Módulo de administración \_ troyano de categoría de amenaza \_ \_ \_ MASSMAILER** | Un troyano que envía un gran volumen de correo electrónico a un destino, diseñado para saturar la bandeja de entrada del destino.
<span id="MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE"></span><span id="mp_threat_category_trojan_monitoringsoftware"></span>**Módulo de administración \_ troyano de categoría de amenaza \_ \_ \_ MONITORINGSOFTWARE** | Un troyano que supervisa la actividad de los usuarios, por ejemplo, lo que el usuario escribe en su pantalla.
<span id="MP_THREAT_CATEGORY_TROJAN_PROXYSERVER"></span><span id="mp_threat_category_trojan_proxyserver"></span>**Módulo de administración \_ Categoría de amenaza, \_ \_ \_ PROXYSERVER de troyano** | Un servidor proxy instalado por un troyano, que proporciona lo que parece ser una conexión a Internet ininterrumpida, al tiempo que se permite el acceso no autorizado al dispositivo infectado.
<span id="MP_THREAT_CATEGORY_VIRUS"></span><span id="mp_threat_category_virus"></span>**Módulo de administración \_ \_ \_ virus de categoría de amenazas** | Malware que se replica, normalmente mediante la infección de otros archivos del sistema, lo que permite la ejecución del código de malware y su propagación cuando estos archivos se activan.
<span id="MP_THREAT_CATEGORY_KNOWN"></span><span id="mp_threat_category_known"></span>**Módulo de administración \_ Categoría de amenaza \_ \_ conocida** | Una amenaza de malware no especificada.
<span id="MP_THREAT_CATEGORY_UNKNOWN"></span><span id="mp_threat_category_unknown"></span>**Módulo de administración \_ Categoría de amenaza \_ \_ desconocida** | Amenaza de malware no especificada que todavía no se ha definido.
<span id="MP_THREAT_CATEGORY_SPP"></span><span id="mp_threat_category_spp"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ spp** | Tecnología antipiratería que requiere que cada instalación de un producto de Windows se active con Microsoft.
<span id="MP_THREAT_CATEGORY_BEHAVIOR"></span><span id="mp_threat_category_behavior"></span>**Módulo de administración \_ \_ \_ comportamiento** de la categoría de amenazas | Tipo de detección basado en acciones de archivo que suelen estar asociadas a actividades malintencionadas.
<span id="MP_THREAT_CATEGORY_VULNERABILTIY"></span><span id="mp_threat_category_vulnerabiltiy"></span>**Módulo de administración \_ Categoría de amenazas \_ \_ VULNERABILTIY** | Cualquier debilidad, proceso administrativo o actividad que haga que un dispositivo sea susceptible de ser aprovechado por una amenaza.
<span id="MP_THREAT_CATEGORY_POLICY"></span><span id="mp_threat_category_policy"></span>**Módulo de administración \_ \_ \_ Directiva de categoría de amenazas** | Conjunto de reglas definidas por un administrador que controlan las características de los dispositivos móviles y de escritorio, como las actualizaciones de software.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Cliente mínimo compatible | Windows 8 (solo aplicaciones de escritorio) |
| Servidor mínimo compatible | Windows Server 2012 (solo aplicaciones de escritorio) |
| Encabezado | MpClient. h |
