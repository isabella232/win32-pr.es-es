---
description: Los códigos de motivo de apagado se usan en las funciones ExitWindowsEx y InitiateSystemShutdownEx en el parámetro dwReason. \_ \_ El sistema procesará los códigos de motivo de número máximo de motivos. El número máximo \_ \_ de razones se define en Reason. h.
ms.assetid: db1ecee0-40eb-4761-b5d8-9cc3c1c98cdf
title: Códigos de motivo de cierre del sistema (Reason. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee2b8b2795dcf350d627b3cf59f85eb374a22cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666716"
---
# <a name="system-shutdown-reason-codes"></a>Códigos de motivo de cierre del sistema

Los códigos de motivo de apagado se usan en las funciones [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) y [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) en el parámetro *dwReason* .

\_ \_ El sistema procesará los códigos de motivo de número máximo de motivos. El número máximo \_ \_ de razones se define en Reason. h.

A continuación se muestran las marcas de motivo principales. Indican el tipo de problema general.



| Constante o valor                                                                                                                                                                                                                                                                                 | Descripción                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_MAJOR_APPLICATION"></span><span id="shtdn_reason_major_application"></span><dl> <dt>**SHTDN \_ MOTIVO \_ principal \_**</dt> de la aplicación <dt>0x00040000</dt> </dl>             | Problema de la aplicación.<br/>                                                                                                                                      |
| <span id="SHTDN_REASON_MAJOR_HARDWARE"></span><span id="shtdn_reason_major_hardware"></span><dl> <dt>**SHTDN \_ MOTIVO \_ principal \_**</dt> del <dt>0x00010000</dt> de hardware </dl>                      | Problema de hardware.<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_LEGACY_API"></span><span id="shtdn_reason_major_legacy_api"></span><dl> <dt>**SHTDN \_ MOTIVO de la \_ \_ \_ API heredada principal**</dt> <dt>0x00070000</dt> </dl>               | Se usó la función [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) en lugar de [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa).<br/> |
| <span id="SHTDN_REASON_MAJOR_OPERATINGSYSTEM"></span><span id="shtdn_reason_major_operatingsystem"></span><dl> <dt>**SHTDN \_ MOTIVO \_ principal de \_ OPERATINGSYSTEM**</dt> <dt>0x00020000</dt> </dl> | Problema del sistema operativo.<br/>                                                                                                                                 |
| <span id="SHTDN_REASON_MAJOR_OTHER"></span><span id="shtdn_reason_major_other"></span><dl> <dt>**SHTDN \_ MOTIVO \_ principal \_ otros**</dt> <dt>0x00000000</dt> </dl>                               | Otro problema.<br/>                                                                                                                                            |
| <span id="SHTDN_REASON_MAJOR_POWER"></span><span id="shtdn_reason_major_power"></span><dl> <dt>**SHTDN \_ MOTIVO de la \_ \_ potencia principal**</dt> <dt>0x00060000</dt> </dl>                               | Error de alimentación.<br/>                                                                                                                                          |
| <span id="SHTDN_REASON_MAJOR_SOFTWARE"></span><span id="shtdn_reason_major_software"></span><dl> <dt>**SHTDN \_ MOTIVO \_ principal \_**</dt> de <dt>0x00030000</dt> de software </dl>                      | Problema de software.<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_SYSTEM"></span><span id="shtdn_reason_major_system"></span><dl> <dt>**SHTDN \_ MOTIVO \_ principal \_ del sistema**</dt> <dt>0x00050000</dt> </dl>                            | Error del sistema.<br/>                                                                                                                                         |



A continuación se muestran las marcas de razón secundaria. Modifican la marca de motivo principal especificada. Puede usar cualquier motivo secundario junto con cualquier razón principal, pero algunas combinaciones no tienen sentido.



| Constante o valor                                                                                                                                                                                                                                                                                                    | Descripción                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------|
| <span id="SHTDN_REASON_MINOR_BLUESCREEN"></span><span id="shtdn_reason_minor_bluescreen"></span><dl> <dt>**SHTDN \_ MOTIVO de 0x0000000F de \_ \_ pantalla azul secundaria**</dt> <dt></dt> </dl>                                   | Evento de bloqueo de pantalla azul.<br/>       |
| <span id="SHTDN_REASON_MINOR_CORDUNPLUGGED"></span><span id="shtdn_reason_minor_cordunplugged"></span><dl> <dt>**SHTDN \_ MOTIVO \_ de \_ CORDUNPLUGGED menor**</dt> <dt>0x0000000b</dt> </dl>                          | Desconecta.<br/>                     |
| <span id="SHTDN_REASON_MINOR_DISK"></span><span id="shtdn_reason_minor_disk"></span><dl> <dt>**SHTDN \_ MOTIVO de 0x00000007 de \_ \_ disco secundario**</dt> <dt></dt> </dl>                                                     | disco.<br/>                          |
| <span id="SHTDN_REASON_MINOR_ENVIRONMENT"></span><span id="shtdn_reason_minor_environment"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_**</dt> de la <dt>0x0000000c</dt> del entorno secundario </dl>                                | Entorno.<br/>                   |
| <span id="SHTDN_REASON_MINOR_HARDWARE_DRIVER"></span><span id="shtdn_reason_minor_hardware_driver"></span><dl> <dt>**SHTDN \_ MOTIVO de 0x0000000d de \_ \_ \_ controlador de hardware secundario**</dt> <dt></dt> </dl>                   | Dispositivo.<br/>                        |
| <span id="SHTDN_REASON_MINOR_HOTFIX"></span><span id="shtdn_reason_minor_hotfix"></span><dl> <dt>**SHTDN \_ MOTIVO de la \_ \_ revisión mínima**</dt> <dt>0x00000011</dt> </dl>                                               | Corrección urgente.<br/>                       |
| <span id="SHTDN_REASON_MINOR_HOTFIX_UNINSTALL"></span><span id="shtdn_reason_minor_hotfix_uninstall"></span><dl> <dt>**SHTDN \_ MOTIVO de la \_ \_ \_ desinstalación de la revisión secundaria**</dt> <dt>0x00000017</dt> </dl>                | Desinstalación de la corrección de acceso frecuente.<br/>        |
| <span id="SHTDN_REASON_MINOR_HUNG"></span><span id="shtdn_reason_minor_hung"></span><dl> <dt>**SHTDN \_ MOTIVO \_ de \_ bloqueo de menor importancia**</dt> <dt></dt> </dl>                                                     | Responder.<br/>                  |
| <span id="SHTDN_REASON_MINOR_INSTALLATION"></span><span id="shtdn_reason_minor_installation"></span><dl> <dt>**SHTDN \_ MOTIVO de la \_ \_ instalación mínima**</dt> <dt>0x00000002</dt> </dl>                             | Instalación.<br/>                  |
| <span id="SHTDN_REASON_MINOR_MAINTENANCE"></span><span id="shtdn_reason_minor_maintenance"></span><dl> <dt>**SHTDN \_ MOTIVO \_ de \_ mantenimiento mínimo**</dt> <dt>0x00000001</dt> </dl>                                | Alimenticia.<br/>                   |
| <span id="SHTDN_REASON_MINOR_MMC"></span><span id="shtdn_reason_minor_mmc"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_**</dt> de la <dt>0x00000019</dt> de MMC secundaria </dl>                                                        | Problema de MMC.<br/>                     |
| <span id="SHTDN_REASON_MINOR_NETWORK_CONNECTIVITY"></span><span id="shtdn_reason_minor_network_connectivity"></span><dl> <dt>**SHTDN \_ MOTIVO de la \_ \_ \_ conectividad de red secundaria**</dt> <dt>0x00000014</dt> </dl>    | Conectividad de red.<br/>          |
| <span id="SHTDN_REASON_MINOR_NETWORKCARD"></span><span id="shtdn_reason_minor_networkcard"></span><dl> <dt>**SHTDN \_ MOTIVO \_ de \_ NETWORKCARD menor**</dt> <dt>0x00000009</dt> </dl>                                | Tarjeta de red.<br/>                  |
| <span id="SHTDN_REASON_MINOR_OTHER"></span><span id="shtdn_reason_minor_other"></span><dl> <dt>**SHTDN \_ MOTIVO \_ menor \_**</dt> , <dt>0x00000000</dt> </dl>                                                  | Otro problema.<br/>                   |
| <span id="SHTDN_REASON_MINOR_OTHERDRIVER"></span><span id="shtdn_reason_minor_otherdriver"></span><dl> <dt>**SHTDN \_ MOTIVO \_ de \_ OTHERDRIVER menor**</dt> <dt>0x0000000e</dt> </dl>                                | Otro evento de controlador.<br/>            |
| <span id="SHTDN_REASON_MINOR_POWER_SUPPLY"></span><span id="shtdn_reason_minor_power_supply"></span><dl> <dt>**SHTDN \_ RAZÓN de la \_ \_ \_ fuente de alimentación secundaria**</dt> <dt>0x0000000A</dt> </dl>                            | Fuente de alimentación.<br/>                  |
| <span id="SHTDN_REASON_MINOR_PROCESSOR"></span><span id="shtdn_reason_minor_processor"></span><dl> <dt>**SHTDN \_ RAZÓN \_ del \_ procesador secundario**</dt> <dt>0x00000008</dt> </dl>                                      | Procesador.<br/>                     |
| <span id="SHTDN_REASON_MINOR_RECONFIG"></span><span id="shtdn_reason_minor_reconfig"></span><dl> <dt>**SHTDN \_ MOTIVO \_ de \_ reconfiguración mínima**</dt> de <dt>0x00000004</dt> </dl>                                         | Volver a configurar.<br/>                   |
| <span id="SHTDN_REASON_MINOR_SECURITY"></span><span id="shtdn_reason_minor_security"></span><dl> <dt>**SHTDN \_ MOTIVO \_ de \_ seguridad menor**</dt> <dt>0x00000013</dt> </dl>                                         | Problema de seguridad.<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX"></span><span id="shtdn_reason_minor_securityfix"></span><dl> <dt>**SHTDN \_ MOTIVO \_ de \_ SECURITYFIX menor**</dt> <dt>0x00000012</dt> </dl>                                | Revisión de seguridad.<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX_UNINSTALL"></span><span id="shtdn_reason_minor_securityfix_uninstall"></span><dl> <dt>**SHTDN \_ MOTIVO \_ leve \_ SECURITYFIX \_ desinstalar**</dt> <dt>0x00000018</dt> </dl> | Desinstalación de revisiones de seguridad.<br/> |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK"></span><span id="shtdn_reason_minor_servicepack"></span><dl> <dt>**SHTDN \_ MOTIVO \_ leve del \_ SERVICEPACK**</dt> <dt>0x00000010</dt> </dl>                                | Service Pack.<br/>                  |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK_UNINSTALL"></span><span id="shtdn_reason_minor_servicepack_uninstall"></span><dl> <dt>**SHTDN \_ MOTIVO \_ leve \_ de \_ desinstalación del SERVICEPACK**</dt> <dt>0x00000016</dt> </dl> | Desinstalación de Service Pack.<br/>   |
| <span id="SHTDN_REASON_MINOR_TERMSRV"></span><span id="shtdn_reason_minor_termsrv"></span><dl> <dt>**SHTDN \_ MOTIVO \_ \_**</dt> de la versión secundaria de TERMSRV <dt>0x00000020</dt> </dl>                                            | Terminal Services.<br/>             |
| <span id="SHTDN_REASON_MINOR_UNSTABLE"></span><span id="shtdn_reason_minor_unstable"></span><dl> <dt>**SHTDN \_ MOTIVO \_ menor \_ inestable**</dt> <dt>0x00000006</dt> </dl>                                         | Stable.<br/>                      |
| <span id="SHTDN_REASON_MINOR_UPGRADE"></span><span id="shtdn_reason_minor_upgrade"></span><dl> <dt>**SHTDN \_ MOTIVO de la \_ \_ actualización secundaria**</dt> <dt>0x00000003</dt> </dl>                                            | Actualización.<br/>                       |
| <span id="SHTDN_REASON_MINOR_WMI"></span><span id="shtdn_reason_minor_wmi"></span><dl> <dt>**SHTDN \_ MOTIVO de 0x00000015 de \_ \_ WMI leve**</dt> <dt></dt> </dl>                                                        | Problema de WMI.<br/>                     |



Las siguientes marcas opcionales proporcionan información adicional sobre el evento.



| Constante o valor                                                                                                                                                                                                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_FLAG_USER_DEFINED"></span><span id="shtdn_reason_flag_user_defined"></span><dl> <dt>**SHTDN \_ Marca de motivo de 0x40000000 \_ \_ \_ definido por el usuario**</dt> <dt></dt> </dl> | El código de motivo lo define el usuario. Para obtener más información, vea definir un código de motivo personalizado. <br/> Si este marcador no está presente, el sistema define el código de motivo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SHTDN_REASON_FLAG_PLANNED"></span><span id="shtdn_reason_flag_planned"></span><dl> <dt>**SHTDN \_ Marca de motivo de 0x80000000 \_ \_ planeada**</dt> <dt></dt> </dl>                 | Se planificó el cierre. El sistema genera un archivo de datos de estado del sistema (SSD). Este archivo contiene información de estado del sistema, como los procesos, los subprocesos, el uso de memoria y la configuración. <br/> Si este marcador no está presente, no se planeó el cierre. Las opciones de notificación e informes se controlan mediante un conjunto de directivas. Por ejemplo, después de iniciar sesión, el sistema muestra un cuadro de diálogo que informa del apagado no planeado si se ha habilitado la Directiva. Se crea un archivo SSD solo si la Directiva de SSD está habilitada en el sistema. El administrador puede usar [Informe de errores de Windows](../wer/windows-error-reporting.md) para enviar los datos de SSD a una ubicación central o a Microsoft.<br/> |



## <a name="remarks"></a>Observaciones

El sistema reconoce las siguientes combinaciones. La tabla indica la cadena que se muestra en el rastreador de eventos de apagado y proporciona una descripción más detallada. La cadena predeterminada es "no se encontró ningún título por este motivo".



| Combinación                                                                                                | Descripción                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| motivo de SHTDN principal de la \_ \_ \_ aplicación \| SHTDN \_ motivo de \_ \_ bloqueo secundario                                            | "Aplicación: sin respuesta" un reinicio o apagado no planeado para solucionar problemas de una aplicación que no responde.<br/>                                                                                                                             |
| motivo de SHTDN principal de la \_ \_ \_ aplicación \| SHTDN motivo de la \_ \_ instalación mínima SHTDN de la \_ marca de \| \_ motivo \_ \_ planeada    | "Aplicación: instalación (planeada)" de un reinicio o apagado planeado para realizar la instalación de la aplicación.<br/>                                                                                                                              |
| motivo de SHTDN principal de la \_ \_ \_ aplicación \| SHTDN \_ motivo del \_ \_ mantenimiento secundario                                     | "Aplicación: mantenimiento (no planeado)" de un reinicio o apagado no planeado para el servicio de una aplicación.<br/>                                                                                                                                    |
| motivo de SHTDN principal de la \_ \_ \_ aplicación \| SHTDN \_ razón de \_ mantenimiento menor SHTDN de la \_ marca de \| \_ motivo \_ \_ planeada     | "Aplicación: mantenimiento (planeado)" un reinicio o apagado planeado para realizar el mantenimiento planeado en una aplicación.<br/>                                                                                                                  |
| motivo SHTDN principal de la \_ \_ \_ aplicación \| SHTDN \_ motivo \_ menor \_ inestable                                        | "Aplicación: inestable" un reinicio o apagado no planeado para solucionar problemas de una aplicación inestable.<br/>                                                                                                                                     |
| motivo de SHTDN \_ \_ principal de \_ hardware SHTDN motivo de la \| \_ \_ \_ instalación mínima                                       | "Hardware: instalación (no planeada)" de un reinicio o apagado no planeado para iniciar o completar la instalación de hardware.<br/>                                                                                                                     |
| motivo de SHTDN \_ \_ principal de \_ hardware SHTDN motivo de la \| \_ \_ \_ instalación mínima \| SHTDN \_ \_ \_ de la marca de motivo       | "Hardware: instalación (planeada)" de un reinicio o apagado planeado para comenzar o completar la instalación de hardware.<br/>                                                                                                                          |
| motivo de SHTDN \_ \_ principal de \_ hardware \| SHTDN razón de \_ \_ \_ mantenimiento menor                                        | "Hardware: mantenimiento (no planeado)": un reinicio o apagado no planeado para el hardware de servicio en el sistema.<br/>                                                                                                                               |
| motivo de SHTDN \_ \_ principal de \_ hardware \| SHTDN razón de \_ \_ mantenimiento menor SHTDN de la marca de \_ \| \_ motivo \_ \_ planeada        | "Hardware: mantenimiento (planeado)" un reinicio o apagado planeado para el hardware del servicio en el sistema.<br/>                                                                                                                                    |
| \_motivo de \_ la \_ API heredada principal \_ de SHTDN                                                                          | "Cierre de la API heredada" este apagado lo inició la función [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) heredada. Las aplicaciones deben usar la función [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) .<br/> |
| motivo de SHTDN \_ \_ principal de \_ OPERATINGSYSTEM \| SHTDN motivo de \_ \_ \_ revisión secundaria                                      | "Sistema operativo: corrección activa (no planeada)" de un reinicio o apagado no planeado para instalar una corrección urgente.<br/>                                                                                                                                        |
| motivo de SHTDN \_ \_ principal de \_ OPERATINGSYSTEM \| SHTDN motivo de \_ \_ revisión secundaria SHTDN de la marca de \_ \| \_ motivo \_ \_ planeada      | "Sistema operativo: corrección activa (planeada)" de un reinicio o apagado planeado para instalar una corrección urgente.<br/>                                                                                                                                             |
| \_razón SHTDN \_ principal \_ OPERATINGSYSTEM \| SHTDN \_ razón \_ de \_ reconfiguración secundaria                                    | "Sistema operativo: reconfiguración (no planeada)" de un reinicio o apagado no planeado para cambiar la configuración del sistema operativo.<br/>                                                                                                        |
| motivo de SHTDN \_ \_ principal \_ OPERATINGSYSTEM \| SHTDN \_ razón de \_ \_ reconfiguración secundaria SHTDN de la marca de \| \_ motivo \_ \_ planeada    | "Sistema operativo: reconfiguración (planeada)" de un reinicio o apagado planeado para cambiar la configuración del sistema operativo.<br/>                                                                                                             |
| \_motivo SHTDN \_ principal \_ OPERATINGSYSTEM \| SHTDN \_ motivo \_ menor \_ SECURITYFIX                                 | "Sistema operativo: corrección de seguridad (no planeada)" de un reinicio o apagado no planeado para instalar una revisión de seguridad.<br/>                                                                                                                            |
| motivo de SHTDN \_ \_ principal \_ OPERATINGSYSTEM \| SHTDN razón de la marca de \_ \_ \_ motivo secundaria SECURITYFIX \| SHTDN \_ \_ \_ planeada | "Sistema operativo: corrección de seguridad (planeada)" un reinicio o apagado planeado para instalar una revisión de seguridad.<br/>                                                                                                                                 |
| motivo de SHTDN \_ \_ principal de \_ OPERATINGSYSTEM SHTDN motivo de la \| \_ \_ marca de causa secundaria del \_ SERVICEPACK \| SHTDN \_ \_ \_ | "Sistema operativo: Service Pack (planeado)" un reinicio o apagado planeado para instalar un Service Pack.<br/>                                                                                                                                   |
| motivo de SHTDN \_ \_ principal \_ OPERATINGSYSTEM \| SHTDN \_ motivo de \_ actualización mínima SHTDN de la \_ marca de \| \_ motivo \_ \_ planeada     | "Sistema operativo: actualización (planeada)" un reinicio o apagado planeado para actualizar la configuración del sistema operativo.<br/>                                                                                                                    |
| motivo de SHTDN \_ \_ principal \_ otros \| motivos de SHTDN \_ \_ menores \_                                                 | "Otro (no planeado)": un apagado o un reinicio no planeado.<br/>                                                                                                                                                                                 |
| motivo de SHTDN \_ \_ principal \_ otro \| motivo de SHTDN \_ menor, \_ \_ otra marca de \| \_ motivo SHTDN \_ \_ planeada                 | "Otro (planeado)": un cierre planeado o un reinicio.<br/>                                                                                                                                                                                      |
| motivo de SHTDN \_ \_ principal \_ otro \| motivo de SHTDN \_ \_ menor \_ bloqueo                                                  | "Otro error: el sistema no responde" el sistema dejó de responder.<br/>                                                                                                                                                                  |
| SHTDN \_ razón \_ importante \_ \| SHTDN \_ razón principal \_ \_ CORDUNPLUGGED                                         | "Error de alimentación: cable desconectado" el equipo estaba desconectado.<br/>                                                                                                                                                                           |
| SHTDN \_ razón \_ importante \_ SHTDN razón de la importancia principal del \| \_ \_ \_ entorno secundario                                           | "Error de alimentación: entorno" se produjo una interrupción del suministro eléctrico.<br/>                                                                                                                                                                                |
| motivo de SHTDN principal SHTDN de la razón de la \_ \_ \_ \| \_ \_ menor \_ pantalla azul                                           | "Error del sistema: error de detención" el equipo mostró un evento de bloqueo de pantalla azul.<br/>                                                                                                                                                        |
| motivo de SHTDN \_ \_ principal SHTDN de la \_ \| \_ \_ \_ conectividad de red secundaria \_                                | "Pérdida de conectividad de red (no planeada)" el equipo debe cerrarse debido a un problema de conectividad de red.<br/>                                                                                                                    |
| motivo de SHTDN \_ \_ principal \_ SHTDN de seguridad de \| \_ \_ \_ seguridad secundaria                                             | "Problema de seguridad" el equipo debe cerrarse debido a un problema de seguridad.<br/>                                                                                                                                                          |



 

También puede definir sus propios motivos de apagado y agregarlos al registro. Cada código de motivo debe almacenarse como un valor del registro en la siguiente clave:**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ confiabilidad \\ UserDefined \\<default \_ System \_ Language \_ ID>**

Esta clave contiene nombres de valores con el formato siguiente: *xxxxx*; *nnn*; *nnnnn*. Los signos de punto y coma delimitan los componentes de un nombre de valor.

<dl> <dt>

<span id="xxxxx"></span><span id="XXXXX"></span>*xxxxx*
</dt> <dd>

Uno a cinco de los siguientes marcadores de control (no se pueden usar otros caracteres).



| Marca | Descripción                                                                                       |
|------|---------------------------------------------------------------------------------------------------|
| P    | Cierre planeado; de lo contrario, un apagado no planeado.                                               |
| C    | Se requiere un comentario. Esta marca debe usarse con S.<br/>                                  |
| B    | Se requiere un identificador. Esta marca se debe utilizar con D.<br/>                                      |
| S    | Muestra el cuadro de diálogo de apagado esperado. Se deben usar S, D o ambos S y D.<br/>   |
| D    | Mostrar el cuadro de diálogo apagado inesperado. Se deben usar S, D o ambos S y D.<br/> |



 

El orden en el que se usan las marcas no es importante. Por ejemplo, CSP indica un apagado planeado en el que se muestra el cuadro de diálogo de apagado esperado y se requiere un comentario.

</dd> <dt>

<span id="nnn"></span><span id="NNN"></span>*nnn*
</dt> <dd>

Motivo principal. Este componente debe ser un número comprendido en el intervalo de 64-255. El intervalo 0-63 está reservado para su uso por el sistema.

</dd> <dt>

<span id="nnnnn"></span><span id="NNNNN"></span>*nnnnn*
</dt> <dd>

Razón secundaria. Este componente debe estar en el intervalo 0-65535.

</dd> </dl>

Los motivos personalizados se ordenan en la interfaz de usuario por el número de motivo principal y después por el número de motivo secundario. Dos razones personalizadas no pueden usar las mismas razones principales y secundarias, a menos que se planee una y la otra no esté planeada. De lo contrario, el sistema usará la primera instancia y omitirá las demás.

Los datos de cada valor del registro son dos cadenas, separadas por \\ n \\ r. La primera cadena es una cadena de título que se mostrará en el cuadro de diálogo de apagado y se escribirá en el registro de eventos. El tamaño máximo es de 64 caracteres. Las cadenas de título deben ser únicas. Los títulos personalizados no pueden coincidir con los títulos estándar definidos por el sistema u otro título personalizado. La segunda cadena es una cadena de descripción que se va a mostrar en el cuadro de diálogo de apagado; es opcional. El tamaño máximo es de 256 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows XP \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2003 \|\]<br/>                         |
| Encabezado<br/>                   | <dl> <dt>Motivo. h</dt> </dl> |



 

 
