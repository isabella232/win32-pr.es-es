---
title: Directivas de grupo
description: Servicio de transferencia inteligente en segundo plano (BITS) utiliza las siguientes directivas de grupo para configurar las transferencias de BITS y la configuración. Para obtener más información sobre qué versión de BITS se usa en diferentes versiones de Windows, vea el tema Novedades.
ms.assetid: 32c7e2b1-bac2-4708-a30c-f6b2a816c1a4
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: f3ff0070c489759055bdaae1d2e68d8718a7bae5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268323"
---
# <a name="group-policies"></a>Directivas de grupo

> [!NOTE]
> Para obtener más información acerca de cómo usar la administración de dispositivos móviles (MDM) para establecer directivas para Servicio de transferencia inteligente en segundo plano (BITS), consulte [Directiva de CSP](/windows/client-management/mdm/policy-configuration-service-provider).

Servicio de transferencia inteligente en segundo plano (BITS) utiliza las siguientes directivas de grupo para configurar las transferencias de BITS y la configuración. Para obtener más información sobre qué versión de BITS se usa en diferentes versiones de Windows, vea el tema [novedades](what-s-new.md) .

> [!NOTE]  
> Si no se establece el valor de la Directiva, BITS usa el valor predeterminado de la Directiva.

**Para habilitar una directiva de BITS**

1.  Abra directiva de grupo escribiendo **gpedit. msc/gpcomputer: "***ComputerName***"** en la ventana de **ejecución** o en el símbolo del sistema en una ventana de cmd.
2.  Las directivas de BITS se encuentran en **configuración del equipo**, **Plantillas administrativas**, **red** **servicio de transferencia inteligente en segundo plano**.
3.  Haga clic con el botón derecho en la Directiva y seleccione **Editar**.
4.  Siga las instrucciones para habilitar y establecer la Directiva.

Las directivas de grupo para bits se encuentran en el registro en **HKEY \_ local \_ Machine** \\ **software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **bits**. Tenga en cuenta que solo las directivas configuradas se enumeran en el registro.

|Directiva|Descripción|
|-|-|
|Valor jobinactivitytimeout<br/>BITS 1,0|De forma predeterminada, BITS mantiene información sobre un trabajo durante 90 días. Si no hay ninguna actividad en el trabajo durante este período de tiempo, BITS cancela el trabajo. El progreso de la transferencia o los cambios de propiedad restablecen el temporizador.<br/> Es posible que tenga que ajustar esta Directiva si el usuario no inicia sesión o mantiene una conexión de red durante largos períodos de tiempo.|
|MaxInternetBandwidth<br/>BITS 2,0|Limita el ancho de banda de red que usa BITS para las transferencias en segundo plano (esta Directiva no afecta a las transferencias en primer plano).<br/>Especifique el límite que se va a usar durante un intervalo de tiempo específico y un límite que se usará en el resto de los casos. Por ejemplo, limite el uso de ancho de banda de red a 10 kilobits por segundo (kbps) de 8:00 A.M. a 5:00 P.M. y usar todo el ancho de banda sin usar disponible el resto del tiempo.<br/>**Nota**: al cambiar el reloj del sistema no se ve afectado el intervalo de tiempo límite de ancho de banda. Por ejemplo, si la hora actual es 2:00 P.M. y el intervalo de limitación de ancho de banda comienza a las 3:00 P.M., el movimiento del reloj del sistema una hora no significa que BITS aplique el límite de ancho de banda una hora antes de que se produzca la limitación de ancho de banda en una hora. Para reflejar el cambio de reloj del sistema en BITS, debe reiniciar el equipo o el servicio BITS.<br/>Especifique el límite en kilobits por segundo. Base el límite del tamaño del vínculo de red, no el tamaño de la tarjeta de interfaz de red (NIC) del equipo. BITS usa aproximadamente dos kilobits si especifica un valor inferior a dos kilobits. Para evitar que se produzcan transferencias de BITS, especifique un límite de cero. Si especifica un límite de cero, BITS coloca todos los trabajos en segundo plano en un estado de error transitorio. (El código de error se establece en BG_E_BLOCKED_BY_POLICY). BITS coloca los trabajos en el estado en cola después de que expire el intervalo de tiempo.<br/> Si deshabilita o no configura esta Directiva, BITS usa todo el ancho de banda sin usar disponible.<br/> Normalmente, esta Directiva se usa para evitar que las transferencias de BITS compitan por el ancho de banda de red cuando el cliente tiene un adaptador de red rápido (10 Mbps) pero está conectado a la red a través de un vínculo de baja velocidad (56 kbps).<br/> Para obtener información sobre cómo usa BITS el ancho de banda de red, consulte ancho de banda de [red](network-bandwidth.md).|
|MaxDownloadTime<br/>BITS 3,0|Determina el período de tiempo que BITS puede gastar en transferir activamente los archivos del trabajo. El valor predeterminado es de 90 días.<br/> Para invalidar esta directiva para un trabajo específico, llame al método [**IBackgroundCopyJob4:: SetMaximumDownloadTime**](/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setmaximumdownloadtime) .|
|MaxJobsPerMachine<br/>BITS 3,0|Limita el número de trabajos que pueden crear los usuarios en el equipo. El valor predeterminado es 300 trabajos. Esta Directiva no se aplica a un usuario con privilegios de administrador o cuentas de servicio.|
|MaxJobsPerUser<br/>BITS 3,0|Limita el número de trabajos que un usuario puede crear en el equipo. El valor predeterminado es 60 trabajos por usuario. Esta Directiva no se aplica a un usuario con privilegios de administrador o cuentas de servicio.|
|MaxFilesPerJob<br/>BITS 3,0|Limita el número de archivos que puede Agregar un usuario a un trabajo. El valor predeterminado es 200 archivos por trabajo. Esta Directiva no se aplica a un usuario con privilegios de administrador o cuentas de servicio.|
|MaxRangesPerFile<br/>BITS 3,0|Limita el número de intervalos que un usuario puede especificar para un archivo. El valor predeterminado es 500 intervalos. Esta Directiva no se aplica a un usuario con privilegios de administrador o cuentas de servicio.|

BITS usa las siguientes directivas de grupo para habilitar y configurar cómo interactúa BITS con BranchCache.

|Directiva|Descripción|
|-|-|
|DisableBranchCache<br/>BITS 4,0|De forma predeterminada, la característica Windows BranchCache está habilitada. Establezca esta directiva para evitar que los clientes de BITS transfieran contenido mediante Windows BranchCache.<br/>**Nota**: esta configuración no afecta al uso de Windows BranchCache por parte de aplicaciones que no sean bits. Esta Directiva no se aplica a las transferencias de BITS a través del bloque de mensajes del servidor (SMB). Esta configuración no tiene ningún efecto si la configuración administrativa del equipo para la caché de rama de Windows deshabilita su uso por completo.|

BITS usa las siguientes directivas de grupo para configurar el límite de ancho de banda.

|Directiva|Descripción|
|-|-|
|EnableMaintenanceLimits<br/>BITS 4,0|Limita el ancho de banda de red que usa BITS para las transferencias en segundo plano durante los días y las horas de mantenimiento. La programación de mantenimiento limita aún más el ancho de banda de red que se usa para las transferencias en segundo plano.<br/> Especifique un límite que se usará para los trabajos en segundo plano durante una programación de mantenimiento. Por ejemplo, si los trabajos de prioridad normal están limitados actualmente a 256 kbps en una programación de trabajo, puede limitar aún más el ancho de banda de red de los trabajos de prioridad normal a 0 Kbps de 8:00 A.M. a 10:00 a.m. en una programación de mantenimiento.<br/>**Nota**: los límites de ancho de banda que se establecen para el período de mantenimiento sustituyen a los límites definidos para el trabajo y otras programaciones.|
|EnableBandwidthLimits<br/>BITS 4,0|Limita el ancho de banda de red que usa BITS para las transferencias en segundo plano durante las horas y los días laborables y no laborables. La programación de trabajo se define mediante un calendario semanal, que consta de los días de la semana y las horas del día. Todas las horas y los días que no estén definidos en una programación de trabajo se consideran horas de descanso.<br/> Especifique un límite que se usará para los trabajos en segundo plano durante una programación de trabajo. Por ejemplo, puede limitar el ancho de banda de red de los trabajos de baja prioridad a 128 kbps desde 8:00 A.M. a 5:00 P.M. de lunes a viernes y, a continuación, establezca el límite en 512 Kbps para las horas no laborables.|


## <a name="related-topics"></a>Temas relacionados
* [Policy CSP](/windows/client-management/mdm/policy-configuration-service-provider)
