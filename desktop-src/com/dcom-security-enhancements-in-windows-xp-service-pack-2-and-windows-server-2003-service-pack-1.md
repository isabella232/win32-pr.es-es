---
title: Mejoras de seguridad de DCOM en Windows XP Service Pack 2 y Windows Server 2003 Service Pack 1
description: Windows Server XP Service Pack 2 (SP2) y Windows Server 2003 Service Pack 1 (SP1) introducen la configuración de seguridad predeterminada mejorada para el modelo de objetos componentes distribuido (DCOM).
ms.assetid: 1917834c-5216-4ef3-a0c2-d8ca63cef53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ad51807e27a9b97e8b05e467d8a84881c3993a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149657"
---
# <a name="dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>Mejoras de seguridad de DCOM en Windows XP Service Pack 2 y Windows Server 2003 Service Pack 1

Windows Server XP Service Pack 2 (SP2) y Windows Server 2003 Service Pack 1 (SP1) introducen la configuración de seguridad predeterminada mejorada para el modelo de objetos componentes distribuido (DCOM). En concreto, introducen derechos más granulares que permiten a un administrador tener un control independiente sobre los permisos locales y remotos para iniciar, activar y obtener acceso a los servidores COM.

## <a name="what-does-dcom-do"></a>¿Qué hace DCOM?

El modelo de objetos componentes (COM) de Microsoft es un sistema independiente de la plataforma, distribuido y orientado a objetos para crear componentes de software binarios que pueden interactuar. El modelo de objetos componentes distribuido (DCOM) permite que las aplicaciones se distribuyan en ubicaciones que tengan más sentido para usted y para la aplicación. El protocolo de conexión DCOM proporciona de forma transparente la compatibilidad con la comunicación confiable, segura y eficaz entre los componentes COM.

## <a name="who-does-this-feature-apply-to"></a>¿A quién se aplica esta característica?

Si utiliza COM solo para componentes COM en proceso, esta característica no se aplica a su caso.

Esta característica se aplica a su caso si tiene una aplicación de servidor COM que cumple uno de los siguientes criterios:

-   El permiso de acceso para la aplicación es menos estricto que el permiso de inicio, que es necesario para ejecutar la aplicación.
-   Normalmente, un cliente COM remoto activa la aplicación sin utilizar una cuenta administrativa.
-   La aplicación está pensada para usarse solo localmente. Esto significa que puede restringir la aplicación de servidor COM para que no sea accesible de forma remota.

## <a name="what-new-functionality-is-added-to-this-feature-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>¿Qué nueva funcionalidad se agrega a esta característica en Windows XP Service Pack 2 y Windows Server 2003 Service Pack 1?

### <a name="computer-wide-restrictions"></a>Restricciones para todo el equipo

Se ha realizado un cambio en COM para proporcionar controles de acceso para todo el equipo que rigen el acceso a todas las solicitudes de llamada, activación o inicio en el equipo. La manera más sencilla de pensar en estos controles de acceso es como una llamada a [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) adicional que se realiza en una lista de control de acceso (ACL) de todo el equipo en cada llamada, activación o inicio de cualquier servidor com del equipo. Si se produce un error en **AccessCheck** , se deniega la solicitud de llamada, activación o inicio. Esto se suma a cualquier **AccessCheck** que se ejecute en las ACL específicas del servidor. En efecto, proporciona un estándar de autorización mínimo que se debe pasar para tener acceso a cualquier servidor COM del equipo. Hay un ACL de equipo para los permisos de inicio que abarcan los derechos de activación e inicio, y una ACL en todo el equipo para los permisos de acceso para cubrir los derechos de llamada. Se pueden configurar a través de Microsoft Management Console (MMC) de servicios de componentes.

Estas ACL para todo el equipo proporcionan una manera de invalidar la configuración de seguridad débil especificada por una aplicación específica a través de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o la configuración de seguridad específica de la aplicación. Esto proporciona un estándar de seguridad mínimo que se debe pasar, independientemente de la configuración del servidor específico.

Estas ACL se comprueban cuando se tiene acceso a las interfaces expuestas por RPCSS. Esto proporciona un método para controlar el acceso a este servicio de sistema.

Estas ACL proporcionan una ubicación centralizada en la que un administrador puede establecer una directiva de autorización general que se aplica a todos los servidores COM del equipo.

> [!Note]  
> El cambio de la configuración de seguridad en todo el equipo afectará a todas las aplicaciones de servidor COM y puede impedir que funcionen correctamente. Si hay aplicaciones de servidor COM con restricciones que son menos rigurosas que las restricciones en todo el equipo, reducir las restricciones en todo el equipo podría exponer estas aplicaciones al acceso no deseado. Por el contrario, si aumenta las restricciones en todo el equipo, es posible que algunas aplicaciones de servidor COM dejen de ser accesibles mediante la llamada a aplicaciones.

 

De forma predeterminada, la configuración de restricciones de equipo de Windows XP SP2 es:



| Permiso        | Administrador                                                                                             | Todos                                            | Anónimas               |
|-------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|-------------------------|
| Launch<br/> | Inicio local<br/> Activación local<br/> Inicio remoto<br/> Activación remota<br/> | Inicio local<br/> Activación local<br/> |                         |
| Access<br/> |                                                                                                           | Acceso local<br/> Acceso remoto<br/>    | Acceso local<br/> |



 

De forma predeterminada, la configuración de restricciones de equipo de Windows Server 2003 SP 1 es la siguiente.



| Permiso        | Administrador                                                                                             | Usuarios COM distribuidos (grupo integrado)                                                                    | Todos                                            | Anónimas                                        |
|-------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------|
| Launch<br/> | Inicio local<br/> Activación local<br/> Inicio remoto<br/> Activación remota<br/> | Inicio local<br/> Activación local<br/> Inicio remoto<br/> Activación remota<br/> | Inicio local<br/> Activación local<br/> | N/D<br/>                                   |
| Access<br/> | N/D<br/>                                                                                            | Acceso local<br/> Acceso remoto<br/>                                                          | Acceso local<br/> Acceso remoto<br/>    | Acceso local<br/> Acceso remoto<br/> |



 

> [!Note]  
> Usuarios COM distribuidos es un nuevo grupo integrado incluido en Windows Server 2003 SP1 para agilizar el proceso de agregar usuarios a la configuración de restricciones de equipos DCOM. Este grupo forma parte de la ACL usada por la configuración de [MachineAccessRestriction](machineaccessrestriction.md) y [MachineLaunchRestriction](machinelaunchrestriction.md) , por lo que la eliminación de usuarios de este grupo afectará a esa configuración.

 

### <a name="why-is-this-change-important-what-threats-does-it-help-mitigate"></a>¿Por qué es importante este cambio? ¿Qué amenazas ayuda a mitigar?

Muchas aplicaciones COM incluyen algún código específico de seguridad (por ejemplo, la llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)), pero usan valores débiles, a menudo para permitir el acceso no autenticado al proceso. Actualmente no hay ninguna manera de que un administrador invalide esta configuración para forzar una mayor seguridad en versiones anteriores de Windows.

La infraestructura COM incluye RPCSS, un servicio del sistema que se ejecuta durante el inicio del sistema y siempre se ejecuta después. Administra la activación de objetos COM y la tabla de objetos en ejecución y proporciona servicios auxiliares a la comunicación remota de DCOM. Expone las interfaces RPC a las que se puede llamar de forma remota. Dado que algunos servidores COM permiten el acceso remoto no autenticado, cualquier usuario puede llamar a estas interfaces, incluidos los usuarios no autenticados. Como resultado, RPCSS puede ser atacado por usuarios malintencionados en equipos remotos no autenticados.

En versiones anteriores de Windows, no había forma de que un administrador entendera el nivel de exposición de los servidores COM en un equipo. Un administrador tiene una idea del nivel de exposición al comprobar sistemáticamente la configuración de seguridad configurada para todas las aplicaciones COM registradas en el equipo, pero, dado que hay aproximadamente 150 servidores COM en una instalación predeterminada de Windows, esa tarea era desalentadora. No había ninguna manera de ver la configuración de un servidor que incorpora seguridad en el software, en breve revisión del código fuente de dicho software.

Las restricciones en todo el equipo de DCOM mitigan estos tres problemas. También proporciona a un administrador la capacidad de deshabilitar la activación, el inicio y las llamadas de DCOM entrantes.

### <a name="what-works-differently"></a>¿Qué funciona de manera diferente?

De forma predeterminada, al grupo todos se le conceden los permisos de inicio local, activación local y llamada de acceso local. Esto permite que todos los escenarios locales funcionen sin modificaciones en el software ni en el sistema operativo.

De forma predeterminada, en Windows XP SP2, al grupo todos se le conceden permisos de llamada de acceso remoto. En Windows Server 2003 SP1, a todos los grupos anónimos se les conceden permisos de acceso remoto. Esto permite la mayoría de los escenarios de cliente COM, incluido el caso habitual en el que un cliente COM pasa una referencia local a un servidor remoto, de modo que el cliente se convierte en un servidor. En Windows XP SP2, esto podría deshabilitar escenarios que requieren llamadas de acceso remoto no autenticadas.

Además, de forma predeterminada, solo los miembros del grupo administradores tienen permisos de inicio y activación remota. De este modo, los usuarios que no son administradores pueden deshabilitar la activación remota de los servidores COM.

### <a name="how-do-i-resolve-these-issues"></a>¿Cómo resolver estos problemas?

Si implementa un servidor COM y espera admitir la activación remota por un cliente COM no administrativo, debe considerar si el riesgo asociado a la habilitación de este proceso es aceptable o si debe modificar la implementación para que no requiera la activación remota por parte de un cliente COM no administrativo o de llamadas remotas no autenticadas.

Si el riesgo es aceptable y desea habilitar la activación remota por parte de un cliente COM no administrativo o de llamadas remotas no autenticadas, debe cambiar la configuración predeterminada para esta característica.

> [!Note]  
> El cambio de la configuración de seguridad en todo el equipo afectará a todas las aplicaciones de servidor COM y puede impedir que funcionen correctamente. Si hay aplicaciones de servidor COM con restricciones que son menos rigurosas que las restricciones en todo el equipo, reducir las restricciones en todo el equipo puede exponer estas aplicaciones al acceso no deseado. Por el contrario, si aumenta las restricciones en todo el equipo, es posible que algunas aplicaciones de servidor COM dejen de ser accesibles mediante la llamada a aplicaciones.

 

Puede cambiar la configuración mediante los servicios de componentes Microsoft Management Console (MMC) o el registro de Windows.

Si utiliza el complemento Servicios de componentes de MMC, esta configuración se puede configurar en la ficha **seguridad com** del cuadro de diálogo **propiedades** del equipo que está administrando. El área **permisos de acceso** se ha modificado para que pueda establecer límites para todo el equipo, además de la configuración predeterminada estándar de los servidores com. Además, puede proporcionar una configuración de ACL independiente para el acceso local y remoto en los límites y los valores predeterminados.

En el área **permisos de inicio y activación** , puede controlar los permisos locales y remotos, así como los límites de todo el equipo y los valores predeterminados. Puede especificar los permisos de inicio y activación locales y remotos de forma independiente.

Como alternativa, puede configurar estas opciones de ACL mediante el registro.

Estas ACL se almacenan en el registro en las siguientes ubicaciones:

``` syntax
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole\MachineAccessRestriction=ACL
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole\MachineLaunchRestriction=ACL
```

Se trata de valores con nombre de tipo \_ binario de registro que contienen datos que describen la ACL de las entidades de seguridad que pueden tener acceso a cualquier clase com u objeto com del equipo. Los derechos de acceso de la ACL son:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Estas ACL se pueden crear mediante las funciones de seguridad normales.

> [!Note]  
> Para proporcionar compatibilidad con versiones anteriores, puede existir una ACL en el formato usado antes de Windows XP SP2 y Windows Server 2003 SP1, que usa solo los derechos de acceso de COM correctos para la \_ \_ ejecución, o puede existir en el nuevo formato usado en Windows XP SP2 y windows Server 2003 SP1, que usa \_ derechos com \_ ejecutarse junto con una combinación de \_ derechos COM \_ ejecutar \_ local, \_ derechos com \_ ejecutar \_ remoto, \_ derechos com \_ activar \_ local y \_ derechos com \_ activar \_ remoto. Tenga en cuenta \_ que \_ los derechos com execute> deben estar siempre presentes; la ausencia de este derecho genera un descriptor de seguridad no válido. Tenga en cuenta también que no debe mezclar el formato antiguo y el nuevo formato en una sola ACL. todas las entradas de control de acceso (ACE) deben conceder solo el derecho de acceso de permisos de COM \_ \_ , o todos deben conceder derechos de com ejecutarse \_ \_ junto con una combinación de \_ derechos COM \_ ejecutar \_ local, \_ derechos com \_ ejecutar \_ remoto, derechos de com \_ \_ activar \_ local y derechos de com \_ \_ activar \_ remoto.

 

> [!Note]  
> Solo los usuarios con derechos de administrador pueden modificar esta configuración.

 

## <a name="what-existing-functionality-is-changing-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>¿Qué funcionalidad existente está cambiando en Windows XP Service Pack 2 y Windows Server 2003 Service Pack 1?

### <a name="rpcss-runs-as-a-network-service"></a>RPCSS se ejecuta como servicio de red

RPCSS es un servicio clave para el asignador de extremos de RPC y la infraestructura de DCOM. Este servicio se ejecutó como sistema local en versiones anteriores de Windows. Para reducir la superficie de ataque de Windows y proporcionar una defensa en profundidad, la funcionalidad del servicio RPCSS se dividió en dos servicios. El servicio RPCSS con toda la funcionalidad original que no requirió privilegios del sistema local ahora se ejecuta en la cuenta servicio de red. Un nuevo servicio de DCOMLaunch que incluye funcionalidad que requiere privilegios de sistema local se ejecuta en la cuenta de sistema local.

### <a name="why-is-this-change-important"></a>¿Por qué es importante este cambio?

Este cambio reduce la superficie expuesta a ataques y proporciona defensa en profundidad para el servicio RPCSS porque una elevación de privilegios en el servicio RPCSS ahora está limitada al privilegio servicio de red.

### <a name="what-works-differently"></a>¿Qué funciona de manera diferente?

Este cambio debe ser transparente para los usuarios porque la combinación de los servicios RPCSS y DCOMLaunch es equivalente al servicio RPCSS anterior proporcionado en versiones anteriores de Windows.

### <a name="more-specific-com-permissions"></a>Permisos COM más específicos

Las aplicaciones de servidor COM tienen dos tipos de permisos: permisos de inicio y permisos de acceso. Los permisos de inicio controlan la autorización para iniciar un servidor COM durante la activación COM si el servidor no se está ejecutando ya. Estos permisos se definen como descriptores de seguridad que se especifican en la configuración del registro. Los permisos de acceso controlan la autorización para llamar a un servidor COM en ejecución. Estos permisos se definen como descriptores de seguridad proporcionados a la infraestructura COM a través de la API de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o mediante la configuración del registro. Los permisos de inicio y acceso permiten o deniegan el acceso basado en entidades de seguridad y no distinguen si el llamador es local en el servidor o remoto.

El primer cambio distingue los derechos de acceso COM, en función de la distancia. Las dos distancias definidas son local y remota. Un mensaje COM local llega a través del Protocolo de llamada a procedimiento remoto local (LRPC), mientras que un mensaje COM remoto llega a través de un protocolo de host de llamada a procedimiento remoto (RPC) como el protocolo de control de transmisión (TCP).

La activación COM es el acto de obtener un proxy de interfaz COM en un cliente llamando a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o a una de sus variantes. Como efecto secundario de este proceso de activación, a veces se debe iniciar un servidor COM para satisfacer la solicitud del cliente. Una ACL de permisos de inicio valida quién tiene permiso para iniciar un servidor COM. Una ACL de permisos de acceso valida quién puede activar un objeto COM o llamar a ese objeto una vez que el servidor COM ya se está ejecutando.

El segundo cambio consiste en que los derechos de llamada y activación están separados para reflejarse en dos operaciones distintas y para pasar el derecho de activación de la ACL de permiso de acceso a la ACL de permiso de inicio. Dado que la activación y el inicio están relacionados con la adquisición de un puntero de interfaz, los derechos de acceso de activación e inicio pertenecen lógicamente a una ACL. Además, dado que siempre se especifican permisos de inicio a través de la configuración (en comparación con los permisos de acceso, que a menudo se especifican mediante programación), la colocación de los derechos de activación en la ACL de permiso de inicio proporciona al administrador un control sobre la activación.

Las entradas de control de acceso (ACE) de permiso de inicio se dividen en cuatro derechos de acceso:

-   Inicio local (LL)
-   Inicio remoto (RL)
-   Activación local (LA)
-   Activación remota (RA)

El descriptor de seguridad de permiso de acceso se divide en dos derechos de acceso:

-   Llamadas de acceso local (LC)
-   Llamadas de acceso remoto (RC)

Esto permite al administrador aplicar configuraciones de seguridad muy específicas. Por ejemplo, puede configurar un servidor COM para que acepte llamadas de acceso local de todos los usuarios, mientras que solo acepta llamadas de acceso remoto de los administradores. Estas distinciones se pueden especificar a través de los cambios en los descriptores de seguridad de los permisos COM.

### <a name="why-is-this-change-important-what-threats-does-it-help-mitigate"></a>¿Por qué es importante este cambio? ¿Qué amenazas ayuda a mitigar?

Las versiones anteriores de la aplicación del servidor COM no tienen ninguna manera de restringir una aplicación para que solo se pueda usar de forma local sin exponer la aplicación en la red mediante DCOM. Cuando un usuario tiene acceso a una aplicación de servidor COM, tiene acceso para uso local y remoto.

Una aplicación de servidor COM podría exponerse a usuarios no autenticados para implementar un escenario de devolución de llamada COM. En este escenario, la aplicación también debe exponer su activación a usuarios no autenticados, lo que podría no ser deseable.

Los permisos COM precisos proporcionan flexibilidad al administrador para controlar la Directiva de permisos COM de un equipo. Estos permisos habilitan la seguridad de los escenarios descritos.

### <a name="what-works-differently-are-there-any-dependencies"></a>¿Qué funciona de manera diferente? ¿Hay alguna dependencia?

Para proporcionar compatibilidad con versiones anteriores, los descriptores de seguridad COM existentes se interpretan para permitir o denegar simultáneamente el acceso local y remoto. Es decir, una entrada de control de acceso (ACE) permite tanto local como remota, o deniega tanto local como remoto.

No hay ningún problema de compatibilidad con versiones anteriores para los derechos de llamada o de inicio. Sin embargo, hay un problema de compatibilidad con los derechos de activación. Si en los descriptores de seguridad existentes para un servidor COM, los permisos de inicio configurados son más restrictivos que los permisos de acceso y son más restrictivos que los mínimos necesarios para los escenarios de activación de cliente, se debe modificar la ACL de permisos de inicio para conceder a los clientes autorizados los permisos de activación adecuados.

En el caso de las aplicaciones COM que usan la configuración de seguridad predeterminada, no hay ningún problema de compatibilidad. En el caso de las aplicaciones que se inician dinámicamente con la activación COM, la mayoría de ellos no tienen problemas de compatibilidad, porque los permisos de inicio ya deben incluir cualquier persona que pueda activar un objeto. De lo contrario, estas aplicaciones generan errores de activación incluso antes de aplicar Windows XP SP2 o Windows Server 2003 SP1, cuando los autores de llamadas sin permiso de inicio intenten activar un objeto y el servidor COM no se esté ejecutando todavía.

Las aplicaciones de mayor preocupación para los problemas de compatibilidad son las aplicaciones COM que ya están iniciadas por otro mecanismo, como el explorador de Windows o el administrador de control de servicios. También puede iniciar estas aplicaciones mediante una activación COM anterior, que invalida los permisos de acceso y de inicio predeterminados y especifica permisos de inicio que son más restrictivos que los permisos de llamada. Para obtener más información acerca de cómo solucionar este problema de compatibilidad, vea "Cómo resolver estos problemas?". en la sección siguiente.

Si un sistema actualizado a Windows XP SP2 o Windows Server 2003 SP1 se revierte a un estado anterior, cualquier ACE que se editó para permitir el acceso local, el acceso remoto o ambos, se interpreta para permitir el acceso local y remoto. Cualquier ACE que se editó para denegar el acceso local, el acceso remoto o ambos, se interpreta para denegar el acceso local y remoto. Siempre que desinstale un Service Pack, debe asegurarse de que ninguna ACE recién establecida cause que las aplicaciones dejen de funcionar.

### <a name="how-do-i-resolve-these-issues"></a>¿Cómo resolver estos problemas?

Si implementa un servidor COM y invalida la configuración de seguridad predeterminada, confirme que la ACL permisos de inicio específicos de la aplicación conceda el permiso de activación a los usuarios adecuados. Si no es así, debe cambiar la ACL de permiso de inicio específica de la aplicación para conceder los derechos de activación de los usuarios adecuados para que las aplicaciones y los componentes de Windows que usan DCOM no generen errores. Estos permisos de inicio específicos de la aplicación se almacenan en el registro.

Las ACL de COM se pueden crear o modificar mediante las funciones de seguridad normales.

## <a name="what-settings-are-added-or-changed-in-windows-xp-service-pack-2"></a>¿Qué valores se agregan o cambian en Windows XP Service Pack 2?

> [!Caution]  
> El uso incorrecto de esta configuración puede provocar errores en las aplicaciones y los componentes de Windows que usan DCOM.

 

En la tabla siguiente se usan estas abreviaturas:

LL: Inicio local

Activación local

RL: inicio remoto

RA: activación remota

Llamadas de acceso local de LC

RC: llamadas de acceso remoto

Lista de Access Control ACL



| Nombre del valor                                                                                         | Location                                                                                                       | Valor predeterminado anterior                                                                                                                                                                     | Valor predeterminado                                                                                                                                                                                                                                                                                                                                                             | Valores posibles                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MachineLaunchRestriction**<br/>                                                              | **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**<br/>                                                 | Todos: LL, LA, RL, RA<br/> Anonymous<br/> LL, LA, RL, RA<br/> (Se trata de una nueva clave del registro. En función del comportamiento existente, estos son los valores efectivos).<br/> | Administrador: LL, LA, RL, RA<br/>                                                                                                                                                                                                                                                                                                                                  | ACL<br/>                                                                                                                                                                                                               |
| **MachineAccessRestriction**<br/>                                                              | **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**<br/>                                                 | Todos los usuarios: LC, RC<br/> Anonymous-LC, RC<br/> (Se trata de una nueva clave del registro. En función del comportamiento existente, estos son los valores efectivos).<br/>                            | Todos: LC, RC<br/> Anónimo: LC<br/>                                                                                                                                                                                                                                                                                                                      | ACL<br/>                                                                                                                                                                                                               |
| **CallFailureLoggingLevel**<br/>                                                               | **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**<br/>                                                 | No es aplicable.<br/>                                                                                                                                                                 | Esta clave del registro no está presente; sin embargo, una clave o un valor que falta se interpreta como 2.<br/> Este evento no se registra de forma predeterminada. Si cambia este valor a 1 para iniciar el registro de esta información para ayudarle a solucionar un problema, asegúrese de supervisar el tamaño del registro de eventos, ya que se trata de un evento que puede generar un gran número de entradas.<br/> | 1-registrar siempre errores de registro de eventos durante una llamada en el proceso de servidor COM.<br/> 2-no registrar nunca errores en el registro de eventos durante una llamada en el proceso del servidor de llamada.<br/>                                                  |
| **InvalidSecurityDescriptorLoggingLevel**<br/>                                                 | **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**<br/>                                                 | No es aplicable.<br/>                                                                                                                                                                 | Esta clave del registro no está presente; sin embargo, una clave o un valor que falta se interpreta como 1.<br/> Este evento se registra de forma predeterminada. Raramente se produce.<br/>                                                                                                                                                                                                    | 1-registrar siempre errores de registro de eventos cuando la infraestructura COM encuentra un descriptor de seguridad no válido.<br/> 2-no registrar nunca errores en el registro de eventos cuando la infraestructura COM encuentra un descriptor de seguridad no válido.<br/> |
| DCOM: restricciones de inicio del equipo en la sintaxis del lenguaje de definición de descriptores de seguridad (SDDL)<br/> | (Objeto directiva de grupo) Configuración del equipo Configuración de \\ Windows \\ Opciones de seguridad Directivas locales \\<br/>  | No es aplicable.<br/>                                                                                                                                                                 | No definida<br/>                                                                                                                                                                                                                                                                                                                                                    | Lista de control de acceso en formato SDDL. La existencia de esta directiva invalida los valores de MachineLaunchRestriction, anteriormente.<br/>                                                                                            |
| DCOM: restricciones de acceso a la máquina en la sintaxis del lenguaje de definición de descriptores de seguridad (SDDL)<br/> | (Objeto directiva de grupo) Configuración del equipo Configuración de \\ Windows \\ Opciones de seguridad Directivas locales \\<br/> | No es aplicable.<br/>                                                                                                                                                                 | No definida<br/>                                                                                                                                                                                                                                                                                                                                                    | Lista de control de acceso en formato SDDL. La existencia de esta directiva invalida los valores de MachineAccessRestriction, anteriormente.<br/>                                                                                            |



 

## <a name="what-settings-are-added-or-changed-in-windows-server-2003-service-pack-1"></a>¿Qué configuraciones se agregan o cambian en Windows Server 2003 Service Pack 1?

> [!Note]  
> El uso incorrecto de esta configuración puede provocar errores en las aplicaciones y los componentes de Windows que usan DCOM.

 

En la tabla siguiente se usan estas abreviaturas:

LL: Inicio local

Activación local

RL: inicio remoto

RA: activación remota

Llamadas de acceso local de LC

RC: llamadas de acceso remoto

Lista de Access Control ACL



| Nombre del valor                                                                                         | Location                                                                                                       | Valor predeterminado anterior                                                                                                                                                             | Valor predeterminado                                                                                                                                                                                                                                                                                                                                                             | Valores posibles                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MachineLaunchRestriction**<br/>                                                              | **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**<br/>                                                 | Todos: LL, LA, RL, RA<br/> Anónimo: LL, LA, RL, RA<br/> (Se trata de una nueva clave del registro. En función del comportamiento existente, estos serían los valores efectivos).<br/> | Administrador: LL, LA, RL, RA<br/> Todos: LL, LA<br/> Usuarios COM distribuidos: LL, LA, RL, RA<br/>                                                                                                                                                                                                                                                     | ACL<br/>                                                                                                                                                                                                               |
| **MachineAccessRestriction**<br/>                                                              | **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**<br/>                                                 | Todos: LC, RC<br/> Anónimo: LC, RC<br/> (Se trata de una nueva clave del registro. En función del comportamiento existente, estos serían los valores efectivos).<br/>                 | Todos: LC, RC<br/> Anónimo: LC, RC<br/>                                                                                                                                                                                                                                                                                                                  | ACL<br/>                                                                                                                                                                                                               |
| **CallFailureLoggingLevel**<br/>                                                               | **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**<br/>                                                 | No es aplicable.<br/>                                                                                                                                                         | Esta clave del registro no está presente; sin embargo, una clave o un valor que falta se interpreta como 2.<br/> Este evento no se registra de forma predeterminada. Si cambia este valor a 1 para iniciar el registro de esta información para ayudarle a solucionar un problema, asegúrese de supervisar el tamaño del registro de eventos, ya que se trata de un evento que puede generar un gran número de entradas.<br/> | 1-registrar siempre errores de registro de eventos cuando la infraestructura COM encuentra un descriptor de seguridad no válido.<br/> 2-no registrar nunca errores en el registro de eventos cuando la infraestructura COM encuentra un descriptor de seguridad no válido.<br/> |
| **InvalidSecurityDescriptorLoggingLevel**<br/>                                                 | **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**<br/>                                                 | No es aplicable.<br/>                                                                                                                                                         | Esta clave del registro no está presente; sin embargo, una clave o un valor que falta se interpreta como 1.<br/> Este evento se registra de forma predeterminada. Raramente se produce.<br/>                                                                                                                                                                                                    | 1-registrar siempre errores de registro de eventos cuando la infraestructura COM encuentra un descriptor de seguridad no válido.<br/> 2-no registrar nunca errores en el registro de eventos cuando la infraestructura COM encuentra un descriptor de seguridad no válido.<br/>         |
| DCOM: restricciones de inicio del equipo en la sintaxis del lenguaje de definición de descriptores de seguridad (SDDL)<br/> | (Objeto directiva de grupo) Configuración del equipo Configuración de \\ Windows \\ Opciones de seguridad Directivas locales \\<br/> | No es aplicable.<br/>                                                                                                                                                         | Sin definir.<br/>                                                                                                                                                                                                                                                                                                                                                   | Lista de control de acceso en formato SDDL. La existencia de esta directiva invalida los valores de MachineLaunchRestriction, anteriormente.<br/>                                                                                            |
| DCOM: restricciones de acceso a la máquina en la sintaxis del lenguaje de definición de descriptores de seguridad (SDDL)<br/> | (Objeto directiva de grupo) Configuración del equipo Configuración de \\ Windows \\ Opciones de seguridad Directivas locales \\<br/> | No es aplicable.<br/>                                                                                                                                                         | Sin definir.<br/>                                                                                                                                                                                                                                                                                                                                                   | Lista de control de acceso en formato SDDL. La existencia de esta directiva invalida los valores de MachineAccessRestriction, anteriormente.<br/>                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

