---
description: Lista del contenido de referencia para la API Windows.
ms.assetid: 9CA123F9-92F1-4761-9468-266DA422F70E
title: Índice de API de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e61a3f738905e98ad9cd1db85dbaa1746d7c613b1cc5b628805bcc3ddbea74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737642"
---
# <a name="windows-api-index"></a>Índice de API de Windows

A continuación se muestra una lista del contenido de referencia de la Windows de programación de aplicaciones (API) para aplicaciones de escritorio y servidor.

Con la API Windows, puede desarrollar aplicaciones que se ejecutan correctamente en todas las versiones de Windows a la vez que aprovecha las características y funcionalidades únicas de cada versión. (Tenga en cuenta que anteriormente se denominaba API Win32. El nombre Windows API refleja con más precisión sus raíces en el Windows de 16 bits y su compatibilidad con aplicaciones de 64 Windows).

## <a name="user-interface"></a>Interfaz de usuario

La API Windows interfaz de usuario crea y usa ventanas para mostrar la salida, solicitar la entrada del usuario y llevar a cabo las demás tareas que admiten la interacción con el usuario. La mayoría de las aplicaciones crean al menos una ventana.

-   [Accesibilidad](../winauto/windows-accessibility-features-reference.md)
-   [Administrador de ventanas de escritorio (DWM)](../dwm/reference.md)
-   [Globalization Services](../intl/globalization-services.md)
-   [Valores altos de PPP](../hidpi/high-dpi-reference.md)
-   [Interfaz de usuario multilingüe (MUI)](../intl/multilingual-user-interface-reference.md)
-   [Compatibilidad con idiomas nacionales (NLS)](../intl/national-language-support-reference.md)
-   [Interfaz de usuario elementos](../devnotes/user-interface.md):

    -   [Botones](../controls/bumper-button-button-control-reference.md)
    -   [Carets](../menurc/caret-functions.md)
    -   [Cuadros combinados](../controls/bumper-combobox-combobox-control-reference.md)
    -   [Cuadros de diálogo comunes](../dlgbox/common-dialog-box-reference.md)
    -   [Controles comunes](../controls/individual-control-info.md)
    -   [Cursores](../menurc/cursor-reference.md)
    -   [Cuadros de diálogo](../dlgbox/dialog-box-reference.md)
    -   [Editar controles](../controls/bumper-edit-control-edit-control-reference.md)
    -   [Controles de encabezado](../controls/bumper-header-control-header-control-reference.md)
    -   [Iconos](../menurc/icon-reference.md)
    -   [Aceleradores de teclado](../menurc/keyboard-accelerator-reference.md)
    -   [Cuadros de lista](../controls/bumper-list-box-list-box-control-reference.md)
    -   [Controles list-view](../controls/bumper-list-view-list-view-control-reference.md)
    -   [Menús](../menurc/menu-reference.md)
    -   [Barras de progreso](../controls/bumper-progress-bar-progress-bar-control-reference.md)
    -   [Hojas de propiedades](../controls/bumper-property-sheet-property-sheets-reference.md)
    -   [Controles rich edit](../controls/bumper-rich-edit-rich-edit-control-reference.md)
    -   [Barras de desplazamiento](../controls/bumper-scroll-bar-scroll-bars-reference.md)
    -   [Controles estáticos](../controls/bumper-static-control-static-control-reference.md)
    -   [Cadenas](../menurc/string-reference.md)
    -   [Barras de herramientas](../controls/bumper-toolbar-toolbar-control-reference.md)
    -   [Información sobre herramientas](../controls/bumper-tooltip-tooltip-control-reference.md)
    -   [Barras de seguimiento](../controls/bumper-trackbar-trackbar-control-reference.md)
    -   [Controles de vista de árbol](../controls/bumper-tree-view-tree-view-control-reference.md)

-   [Windows Administrador de animaciones](../uianimation/windows-animation-reference.md)
-   [Windows Marco de la cinta de opciones](../windowsribbon/windowsribbon-reference-entry.md)

## <a name="windows-environment-shell"></a>Windows entorno (Shell)

-   [Windows Sistema de propiedades](../properties/property-system-reference.md)
-   [Windows Cáscara](/previous-versions/windows/desktop/legacy/ff521731(v=vs.85))
-   [Windows Search](../search/-search-reference-entry-page.md)
-   [Consolas](/windows/console/console-reference)

## <a name="user-input-and-messaging"></a>Entrada y mensajería del usuario

-   [Interacción del usuario](../user-interaction.md)
    -   [Manipulación directa](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)
    -   [Entrada de entrada de lápiz](/previous-versions/windows/desktop/input_ink/input-ink-portal)
    -   [Configuración de comentarios de entrada](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
    -   [Contexto de interacción](/previous-versions/windows/desktop/input_intcontext/interaction-context-portal)
    -   [Pila de entrada de dispositivo de puntero](/previous-versions/windows/desktop/input_pointerdevice/pointer-device-stack-portal)
    -   [Mensajes y notificaciones de entrada de puntero](/previous-versions/windows/desktop/inputmsg/messages-and-notifications)
    -   [Entrada del controlador radial](/previous-versions/windows/desktop/input_radial/radialcontroller-portal)
    -   [Text Services Framework (TSF)](../tsf/text-services-framework.md)
    -   [Prueba de impacto táctil](/previous-versions/windows/desktop/input_touchhittest/touch-hit-testing-portal)
    -   [Inserción táctil](/previous-versions/windows/desktop/input_touchinjection/touch-injection-portal)
-   [Interacción del usuario heredado](../legacy-user-interaction-features.md)
    -   [Entrada táctil](../wintouch/windows-touch-portal.md)
    -   [Entrada de teclado](../inputdev/keyboard-input.md)
    -   [Entrada del mouse](../inputdev/mouse-input.md)
    -   [Entrada sin procesar](../inputdev/raw-input.md)
-   [Windows y mensajes](../winmsg/windowing.md):

    -   [Mensajes y colas de mensajes](../winmsg/message-and-message-queue-reference.md)
    -   [Windows](../winmsg/window-reference.md)
    -   [Clases de ventanas](../winmsg/window-class-reference.md)
    -   [Procedimientos de ventana](../winmsg/window-procedure-reference.md)
    -   [Timers](../winmsg/timer-reference.md) (Temporizadores)
    -   [Propiedades de la ventana](../winmsg/window-property-reference.md)
    -   [Enlaces](../winmsg/hook-reference.md)

## <a name="data-access-and-storage"></a>Acceso a datos y almacenamiento

-   [Servicio de transferencia inteligente en segundo plano (BITS)](../bits/bits-reference.md)
-   [Copia de seguridad de datos](../backup/backup.md)
    -   [Backup](../backup/backup-reference.md)
    -   [Desduplicación de datos](/previous-versions/windows/desktop/dedup/data-deduplication-api-reference)
    -   [Instantánea de volumen](../vss/volume-shadow-copy-reference.md)
    -   [Copias de seguridad de Windows Server](/previous-versions/windows/desktop/wsb/windows-server-backup-api-interfaces)
-   [Data Exchange](../dataxchg/data-exchange.md):

    -   [Portapapeles](../dataxchg/clipboard-reference.md)
    -   [datos dinámicos Exchange (DDE)](../dataxchg/dynamic-data-exchange-reference.md)
    -   [datos dinámicos Exchange Management (DDEML)](../dataxchg/dynamic-data-exchange-management-library-reference.md)

-   [Administración de directorios](../fileio/directory-management-reference.md)
-   [Administración de discos](../fileio/disk-management-reference.md)
-   [Sistema de archivos distribuido (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system-reference)
-   [Replicación del sistema de archivos distribuido](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes)
-   [Motor de Storage extensible](../extensible-storage-engine/extensible-storage-engine-reference.md)
-   [Archivos y E/S (sistema de archivos local)](../fileio/file-management-reference.md)
-   [API de la biblioteca de detección de iSCSI](/previous-versions/windows/desktop/iscsidisc/iscsi-discovery-library-reference)
-   [Archivos sin conexión](/previous-versions/windows/desktop/offlinefiles/offline-files-reference)
-   [Packaging](/previous-versions/windows/desktop/opc/packaging-programming-reference)
-   [Compresión diferencial remota](/previous-versions/windows/desktop/rdc/remote-differential-compression-reference)
-   [NTFS de transacciones](../fileio/transactional-ntfs-reference.md)
-   [Administración del volumen](../fileio/volume-management-reference.md)
-   [Disco duro virtual (VHD)](/previous-versions/windows/desktop/legacy/dd323700(v=vs.85))
-   [Administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [Windows Data Access Components](/previous-versions/windows/desktop/legacy/aa968814(v=vs.85)) (Componentes de Windows Data Access)
    -   [Microsoft Open Database Connectivity (ODBC)](/sql/odbc/reference/syntax/odbc-reference)
    -   [Microsoft OLE DB](/previous-versions/windows/desktop/ms718050(v=vs.85))
    -   [Microsoft ActiveX Data Objects (ADO)](/sql/ado/reference/ado-programmer-s-reference)

## <a name="diagnostics"></a>Diagnóstico

La [API de diagnóstico le](/previous-versions//bb648685(v=vs.85)) permite solucionar problemas de aplicaciones o sistemas y supervisar el rendimiento.

-   [Recuperación y reinicio de aplicaciones](../recovery/application-recovery-and-restart-reference.md)
-   [Depuración](../debug/debugging-reference.md)
-   [Tratamiento de errores](../debug/error-handling-reference.md)
-   [Registro de eventos](../eventlog/event-logging-reference.md)
-   [Seguimiento de eventos](../etw/event-tracing-reference.md)
-   [Generación de perfiles de contadores de hardware (HCP)](/previous-versions/windows/desktop/hcp/hcp-reference)
-   [Marco de diagnóstico de redes (NDF)](../ndf/ndf-reference.md)
-   [Monitor de red](../netmon2/reference.md)
-   [Contadores de rendimiento](../perfctrs/performance-counters-reference.md)
-   [Registros y alertas de rendimiento (PLA)](/previous-versions/windows/desktop/pla/performance-logs-and-alerts-reference)
-   [Creación de instantáneas de procesos](/previous-versions/windows/desktop/proc_snap/process-snapshotting-reference)
-   [Estado del proceso (PSAPI)](../psapi/psapi-reference.md)
-   [Control estructurado de excepciones](../debug/structured-exception-handling-reference.md)
-   [Monitor de sistema](../sysmon/system-monitor-reference.md)
-   [Recorrido de cadena de espera](../debug/wait-chain-traversal.md)
-   [Informe de errores de Windows (WER)](../wer/wer-reference.md)
-   [Registro de sucesos de Windows](../wes/windows-event-log-reference.md)
-   [Plataforma de solución de problemas de Windows](/previous-versions/windows/desktop/wintt/windows-troubleshooting-reference)

## <a name="graphics-and-multimedia"></a>Gráficos y multimedia

Las [API de gráficos, multimedia,](/previous-versions//aa969176(v=vs.85)) [audio](../audio-and-video.md) y vídeo permiten a las aplicaciones incorporar texto, gráficos, audio y vídeo con formato.

-   [Core Audio](../coreaudio/programming-reference.md)
-   [Direct2D](../direct2d/reference.md)
-   [DirectComposition](../directcomp/reference.md)
-   [DirectShow](../directshow/directshow-reference.md)
-   [DirectWrite](../directwrite/reference.md)
-   [DirectX](../directx-sdk--august-2009-.md)
-   [Interfaz de dispositivo gráfico (GDI)](../gdi/windows-gdi.md)
-   [GDI+](../gdiplus/-gdiplus-class-gdi-reference.md)
-   [Streaming multimedia](../mediastreaming/media-streaming-api-portal.md)
-   [Microsoft Media Foundation](../medfound/media-foundation-programming-reference.md)
-   [Tecnologías de televisión de Microsoft](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-application-interface)
-   [Opengl](../opengl/opengl-reference.md)
-   [Supervisión de la configuración](../monitor/monitor-configuration-reference.md)
-   [Varios monitores de pantalla](../gdi/multiple-display-monitors-reference.md)
-   [Adquisición de imágenes](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [Sistema de colores de Windows](../wcs/reference.md)
-   [Windows Imaging Component (WIC)](../wic/-wic-codec-reference.md)
-   [Windows Códec de audio y vídeo multimedia y DSP](/previous-versions//dd443208(v=vs.85))
-   [Windows Media Center](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [Formato de Windows Media](../wmformat/programming-reference.md)
-   [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal)
-   [Reproductor de Windows Media](../wmp/windows-media-player-object-model-reference.md)
-   [Servicios de Windows Media](/previous-versions/windows/desktop/dd893580(v=vs.85))
-   [Windows Movie Maker  ](/previous-versions/windows/desktop/wmmdvdm/windows-movie-maker-apis)
-   [Windows Multimedia](../multimedia/multimedia-reference.md)

## <a name="devices"></a>Dispositivos

-   [AllJoyn](/previous-versions/windows/desktop/alljoyn/alljoyn-api-portal)
-   [Recursos de comunicaciones](../devio/communications-reference.md)
-   [Acceso a dispositivos](/previous-versions/windows/desktop/deviceaccess/device-access-api-c---programming-reference)
-   [Administración de dispositivos](../devio/device-management-reference.md)
-   [Almacenamiento mejorado](/previous-versions/windows/desktop/enstor/enhanced-storage-reference)
-   [Detección de funciones](/previous-versions/windows/desktop/fundisc/function-discovery-reference)
-   [Control de imágenes](../imapi/imapi-reference.md)
-   [Ubicación](../locationapi/windows-location-programming-reference.md)
-   [Base de datos de asociación PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x-association-database-reference)
-   [Impresión](/windows-hardware/drivers/print/introduction-to-printing)
    -   [Administrador de trabajos de impresión](../printdocs/printing-and-print-spooler-reference.md)
    -   [Imprimir paquete de documento](../printdocs/tailored-app-printing-api.md)
    -   [Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
    -   [Imprimir vale](../printdocs/print-ticket-api.md)
    -   [XPS Print](../printdocs/xpsprint-api.md)
-   [Sensores](../sensorsapi/sensor-api-programming-reference.md)
-   [Servicio de notificación de eventos del sistema (SENS)](../sens/sens-reference.md)
-   [Ayuda de la herramienta](../toolhelp/tool-help-reference.md)
-   [UPnP](../upnp/universal-plug-and-play-start-page.md)
-   [Servicios web en dispositivos](../wsdapi/web-services-for-devices-reference.md)
-   [Adquisición de imágenes de Windows (WIA)](../wia/-wia-reference.md)
-   [Windows Archivos Administrador de dispositivos](../wmdm/programming-reference.md)
-   [Windows Dispositivos portátiles](../wpd_sdk/programming-reference.md)

## <a name="system-services"></a>Servicios del sistema

Las [API de Servicios](/previous-versions//aa969179(v=vs.85)) del sistema ofrecen a las aplicaciones acceso a los recursos del equipo y a las características del sistema operativo subyacente, como memoria, sistemas de archivos, dispositivos, procesos y subprocesos.

-   [COM](../com/reference.md)
-   [Com +](../cossdk/com--reference.md)
-   [API de compresión](../cmpapi/-compression-portal.md)
-   [Coordinador de transacciones distribuidas (DTC)](/previous-versions/windows/desktop/ms686108(v=vs.85))
-   [Bibliotecas de vínculos dinámicos (DLL)](../dlls/dynamic-link-library-functions.md)
-   [API de ayuda](/previous-versions/windows/desktop/helpapi/help-api-reference)
-   [Comunicaciones entre procesos:](../ipc/interprocess-communications.md)
    -   [Mailslots](../ipc/mailslot-functions.md)
    -   [Pipes](../ipc/pipe-functions.md) (Operaciones de canalización de .NET Framework)
-   [Administrador de transacciones de kernel (KTM)](../ktm/ktm-reference.md)
-   [Administración de memoria](../memory/memory-management-reference.md)
-   [Grabadora de operaciones](/previous-versions/windows/desktop/oprec/-operation-portal)
-   [Administración de energía](../power/power-management-reference.md)
-   [Servicios de Escritorio remoto](../termserv/terminal-services-reference.md)
-   [Procesos](../procthread/process-and-thread-reference.md)
-   [Servicios](../services/service-reference.md)
-   [Sincronización](../sync/synchronization-reference.md)
-   [Subprocesos](../procthread/process-and-thread-reference.md)
-   [Windows Uso compartido de escritorio](/previous-versions/windows/desktop/rdp/windows-desktop-sharing-reference)
-   [Windows Información del sistema](../sysinfo/windows-system-information.md)
    -   [Identificador y objetos](../sysinfo/handle-and-object-functions.md)
    -   [Registro](../sysinfo/registry-reference.md)
    -   [Time](../sysinfo/time-reference.md)
    -   [Proveedor de hora](../sysinfo/time-provider-reference.md)

## <a name="security-and-identity"></a>Seguridad e identidad

Las [API de seguridad e](../devnotes/security.md) identidad habilitan la autenticación de contraseñas durante el inicio de sesión, la protección discrecional para todos los objetos del sistema compartibles, el control de acceso con privilegios, la administración de derechos y la auditoría de seguridad.

-   [Autenticación](../secauthn/authentication-reference.md)
-   [Autorización](../secauthz/authorization-reference.md)
-   [Inscripción de certificados](../seccertenroll/certificate-enrollment-api-reference.md)
-   [Criptografía](../seccrypto/cryptography-reference.md)
-   [Cryptographic Next Generation (CNG)](../seccng/cng-reference.md)
-   [Servicios de directorio](/previous-versions//ms682458(v=vs.85))
    -   [Active Directory Domain Services](../ad/active-directory-domain-services-reference.md)
    -   [Active Directory interfaces de servicio (ADSI)](../adsi/adsi-reference.md)
-   [Protocolo de autenticación extensible (EAP)](../eap/extensible-authentication-protocol-reference.md)
-   [Host del protocolo de autenticación extensible (EAPHost)](../eaphost/about-eap-host.md)
-   [Administración de contraseñas de MS-CHAP](/previous-versions/windows/desktop/mschap/ms-chap-password-management-reference)
-   [Protección de acceso a redes (NAP)](../nap/nap-reference.md)
-   [Extensiones del servidor de directivas de red (NPS)](../nps/ias-internet-authentication-service-reference.md)
-   [Controles parentales](../parcon/parental-controls-reference.md)
-   [Proveedores WMI de seguridad](../secprov/security-wmi-providers-reference.md)
-   [Servicios de base TPM (TBS)](../tbs/tbs-reference.md)
-   [Marco biométrico de Windows](../secbiomet/biometric-service-api-reference.md)

## <a name="application-installation-and-servicing"></a>Instalación y mantenimiento de aplicaciones

-   [Explorador de juegos](/previous-versions/windows/desktop/legacy/ee415251(v=vs.85))
-   [Ensamblados en paralelo](../sbscs/side-by-side-assemblies-reference.md)
-   [API de empaquetado, implementación y consulta](../appxpkg/api-reference.md
)
-   [Licencia de desarrollador](../devlic/developer-license-apis.md)
-   [Administrador de reinicio](../rstmgr/restart-manager-reference.md)
-   [Windows Installer](../msi/windows-installer-portal.md)

## <a name="system-admin-and-management"></a>Administración y administración del sistema

Las [interfaces de](../srvnodes/system-administration.md) administración del sistema permiten instalar, configurar y dar servicio a aplicaciones o sistemas.

-   [datos de la configuración de arranque (BCD) WMI](/previous-versions/windows/desktop/bcd/bcd-reference)
-   [Clústeres de conmutación por error](/previous-versions/windows/desktop/mscs/failover-cluster-apis-portal)
-   [Administrador de recursos del servidor de archivos (FSRM)](/previous-versions/windows/desktop/fsrm/fsrm-reference)
-   [Directiva de grupo](/previous-versions/windows/desktop/Policy/group-policy-reference)
-   [Microsoft Management Console (MMC) 2.0](/previous-versions/windows/desktop/mmc/mmc-reference)
-   [NetShell](/previous-versions/windows/desktop/netshell/netshell-reference)
-   [Configuración Infraestructura de administración](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [Registro de inventario de software](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
-   [Licencias de software](/previous-versions/windows/desktop/secslapi/software-licensing-api-reference)
-   [Administrador de reinicio](../rstmgr/restart-manager-portal.md)
-   [Configuración Infraestructura de administración](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [Restaurar sistema](../sr/system-restore-portal.md)
-   [Cierre del sistema](../shutdown/system-shutdown.md)
-   [Programador de tareas](../taskschd/task-scheduler-start-page.md)
-   [Registro de acceso de usuarios](/previous-versions/windows/desktop/ual/user-access-logging-reference)
-   [Windows Virtual PC](../vpc/virtual-pc-reference.md)
-   [Microsoft Virtual Server](/previous-versions/windows/desktop/msvs/microsoft-virtual-server-reference)
-   [Proveedor de equilibrio de carga de red](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-reference)
-   [Windows Defender WMI v2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
-   [Windows Servicios de implementación](../wds/windows-deployment-services-portal.md)
-   [Windows Genuine Advantage](/previous-versions/windows/desktop/wingen/windows-genuine-advantage-api-functions)
-   [Windows Infraestructura de administración](/previous-versions/windows/desktop/wmi_v2/wmi-reference)
-   [Instrumental de administración de Windows (WMI)](../wmisdk/wmi-reference.md)
-   [Administración remota de Windows](../winrm/portal.md)
-   [Windows Protección de recursos](../wfp/windows-resource-protection-portal.md)
-   [Windows Server Update Services](/previous-versions/windows/desktop/ms744624(v=vs.85))
-   [Windows Herramienta de evaluación del sistema](../winsat/winsat-reference.md)
-   [Agente de Windows Update](../wua_sdk/portal-client.md)

## <a name="networking-and-internet"></a>Redes e Internet

Las [API de](../devnotes/networking.md) red permiten la comunicación entre aplicaciones a través de una red. También puede crear y administrar el acceso a recursos compartidos, como directorios e impresoras de red.

-   [Sistema de nombres de dominio (DNS)](../dns/dns-reference.md)
-   [Protocolo de configuración dinámica de host (DHCP)](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
-   [Servicio de fax](/previous-versions/windows/desktop/fax/-mfax-fax-service-reference)
-   [Get Connected Wizard](/previous-versions/windows/desktop/get_connected/get-connected-wizard-api-reference)
-   [Servidor HTTP](../http/http-server-api-reference.md)
-   [Uso compartido de conexión a Internet y firewall](/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference)
-   [Asistente IP](../iphlp/ip-helper-function-reference.md)
-   [Firewall de conexión a Internet IPv6](/previous-versions/windows/desktop/ics/ipv6-firewall-configuration-reference)
-   [Base de información de administración](/previous-versions/windows/desktop/mib/management-information-base-reference)
-   [Cola de mensajes (MSMQ)](/previous-versions/windows/desktop/legacy/ms700112(v=vs.85))
-   [Protocolo de asignación dinámica de cliente de dirección de multidifusión (MADCAP)](/previous-versions/windows/desktop/madcap/madcap-reference)
-   [Traducción de direcciones de red (NAT)](/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference)
-   [Administrador de listas de redes (NLM)](../nla/network-list-manager-api-reference.md)
-   [Administración de red](../netmgmt/network-management-reference.md)
-   [Administración de recursos compartidos de red](../netshare/network-share-management-reference.md)
-   [Punto a punto](../p2psdk/portal.md)
-   [Calidad de servicio (QOS)](/previous-versions/windows/desktop/qos/qos-reference)
-   [Llamada a procedimiento remoto](../rpc/reference.md)
-   [Servicio de enrutamiento y acceso remoto (RAS)](../rras/portal.md)
-   [Protocolo simple de administración de redes (SNMP)](../snmp/snmp-reference.md):
-   [Administración de SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)
-   [Interfaces de programación de aplicaciones de telefonía (TAPI)](../tapi/telephony-application-programming-interfaces.md)
-   [WebDAV](../webdav/webdav-api-reference.md)
-   [Componente de protocolo WebSocket](../websock/web-socket-protocol-component-api-portal.md)
-   Redes inalámbricas:
    -   [Bluetooth](../bluetooth/bluetooth-reference.md)
    -   [Irda](/previous-versions/windows/desktop/irda/irda-and-windows-sockets-reference)
    -   [Banda ancha móvil](../mbn/mobile-broadband-networks-api-reference.md)
    -   [Wi-Fi nativo](../nativewifi/native-wifi-reference.md)
    -   [Windows Connect Now](../wcn/windows-connect-now-reference.md)
    -   [Administrador de conexiones de Windows](../wcm/windows-connection-manager-reference.md)
-   [Plataforma de filtrado de Windows](../fwp/fwp-reference.md)
-   [Firewall de Windows con seguridad avanzada](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference)
-   [Windows Servicios HTTP (WinHTTP)](../winhttp/winhttp-reference.md)
-   [Windows Internet (WinINet)](../wininet/wininet-reference.md)
-   [Windows Redes (WNet)](../wnet/windows-networking-reference.md)
-   [Windows Virtualización de red](/previous-versions/windows/desktop/wnv/windows-network-virtualization-portal)
-   [Windows Plataforma RSS](/previous-versions/windows/desktop/ms684702(v=vs.85))
-   [Windows Sockets (Winsock)](../winsock/winsock-reference.md)
-   [Windows Servicios web](../wsw/windows-web-services-reference.md)
-   [Solicitud extendida HTTP XML](/previous-versions/windows/desktop/ixhr2/ixmlhttprequest2-portal)

## <a name="deprecated-or-legacy-apis"></a>API en desuso o heredadas

Las siguientes son tecnologías y API que están obsoletas o que se han reemplazado o que han quedado en desuso de los Windows operativos de cliente y servidor.

-   [Directmusic](/previous-versions/ms807133(v=msdn.10))
-   [DirectSound](/previous-versions/windows/desktop/ee416975(v=vs.85))
-   [El SDK udDI de Microsoft](/previous-versions/windows/desktop/aa966237(v=bts.10)) ahora se incluye [con Microsoft BizTalk Server](/previous-versions/bb905520(v=msdn.10)).
-   [Red datos dinámicos Exchange (DDE)](../ipc/network-dde-reference.md)
-   [Servicio de instalación remota:](/previous-versions/windows/it-pro/windows-server-2003/cc786442(v=ws.10))use [Windows Deployment Services en](../wds/windows-deployment-services-portal.md) su lugar.
-   [Servicio de disco virtual (VDS):](../vds/vds-reference.md)use [Windows Storage en su](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal) lugar.
-   Terminal Services: use [Servicios de Escritorio remoto](../termserv/terminal-services-reference.md).
-   [Windows Media Rights Manager](/previous-versions//bb614742(v=vs.85))
-   [Windows Messaging (MAPI):](/previous-versions/windows/desktop/windowsmapi/mapi-stub-library-and-simple-mapi)use [Office EN SU LUGAR.](/previous-versions/office/developer/office-2007/cc765775(v=office.12))
-   [Windows Platform de Platform:](/previous-versions/windows/desktop/gadgetplatform/windows-gadget-platform-portal)en su lugar, cree aplicaciones para UWP.
-   [Windows barra lateral:](/previous-versions/windows/desktop/sidebar/-sidebar-ref-entry)cree aplicaciones para UWP en su lugar.
-   [Windows SideShow:](/previous-versions//ms744179(v=vs.85))Sin reemplazo.
-   [Efectos de imagen de WPF](/previous-versions/windows/desktop/wibe/-wibe-about-bitmapeffects)
