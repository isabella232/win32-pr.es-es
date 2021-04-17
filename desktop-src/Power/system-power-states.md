---
description: Para el usuario, el sistema parece estar activado o desactivado.
ms.assetid: 3d897a88-125e-457f-9ea7-ac2056b0767a
title: Estados de energía del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f18cf6323ae852a871869066a2e9baa2860e6978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677887"
---
# <a name="system-power-states"></a>Estados de energía del sistema

Para el usuario, el sistema parece estar activado o desactivado. No hay ningún otro estado detectable. Sin embargo, el sistema admite varios Estados de energía que se corresponden con los Estados de energía definidos en la especificación de interfaz avanzada de configuración y energía (ACPI). También hay variaciones de estos Estados, como la suspensión híbrida y el inicio rápido. En este tema se presentan estos Estados y se describe cómo se relacionan entre sí.

> [!NOTE]
> Los integradores de sistemas y los programadores que crean controladores o aplicaciones con un servicio de sistema deben tener especial cuidado con los problemas de calidad de los controladores, como pérdidas de memoria. Aunque la calidad del controlador siempre ha sido importante, el tiempo de actividad entre los reinicios del kernel puede ser mucho mayor que en las versiones anteriores del sistema operativo, ya que en las suspensión y apagados iniciados por el usuario, el kernel, los controladores y los servicios se conservarán y restaurarán, no se volverá a iniciar.

 

En la tabla siguiente se enumeran los Estados de energía de ACPI del consumo de energía más alto al más bajo.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado de energía</th>
<th>Estado de ACPI</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>En funcionamiento<br/></td>
<td>S0<br/></td>
<td>El sistema es totalmente utilizable. Los componentes de hardware que no están en uso pueden ahorrar energía introduciendo un estado de energía inferior.<br/></td>
</tr>
<tr class="even">
<td>En reposo<br/> (En espera moderna)<br/></td>
<td>Inactividad de baja energía S0<br/></td>
<td>Algunos sistemas SoC admiten un estado de inactividad de baja energía conocido como <a href="/windows-hardware/design/device-experiences/modern-standby">Standby moderno</a>. En este estado, el sistema puede cambiar rápidamente de un estado de baja energía a un estado de alta potencia, de modo que pueda responder rápidamente a los eventos de hardware y de red. Los sistemas que admiten el modo de espera moderno no usan S1-S3.<br/></td>
</tr>
<tr class="odd">
<td>En reposo<br/></td>
<td>S1<br/> S2<br/> S3<br/></td>
<td>Parece que el sistema está desactivado. La potencia consumida en estos Estados (S1-S3) es menor que S0 y más que S4; S3 consume menos energía que S2 y S2 consume menos energía que S1. Normalmente, los sistemas admiten uno de estos tres Estados, no los tres.<br/> En estos Estados (S1-S3), la memoria volátil se mantiene actualizada para mantener el estado del sistema. Algunos componentes permanecen encendidos, por lo que el equipo puede reactivarse desde la entrada del teclado, la LAN o un dispositivo USB.<br/> La <em>suspensión híbrida</em>, que se usa en los equipos de escritorio, es el lugar en el que un sistema utiliza un archivo de hibernación con S1-S3. El archivo de hibernación guarda el estado del sistema en caso de que el sistema pierda alimentación mientras está en suspensión.<br/>
<blockquote>
[!Note]<br />
Los sistemas SoC que admiten el modo de espera moderno (el estado de inactividad de baja energía) no usan S1-S3.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>Hibernar<br/></td>
<td>S4<br/></td>
<td>Parece que el sistema está desactivado. El consumo de energía se reduce al nivel más bajo. El sistema guarda el contenido de la memoria volátil en un archivo de hibernación para conservar el estado del sistema. Algunos componentes permanecen encendidos, por lo que el equipo puede reactivarse desde la entrada del teclado, la LAN o un dispositivo USB. El contexto de trabajo se puede restaurar si se almacena en un medio no volátil. <br/> <em>Inicio rápido</em> es donde el usuario cierra la sesión antes de que se cree el archivo de hibernación. Esto permite un archivo de hibernación más pequeño, más adecuado para sistemas con menos capacidades de almacenamiento.<br/></td>
</tr>
<tr class="odd">
<td>Soft off<br/></td>
<td>S5<br/></td>
<td>Parece que el sistema está desactivado. Este estado se compone de un ciclo de arranque y de apagado completo.<br/></td>
</tr>
<tr class="even">
<td>Mecánico desactivado<br/></td>
<td>G3<br/></td>
<td>El sistema está completamente apagado y no consume energía. El sistema vuelve al estado de funcionamiento solo después de un reinicio completo.<br/></td>
</tr>
</tbody>
</table>



 

La enumeración de [**\_ \_ Estado de energía del sistema**](/windows/desktop/api/WinNT/ne-winnt-system_power_state) define los valores que se usan para especificar los Estados de energía del sistema.

## <a name="working-state-s0"></a>Estado de funcionamiento (S0)

Durante el estado de funcionamiento, el sistema está activo y en ejecución. En términos simples, el dispositivo está "activado". Si la pantalla está activada o desactivada, el dispositivo se encuentra en un estado de ejecución completa. Para ahorrar energía, especialmente en los dispositivos con batería, es muy recomendable que se apaguen los componentes de hardware cuando no se usen.

> [!IMPORTANT]
> Desactivación de los componentes de hardware siempre que no se usen, independientemente del estado. El consumo de energía bajo es una consideración importante para los consumidores de dispositivos móviles.

 

## <a name="sleep-state-modern-standby"></a>Estado de suspensión (en espera moderna)

En el modo inactivo de baja energía S0 del estado de funcionamiento, también conocido como [Standby moderno](/windows-hardware/design/device-experiences/modern-standby), el sistema permanece parcialmente en ejecución. Durante el tiempo de espera moderno, el sistema puede mantenerse actualizado siempre que haya una red adecuada disponible y reactivarse cuando sea necesaria una acción en tiempo real, como el mantenimiento del sistema operativo. El modo de espera moderno es significativamente más rápido que S1-S3. Para obtener más información, consulte el [modo de espera moderno](/windows-hardware/design/device-experiences/modern-standby).

> [!Note]  
> El modo de espera moderno solo está disponible en algunos sistemas SoC. Cuando se admite, el sistema no admite S1-S3.

 

## <a name="sleep-state-s1-s3"></a>Estado de suspensión (S1-S3)

El sistema entra en suspensión en función de una serie de criterios, como la actividad de usuario o aplicación y las preferencias que el usuario establece en la página de configuración de **Power &** de la aplicación de **configuración** . De forma predeterminada, el sistema usa el estado de suspensión con el menor nivel admitido por todos los dispositivos de reactivación habilitados. Para obtener más información sobre el modo en que el sistema determina cuándo entrar en suspensión, vea [criterios de suspensión del sistema](system-sleep-criteria.md).

Antes de que el sistema entre en suspensión, determina el estado de suspensión adecuado, notifica a las aplicaciones y controladores de la transición pendiente y, a continuación, realiza la transición del sistema al estado de suspensión. En el caso de una transición crítica, como cuando se alcanza el umbral crítico de la batería, el sistema no notifica a las aplicaciones y los controladores. Las aplicaciones deben estar preparadas para esto y realizar la acción adecuada cuando el sistema vuelva al estado de funcionamiento.

En estos Estados (S1-S3), la memoria volátil se mantiene actualizada para mantener el estado del sistema. Algunos componentes permanecen encendidos, por lo que el equipo puede reactivarse desde la entrada del teclado, la LAN o un dispositivo USB.

El sistema también se activa tras la suspensión en respuesta a la actividad del usuario o a un evento de reactivación definido por una aplicación. Para obtener más información, consulte [eventos de reactivación del sistema](system-wake-up-events.md). La cantidad de tiempo que tarda el sistema en activarse depende del estado de suspensión desde el que se va a activar. El sistema tarda más tiempo en reactivarse de un estado de bajo consumo (S3) que en un estado de mayor potencia (S1) debido al trabajo adicional que puede tener que hacer el hardware (estabilizar la fuente de alimentación, reinicializar el procesador, etc.).

> [!Caution]  
> Cuando se llama a [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate), el valor **necesario de es \_ AWAYMODE \_** debe usarse solo cuando las aplicaciones multimedia que requieren el sistema llevan a cabo tareas en segundo plano, como grabar contenido de televisión o multimedia de streaming en otros dispositivos mientras el sistema parece estar en modo de suspensión. Las aplicaciones que no requieren un procesamiento en segundo plano crítico o que se ejecutan en equipos portátiles no deben habilitar el modo de ubicación, ya que impide que el sistema consiga la capacidad de suspensión.

 

### <a name="hybrid-sleep-s1-s3--hibernation-file"></a>Suspensión híbrida (S1-S3 + archivo de hibernación)

La *suspensión híbrida* es un estado especial que es una combinación de los Estados de suspensión e hibernación, cuando un sistema utiliza un archivo de hibernación con S1-S3. Solo está disponible en algunos sistemas. Cuando está habilitada, el sistema escribe un archivo de hibernación, pero entra en un estado de suspensión de mayor actividad. Si se pierde la alimentación mientras el sistema está en suspensión, el sistema se reactiva desde la hibernación, lo que tarda más tiempo pero restaura el estado del sistema del usuario.

## <a name="hibernate-state-s4"></a>Estado de hibernación (S4)

Windows usa la hibernación para proporcionar una experiencia de inicio rápido. Cuando está disponible, también se usa en dispositivos móviles para ampliar la duración de la batería utilizable de un sistema al ofrecer un mecanismo para guardar todo el estado del usuario antes de apagar el sistema. En una transición de hibernación, todo el contenido de la memoria se escribe en un archivo de la unidad del sistema principal, el *archivo de hibernación*. Así se conserva el estado del sistema operativo, las aplicaciones y los dispositivos. En el caso de que la superficie de memoria combinada consuma toda la memoria física, el archivo de hibernación debe ser lo suficientemente grande como para asegurarse de que habrá espacio para guardar todo el contenido de la memoria física. Puesto que los datos se escriben en un almacenamiento no volátil, DRAM no necesita mantener la auto-actualización y se puede apagar, lo que significa que el consumo de energía de la hibernación es muy bajo, casi lo mismo que el apagado.

Durante un apagado y un arranque completos (S5), toda la sesión de usuario se anula y se reinicia en el siguiente arranque. Por el contrario, durante una hibernación (S4), se cierra la sesión de usuario y se guarda el estado de usuario.

### <a name="fast-startup-reduced-hibernation-file"></a>Inicio rápido (archivo de hibernación reducido)

*Inicio rápido* es un tipo de apagado que usa un archivo de hibernación para acelerar el arranque posterior. Durante este tipo de cierre, se cierra la sesión del usuario antes de que se cree el archivo de hibernación. El inicio rápido permite un archivo de hibernación más pequeño, más adecuado para sistemas con menos capacidades de almacenamiento. Para obtener más información, vea [tipos de archivo de hibernación](#hibernation-file-types).

Cuando se usa el inicio rápido, el sistema se muestra al usuario como si se produjera un cierre completo (S5), aunque el sistema haya pasado realmente por S4. Esto incluye el modo en que el sistema responde a las alarmas de activación de dispositivos.

El inicio rápido cierra la sesión de las sesiones de usuario, pero el contenido del kernel (sesión 0) se escribe en el disco duro. Esto permite un arranque más rápido.

Para iniciar mediante programación un apagado de estilo de inicio rápido, llame a la función [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) con la marca **\_ híbrida Shutdown** o la función [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) con la marca de **\_ \_ apagado híbrido EWX** .

> [!Note]  
> A partir de Windows 8, el inicio rápido es la transición predeterminada cuando se solicita un cierre del sistema. Un cierre completo (S5) se produce cuando se solicita un reinicio del sistema (o una aplicación llama a una API de cierre).

 

### <a name="entering-hibernation"></a>Entrando en hibernación

Cuando se realiza una solicitud de hibernación, se producen los siguientes pasos cuando el sistema entra en hibernación:

1.  Se notifica a las aplicaciones y los servicios
2.  Se notifica a los controladores
3.  El estado del sistema y del usuario se guarda en el disco en un formato comprimido
4.  Se notifica al firmware

> [!Note]  
> A partir de Windows 8, todos los núcleos del sistema se utilizan para comprimir los datos en memoria y escribirlos en el disco.

 

Para iniciar mediante programación una transición de hibernación, llame a la función [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .

### <a name="resuming-from-hibernation"></a>Reanudando la hibernación

Cuando un sistema se reanuda de la hibernación.

Cuando se enciende un sistema, se producen los siguientes pasos cuando el sistema se reanuda de la hibernación.

1.  POST del sistema
2.  La memoria del sistema se descomprime y se restaura desde el archivo de hibernación
3.  Inicialización de dispositivos
4.  Los controladores se restauran al estado en que se encontraban antes de la hibernación
5.  Los servicios se restauran al estado en que se encontraban antes de la hibernación
6.  El sistema está disponible para el inicio de sesión

Una reanudación de la hibernación comienza con una publicación del sistema similar a un apagado S5. El administrador de arranque del sistema operativo determina que se requiere una reanudación de la hibernación detectando un archivo de hibernación válido. Después, dirige el sistema para que se reanude, restaure el contenido de la memoria y todos los registros arquitectónicos. En el caso de una reanudación de la hibernación, el contenido de la memoria del sistema se vuelve a leer desde el disco, se descomprime y se restaura, lo que pone al sistema en el estado exacto en el que se encontraba cuando se hibernaba. Una vez restaurada la memoria, los dispositivos se vuelven a iniciar, el equipo vuelve a un estado de ejecución listo para el inicio de sesión.

> [!Note]  
> Durante una reanudación de la hibernación, se notifica a los controladores y servicios, pero no se reinician. Solo se restauran al estado en que se encontraban antes de la hibernación.

 

### <a name="hibernation-file-types"></a>Tipos de archivos de hibernación

Los archivos de hibernación se usan para la suspensión híbrida, el inicio rápido y la hibernación estándar (descrita anteriormente). Hay dos tipos, diferenciados por tamaño, un archivo de hibernación de tamaño completo y reducido. Solo el inicio rápido puede usar un archivo de hibernación reducido.



| Tipo de archivo de hibernación | Tamaño predeterminado           | Admite...                           |
|-----------------------|------------------------|---------------------------------------|
| Completo                  | 40% de la memoria física | hibernación, suspensión híbrida, Inicio rápido |
| Reduci               | 20% de la memoria física | Inicio rápido                          |



 

Para comprobar o cambiar el tipo de archivo de hibernación utilizado, ejecute la utilidad **powercfg.exe** . En los siguientes ejemplos se muestra cómo. Para más información, vea `powercfg /? hibernate`.



|                                                                         |                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ejemplo                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                        |
| `powercfg /a`<br/>                                                | **Compruebe el tipo de archivo de hibernación.** Cuando se usa un archivo de hibernación completa, el estado de los resultados es una opción disponible. Cuando se usa un archivo de hibernación reducido, los resultados indicarán que no se admite la hibernación. Si el sistema no tiene ningún archivo de hibernación, los resultados indicarán que no se ha habilitado la hibernación.<br/> |
| `powercfg /h /type full`<br/>                                     | **Cambie el tipo de archivo de hibernación a completo.** Esto no se recomienda en sistemas con menos de 32 GB de almacenamiento.<br/>                                                                                                                                                                                                                        |
| `powercfg /h /type reduced`<br/>                                  | **Cambie el tipo de archivo de hibernación a reducido.** Si el comando devuelve "el parámetro es incorrecto", vea el ejemplo siguiente.<br/>                                                                                                                                                                                                        |
| `powercfg /h /size 0`<br/> `powercfg /h /type reduced`<br/> | **Vuelva a intentar cambiar el tipo de archivo de hibernación a reducido.** Si el archivo de hibernación se establece en un tamaño personalizado superior al 40%, primero debe establecer el tamaño del archivo en cero. A continuación, vuelva a intentar la configuración reducida.<br/>                                                                                                                       |



 

## <a name="soft-off-state-s5"></a>Estado débil (S5)

El estado débil es cuando el sistema se cierra por completo sin un archivo de hibernación. Soft off también se conoce como "apagado completo". Durante un apagado y un arranque completos, toda la sesión de usuario se anula y se reinicia en el siguiente arranque. Por lo tanto, un arranque o inicio desde este estado tarda mucho más tiempo que S1-S4. Un cierre completo (S5) se produce cuando se solicita un reinicio del sistema (o una aplicación llama a una API de cierre).

## <a name="mechanical-off-state-g3"></a>Estado mecánico (G3)

En este estado, el sistema está completamente apagado y no consume energía. El sistema vuelve al estado de funcionamiento solo después de un reinicio completo.

## <a name="wake-on-lan-behavior"></a>Comportamiento de Wake on LAN

La característica Wake-on-LAN (WOL) activa el equipo desde un estado de baja energía cuando un adaptador de red detecta un evento WOL (normalmente, un paquete Ethernet especialmente construido).

WOL es compatible con Sleep (S3) o Hibernate (S4). No se admite en Estados de cierre de inicio rápido o débil (S5). Las NIC no están preparadas para la reactivación en estos Estados porque los usuarios no esperan que sus sistemas se reactiven por sí solos.

> [!Note]  
> WOL no es compatible oficialmente con Soft off (S5). Sin embargo, es posible que el BIOS de algunos sistemas admita NIC Arming para Wake, aunque Windows no esté implicado en el proceso.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> </dl>
