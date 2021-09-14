---
title: Establecer System-Wide seguridad mediante DCOMCNFG
description: Si desea que todas las aplicaciones de un equipo que no proporcionan su propia seguridad compartan la misma configuración de seguridad predeterminada, establecería la seguridad en todo el sistema.
ms.assetid: 23d1e222-c00b-497c-adc8-4ae14c5bdd98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7feaaf356263a48c2c93eb9b3b3764b7352cd39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361704"
---
# <a name="setting-system-wide-security-using-dcomcnfg"></a>Establecer System-Wide seguridad mediante DCOMCNFG

El cambio de la configuración de seguridad de todo el sistema afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso. Esto puede impedir que estas aplicaciones funcionen correctamente. Si va a cambiar la configuración de seguridad de todo el sistema para que afecte a la configuración de seguridad de una aplicación COM determinada, en su lugar debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM concreta. Para obtener más información sobre cómo establecer la seguridad de todo el proceso, vea [Establecer la seguridad en todo el proceso.](setting-processwide-security.md)

Si desea que todas las aplicaciones de un equipo que no proporcionan su propia seguridad compartan la misma configuración de seguridad predeterminada, establecería la seguridad en todo el sistema. El Dcomcnfg.exe facilita la configuración de valores predeterminados en el Registro que se aplican a todas las aplicaciones de un equipo.

Es importante comprender que si el cliente o servidor llama explícitamente a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer la seguridad de todo el proceso, se omitirá la configuración predeterminada en el Registro y los parámetros de **CoInitializeSecurity** se usarán en su lugar para la configuración de seguridad del proceso. Además, si usa Dcomcnfg.exe configuración de seguridad para un proceso determinado, la configuración predeterminada del equipo se reemplaza por la configuración del proceso.

Al habilitar la seguridad en todo el sistema, debe establecer el nivel de autenticación en un valor distinto de Ninguno y debe establecer los permisos de inicio y acceso. Tiene la opción de establecer el nivel de suplantación predeterminado y también puede habilitar el seguimiento de referencias. En los temas siguientes se proporcionan procedimientos paso a paso:

-   [Establecer System-Wide nivel de autenticación predeterminado](#setting-system-wide-default-authentication-level)
-   [Establecer System-Wide permisos de inicio](#setting-system-wide-launch-permissions)
-   [Establecer System-Wide permisos de acceso](#setting-system-wide-access-permissions)
-   [Establecer System-Wide nivel de suplantación](#setting-system-wide-impersonation-level)
-   [Configuración del System-Wide de referencia](#setting-system-wide-reference-tracking)
-   [Habilitación y deshabilitación de DCOM](#enabling-and-disabling-dcom)
-   [Temas relacionados](#related-topics)

## <a name="setting-system-wide-default-authentication-level"></a>Establecer System-Wide nivel de autenticación predeterminado

El nivel de autenticación se usa para decir a COM en qué nivel quiere que se autentique el cliente. Estos niveles ofrecen varios niveles de protección, desde la no protección hasta el cifrado completo. Para habilitar la seguridad de un equipo, debe elegir un nivel de autenticación distinto de Ninguno. Puede elegir este tipo de configuración, mediante Dcomcnfg.exe, completando los pasos siguientes.

**Para establecer el nivel de autenticación en todo el sistema**

1.  Ejecute Dcomcnfg.exe.

2.  Elija la **pestaña Propiedades predeterminadas.**

3.  En el **cuadro de lista Nivel de autenticación** predeterminada, elija un valor distinto de **(Ninguno).**

4.  Si va a establecer más propiedades para el equipo, haga clic en el botón **Aplicar** para aplicar el nuevo nivel de autenticación. De lo contrario, **haga clic en** Aceptar para aplicar los cambios y salir Dcomcnfg.exe.

## <a name="setting-system-wide-launch-permissions"></a>Establecer System-Wide permisos de inicio

Los permisos de inicio que establece con Dcomcnfg.exe determinan una lista de usuarios, a cada uno de los cuales se le concede o se deniega explícitamente el permiso para iniciar cualquier servidor que no proporcione su propia configuración de permisos de inicio. Al establecer permisos de inicio, puede agregar o quitar uno o varios usuarios o grupos de esta lista. Para cada usuario que agregue, debe especificar si se concede o se deniega el permiso de inicio al usuario.

**Para establecer permisos de inicio para un equipo**

1.  En la **página de propiedades Seguridad** predeterminada  Dcomcnfg.exe, elija el botón Editar valor predeterminado en el área Permisos de **inicio predeterminados.**

2.  Para quitar usuarios o grupos, seleccione el usuario o grupo que desea quitar y elija el **botón** Quitar. El usuario o grupo seleccionado ya no aparecerá en el cuadro de lista. Cuando haya terminado de quitar usuarios y grupos, elija **Aceptar.**

3.  Si desea agregar un usuario o grupo, elija el **botón** Agregar.

4.  Si conoce el nombre de usuario completo que desea agregar, escriba en el **cuadro de** texto Agregar nombres. Si no conoce el nombre de usuario, consulte Establecer la seguridad de todo el proceso **mediante DCOMCNFG** para encontrarlo. Cuando haya ubicado el nombre de usuario, seleccione el usuario o grupo en el cuadro **de** lista Nombres y elija el **botón** Agregar.

5.  En el **cuadro de lista Tipo** de acceso, seleccione el tipo de acceso **(Permitir inicio** o Denegar **inicio).** Para agregar otros usuarios que también tendrán el tipo de acceso seleccionado, repita el paso 4. Cuando haya terminado de agregar usuarios para el tipo de acceso seleccionado, elija el **botón** Aceptar.

6.  Para agregar usuarios que tendrán un tipo de acceso diferente, repita los pasos 4 y 5. De lo contrario, **elija Aceptar** para aplicar los cambios.

## <a name="setting-system-wide-access-permissions"></a>Establecer System-Wide permisos de acceso

Dcomcnfg.exe permite establecer permisos de acceso para controlar la lista de usuarios a los que se concede o deniega el acceso a los métodos de esos servidores que no proporcionan sus propios permisos de acceso. Puede agregar usuarios o grupos a la lista, especificando si se concede o se deniega el permiso de acceso. También puede quitar usuarios de la lista.

Al establecer permisos de acceso, debe asegurarse de que SYSTEM se incluye en la lista de usuarios a los que se concede acceso. Si ha concedido permisos de acceso a Todos, SYSTEM se incluye implícitamente.

El proceso de configuración de permisos de acceso para un equipo es similar a establecer los permisos de inicio. Se deben realizar los pasos siguientes.

**Para establecer permisos de acceso para un equipo**

1.  En la **página de propiedades Seguridad** predeterminada  Dcomcnfg.exe, elija el botón Editar predeterminado en el área Permisos de **acceso predeterminados.**

2.  Para quitar usuarios o grupos, seleccione el usuario o grupo que desea quitar y elija el **botón** Quitar. El usuario o grupo seleccionado ya no aparecerá en el cuadro de lista. Cuando haya terminado de quitar usuarios y grupos, elija **Aceptar.**

3.  Si desea agregar un usuario o un grupo, elija el **botón** Agregar.

4.  Si conoce el nombre de usuario completo que desea agregar, escriba en el **cuadro de** texto Agregar nombres. Si no conoce el nombre de usuario, vea Establecer la seguridad de todo el proceso [mediante DCOMCNFG](setting-processwide-security-using-dcomcnfg.md) para encontrarlo. Cuando haya ubicado el nombre de usuario, seleccione el usuario o grupo en el cuadro **de** lista Nombres y elija el **botón** Agregar.

5.  En el **cuadro de lista Tipo** de acceso, seleccione el tipo de acceso **(Permitir acceso** o Denegar **acceso).** Para agregar otros usuarios que tendrán el tipo de acceso seleccionado, repita el paso 4. Cuando haya terminado de agregar usuarios para el tipo de acceso seleccionado, elija el **botón** Aceptar.

6.  Para agregar usuarios que tendrán un tipo de acceso diferente, repita los pasos 4 y 5. De lo contrario, **elija Aceptar** para aplicar los cambios.

## <a name="setting-system-wide-impersonation-level"></a>Establecer System-Wide nivel de suplantación

El nivel de suplantación, establecido por el cliente, determina la cantidad de autoridad dada al servidor para actuar en nombre del cliente. Por ejemplo, cuando el cliente ha establecido su nivel de suplantación en delegado, el servidor puede acceder a los recursos locales y remotos como el cliente y el servidor puede traspasar varios límites del equipo si se establece la funcionalidad de protección. Para ayudar a determinar el nivel de suplantación que debe elegir, vea [Niveles de suplantación](impersonation-levels.md) y [Arroba.](cloaking.md)

Al establecer el nivel de suplantación predeterminado para todo el equipo, se indica a COM qué nivel de suplantación se debe usar cuando un cliente determinado del equipo no especifica un nivel de suplantación mediante programación mediante [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

**Para establecer el nivel de suplantación de un equipo**

1.  Cuando Dcomcnfg.exe, elija la **pestaña Propiedades predeterminadas.**

2.  En el **cuadro de lista Nivel** de suplantación predeterminado , elija el nivel de suplantación que desee.

3.  Si va a establecer más propiedades para el equipo, elija el botón **Aplicar** para aplicar el nuevo nivel de suplantación. En caso contrario, **elija Aceptar** para aplicar los cambios y salir Dcomcnfg.exe.

## <a name="setting-system-wide-reference-tracking"></a>Configuración del System-Wide de referencia

Al habilitar el seguimiento de referencias, pide a COM que realice comprobaciones de seguridad adicionales y que realice un seguimiento de la información que evitará que los objetos se liberan demasiado pronto. Tenga en cuenta que estas comprobaciones adicionales son costosas. Para obtener más información sobre el seguimiento de referencias, vea [Seguimiento de referencias.](reference-tracking.md) Siga estos pasos para habilitar o deshabilitar el seguimiento de referencias.

**Para establecer el seguimiento de referencias de un equipo**

1.  Cuando Dcomcnfg.exe, elija la **pestaña Propiedades predeterminadas.**

2.  Para habilitar (o deshabilitar) el seguimiento de referencias, active (o desactive) la casilla Proporcionar seguridad adicional para el seguimiento de **referencias** cerca de la parte inferior de la página.

3.  Si va a establecer más propiedades para el equipo, elija el **botón** Aplicar para aplicar la nueva configuración. En caso contrario, **elija Aceptar** para aplicar los cambios y salir Dcomcnfg.exe.

## <a name="enabling-and-disabling-dcom"></a>Habilitación y deshabilitación de DCOM

Cuando un equipo forma parte de una red, el protocolo de conexión DCOM permite que los objetos COM de ese equipo se comuniquen con objetos COM en otros equipos. Puede deshabilitar DCOM para un equipo determinado, pero al hacerlo se deshabilitará toda la comunicación entre los objetos de ese equipo y los objetos de otros equipos.

Deshabilitar DCOM en un equipo no tiene ningún efecto en los objetos COM locales. COM sigue buscando los permisos de inicio que ha especificado. Si no se ha especificado ningún permiso de inicio, se usan los permisos de inicio predeterminados. Aunque deshabilite DCOM, si un usuario tiene acceso físico al equipo, podría iniciar un servidor en el equipo a menos que establezca permisos de inicio que no lo permitan.

> [!Note]  
> Si deshabilita DCOM en un equipo remoto, no podrá acceder a ese equipo de forma remota después para volver a habilitar DCOM. Para volver a habilitar DCOM, necesitará acceso físico a ese equipo.

 

**Para habilitar o deshabilitar manualmente DCOM para un equipo**

1.  Ejecute Dcomcnfg.exe.

2.  Elija la **pestaña Propiedades predeterminadas.**

3.  Active (o desactive) la **casilla Habilitar COMÂ distribuido en este** equipo.

4.  Si va a establecer más propiedades para el equipo, haga clic en el botón **Aplicar** para habilitar (o deshabilitar) DCOM. De lo contrario, **haga clic en** Aceptar para aplicar los cambios y salir Dcomcnfg.exe.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad en todo el proceso](setting-processwide-security.md)
</dt> </dl>

 

 




