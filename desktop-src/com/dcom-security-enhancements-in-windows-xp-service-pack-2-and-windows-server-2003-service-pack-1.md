---
title: Mejoras de seguridad de DCOM en Windows XP Service Pack 2 y Windows Server 2003 Service Pack 1
description: Windows Server XP Service Pack 2 (SP2) y Windows Server 2003 Service Pack 1 (SP1) presentan una configuración de seguridad predeterminada mejorada para el Modelo de objetos de componente distribuido (DCOM).
ms.assetid: 1917834c-5216-4ef3-a0c2-d8ca63cef53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d093186f3d0a028112248409b71e0d71ed084e15cc075a1aced7a589aa0733ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501335"
---
# <a name="dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>Mejoras de seguridad de DCOM en Windows XP Service Pack 2 y Windows Server 2003 Service Pack 1

Windows Server XP Service Pack 2 (SP2) y Windows Server 2003 Service Pack 1 (SP1) presentan una configuración de seguridad predeterminada mejorada para el Modelo de objetos de componente distribuido (DCOM). En concreto, presentan derechos más pormenorizados que permiten a un administrador tener un control independiente sobre los permisos locales y remotos para iniciar, activar y acceder a servidores COM.

## <a name="what-does-dcom-do"></a>¿Qué hace DCOM?

Microsoft Component Object Model (COM) es un sistema orientado a objetos, distribuido e independiente de la plataforma para crear componentes de software binarios que pueden interactuar. El Modelo de objetos componentes distribuidos (DCOM) permite que las aplicaciones se distribuyen entre ubicaciones que más le conste y a la aplicación. El protocolo de conexión DCOM proporciona de forma transparente compatibilidad para una comunicación confiable, segura y eficaz entre componentes COM.

## <a name="who-does-this-feature-apply-to"></a>¿A quién se aplica esta característica?

Si usa COM solo para componentes COM en proceso, esta característica no se aplica a usted.

Esta característica se aplica a usted si tiene una aplicación de servidor COM que cumple uno de los siguientes criterios:

-   El permiso de acceso para la aplicación es menos estricto que el permiso de inicio, que es necesario para ejecutar la aplicación.
-   Normalmente, un cliente COM remoto activa la aplicación sin usar una cuenta administrativa.
-   La aplicación está pensada para usarse solo localmente. Esto significa que puede restringir la aplicación de servidor COM para que no sea accesible de forma remota.

## <a name="what-new-functionality-is-added-to-this-feature-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>¿Qué funcionalidad nueva se agrega a esta característica en Windows XP Service Pack 2 y Windows Server 2003 Service Pack 1?

### <a name="computer-wide-restrictions"></a>Restricciones de todo el equipo

Se ha realizado un cambio en COM para proporcionar controles de acceso a todo el equipo que rigen el acceso a todas las solicitudes de llamada, activación o inicio en el equipo. La manera más sencilla de pensar en estos controles de acceso es como una llamada [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) adicional que se realiza en una lista de control de acceso (ACL) de todo el equipo en cada llamada, activación o inicio de cualquier servidor COM en el equipo. Si se **produce un error en AccessCheck,** se deniega la llamada, la activación o la solicitud de inicio. Esto se suma a cualquier **AccessCheck que** se ejecute en las ACL específicas del servidor. En efecto, proporciona un estándar de autorización mínimo que se debe pasar para tener acceso a cualquier servidor COM del equipo. Hay una ACL de todo el equipo para los permisos de inicio para cubrir los derechos de activación e inicio, y una ACL de todo el equipo para los permisos de acceso para cubrir los derechos de llamada. Se pueden configurar a través del servicio de componentes Microsoft Management Console (MMC).

Estas ACL de todo el equipo proporcionan una manera de invalidar la configuración de seguridad débil especificada por una aplicación específica a través de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o la configuración de seguridad específica de la aplicación. Esto proporciona un estándar de seguridad mínimo que se debe pasar, independientemente de la configuración del servidor específico.

Estas ACL se comprueban cuando se accede a las interfaces expuestas por RPCSS. Esto proporciona un método para controlar el acceso a este servicio del sistema.

Estas ACL proporcionan una ubicación centralizada donde un administrador puede establecer una directiva de autorización general que se aplica a todos los servidores COM del equipo.

> [!Note]  
> Cambiar la configuración de seguridad de todo el equipo afectará a todas las aplicaciones de servidor COM y podría impedir que funcionen correctamente. Si hay aplicaciones de servidor COM que tienen restricciones menos estrictas que las restricciones de todo el equipo, reducir las restricciones de todo el equipo podría exponer estas aplicaciones al acceso no deseado. Por el contrario, si aumenta las restricciones de todo el equipo, es posible que algunas aplicaciones de servidor COM ya no sean accesibles mediante una llamada a las aplicaciones.

 

De forma predeterminada, Windows configuración de restricciones de equipos XP SP2 son:



| Permiso        | Administrador                                                                                             | Todos.                                            | Anónimo               |
|-------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|-------------------------|
| Launch<br/> | Inicio local<br/> Activación local<br/> Inicio remoto<br/> Activación remota<br/> | Inicio local<br/> Activación local<br/> |                         |
| Acceso<br/> |                                                                                                           | Acceso local<br/> Acceso remoto<br/>    | Acceso local<br/> |



 

De forma predeterminada, Windows configuración de restricciones de equipo de Server 2003 SP 1 es la siguiente.



| Permiso        | Administrador                                                                                             | Usuarios COM distribuidos (grupo integrado)                                                                    | Todos.                                            | Anónimo                                        |
|-------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------|
| Launch<br/> | Inicio local<br/> Activación local<br/> Inicio remoto<br/> Activación remota<br/> | Inicio local<br/> Activación local<br/> Inicio remoto<br/> Activación remota<br/> | Inicio local<br/> Activación local<br/> | N/D<br/>                                   |
| Acceso<br/> | N/D<br/>                                                                                            | Acceso local<br/> Acceso remoto<br/>                                                          | Acceso local<br/> Acceso remoto<br/>    | Acceso local<br/> Acceso remoto<br/> |



 

> [!Note]  
> Usuarios COM distribuidos es un nuevo grupo integrado incluido con Windows Server 2003 SP1 para acelerar el proceso de agregar usuarios a la configuración de restricciones de equipos DCOM. Este grupo forma parte de la ACL que usan las opciones [MachineAccessRestriction](machineaccessrestriction.md) y [MachineLaunchRestriction,](machinelaunchrestriction.md) por lo que la eliminación de usuarios de este grupo afectará a esa configuración.

 

### <a name="why-is-this-change-important-what-threats-does-it-help-mitigate"></a>¿Por qué es importante este cambio? ¿Qué amenazas ayuda a mitigar?

Muchas aplicaciones COM incluyen código específico de seguridad (por ejemplo, llamar a [**CoInitializeSecurity),**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)pero usan configuraciones débiles, lo que a menudo permite el acceso no autenticado al proceso. Actualmente no hay ninguna manera de que un administrador invalide esta configuración para forzar una mayor seguridad en versiones anteriores de Windows.

La infraestructura COM incluye RPCSS, un servicio del sistema que se ejecuta durante el inicio del sistema y que siempre se ejecuta después de eso. Administra la activación de objetos COM y la tabla de objetos en ejecución y proporciona servicios auxiliares a la comunicación remota de DCOM. Expone las interfaces RPC a las que se puede llamar de forma remota. Dado que algunos servidores COM permiten el acceso remoto no autenticado, cualquiera puede llamar a estas interfaces, incluidos los usuarios no autenticados. Como resultado, los usuarios malintencionados pueden atacar RPCSS en equipos remotos no autenticados.

En versiones anteriores de Windows, no había forma de que un administrador entienda el nivel de exposición de los servidores COM en un equipo. Un administrador se ha hecho una idea del nivel de exposición comprobando sistemáticamente la configuración de seguridad configurada para todas las aplicaciones COM registradas en el equipo, pero, dado que hay unos 150 servidores COM en una instalación predeterminada de Windows, esa tarea era desalentador. No había ninguna manera de ver la configuración de un servidor que incorpora seguridad en el software, sin necesidad de revisar el código fuente de ese software.

Las restricciones de todo el equipo de DCOM mitigan estos tres problemas. También proporciona a un administrador la capacidad de deshabilitar la activación, el inicio y las llamadas entrantes de DCOM.

### <a name="what-works-differently"></a>¿Qué funciona de manera diferente?

De forma predeterminada, al grupo Todos se le conceden permisos de inicio local, activación local y llamada de acceso local. Esto permite que todos los escenarios locales funcionen sin modificaciones en el software o el sistema operativo.

De forma predeterminada, en Windows XP SP2, al grupo Todos se le conceden permisos de llamada de acceso remoto. En Windows Server 2003 SP1, se conceden permisos de acceso remoto a los grupos Todos y Anónimos. Esto permite la mayoría de los escenarios de cliente COM, incluido el caso común en el que un cliente COM pasa una referencia local a un servidor remoto, convirtiendo el cliente en un servidor. En Windows XP SP2, esto podría deshabilitar escenarios que requieren llamadas de acceso remoto no autenticadas.

Además, de forma predeterminada, solo a los miembros del grupo Administradores se les conceden permisos de activación e inicio remotos. Esto deshabilita las activaciones remotas de los usuarios que no son administradores en los servidores COM instalados.

### <a name="how-do-i-resolve-these-issues"></a>Cómo resolver estos problemas?

Si implementa un servidor COM y espera admitir la activación remota por parte de un cliente COM no administrativo, debe considerar si el riesgo asociado a habilitar este proceso es aceptable o si debe modificar la implementación para no requerir la activación remota por parte de un cliente COM no administrativo o llamadas remotas no autenticadas.

Si el riesgo es aceptable y desea habilitar la activación remota mediante un cliente COM no administrativo o llamadas remotas no autenticadas, debe cambiar la configuración predeterminada para esta característica.

> [!Note]  
> Cambiar la configuración de seguridad de todo el equipo afectará a todas las aplicaciones de servidor COM y podría impedir que funcionen correctamente. Si hay aplicaciones de servidor COM que tienen restricciones menos estrictas que las restricciones de todo el equipo, la reducción de las restricciones de todo el equipo puede exponer estas aplicaciones al acceso no deseado. Por el contrario, si aumenta las restricciones de todo el equipo, es posible que algunas aplicaciones de servidor COM ya no sean accesibles mediante una llamada a las aplicaciones.

 

Puede cambiar los valores de configuración mediante el registro de Microsoft Management Console componentes (MMC) o Windows componentes.

Si usa el complemento MMC de Servicios de componentes, esta configuración  se puede configurar en la pestaña Seguridad **COM** del cuadro de diálogo Propiedades del equipo que está administrando. El área Permisos de acceso se ha modificado para permitirle establecer **límites** de todo el equipo además de la configuración predeterminada estándar para los servidores COM. Además, puede proporcionar una configuración de ACL independiente para el acceso local y remoto en los límites y los valores predeterminados.

En el **área Permisos** de inicio y activación, puede controlar los permisos locales y remotos, así como los límites de todo el equipo y los valores predeterminados. Puede especificar permisos de activación e inicio locales y remotos de forma independiente.

Como alternativa, puede configurar estas opciones de ACL mediante el Registro.

Estas ACL se almacenan en el registro en las siguientes ubicaciones:

``` syntax
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole\MachineAccessRestriction=ACL
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole\MachineLaunchRestriction=ACL
```

Se trata de valores con nombre de tipo REG BINARY que contienen datos que describen la ACL de las entidades de seguridad que pueden tener acceso a cualquier clase COM o objeto \_ COM en el equipo. Los derechos de acceso en la ACL son:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Estas ACL se pueden crear mediante funciones de seguridad normales.

> [!Note]  
> Para proporcionar compatibilidad con versiones anteriores, puede existir una ACL en el formato usado antes de Windows XP SP2 y Windows Server 2003 SP1, que usa solo el derecho de acceso COM RIGHTS EXECUTE, o puede existir en el nuevo formato usado en Windows XP SP2 y \_ Windows Server 2003 SP1, que usa COM RIGHTS EXECUTE junto con una combinación de DERECHOS \_ COM EXECUTE \_ \_ \_ \_ \_ LOCAL, COM RIGHTS EXECUTE REMOTE, COM RIGHTS ACTIVATE LOCAL y \_ COM RIGHTS ACTIVATE \_ \_ \_ \_ \_ \_ \_ \_ REMOTE. Tenga en cuenta que LOS DERECHOS> COM deben estar siempre presentes; la ausencia de este derecho \_ genera un descriptor de seguridad no \_ válido. Tenga en cuenta también que no debe mezclar el formato anterior y el nuevo formato dentro de una sola ACL; Todas las entradas de control de acceso (ACE) solo deben conceder el derecho de acceso COM RIGHTS EXECUTE, o bien todas deben conceder DERECHOS COM EXECUTE junto con una combinación de DERECHOS \_ \_ COM EXECUTE \_ \_ \_ \_ \_ LOCAL, COM RIGHTS EXECUTE REMOTE, COM RIGHTS ACTIVATE LOCAL y \_ COM RIGHTS ACTIVATE \_ \_ \_ \_ \_ \_ \_ \_ REMOTE.

 

> [!Note]  
> Solo los usuarios con derechos de administrador pueden modificar esta configuración.

 

## <a name="what-existing-functionality-is-changing-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>¿Qué funcionalidad existente está cambiando en Windows XP Service Pack 2 y Windows Server 2003 Service Pack 1?

### <a name="rpcss-runs-as-a-network-service"></a>RPCSS se ejecuta como un servicio de red

RPCSS es un servicio clave para el asignador de puntos de conexión RPC y la infraestructura de DCOM. Este servicio se ejecutó como sistema local en versiones anteriores de Windows. Para reducir la superficie de ataque de Windows y proporcionar defensa en profundidad, la funcionalidad del servicio RPCSS se dividió en dos servicios. El servicio RPCSS con toda la funcionalidad original que no requiere privilegios de sistema local ahora se ejecuta en la cuenta de servicio de red. Un nuevo servicio DCOMLaunch que incluye funcionalidad que requiere privilegios de sistema local se ejecuta en la cuenta sistema local.

### <a name="why-is-this-change-important"></a>¿Por qué es importante este cambio?

Este cambio reduce la superficie de ataque y proporciona una defensa en profundidad para el servicio RPCSS porque una elevación de privilegios en el servicio RPCSS ahora se limita al privilegio Servicio de red.

### <a name="what-works-differently"></a>¿Qué funciona de manera diferente?

Este cambio debe ser transparente para los usuarios porque la combinación de los servicios RPCSS y DCOMLaunch es equivalente al servicio RPCSS anterior proporcionado en versiones anteriores de Windows.

### <a name="more-specific-com-permissions"></a>Permisos COM más específicos

Las aplicaciones de servidor COM tienen dos tipos de permisos: permisos de inicio y permisos de acceso. Los permisos de inicio controlan la autorización para iniciar un servidor COM durante la activación com si el servidor aún no se está ejecutando. Estos permisos se definen como descriptores de seguridad que se especifican en la configuración del Registro. Los permisos de acceso controlan la autorización para llamar a un servidor COM en ejecución. Estos permisos se definen como descriptores de seguridad proporcionados a la infraestructura COM a través de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) API o mediante la configuración del Registro. Los permisos de inicio y acceso permiten o deniegan el acceso en función de las entidades de seguridad, y no distinguen si el autor de la llamada es local para el servidor o remoto.

El primer cambio distingue los derechos de acceso COM, en función de la distancia. Las dos distancias definidas son Local y Remote. Un mensaje COM local llega mediante el protocolo de llamada a procedimiento remoto local (LRPC), mientras que un mensaje COM remoto llega mediante un protocolo host de llamada a procedimiento remoto (RPC), como el protocolo de control de transmisión (TCP).

La activación COM es el acto de obtener un proxy de interfaz COM en un cliente mediante una llamada a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o a una de sus variantes. Como efecto secundario de este proceso de activación, a veces se debe iniciar un servidor COM para satisfacer la solicitud del cliente. Una ACL de permisos de inicio declara quién puede iniciar un servidor COM. Una ACL de permisos de acceso declara quién puede activar un objeto COM o llamar a ese objeto una vez que el servidor COM ya se está ejecutando.

El segundo cambio es que los derechos de llamada y activación se separan para reflejarse en dos operaciones distintas y para mover la activación directamente desde la ACL del permiso de acceso a la ACL del permiso de inicio. Dado que la activación y el inicio están relacionados con la adquisición de un puntero de interfaz, los derechos de acceso de activación e inicio pertenecen lógicamente a una ACL. Y dado que siempre se especifican permisos de inicio a través de la configuración (en comparación con los permisos de acceso, que a menudo se especifican mediante programación), colocar los derechos de activación en la ACL de permisos de inicio proporciona al administrador control sobre la activación.

Las entradas de control de acceso (ACE) del permiso de inicio se divide en cuatro derechos de acceso:

-   Inicio local (LL)
-   Inicio remoto (RL)
-   Activación local (LA)
-   Activación remota (RA)

El descriptor de seguridad del permiso de acceso se divide en dos derechos de acceso:

-   Llamadas de acceso local (LC)
-   Llamadas de acceso remoto (RC)

Esto permite al administrador aplicar configuraciones de seguridad muy específicas. Por ejemplo, puede configurar un servidor COM para que acepte llamadas de acceso local de todos los usuarios, al tiempo que solo acepta llamadas de acceso remoto de administradores. Estas distinciones se pueden especificar mediante cambios en los descriptores de seguridad de permisos COM.

### <a name="why-is-this-change-important-what-threats-does-it-help-mitigate"></a>¿Por qué es importante este cambio? ¿Qué amenazas ayuda a mitigar?

Las versiones anteriores de la aplicación de servidor COM no tienen ninguna manera de restringir una aplicación para que solo se pueda usar localmente sin exponer la aplicación en la red mediante DCOM. Cuando un usuario tiene acceso a una aplicación de servidor COM, tiene acceso para uso local y remoto.

Una aplicación de servidor COM podría exponerse a usuarios no autenticados para implementar un escenario de devolución de llamada COM. En este escenario, la aplicación también debe exponer su activación a usuarios no autenticados, lo que podría no ser deseable.

Los permisos COM precisos proporcionan flexibilidad al administrador para controlar la directiva de permisos COM de un equipo. Estos permisos habilitan la seguridad para los escenarios descritos.

### <a name="what-works-differently-are-there-any-dependencies"></a>¿Qué funciona de manera diferente? ¿Hay dependencias?

Para proporcionar compatibilidad con versiones anteriores, los descriptores de seguridad COM existentes se interpretan para permitir o denegar el acceso local y remoto simultáneamente. Es decir, una entrada de control de acceso (ACE) permite tanto local como remota, o deniega tanto local como remota.

No hay ningún problema de compatibilidad con versiones anteriores para los derechos de llamada o inicio. Sin embargo, hay un problema de compatibilidad de derechos de activación. Si, en los descriptores de seguridad existentes para un servidor COM, los permisos de inicio configurados son más restrictivos que los permisos de acceso y son más restrictivos que los mínimos necesarios para escenarios de activación de cliente, la ACL de permisos de inicio debe modificarse para conceder a los clientes autorizados los permisos de activación adecuados.

En el caso de las aplicaciones COM que usan la configuración de seguridad predeterminada, no hay ningún problema de compatibilidad. En el caso de las aplicaciones que se inician dinámicamente con la activación COM, la mayoría no tienen problemas de compatibilidad, ya que los permisos de inicio ya deben incluir a cualquier persona que pueda activar un objeto. De lo contrario, estas aplicaciones generan errores de activación incluso antes de aplicar Windows XP SP2 o Windows Server 2003 SP1, cuando los llamadores sin permiso de inicio intentan activar un objeto y el servidor COM aún no se está ejecutando.

Las aplicaciones que más se preocupa por los problemas de compatibilidad son las aplicaciones COM que ya se han iniciado con algún otro mecanismo, como Windows Explorer o Service Control Manager. También puede iniciar estas aplicaciones mediante una activación COM anterior, que invalida los permisos de acceso e inicio predeterminados y especifica permisos de inicio que son más restrictivos que los permisos de llamada. Para obtener más información sobre cómo solucionar este problema de compatibilidad, vea "¿Cómo resolver estos problemas?" en la sección siguiente.

Si un sistema actualizado a Windows XP SP2 o Windows Server 2003 SP1 se revierte a un estado anterior, cualquier ACE que se haya editado para permitir el acceso local, el acceso remoto o ambos, se interpretará para permitir el acceso local y remoto. Cualquier ACE que se haya editado para denegar el acceso local, el acceso remoto o ambos, se interpreta para denegar el acceso local y remoto. Cada vez que desinstale un Service Pack, debe asegurarse de que ningún ACE recién establecido hace que las aplicaciones dejen de funcionar.

### <a name="how-do-i-resolve-these-issues"></a>Cómo resolver estos problemas?

Si implementa un servidor COM e invalida la configuración de seguridad predeterminada, confirme que la ACL de permisos de inicio específicos de la aplicación concede permiso de activación a los usuarios adecuados. Si no es así, debe cambiar la ACL del permiso de inicio específico de la aplicación para conceder a los usuarios adecuados derechos de activación para que las aplicaciones y los componentes de Windows que usan DCOM no den error. Estos permisos de inicio específicos de la aplicación se almacenan en el Registro.

Las ACL COM se pueden crear o modificar mediante funciones de seguridad normales.

## <a name="what-settings-are-added-or-changed-in-windows-xp-service-pack-2"></a>¿Qué configuración se agrega o cambia en Windows XP Service Pack 2?

> [!Caution]  
> El uso incorrecto de esta configuración puede hacer que se Windows aplicaciones y componentes que usan DCOM.

 

En la tabla siguiente, se usan estas abreviaturas:

LL: inicio local

LA: activación local

RL: inicio remoto

RA: activación remota

LC: llamadas de acceso local

RC: llamadas de acceso remoto

ACL: Access Control lista



| Nombre de la configuración                                                                                         | Location                                                                                                       | Valor predeterminado anterior                                                                                                                                                                     | Valor predeterminado                                                                                                                                                                                                                                                                                                                                                             | Valores posibles                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MachineLaunchRestriction**<br/>                                                              | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Todos: LL, LA, RL, RA<br/> Anónimo:<br/> LL, LA, RL, RA<br/> (Se trata de una nueva clave del Registro. En función del comportamiento existente, estos son los valores efectivos).<br/> | Administrador: LL, LA, RL, RA<br/>                                                                                                                                                                                                                                                                                                                                  | ACL<br/>                                                                                                                                                                                                               |
| **MachineAccessRestriction**<br/>                                                              | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Todos: LC, RC<br/> Anónimo: LC, RC<br/> (Se trata de una nueva clave del Registro. En función del comportamiento existente, estos son los valores efectivos).<br/>                            | Todos: LC, RC<br/> Anónimo: LC<br/>                                                                                                                                                                                                                                                                                                                      | ACL<br/>                                                                                                                                                                                                               |
| **CallFailureLoggingLevel**<br/>                                                               | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | No es aplicable.<br/>                                                                                                                                                                 | Esta clave del Registro no está presente; sin embargo, una clave o un valor que faltan se interpreta como 2.<br/> Este evento no se registra de forma predeterminada. Si cambia este valor a 1 para empezar a registrar esta información para ayudarle a solucionar un problema, asegúrese de supervisar el tamaño del registro de eventos, ya que se trata de un evento que puede generar un gran número de entradas.<br/> | 1 - Registre siempre los errores del registro de eventos durante una llamada en el proceso del servidor COM.<br/> 2 - Nunca registre errores del registro de eventos durante una llamada en el proceso del servidor de llamadas.<br/>                                                  |
| **InvalidSecurityDescriptorLoggingLevel**<br/>                                                 | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | No es aplicable.<br/>                                                                                                                                                                 | Esta clave del Registro no está presente; sin embargo, una clave o un valor que faltan se interpreta como 1.<br/> Este evento se registra de forma predeterminada. Rara vez debería producirse.<br/>                                                                                                                                                                                                    | 1 - Registre siempre los errores del registro de eventos cuando la infraestructura COM encuentre un descriptor de seguridad no válido.<br/> 2 - No registre nunca errores de registro de eventos cuando la infraestructura COM encuentre un descriptor de seguridad no válido.<br/> |
| DCOM:Restricciones de inicio de máquina en la sintaxis del lenguaje de definición de descriptores de seguridad (SDDL)<br/> | (directiva de grupo objeto ) Configuración del equipo \\ Windows Configuración opciones de seguridad de directivas \\ \\ locales<br/>  | No es aplicable.<br/>                                                                                                                                                                 | No definida<br/>                                                                                                                                                                                                                                                                                                                                                    | Lista de control de acceso en formato SDDL. La existencia de esta directiva invalida los valores de MachineLaunchRestriction, anteriormente.<br/>                                                                                            |
| DCOM:Restricciones de acceso a la máquina en la sintaxis del lenguaje de definición de descriptores de seguridad (SDDL)<br/> | (directiva de grupo objeto) Configuración del equipo \\ Windows Configuración opciones de seguridad de directivas \\ \\ locales<br/> | No es aplicable.<br/>                                                                                                                                                                 | No definida<br/>                                                                                                                                                                                                                                                                                                                                                    | Lista de control de acceso en formato SDDL. La existencia de esta directiva invalida los valores de MachineAccessRestriction, anteriormente.<br/>                                                                                            |



 

## <a name="what-settings-are-added-or-changed-in-windows-server-2003-service-pack-1"></a>¿Qué configuraciones se agregan o cambian en Windows Server 2003 Service Pack 1?

> [!Note]  
> El uso incorrecto de esta configuración puede hacer que se Windows aplicaciones y componentes que usan DCOM.

 

En la tabla siguiente, se usan estas abreviaturas:

LL: inicio local

LA: activación local

RL: inicio remoto

RA: activación remota

LC: llamadas de acceso local

RC: llamadas de acceso remoto

ACL: Access Control lista



| Nombre de la configuración                                                                                         | Location                                                                                                       | Valor predeterminado anterior                                                                                                                                                             | Valor predeterminado                                                                                                                                                                                                                                                                                                                                                             | Valores posibles                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MachineLaunchRestriction**<br/>                                                              | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Todos: LL, LA, RL, RA<br/> Anónimo: LL, LA, RL, RA<br/> (Se trata de una nueva clave del Registro. En función del comportamiento existente, estos serían los valores efectivos).<br/> | Administrador: LL, LA, RL, RA<br/> Todos: LL, LA<br/> Usuarios COM distribuidos: LL, LA, RL, RA<br/>                                                                                                                                                                                                                                                     | ACL<br/>                                                                                                                                                                                                               |
| **MachineAccessRestriction**<br/>                                                              | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Todos: LC, RC<br/> Anónimo: LC, RC<br/> (Se trata de una nueva clave del Registro. En función del comportamiento existente, estos serían los valores efectivos).<br/>                 | Todos: LC, RC<br/> Anónimo: LC, RC<br/>                                                                                                                                                                                                                                                                                                                  | ACL<br/>                                                                                                                                                                                                               |
| **CallFailureLoggingLevel**<br/>                                                               | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | No es aplicable.<br/>                                                                                                                                                         | Esta clave del Registro no está presente; sin embargo, una clave o un valor que faltan se interpreta como 2.<br/> Este evento no se registra de forma predeterminada. Si cambia este valor a 1 para empezar a registrar esta información para ayudarle a solucionar un problema, asegúrese de supervisar el tamaño del registro de eventos, ya que se trata de un evento que puede generar un gran número de entradas.<br/> | 1 - Registre siempre los errores del registro de eventos cuando la infraestructura COM encuentre un descriptor de seguridad no válido.<br/> 2 - No registre nunca errores de registro de eventos cuando la infraestructura COM encuentre un descriptor de seguridad no válido.<br/> |
| **InvalidSecurityDescriptorLoggingLevel**<br/>                                                 | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | No es aplicable.<br/>                                                                                                                                                         | Esta clave del Registro no está presente; sin embargo, una clave o un valor que faltan se interpreta como 1.<br/> Este evento se registra de forma predeterminada. Rara vez debería producirse.<br/>                                                                                                                                                                                                    | 1 - Registre siempre los errores del registro de eventos cuando la infraestructura COM encuentre un descriptor de seguridad no válido.<br/> 2 - Nunca registre errores del registro de eventos cuando la infraestructura COM encuentre un descriptor de seguridad no válido.<br/>         |
| DCOM:Restricciones de inicio de máquina en la sintaxis del lenguaje de definición de descriptores de seguridad (SDDL)<br/> | (directiva de grupo objeto) Opciones de seguridad \\ Windows Configuración directivas locales del \\ \\ equipo<br/> | No es aplicable.<br/>                                                                                                                                                         | Sin definir.<br/>                                                                                                                                                                                                                                                                                                                                                   | Lista de control de acceso en formato SDDL. La existencia de esta directiva invalida los valores de MachineLaunchRestriction, anteriormente.<br/>                                                                                            |
| DCOM:Restricciones de acceso a la máquina en la sintaxis del lenguaje de definición de descriptores de seguridad (SDDL)<br/> | (directiva de grupo objeto) Opciones de seguridad \\ Windows Configuración directivas locales del \\ \\ equipo<br/> | No es aplicable.<br/>                                                                                                                                                         | Sin definir.<br/>                                                                                                                                                                                                                                                                                                                                                   | Lista de control de acceso en formato SDDL. La existencia de esta directiva invalida los valores de MachineAccessRestriction, anteriormente.<br/>                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

