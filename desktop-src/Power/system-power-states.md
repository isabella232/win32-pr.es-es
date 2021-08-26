---
description: Para el usuario, el sistema parece estar on o off.
ms.assetid: 3d897a88-125e-457f-9ea7-ac2056b0767a
title: Estados de energía del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eb93931326b67c7469b6a8ae256892e2dd77d4b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469912"
---
# <a name="system-power-states"></a>Estados de energía del sistema

Para el usuario, el sistema parece estar on o off. No hay ningún otro estado detectable. Sin embargo, el sistema admite varios estados de energía que se corresponden con los estados de energía definidos en la especificación Interfaz avanzada de configuración y energía (ACPI). También hay variaciones de estos estados, como la suspensión híbrida y el inicio rápido. En este tema se presentan estos estados y se describe cómo se relacionan entre sí.

> [!NOTE]
> Los integradores del sistema y los desarrolladores que crean controladores o aplicaciones con un servicio del sistema deben tener especial cuidado con los problemas de calidad del controlador, como las pérdidas de memoria. Aunque la calidad del controlador siempre ha sido importante, el tiempo de espera entre los reinicios del kernel puede ser significativamente más largo que en versiones anteriores del sistema operativo porque, en los tiempos de suspensión y apagado iniciados por el usuario, el kernel, los controladores y los servicios se conservarán y restaurarán, no se volverán a iniciar.

 

En la tabla siguiente se enumeran los estados de energía ACPI de mayor a menor consumo de energía.




| Estado de energía | Estado ACPI | Descripción | 
|-------------|------------|-------------|
| En funcionamiento<br /> | S0<br /> | El sistema es totalmente utilizable. Los componentes de hardware que no están en uso pueden ahorrar energía si entran en un estado de energía inferior.<br /> | 
| En reposo<br /> (Espera moderna)<br /> | S0 de bajo consumo de energía inactiva<br /> | Algunos sistemas SoC admiten un estado de inactividad de bajo consumo conocido como <a href="/windows-hardware/design/device-experiences/modern-standby">espera moderna.</a> En este estado, el sistema puede cambiar rápidamente de un estado de bajo consumo a un estado de alta energía, de modo que pueda responder rápidamente a eventos de hardware y red. Los sistemas que admiten el modo de espera moderno no usan S1-S3.<br /> | 
| En reposo<br /> | S1<br /> S2<br /> S3<br /> | Parece que el sistema está desactivado. La energía consumida en estos estados (S1-S3) es menor que S0 y más de S4; S3 consume menos energía que S2 y S2 consume menos energía que S1. Normalmente, los sistemas admiten uno de estos tres estados, no los tres.<br /> En estos estados (S1-S3), la memoria volátil se mantiene actualizado para mantener el estado del sistema. Algunos componentes permanecen encendidos para que el equipo pueda reactivar desde la entrada del teclado, la LAN o un dispositivo USB.<br /><em>La suspensión</em>híbrida, que se usa en los escritorios, es donde un sistema usa un archivo de hibernación con S1-S3. El archivo de hibernación guarda el estado del sistema en caso de que el sistema pierda energía mientras está en suspensión.<br /><blockquote>[!Note]<br />Los sistemas SoC que admiten el modo de espera moderno (el estado de inactividad de bajo consumo) no usan S1-S3.</blockquote><br /><br /> | 
| Hibernar<br /> | S4<br /> | Parece que el sistema está desactivado. El consumo de energía se reduce al nivel más bajo. El sistema guarda el contenido de la memoria volátil en un archivo de hibernación para conservar el estado del sistema. Algunos componentes permanecen encendidos para que el equipo pueda reactivar desde la entrada del teclado, la LAN o un dispositivo USB. El contexto de trabajo se puede restaurar si se almacena en medios no volátiles. <br /><em>El inicio rápido</em> es donde el usuario ha cerrado la sesión antes de crear el archivo de hibernación. Esto permite un archivo de hibernación más pequeño, más adecuado para sistemas con menos capacidades de almacenamiento.<br /> | 
| Soft Off<br /> | S5<br /> | Parece que el sistema está desactivado. Este estado se compone de un ciclo completo de apagado y arranque.<br /> | 
| Apagado mecánico<br /> | G3<br /> | El sistema está completamente apagado y no consume energía. El sistema vuelve al estado de funcionamiento solo después de un reinicio completo.<br /> | 




 

La [**\_ enumeración SYSTEM POWER \_ STATE**](/windows/desktop/api/WinNT/ne-winnt-system_power_state) define los valores que se usan para especificar los estados de energía del sistema.

## <a name="working-state-s0"></a>Estado de trabajo (S0)

Durante el estado de funcionamiento, el sistema está activo y en ejecución. En términos simples, el dispositivo está "on". Independientemente de si la pantalla está o no, el dispositivo se encuentra en un estado de ejecución completo. Para ahorrar energía, especialmente en dispositivos con batería, se recomienda encarecidamente encender los componentes de hardware cuando no se usan.

> [!IMPORTANT]
> Apague los componentes de hardware siempre que no se utilicen, independientemente del estado. El bajo consumo de energía es una consideración importante para los consumidores de dispositivos móviles.

 

## <a name="sleep-state-modern-standby"></a>Estado de suspensión (espera moderna)

En el modo inactivo de bajo consumo S0 del estado de trabajo, también conocido como espera [moderna,](/windows-hardware/design/device-experiences/modern-standby)el sistema permanece parcialmente en ejecución. Durante el modo de espera moderno, el sistema puede mantenerse actualizado siempre que haya disponible una red adecuada y también reactivar cuando se requiera una acción en tiempo real, como el mantenimiento del sistema operativo. El modo de espera moderno se reactiva significativamente más rápido que S1-S3. Para obtener más información, vea [Modern Standby](/windows-hardware/design/device-experiences/modern-standby).

> [!Note]  
> El modo de espera moderno solo está disponible en algunos sistemas SoC. Cuando se admite, el sistema no admite S1-S3.

 

## <a name="sleep-state-s1-s3"></a>Estado de suspensión (S1-S3)

El sistema entra en suspensión en función de una serie de criterios, incluida la actividad del usuario o la aplicación y las preferencias que el usuario establece en la página de suspensión de **Power &** de la **Configuración** aplicación. De forma predeterminada, el sistema usa el estado de suspensión de menor potencia compatible con todos los dispositivos de reactivación habilitados. Para obtener más información sobre cómo el sistema determina cuándo entrar en suspensión, vea [Criterios de suspensión del sistema](system-sleep-criteria.md).

Antes de que el sistema entre en suspensión, determina el estado de suspensión adecuado, notifica a las aplicaciones y los controladores la transición pendiente y, a continuación, pasa el sistema al estado de suspensión. En el caso de una transición crítica, como cuando se alcanza el umbral de batería crítico, el sistema no notifica a las aplicaciones ni a los controladores. Las aplicaciones deben estar preparadas para esto y realizar la acción adecuada cuando el sistema vuelva al estado de funcionamiento.

En estos estados (S1-S3), la memoria volátil se mantiene actualizado para mantener el estado del sistema. Algunos componentes permanecen encendidos para que el equipo pueda reactivar desde la entrada del teclado, la LAN o un dispositivo USB.

El sistema también se reactiva de la suspensión en respuesta a la actividad del usuario o a un evento de reactivación definido por una aplicación. Para obtener más información, vea [Eventos de reactivación del sistema.](system-wake-up-events.md) La cantidad de tiempo que tarda el sistema en reactivarse depende del estado de suspensión desde el que se está reactivando. El sistema tarda más tiempo en reactivarse desde un estado de menor potencia (S3) que desde un estado de mayor potencia (S1) debido al trabajo adicional que puede tener que hacer el hardware (estabilizar la fuente de alimentación, reinicializar el procesador, etc.).

> [!Caution]  
> Al llamar a [**SetThreadExecutionState,**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate)el valor **ES \_ AWAYMODE \_ REQUIRED** solo debe usarse cuando sea absolutamente necesario para las aplicaciones multimedia que requieren que el sistema realice tareas en segundo plano, como grabar contenido de televisión o transmitir contenido multimedia a otros dispositivos mientras el sistema parece estar en modo de inmoción. Las aplicaciones que no requieren un procesamiento en segundo plano crítico o que se ejecutan en equipos portátiles no deben habilitar el modo de salida porque impide que el sistema conserve energía al entrar en suspensión verdadera.

 

### <a name="hybrid-sleep-s1-s3--hibernation-file"></a>Suspensión híbrida (S1-S3 + archivo de hibernación)

*La suspensión* híbrida es un estado especial que es una combinación de los estados de suspensión e hibernación, es cuando un sistema usa un archivo de hibernación con S1-S3. Solo está disponible en algunos sistemas. Cuando se habilita, el sistema escribe un archivo de hibernación, pero entra en un estado de suspensión de mayor potencia. Si se pierde energía mientras el sistema está en suspensión, el sistema se reactiva de la hibernación, lo que tarda más tiempo, pero restaura el estado del sistema del usuario.

## <a name="hibernate-state-s4"></a>Estado de hibernación (S4)

Windows utiliza la hibernación para proporcionar una experiencia de inicio rápido. Cuando está disponible, también se usa en dispositivos móviles para ampliar la duración útil de la batería de un sistema, ya que proporciona un mecanismo para guardar todo el estado del usuario antes de apagar el sistema. En una transición de hibernación, todo el contenido de la memoria se escribe en un archivo en la unidad del sistema principal, el *archivo de hibernación*. Esto conserva el estado del sistema operativo, las aplicaciones y los dispositivos. En el caso de que la superficie de memoria combinada consuma toda la memoria física, el archivo de hibernación debe ser lo suficientemente grande como para asegurarse de que habrá espacio para guardar todo el contenido de la memoria física. Puesto que los datos se escriben en un almacenamiento no volátil, DRAM no necesita mantener la actualización automática y se puede apagar, lo que significa que el consumo de energía de hibernación es muy bajo, casi igual que el apagado.

Durante un apagado y arranque completos (S5), toda la sesión de usuario se cierra y se reinicia en el siguiente arranque. Por el contrario, durante una hibernación (S4), la sesión del usuario se cierra y se guarda el estado de usuario.

### <a name="fast-startup-reduced-hibernation-file"></a>Inicio rápido (archivo de hibernación reducido)

*El inicio rápido* es un tipo de apagado que usa un archivo de hibernación para acelerar el arranque posterior. Durante este tipo de apagado, el usuario se cierra antes de crear el archivo de hibernación. El inicio rápido permite un archivo de hibernación más pequeño, más adecuado para los sistemas con menos funcionalidades de almacenamiento. Para obtener más información, vea [Tipos de archivo de hibernación.](#hibernation-file-types)

Cuando se usa el inicio rápido, el sistema aparece al usuario como si se hubiera producido un apagado completo (S5), aunque el sistema haya pasado realmente por S4. Esto incluye cómo responde el sistema a las alarmas de reactivación del dispositivo.

El inicio rápido cierra las sesiones de usuario, pero el contenido del kernel (sesión 0) se escribe en el disco duro. Esto permite un arranque más rápido.

Para iniciar mediante programación un cierre de estilo de inicio rápido, llame a la función [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) con la marca **SHUTDOWN \_ HYBRID** o la función [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) con la marca **EWX \_ HYBRID \_ SHUTDOWN.**

> [!Note]  
> A partir Windows 8, el inicio rápido es la transición predeterminada cuando se solicita un apagado del sistema. Se produce un apagado completo (S5) cuando se solicita un reinicio del sistema (o una aplicación llama a una API de apagado).

 

### <a name="entering-hibernation"></a>Entrar en hibernación

Cuando se realiza una solicitud de hibernación, se producen los pasos siguientes a medida que el sistema entra en hibernación:

1.  Se notifica a las aplicaciones y servicios
2.  Se notifica a los controladores
3.  El estado del usuario y del sistema se guarda en el disco en un formato comprimido
4.  Se notifica el firmware

> [!Note]  
> A partir Windows 8, todos los núcleos del sistema se usan para comprimir los datos en memoria y escribir en el disco.

 

Para iniciar una transición de hibernación mediante programación, llame a la [**función SetSuspendState.**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate)

### <a name="resuming-from-hibernation"></a>Reanudación de la hibernación

Cuando un sistema se reanuda desde la hibernación.

Cuando un sistema está encendido, se producen los pasos siguientes a medida que el sistema se reanuda desde la hibernación.

1.  Post del sistema
2.  La memoria del sistema se descomprime y restaura desde el archivo de hibernación.
3.  Inicialización de dispositivos
4.  Los controladores se restauran al estado en que se encontraban antes de la hibernación
5.  Los servicios se restauran al estado en que estaban antes de la hibernación
6.  El sistema está disponible para el inicio de sesión

Una reanudación desde la hibernación comienza con un POST del sistema que es similar a un cierre S5. El administrador de arranque del sistema operativo determina que se requiere una reanudación desde la hibernación mediante la detección de un archivo de hibernación válido. A continuación, hace que el sistema se reanude, restaurando el contenido de la memoria y todos los registros arquitectónicos. En el caso de un reanudación desde la hibernación, el contenido de la memoria del sistema se leen desde el disco, se descomprimen y se restauran, lo que coloca el sistema en el estado exacto en el que estaba cuando estaba hibernado. Una vez restaurada la memoria, los dispositivos se vuelven a iniciar y la máquina vuelve a un estado en ejecución, listo para el inicio de sesión.

> [!Note]  
> Durante una reanudación desde la hibernación, se notifica a los controladores y servicios, pero no se reinician. Solo se restauran al estado en el que estaban antes de la hibernación.

 

### <a name="hibernation-file-types"></a>Tipos de archivo de hibernación

Los archivos de hibernación se usan para la suspensión híbrida, el inicio rápido y la hibernación estándar (descrita anteriormente). Hay dos tipos, diferenciados por tamaño, un archivo de hibernación de tamaño completo y reducido. Solo el inicio rápido puede usar un archivo de hibernación reducido.



| Tipo de archivo hibernación | Tamaño predeterminado           | Soporta...                           |
|-----------------------|------------------------|---------------------------------------|
| Completo                  | 40 % de la memoria física | hibernate, suspensión híbrida, inicio rápido |
| Reducido               | 20 % de memoria física | inicio rápido                          |



 

Para comprobar o cambiar el tipo de archivo de hibernación utilizado, ejecute la **powercfg.exe** de estado. En los ejemplos siguientes se muestra cómo. Para más información, vea `powercfg /? hibernate`.



| Ejemplo                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `powercfg /a`<br/>                                                | **Compruebe el tipo de archivo de hibernación.** Cuando se usa un archivo de hibernación completo, los resultados muestran que la hibernación es una opción disponible. Cuando se usa un archivo de hibernación reducido, los resultados dirán que no se admite la hibernación. Si el sistema no tiene ningún archivo de hibernación, los resultados dirán que no se ha habilitado la hibernación.<br/> |
| `powercfg /h /type full`<br/>                                     | **Cambie el tipo de archivo de hibernación a completo.** Esto no se recomienda en sistemas con menos de 32 GB de almacenamiento.<br/>                                                                                                                                                                                                                        |
| `powercfg /h /type reduced`<br/>                                  | **Cambie el tipo de archivo de hibernación a reducido.** Si el comando devuelve "el parámetro es incorrecto", vea el ejemplo siguiente.<br/>                                                                                                                                                                                                        |
| `powercfg /h /size 0`<br/> `powercfg /h /type reduced`<br/> | **Vuelva a intentar cambiar el tipo de archivo de hibernación a reducido.** Si el archivo de hibernación se establece en un tamaño personalizado superior al 40 %, primero debe establecer el tamaño del archivo en cero. A continuación, vuelva a intentar la configuración reducida.<br/>                                                                                                                       |



 

## <a name="soft-off-state-s5"></a>Estado de apagado flexible (S5)

El estado de suspensión es cuando el sistema se apaga completamente sin un archivo de hibernación. El apagado temporal también se conoce como "apagado completo". Durante un apagado y arranque completos, toda la sesión de usuario se despedía y se reiniciaba en el siguiente arranque. Por lo tanto, un arranque o inicio desde este estado tarda mucho más que S1-S4. Se produce un apagado completo (S5) cuando se solicita un reinicio del sistema (o una aplicación llama a una API de apagado).

## <a name="mechanical-off-state-g3"></a>Estado de apagado mecánico (G3)

En este estado, el sistema está completamente apagado y no consume energía. El sistema vuelve al estado de funcionamiento solo después de un reinicio completo.

## <a name="wake-on-lan-behavior"></a>Comportamiento de Wake-on-LAN

La característica wake-on-LAN (LAN) reactiva el equipo desde un estado de bajo consumo cuando un adaptador de red detecta un evento DESEMP (normalmente, un paquete Ethernet construido especialmente).

SE ADMITEN DESDE suspensión (S3) o hibernación (S4). No se admite desde los estados de inicio rápido o apagado temporal (S5). Las NIC no están a la espera de reactivación en estos estados porque los usuarios no esperan que sus sistemas se reactivan por sí mismos.

> [!Note]  
> NO se admite oficialmente DESDE la salida flexible (S5). Sin embargo, el BIOS en algunos sistemas puede admitir el uso de NIC para la reactivación, aunque Windows no esté implicado en el proceso.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> </dl>
