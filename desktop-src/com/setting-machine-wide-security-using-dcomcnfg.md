---
title: Establecer la seguridad de System-Wide mediante DCOMCNFG
description: Si desea que todas las aplicaciones de un equipo que no proporcionan su propia seguridad compartan la misma configuración de seguridad predeterminada, debe establecer la seguridad en todo el sistema.
ms.assetid: 23d1e222-c00b-497c-adc8-4ae14c5bdd98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7feaaf356263a48c2c93eb9b3b3764b7352cd39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418916"
---
# <a name="setting-system-wide-security-using-dcomcnfg"></a>Establecer la seguridad de System-Wide mediante DCOMCNFG

El cambio de la configuración de seguridad de todo el sistema afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso. Esto puede impedir que dichas aplicaciones funcionen correctamente. Si va a cambiar la configuración de seguridad de todo el sistema para que afecte a la configuración de seguridad de una aplicación COM determinada, debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM en particular. Para obtener más información acerca de cómo establecer la seguridad de todo el proceso, consulte [configuración de la seguridad de todo el proceso](setting-processwide-security.md).

Si desea que todas las aplicaciones de un equipo que no proporcionan su propia seguridad compartan la misma configuración de seguridad predeterminada, debe establecer la seguridad en todo el sistema. El uso de Dcomcnfg.exe facilita el establecimiento de valores predeterminados en el registro que se aplican a todas las aplicaciones de un equipo.

Es importante comprender que si el cliente o el servidor llama explícitamente a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer la seguridad de todo el proceso, se omitirá la configuración predeterminada del registro y se usarán los parámetros para **CoInitializeSecurity** en lugar de la configuración de seguridad para el proceso. Además, si utiliza Dcomcnfg.exe para especificar la configuración de seguridad para un proceso determinado, la configuración predeterminada del equipo es invalidada por la configuración del proceso.

Al habilitar la seguridad en todo el sistema, debe establecer el nivel de autenticación en un valor distinto de ninguno y debe establecer los permisos de acceso y de inicio. Tiene la opción de establecer el nivel de suplantación predeterminado y también puede habilitar el seguimiento de referencias. En los temas siguientes se proporcionan procedimientos paso a paso:

-   [Establecer System-Wide nivel de autenticación predeterminado](#setting-system-wide-default-authentication-level)
-   [Configuración de los permisos de inicio de System-Wide](#setting-system-wide-launch-permissions)
-   [Configuración de permisos de acceso System-Wide](#setting-system-wide-access-permissions)
-   [Establecer System-Wide nivel de suplantación](#setting-system-wide-impersonation-level)
-   [Configuración del seguimiento de referencia de System-Wide](#setting-system-wide-reference-tracking)
-   [Habilitar y deshabilitar DCOM](#enabling-and-disabling-dcom)
-   [Temas relacionados](#related-topics)

## <a name="setting-system-wide-default-authentication-level"></a>Establecer System-Wide nivel de autenticación predeterminado

El nivel de autenticación se utiliza para indicar a COM en qué nivel desea que se autentique el cliente. Estos niveles ofrecen varios niveles de protección, desde sin protección hasta el cifrado completo. Para habilitar la seguridad de un equipo, debe elegir un nivel de autenticación distinto de ninguno. Puede elegir esta opción, mediante Dcomcnfg.exe, completando los pasos siguientes.

**Para establecer el nivel de autenticación para todo el sistema**

1.  Ejecute Dcomcnfg.exe.

2.  Elija la pestaña **propiedades predeterminadas** .

3.  En el cuadro de lista **nivel de AuthenticationÂ de DefaultÂ** , elija un valor distinto de **(ninguno)**.

4.  Si va a establecer más propiedades para el equipo, haga clic en el botón **aplicar** para aplicar el nuevo nivel de autenticación. De lo contrario, haga clic en **Aceptar** para aplicar los cambios y salir del Dcomcnfg.exe.

## <a name="setting-system-wide-launch-permissions"></a>Configuración de los permisos de inicio de System-Wide

Los permisos de inicio que se establecen con Dcomcnfg.exe determinan una lista de usuarios, cada uno de los cuales tiene permisos concedidos o denegados explícitamente para iniciar cualquier servidor que no proporcione su propia configuración de los permisos de inicio. Al establecer los permisos de inicio, puede Agregar o quitar uno o varios usuarios o grupos de esta lista. Para cada usuario que agregue, debe especificar si se concede o se deniega el permiso de inicio al usuario.

**Para establecer los permisos de inicio de un equipo**

1.  En la página de propiedades **seguridad predeterminada** de Dcomcnfg.exe, elija el botón **Editar predeterminado** en el área **permisos de inicio predeterminados** .

2.  Para quitar usuarios o grupos, seleccione el usuario o grupo que desea quitar y elija el botón **quitar** . El usuario o grupo seleccionado ya no aparecerá en el cuadro de lista. Cuando haya terminado de quitar usuarios y grupos, elija **Aceptar**.

3.  Si desea agregar un usuario o un grupo, elija el botón **Agregar** .

4.  Si conoce el nombre de usuario completo que desea agregar, escríbalo en el cuadro de texto **Agregar nombres** . Si no conoce el nombre de usuario, consulte Configuración de la **seguridad de Processwide con DCOMCNFG** para encontrarlo. Cuando haya encontrado el nombre de usuario, seleccione el usuario o grupo en el cuadro de lista **nombres** y elija el botón **Agregar** .

5.  En el cuadro **de lista tipo de acceso** , seleccione el tipo de acceso ( **permitir** iniciar o **denegar el inicio**). Para agregar otros usuarios que también tendrán el tipo de acceso seleccionado, repita el paso 4. Cuando haya terminado de agregar usuarios para el tipo de acceso seleccionado, elija el botón **Aceptar** .

6.  Para agregar usuarios que tengan un tipo de acceso diferente, repita los pasos 4 y 5. De lo contrario, elija **Aceptar** para aplicar los cambios.

## <a name="setting-system-wide-access-permissions"></a>Configuración de permisos de acceso System-Wide

Dcomcnfg.exe le permite establecer permisos de acceso para controlar la lista de usuarios a los que se concede o deniega el acceso a los métodos de los servidores que no proporcionan sus propios permisos de acceso. Puede Agregar usuarios o grupos a la lista, especificando si se concede o se deniega el permiso de acceso. También puede quitar usuarios de la lista.

Al establecer los permisos de acceso, debe asegurarse de que el sistema está incluido en la lista de usuarios a los que se concede acceso. Si ha concedido permisos de acceso a todos, el sistema se incluye implícitamente.

El proceso de configuración de permisos de acceso para un equipo es similar al establecimiento de permisos de inicio. Se deben realizar los siguientes pasos.

**Para establecer permisos de acceso para un equipo**

1.  En la página de propiedades **seguridad predeterminada** de Dcomcnfg.exe, elija el botón **Editar predeterminado** en el área **permisos de acceso predeterminados** .

2.  Para quitar usuarios o grupos, seleccione el usuario o grupo que desea quitar y elija el botón **quitar** . El usuario o grupo seleccionado ya no aparecerá en el cuadro de lista. Cuando haya terminado de quitar usuarios y grupos, elija **Aceptar**.

3.  Si desea agregar un usuario o un grupo, elija el botón **Agregar** .

4.  Si conoce el nombre de usuario completo que desea agregar, escríbalo en el cuadro de texto **Agregar nombres** . Si no conoce el nombre de usuario, consulte Configuración de la [seguridad de todo el proceso mediante DCOMCNFG](setting-processwide-security-using-dcomcnfg.md) para encontrarlo. Cuando haya encontrado el nombre de usuario, seleccione el usuario o grupo en el cuadro de lista **nombres** y elija el botón **Agregar** .

5.  En el cuadro **de lista tipo de acceso** , seleccione el tipo de acceso ( **permitir acceso** o **denegar acceso**). Para agregar otros usuarios que tendrán el tipo de acceso seleccionado, repita el paso 4. Cuando haya terminado de agregar usuarios para el tipo de acceso seleccionado, elija el botón **Aceptar** .

6.  Para agregar usuarios que tengan un tipo de acceso diferente, repita los pasos 4 y 5. De lo contrario, elija **Aceptar** para aplicar los cambios.

## <a name="setting-system-wide-impersonation-level"></a>Establecer System-Wide nivel de suplantación

El nivel de suplantación, establecido por el cliente, determina la cantidad de autoridad asignada al servidor para que actúe en nombre del cliente. Por ejemplo, cuando el cliente ha establecido su nivel de suplantación en Delegate, el servidor puede tener acceso a los recursos locales y remotos como el cliente y el servidor puede esconder varios límites de equipo si se establece la capacidad de cloaking. Para ayudar a determinar qué nivel de suplantación debe elegir, vea [niveles de suplantación](impersonation-levels.md) y [Cloaking](cloaking.md).

Al establecer el nivel de suplantación predeterminado para todo el equipo, se indica a COM qué nivel de suplantación se debe utilizar cuando un cliente determinado del equipo no especifica un nivel de suplantación mediante programación con [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

**Para establecer el nivel de suplantación de un equipo**

1.  Con Dcomcnfg.exe en ejecución, elija la pestaña **propiedades predeterminadas** .

2.  En el cuadro de lista **nivel de suplantación predeterminado** , elija el nivel de suplantación que desee.

3.  Si va a establecer más propiedades para el equipo, elija el botón **aplicar** para aplicar el nuevo nivel de suplantación. De lo contrario, elija **Aceptar** para aplicar los cambios y salir de Dcomcnfg.exe.

## <a name="setting-system-wide-reference-tracking"></a>Configuración del seguimiento de referencia de System-Wide

Al habilitar el seguimiento de referencias, se pide a COM que realice comprobaciones de seguridad adicionales y realice un seguimiento de la información que evitará que los objetos se liberen demasiado pronto. Tenga en cuenta que estas comprobaciones adicionales son costosas. Para obtener más información sobre el seguimiento de referencias, vea [seguimiento de referencias](reference-tracking.md). Siga estos pasos para habilitar o deshabilitar el seguimiento de referencias.

**Para establecer el seguimiento de referencia de un equipo**

1.  Con Dcomcnfg.exe en ejecución, elija la pestaña **propiedades predeterminadas** .

2.  Para habilitar (o deshabilitar) el seguimiento de referencia, Active o desactive la casilla **proporcionar seguridad adicional para el seguimiento de referencias** cerca de la parte inferior de la página.

3.  Si va a establecer más propiedades para el equipo, elija el botón **aplicar** para aplicar la nueva configuración. De lo contrario, elija **Aceptar** para aplicar los cambios y salir de Dcomcnfg.exe.

## <a name="enabling-and-disabling-dcom"></a>Habilitar y deshabilitar DCOM

Cuando un equipo forma parte de una red, el protocolo de conexión DCOM permite que los objetos COM de ese equipo se comuniquen con objetos COM en otros equipos. Puede deshabilitar DCOM para un equipo determinado, pero si lo hace, se deshabilitará toda la comunicación entre los objetos de ese equipo y los objetos de otros equipos.

Deshabilitar DCOM en un equipo no tiene ningún efecto en los objetos COM locales. COM sigue buscando los permisos de inicio que ha especificado. Si no se ha especificado ningún permiso de inicio, se usan los permisos de inicio predeterminados. Aunque deshabilite DCOM, si un usuario tiene acceso físico al equipo, podría iniciar un servidor en el equipo a menos que establezca permisos de inicio para no permitirlo.

> [!Note]  
> Si deshabilita DCOM en un equipo remoto, no podrá obtener acceso remoto a ese equipo posteriormente para volver a habilitar DCOM. Para volver a habilitar DCOM, necesitará acceso físico a ese equipo.

 

**Para habilitar (o deshabilitar) DCOM manualmente para un equipo**

1.  Ejecute Dcomcnfg.exe.

2.  Elija la pestaña **propiedades de DefaultÂ** .

3.  Active o desactive la casilla **Habilitar Distributed COMÂ en este equipo** .

4.  Si va a establecer más propiedades para el equipo, haga clic en el botón **aplicar** para habilitar (o deshabilitar) DCOM. De lo contrario, haga clic en **Aceptar** para aplicar los cambios y salir del Dcomcnfg.exe.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad de todo el proceso](setting-processwide-security.md)
</dt> </dl>

 

 




