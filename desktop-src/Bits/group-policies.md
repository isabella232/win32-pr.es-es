---
title: Directivas de grupo
description: Servicio de transferencia inteligente en segundo plano (BITS) usa las siguientes directivas de grupo para configurar las transferencias y las opciones de BITS. Para obtener más información sobre la versión de BITS que usan las distintas versiones de Windows, vea el tema Novedades.
ms.assetid: 32c7e2b1-bac2-4708-a30c-f6b2a816c1a4
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: f3ff0070c489759055bdaae1d2e68d8718a7bae5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361490"
---
# <a name="group-policies"></a>Directivas de grupo

> [!NOTE]
> Para obtener más información sobre cómo usar la administración de dispositivos móviles (MDM) para establecer directivas para Servicio de transferencia inteligente en segundo plano (BITS), vea [POLICY CSP](/windows/client-management/mdm/policy-configuration-service-provider).

Servicio de transferencia inteligente en segundo plano (BITS) usa las siguientes directivas de grupo para configurar las transferencias y las opciones de BITS. Para obtener más información sobre qué versión de BITS usan las distintas versiones de Windows, vea [el](what-s-new.md) tema Novedades.

> [!NOTE]  
> Si no se establece el valor de directiva, BITS usa el valor de directiva predeterminado.

**Para habilitar una directiva de BITS**

1.  Para directiva de grupo escriba **gpedit.msc /gpcomputer:"**_ComputerName_"  *_en_* la ventana Ejecutar o en el símbolo del sistema en una ventana cmd.
2.  Las directivas de BITS se encuentran en **Configuración del** **equipo , Plantillas administrativas**, **Red** **, Servicio de transferencia inteligente en segundo plano**.
3.  Haga clic con el botón derecho en la directiva y seleccione **Editar.**
4.  Siga las instrucciones para habilitar y establecer la directiva.

Las directivas de grupo para BITS se encuentran en el Registro en **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **BITS**. Tenga en cuenta que solo las directivas configuradas se muestran en el Registro.

|Directiva|Descripción|
|-|-|
|JobInactivityTimeout<br/>BITS 1.0|De forma predeterminada, BITS mantiene información sobre un trabajo durante 90 días. Si no hay ninguna actividad en el trabajo durante este período de tiempo, BITS cancela el trabajo. Los cambios de propiedad o progreso de transferencia restablecen el temporizador.<br/> Es posible que tenga que ajustar esta directiva si el usuario no inicia sesión o mantiene una conexión de red durante largos períodos de tiempo.|
|MaxInternetBandwidth<br/>BITS 2.0|Limita el ancho de banda de red que BITS usa para las transferencias en segundo plano (esta directiva no afecta a las transferencias en primer plano).<br/>Especifique un límite que se usará durante un intervalo de tiempo específico y un límite para usarlo en el resto de horas. Por ejemplo, limite el uso del ancho de banda de red a 10 kilobits por segundo (Kbps) a partir de las 8:00 a. m. a las 5:00 p. m. y usan todo el ancho de banda disponible sin usar el resto del tiempo.<br/>**Nota:** Cambiar el reloj del sistema no afecta al intervalo de tiempo de limitación de ancho de banda. Por ejemplo, si la hora actual es las 2:00 p. m. y el intervalo de limitación de ancho de banda comienza a las 3:00 p. m., mover el reloj del sistema hacia delante una hora no significa que BITS aplique la limitación de ancho de banda una hora antes de que se produzca la limitación de ancho de banda en una hora. Para reflejar el cambio de reloj del sistema en BITS, debe reiniciar el equipo o el servicio BITS.<br/>Especifique el límite en kilobits por segundo. Base el límite en el tamaño del vínculo de red, no en el tamaño de la tarjeta de interfaz de red (NIC) del equipo. BITS usa aproximadamente dos kilobits si especifica un valor inferior a dos kilobits. Para evitar que se produzcan transferencias de BITS, especifique un límite de cero. Si especifica un límite de cero, BITS coloca todos los trabajos en segundo plano en un estado de error transitorio. (El código de error se establece en BG_E_BLOCKED_BY_POLICY). BITS coloca los trabajos en el estado en cola después de que expire el intervalo de tiempo.<br/> Si deshabilita o no configura esta directiva, BITS usa todo el ancho de banda disponible sin usar.<br/> Normalmente, se usa esta directiva para evitar que las transferencias BITS compitiendo por el ancho de banda de red cuando el cliente tiene un adaptador de red rápido (10 Mbps), pero está conectado a la red a través de un vínculo lento (56 Kbps).<br/> Para obtener información sobre cómo BITS usa el ancho de banda de red, vea [Ancho de banda de red.](network-bandwidth.md)|
|MaxDownloadTime<br/>BITS 3.0|Determina el tiempo que BITS puede dedicar activamente a transferir los archivos en el trabajo. El valor predeterminado es de 90 días.<br/> Para invalidar esta directiva para un trabajo específico, llame al método [**IBackgroundCopyJob4::SetMaximumDownloadTime.**](/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setmaximumdownloadtime)|
|MaxJobsPerMachine<br/>BITS 3.0|Limita el número de trabajos que los usuarios pueden crear en el equipo. El valor predeterminado es 300 trabajos. Esta directiva no se aplica a un usuario con privilegios de administrador o cuentas de servicio.|
|MaxJobsPerUser<br/>BITS 3.0|Limita el número de trabajos que un usuario puede crear en el equipo. El valor predeterminado es 60 trabajos por usuario. Esta directiva no se aplica a un usuario con privilegios de administrador o cuentas de servicio.|
|MaxFilesPerJob<br/>BITS 3.0|Limita el número de archivos que un usuario puede agregar a un trabajo. El valor predeterminado es 200 archivos por trabajo. Esta directiva no se aplica a un usuario con privilegios de administrador o cuentas de servicio.|
|MaxRangesPerFile<br/>BITS 3.0|Limita el número de intervalos que un usuario puede especificar para un archivo. El valor predeterminado es 500 intervalos. Esta directiva no se aplica a un usuario con privilegios de administrador o cuentas de servicio.|

BITS usa las siguientes directivas de grupo para habilitar y configurar cómo bits interactúa con BranchCache.

|Directiva|Descripción|
|-|-|
|DisableBranchCache<br/>BITS 4.0|De forma predeterminada, la Windows BranchCache está habilitada. Establezca esta directiva para evitar que los clientes bits transfieran contenido mediante Windows BranchCache.<br/>**Nota:** Esta configuración no afecta al uso de Windows BranchCache por aplicaciones que no son BITS. Esta directiva no se aplica a las transferencias de BITS a través del Bloque de mensajes del servidor (SMB). Esta configuración no tiene ningún efecto si la configuración administrativa del equipo para Windows Branch Cache deshabilita completamente su uso.|

BITS usa las siguientes directivas de grupo para configurar la limitación de ancho de banda.

|Directiva|Descripción|
|-|-|
|EnableMaintenanceLimits<br/>BITS 4.0|Limita el ancho de banda de red que BITS usa para las transferencias en segundo plano durante los días y horas de mantenimiento. Las programaciones de mantenimiento limitan aún más el ancho de banda de red que se usa para las transferencias en segundo plano.<br/> Especifique un límite que se usará para los trabajos en segundo plano durante una programación de mantenimiento. Por ejemplo, si los trabajos de prioridad normal están limitados actualmente a 256 Kbps según una programación de trabajo, puede limitar aún más el ancho de banda de red de los trabajos de prioridad normal a 0 Kbps desde las 8:00 a. m. a 10:00 a.m. según una programación de mantenimiento.<br/>**Nota:** Los límites de ancho de banda que se establecen para el período de mantenimiento reemplazan a los límites definidos para el trabajo y otras programaciones.|
|EnableBandwidthLimits<br/>BITS 4.0|Limita el ancho de banda de red que BITS usa para las transferencias en segundo plano durante los días y horas de trabajo y no laborables. La programación de trabajo se define mediante un calendario semanal, que consta de días de la semana y horas del día. Todas las horas y días que no están definidos en una programación de trabajo se consideran horas no laborables.<br/> Especifique un límite que se usará para los trabajos en segundo plano durante una programación de trabajo. Por ejemplo, puede limitar el ancho de banda de red de los trabajos de prioridad baja a 128 Kbps a partir de las 8:00 a. m. a las 5:00 p. m. de lunes a viernes y, a continuación, establezca el límite en 512 Kbps para las horas que no son de trabajo.|


## <a name="related-topics"></a>Temas relacionados
* [Policy CSP](/windows/client-management/mdm/policy-configuration-service-provider)
