---
description: Las funciones ExitWindowsEx e InitiateSystemShutdownEx usan los códigos de motivo de apagado en el parámetro dwReason. El sistema procesará un máximo de códigos de motivo \_ MAX NUM \_ REASONS. MAX \_ NUM REASONS se define en \_ reason.h.
ms.assetid: db1ecee0-40eb-4761-b5d8-9cc3c1c98cdf
title: Códigos de motivo de apagado del sistema (Reason.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef40cf53afd3abaf261e15f2caba735dea7963ee5b5f19cebc78c63a373962fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073205"
---
# <a name="system-shutdown-reason-codes"></a>Códigos de motivo de apagado del sistema

Las funciones [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) e [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) usan los códigos de motivo de apagado en el *parámetro dwReason.*

El sistema procesará un máximo de códigos de motivo \_ MAX NUM \_ REASONS. MAX \_ NUM REASONS se define en \_ reason.h.

A continuación se muestra la razón principal de las marcas. Indican el tipo de problema general.



| Constante o valor                                                                                                                                                                                                                                                                                 | Descripción                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_MAJOR_APPLICATION"></span><span id="shtdn_reason_major_application"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DE LA \_ APLICACIÓN**</dt> <dt>PRINCIPAL 0x00040000</dt> </dl>             | Problema de la aplicación.<br/>                                                                                                                                      |
| <span id="SHTDN_REASON_MAJOR_HARDWARE"></span><span id="shtdn_reason_major_hardware"></span><dl> <dt>**SHTDN \_ MOTIVO \_ PRINCIPAL \_ DEL HARDWARE**</dt> <dt>0x00010000</dt> </dl>                      | Problema de hardware.<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_LEGACY_API"></span><span id="shtdn_reason_major_legacy_api"></span><dl> <dt>**SHTDN \_ MOTIVO \_ PRINCIPAL DE LA API \_ \_ HEREDADA**</dt> <dt>0x00070000</dt> </dl>               | Se [**usó la función InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) en lugar de [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa).<br/> |
| <span id="SHTDN_REASON_MAJOR_OPERATINGSYSTEM"></span><span id="shtdn_reason_major_operatingsystem"></span><dl> <dt>**SHTDN \_ MOTIVO \_ PRINCIPAL \_ DEL SISTEMA**</dt> OPERATIVO <dt>0x00020000</dt> </dl> | Problema del sistema operativo.<br/>                                                                                                                                 |
| <span id="SHTDN_REASON_MAJOR_OTHER"></span><span id="shtdn_reason_major_other"></span><dl> <dt>**SHTDN \_ REASON \_ MAJOR \_ OTHER**</dt> <dt>0x00000000</dt> </dl>                               | Otro problema.<br/>                                                                                                                                            |
| <span id="SHTDN_REASON_MAJOR_POWER"></span><span id="shtdn_reason_major_power"></span><dl> <dt>**SHTDN \_ MOTIVO \_ PRINCIPAL \_ DE POWER**</dt> <dt>0X00060000</dt> </dl>                               | Error de alimentación.<br/>                                                                                                                                          |
| <span id="SHTDN_REASON_MAJOR_SOFTWARE"></span><span id="shtdn_reason_major_software"></span><dl> <dt>**SHTDN \_ MOTIVO \_ PRINCIPAL \_ DEL SOFTWARE**</dt> <dt>0x00030000</dt> </dl>                      | Problema de software.<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_SYSTEM"></span><span id="shtdn_reason_major_system"></span><dl> <dt>**SHTDN \_ REASON \_ MAJOR \_ SYSTEM**</dt> <dt>0x00050000</dt> </dl>                            | Error del sistema.<br/>                                                                                                                                         |



A continuación se muestra la razón secundaria de las marcas. Modifican la marca de motivo principal especificada. Puede usar cualquier razón secundaria junto con cualquier razón principal, pero algunas combinaciones no tienen sentido.



| Constante o valor                                                                                                                                                                                                                                                                                                    | Descripción                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------|
| <span id="SHTDN_REASON_MINOR_BLUESCREEN"></span><span id="shtdn_reason_minor_bluescreen"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ BLUESCREEN**</dt> <dt>0x0000000F</dt> </dl>                                   | Evento de bloqueo de pantalla azul.<br/>       |
| <span id="SHTDN_REASON_MINOR_CORDUNPLUGGED"></span><span id="shtdn_reason_minor_cordunplugged"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ CORDUNPLUGGED**</dt> <dt>0x0000000b</dt> </dl>                          | Desenchufado.<br/>                     |
| <span id="SHTDN_REASON_MINOR_DISK"></span><span id="shtdn_reason_minor_disk"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ DISK**</dt> <dt>0x00000007</dt> </dl>                                                     | disco.<br/>                          |
| <span id="SHTDN_REASON_MINOR_ENVIRONMENT"></span><span id="shtdn_reason_minor_environment"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ ENVIRONMENT**</dt> <dt>0x0000000c</dt> </dl>                                | Entorno.<br/>                   |
| <span id="SHTDN_REASON_MINOR_HARDWARE_DRIVER"></span><span id="shtdn_reason_minor_hardware_driver"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR HARDWARE DRIVER \_ \_ 0x0000000d**</dt> <dt></dt> </dl>                   | Conductor.<br/>                        |
| <span id="SHTDN_REASON_MINOR_HOTFIX"></span><span id="shtdn_reason_minor_hotfix"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DE \_ REVISIÓN SECUNDARIA**</dt> <dt>0x00000011</dt> </dl>                                               | Corrección rápida.<br/>                       |
| <span id="SHTDN_REASON_MINOR_HOTFIX_UNINSTALL"></span><span id="shtdn_reason_minor_hotfix_uninstall"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DE LA \_ \_ DESINSTALACIÓN DE REVISIONES**</dt> <dt>SECUNDARIAS 0x00000017</dt> </dl>                | Desinstalación de corrección rápida.<br/>        |
| <span id="SHTDN_REASON_MINOR_HUNG"></span><span id="shtdn_reason_minor_hung"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ HUNG**</dt> <dt>0x00000005</dt> </dl>                                                     | Insensible.<br/>                  |
| <span id="SHTDN_REASON_MINOR_INSTALLATION"></span><span id="shtdn_reason_minor_installation"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DE \_ INSTALACIÓN SECUNDARIA**</dt> <dt>0x00000002</dt> </dl>                             | Instalación.<br/>                  |
| <span id="SHTDN_REASON_MINOR_MAINTENANCE"></span><span id="shtdn_reason_minor_maintenance"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DE MANTENIMIENTO \_ MENOR**</dt> <dt>0x00000001</dt> </dl>                                | Mantenimiento.<br/>                   |
| <span id="SHTDN_REASON_MINOR_MMC"></span><span id="shtdn_reason_minor_mmc"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ MMC**</dt> <dt>0x00000019</dt> </dl>                                                        | Problema de MMC.<br/>                     |
| <span id="SHTDN_REASON_MINOR_NETWORK_CONNECTIVITY"></span><span id="shtdn_reason_minor_network_connectivity"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DE LA CONECTIVIDAD \_ \_ DE**</dt> <dt>RED SECUNDARIA 0x00000014</dt> </dl>    | Conectividad de red.<br/>          |
| <span id="SHTDN_REASON_MINOR_NETWORKCARD"></span><span id="shtdn_reason_minor_networkcard"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ NETWORKCARD**</dt> <dt>0x00000009</dt> </dl>                                | Tarjeta de red.<br/>                  |
| <span id="SHTDN_REASON_MINOR_OTHER"></span><span id="shtdn_reason_minor_other"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ OTHER**</dt> <dt>0x00000000</dt> </dl>                                                  | Otro problema.<br/>                   |
| <span id="SHTDN_REASON_MINOR_OTHERDRIVER"></span><span id="shtdn_reason_minor_otherdriver"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ OTHERDRIVER**</dt> <dt>0x0000000e</dt> </dl>                                | Otro evento de controlador.<br/>            |
| <span id="SHTDN_REASON_MINOR_POWER_SUPPLY"></span><span id="shtdn_reason_minor_power_supply"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ POWER \_ SUPPLY**</dt> <dt>0x0000000a</dt> </dl>                            | Fuente de alimentación.<br/>                  |
| <span id="SHTDN_REASON_MINOR_PROCESSOR"></span><span id="shtdn_reason_minor_processor"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ PROCESSOR**</dt> <dt>0x00000008</dt> </dl>                                      | Procesador.<br/>                     |
| <span id="SHTDN_REASON_MINOR_RECONFIG"></span><span id="shtdn_reason_minor_reconfig"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ RECONFIG**</dt> <dt>0x00000004</dt> </dl>                                         | Reconfigurar.<br/>                   |
| <span id="SHTDN_REASON_MINOR_SECURITY"></span><span id="shtdn_reason_minor_security"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ SECURITY**</dt> <dt>0x00000013</dt> </dl>                                         | Problema de seguridad.<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX"></span><span id="shtdn_reason_minor_securityfix"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ SECURITYFIX**</dt> <dt>0x00000012</dt> </dl>                                | Revisión de seguridad.<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX_UNINSTALL"></span><span id="shtdn_reason_minor_securityfix_uninstall"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ SECURITYFIX \_ UNINSTALL**</dt> <dt>0x00000018</dt> </dl> | Desinstalación de revisiones de seguridad.<br/> |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK"></span><span id="shtdn_reason_minor_servicepack"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ SERVICEPACK**</dt> <dt>0x00000010</dt> </dl>                                | Service Pack.<br/>                  |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK_UNINSTALL"></span><span id="shtdn_reason_minor_servicepack_uninstall"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DE \_ LA DESINSTALACIÓN DE SERVICEPACK \_**</dt> <dt>0X00000016</dt> </dl> | Desinstalación de Service Pack.<br/>   |
| <span id="SHTDN_REASON_MINOR_TERMSRV"></span><span id="shtdn_reason_minor_termsrv"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ TERMSRV**</dt> <dt>0x00000020</dt> </dl>                                            | Terminal Services.<br/>             |
| <span id="SHTDN_REASON_MINOR_UNSTABLE"></span><span id="shtdn_reason_minor_unstable"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ UNSTABLE**</dt> <dt>0x00000006</dt> </dl>                                         | Inestable.<br/>                      |
| <span id="SHTDN_REASON_MINOR_UPGRADE"></span><span id="shtdn_reason_minor_upgrade"></span><dl> <dt>**SHTDN \_ MOTIVO \_ DE \_ LA ACTUALIZACIÓN**</dt> SECUNDARIA <dt>0x00000003</dt> </dl>                                            | Actualización.<br/>                       |
| <span id="SHTDN_REASON_MINOR_WMI"></span><span id="shtdn_reason_minor_wmi"></span><dl> <dt>**SHTDN \_ REASON \_ MINOR \_ WMI**</dt> <dt>0x00000015</dt> </dl>                                                        | Problema de WMI.<br/>                     |



Las siguientes marcas opcionales proporcionan información adicional sobre el evento.



| Constante o valor                                                                                                                                                                                                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_FLAG_USER_DEFINED"></span><span id="shtdn_reason_flag_user_defined"></span><dl> <dt>**SHTDN \_ REASON \_ FLAG \_ USER \_ DEFINED**</dt> <dt>0x40000000</dt> </dl> | El usuario define el código de motivo. Para obtener más información, vea Definir un código de motivo personalizado. <br/> Si esta marca no está presente, el sistema define el código de motivo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SHTDN_REASON_FLAG_PLANNED"></span><span id="shtdn_reason_flag_planned"></span><dl> <dt>**SHTDN \_ REASON \_ FLAG \_ PLANNED**</dt> <dt>0x80000000</dt> </dl>                 | El cierre estaba planeado. El sistema genera un archivo de datos de estado del sistema (SSD). Este archivo contiene información de estado del sistema, como los procesos, subprocesos, uso de memoria y configuración. <br/> Si esta marca no está presente, el cierre no estaba planeado. Las opciones de notificación e informes se controlan mediante un conjunto de directivas. Por ejemplo, después de iniciar sesión, el sistema muestra un cuadro de diálogo que informa del apagado no planeado si se ha habilitado la directiva. Solo se crea un archivo SSD si la directiva ssd está habilitada en el sistema. El administrador puede usar [Informe de errores de Windows](../wer/windows-error-reporting.md) para enviar los datos ssd a una ubicación central o a Microsoft.<br/> |



## <a name="remarks"></a>Comentarios

El sistema reconoce las siguientes combinaciones. La tabla indica la cadena que se muestra en el Seguimiento de eventos de apagado y proporciona una descripción más detallada. La cadena predeterminada es "No se encontró ningún título por este motivo".



| Combinación                                                                                                | Descripción                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SHTDN \_ MOTIVO PRINCIPAL DE LA APLICACIÓN \_ \_ \| SHTDN \_ MOTIVO MENOR DE LA \_ \_ DESAHORA                                            | "Aplicación: no responde" Un reinicio o apagado no planeados para solucionar problemas de una aplicación que no responde.<br/>                                                                                                                             |
| SHTDN MOTIVO PRINCIPAL DE LA APLICACIÓN SHTDN MOTIVO DE LA INSTALACIÓN SECUNDARIA MARCA DE MOTIVO DE \_ \_ \_ \| \_ \_ \_ \| SHTDN \_ \_ \_ PLANEADA    | "Aplicación: instalación (planeada)" Reinicio planeado o apagado para realizar la instalación de la aplicación.<br/>                                                                                                                              |
| SHTDN \_ MOTIVO PRINCIPAL DE MANTENIMIENTO MENOR DE LA APLICACIÓN \_ \_ \| SHTDN \_ \_ \_                                     | "Aplicación: Mantenimiento (no planeado)" Un reinicio o apagado no planeado para dar servicio a una aplicación.<br/>                                                                                                                                    |
| SHTDN MOTIVO PRINCIPAL DE LA APLICACIÓN SHTDN MOTIVO DE MANTENIMIENTO MENOR MARCA DE MOTIVO DE \_ \_ \_ \| \_ \_ \_ \| SHTDN \_ \_ \_ PLANEADA     | "Aplicación: mantenimiento (planeado)" Reinicio planeado o apagado para realizar el mantenimiento planeado en una aplicación.<br/>                                                                                                                  |
| SHTDN \_ MOTIVO PRINCIPAL DE LA APLICACIÓN \_ \_ \| SHTDN \_ MOTIVO MENOR \_ \_ INESTABLE                                        | "Aplicación: inestable" Reinicio o apagado no planeado para solucionar problemas de una aplicación inestable.<br/>                                                                                                                                     |
| SHTDN MOTIVO PRINCIPAL DE LA INSTALACIÓN SECUNDARIA \_ \_ DE HARDWARE \_ \| SHTDN \_ \_ \_                                       | "Hardware: Instalación (no planeada)" Un reinicio o apagado no planeados para iniciar o completar la instalación de hardware.<br/>                                                                                                                     |
| SHTDN MOTIVO PRINCIPAL DE LA RAZÓN DE LA INSTALACIÓN SECUNDARIA DE LA MARCA DE MOTIVO DE LA INSTALACIÓN \_ \_ DE \_ \| \_ \_ \_ \| SHTDN \_ \_ \_ PLANEADA       | "Hardware: Instalación (planeada)" Reinicio planeado o apagado para iniciar o completar la instalación de hardware.<br/>                                                                                                                          |
| SHTDN \_ MOTIVO PRINCIPAL DE MANTENIMIENTO MENOR DE HARDWARE \_ \_ \| SHTDN \_ \_ \_                                        | "Hardware: Mantenimiento (no planeado)" Un reinicio o apagado no planeado para el hardware de servicio en el sistema.<br/>                                                                                                                               |
| SHTDN MOTIVO PRINCIPAL DE HARDWARE SHTDN MOTIVO DE MANTENIMIENTO MENOR MARCA DE MOTIVO DE \_ \_ \_ \| \_ \_ \_ \| SHTDN \_ \_ \_ PLANEADA        | "Hardware: Mantenimiento (planeado)" Reinicio planeado o apagado del hardware de servicio en el sistema.<br/>                                                                                                                                    |
| SHTDN \_ REASON \_ MAJOR \_ LEGACY \_ API                                                                          | "Legacy API shutdown" Este apagado se inició mediante la función [**initiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) heredada. Las aplicaciones deben usar [**la función InitiateSystemShutdownEx.**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)<br/> |
| SHTDN MOTIVO PRINCIPAL DE LA REVISIÓN SECUNDARIA DEL SISTEMA OPERATIVO \_ \_ \_ \| SHTDN \_ \_ \_                                      | "Sistema operativo: corrección rápida (no planeada)" Un reinicio o apagado no planeados para instalar una corrección rápida.<br/>                                                                                                                                        |
| SHTDN MOTIVO PRINCIPAL DEL SISTEMA OPERATIVO SHTDN MOTIVO DE LA REVISIÓN SECUNDARIA \_ \_ \_ \| \_ \_ \_ \| SHTDN \_ \_ REASON FLAG \_ PLANNED      | "Sistema operativo: corrección rápida (planeada)" Reinicio planeado o apagado para instalar una corrección de accesos.<br/>                                                                                                                                             |
| SHTDN MOTIVO PRINCIPAL DE LA RECONFIGURACIÓN SECUNDARIA DEL SISTEMA OPERATIVO \_ \_ \_ \| SHTDN \_ \_ \_                                    | "Sistema operativo: Reconfiguración (no planeada)" Un reinicio o apagado no planeados para cambiar la configuración del sistema operativo.<br/>                                                                                                        |
| SHTDN MOTIVO PRINCIPAL DEL SISTEMA OPERATIVO \_ \_ \_ \| SHTDN MOTIVO DE LA RECONFIGURACIÓN SECUNDARIA DE LA MARCA DE MOTIVO \_ \_ DE \_ \| SHTDN \_ \_ \_ PLANEADA    | "Sistema operativo: reconfiguración (planeada)" Reinicio planeado o apagado para cambiar la configuración del sistema operativo.<br/>                                                                                                             |
| SHTDN MOTIVO PRINCIPAL DEL SISTEMA OPERATIVO \_ \_ \_ \| SHTDN \_ MOTIVO DE LA \_ \_ CORRECCIÓN DE SEGURIDAD SECUNDARIA                                 | "Sistema operativo: corrección de seguridad (no planeada)" Un reinicio o apagado no planeado para instalar una revisión de seguridad.<br/>                                                                                                                            |
| SHTDN MOTIVO PRINCIPAL DEL SISTEMA OPERATIVO SHTDN MOTIVO DE SEGURIDAD SECUNDARIA MARCA DE MOTIVO \_ \_ \_ \| \_ \_ \_ \| SHTDN \_ \_ \_ PLANEADA | "Sistema operativo: corrección de seguridad (planeada)" Un reinicio planeado o apagado para instalar una revisión de seguridad.<br/>                                                                                                                                 |
| SHTDN MOTIVO PRINCIPAL DEL SISTEMA OPERATIVO \_ \_ \_ \| SHTDN \_ MOTIVO MENOR \_ \_ SERVICEPACK \| SHTDN \_ REASON FLAG \_ \_ PLANNED | "Sistema operativo: Service Pack (planeado)" Reinicio planeado o apagado para instalar un Service Pack.<br/>                                                                                                                                   |
| SHTDN MOTIVO PRINCIPAL DEL SISTEMA OPERATIVO SHTDN MOTIVO DE LA ACTUALIZACIÓN SECUNDARIA MARCA DE MOTIVO DE \_ \_ \_ \| \_ \_ \_ \| SHTDN \_ \_ \_ PLANEADA     | "Sistema operativo: actualización (planeada)" Reinicio planeado o apagado para actualizar la configuración del sistema operativo.<br/>                                                                                                                    |
| SHTDN \_ REASON \_ MAJOR \_ OTHER \| SHTDN \_ REASON \_ MINOR \_ OTHER                                                 | "Otros (no planeados)" Un apagado o reinicio no planeados.<br/>                                                                                                                                                                                 |
| SHTDN \_ MOTIVO PRINCIPAL OTRO MOTIVO DE SHTDN MENOR OTRA MARCA DE MOTIVO DE \_ \_ \| \_ \_ \_ \| SHTDN \_ \_ \_ PLANEADA                 | "Otros (planeados)" Un apagado planeado o reinicio.<br/>                                                                                                                                                                                      |
| SHTDN \_ REASON \_ MAJOR \_ OTHER \| SHTDN \_ REASON \_ MINOR \_ HUNG                                                  | "Other Failure: System Unresponsive" The system became unresponsive.<br/>                                                                                                                                                                  |
| SHTDN MOTIVO PRINCIPAL DE LA RAZÓN PRINCIPAL \_ DE \_ \_ \| SHTDN \_ MINOR \_ \_ CORDUNPLUGGED                                         | "Power Failure: Cable Unplugged" (Error de alimentación: cable desconectado) El equipo estaba desconectado.<br/>                                                                                                                                                                           |
| SHTDN MOTIVO PRINCIPAL DE LA RAZÓN DEL ENTORNO MENOR \_ \_ DE \_ \| SHTDN \_ \_ \_                                           | "Power Failure: Environment" Se ha producido una interrupción del suministro eléctrico.<br/>                                                                                                                                                                                |
| SHTDN \_ MOTIVO PRINCIPAL DEL SISTEMA \_ \_ \| SHTDN \_ REASON MINOR \_ \_ BLUESCREEN                                           | "Error del sistema: Error de detección" El equipo mostró un evento de bloqueo de pantalla azul.<br/>                                                                                                                                                        |
| SHTDN \_ MOTIVO PRINCIPAL DEL SISTEMA \_ \_ \| SHTDN \_ MOTIVO DE LA CONECTIVIDAD DE RED \_ \_ \_ SECUNDARIA                                | "Pérdida de conectividad de red (no planeada)" El equipo debe apagarse debido a un problema de conectividad de red.<br/>                                                                                                                    |
| SHTDN \_ MOTIVO PRINCIPAL DE SEGURIDAD SECUNDARIA DEL SISTEMA \_ \_ \| SHTDN \_ \_ \_                                             | "Problema de seguridad" El equipo debe apagarse debido a un problema de seguridad.<br/>                                                                                                                                                          |



 

También puede definir sus propios motivos de apagado y agregarlos al registro. Cada código de motivo debe almacenarse como un valor del Registro en la clave **siguiente: HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Reliability \\ \\ UserDefined \\<\_ \_ \_** default system language ID>

Esta clave contiene nombres de valor con el formato siguiente: *xxxxx*; *nnn*; *nnnnn.* Los puntos y coma delimitan los componentes de un nombre de valor.

<dl> <dt>

<span id="xxxxx"></span><span id="XXXXX"></span>*Xxxxx*
</dt> <dd>

De uno a cinco de las siguientes marcas de control (no se puede usar ningún otro carácter).



| Marca | Descripción                                                                                       |
|------|---------------------------------------------------------------------------------------------------|
| P    | Apagado planeado; de lo contrario, un apagado no planeado.                                               |
| C    | Se requiere un comentario. Esta marca debe usarse con S.<br/>                                  |
| B    | Se requiere un identificador. Esta marca debe usarse con D.<br/>                                      |
| S    | Muestra el cuadro de diálogo de apagado esperado. Se deben usar S, D o S y D.<br/>   |
| D    | Muestra el cuadro de diálogo de apagado inesperado. Se deben usar S, D o S y D.<br/> |



 

El orden en el que se usan las marcas no es importante. Por ejemplo, CSP indica un apagado planeado donde se muestra el cuadro de diálogo de apagado esperado y se requiere un comentario.

</dd> <dt>

<span id="nnn"></span><span id="NNN"></span>*Nnn*
</dt> <dd>

Motivo principal. Este componente debe ser un número en el intervalo 64-255. El intervalo 0-63 está reservado para que lo use el sistema.

</dd> <dt>

<span id="nnnnn"></span><span id="NNNNN"></span>*nnnnn*
</dt> <dd>

Razón secundaria. Este componente debe estar en el intervalo 0-65535.

</dd> </dl>

Las razones personalizadas se ordenan en la interfaz de usuario por número de motivo principal y, a continuación, por número de motivo menor. No hay dos razones personalizadas que puedan usar las mismas razones principales y secundarias, a menos que una esté planeada y la otra no esté planeada. De lo contrario, el sistema usará la primera instancia y omitirá las demás.

Los datos de cada valor del Registro son dos cadenas, separadas \\ por n \\ r. La primera cadena es una cadena de título que se mostrará en el cuadro de diálogo de cierre y se escribirá en el registro de eventos. El tamaño máximo es de 64 caracteres. Las cadenas de título deben ser únicas. Los títulos personalizados no pueden coincidir con los títulos estándar definidos por el sistema ni con otro título personalizado. La segunda cadena es una cadena de descripción que se va a mostrar en el cuadro de diálogo de apagado; es opcional. El tamaño máximo es de 256 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones \[ de escritorio XP para aplicaciones para \| UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2003 \[ \| aplicaciones para UWP\]<br/>                         |
| Header<br/>                   | <dl> <dt>Reason.h</dt> </dl> |



 

 
