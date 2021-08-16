---
title: Establecer Process-Wide seguridad mediante DCOMCNFG
description: Es posible que quiera habilitar la seguridad para una aplicación determinada si una aplicación tiene necesidades de seguridad que son diferentes de las que requieren otras aplicaciones en el equipo.
ms.assetid: 04a7f688-78a3-490a-bcfa-862824a05422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ace37c685748983d36b8a1e27a406fb8a81034d82ab793e77c4def960dfa2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309110"
---
# <a name="setting-process-wide-security-using-dcomcnfg"></a>Establecer Process-Wide seguridad mediante DCOMCNFG

Es posible que quiera habilitar la seguridad para una aplicación determinada si una aplicación tiene necesidades de seguridad que son diferentes de las que requieren otras aplicaciones en el equipo. Por ejemplo, puede decidir usar la configuración de todo el sistema para las aplicaciones que requieren un bajo nivel de seguridad al establecer un mayor nivel de seguridad para una aplicación determinada.

Sin embargo, a veces no se usa la configuración de seguridad en el Registro que se aplica a una aplicación determinada. Por ejemplo, la configuración de todo el proceso que establezca en el Registro mediante Dcomcnfg.exe se invalidará si un cliente llama a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) para establecer la seguridad de un proxy de interfaz determinado. De forma similar, si un cliente o servidor (o ambos) llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer la seguridad de un proceso, se omitirá la configuración del Registro y se usarán en su lugar los parámetros especificados en **CoInitializeSecurity.**

Al habilitar la seguridad de una aplicación, es posible que sea necesario modificar varias configuraciones. Estos incluyen el nivel de autenticación, la ubicación, los permisos de inicio, los permisos de acceso y la identidad. Para ver los procedimientos paso a paso, consulte lo siguiente:

-   [Establecer el nivel de autenticación de una aplicación](#setting-the-authentication-level-for-an-application)
-   [Establecer la ubicación de una aplicación](#setting-the-location-for-an-application)
-   [Establecer permisos de inicio para una aplicación](#setting-launch-permissions-for-an-application)
-   [Establecer permisos de acceso para una aplicación](#setting-access-permissions-for-an-application)
-   [Establecer la identidad de una aplicación](#setting-the-identity-for-an-application)
-   [Examinar la base de datos de usuario](#browsing-the-user-database)
-   [Dcomcnfg.exe y aplicaciones de 64 bits](#dcomcnfgexe-and-64-bit-applications)
-   [Temas relacionados](#related-topics)

## <a name="setting-the-authentication-level-for-an-application"></a>Establecer el nivel de autenticación de una aplicación

Para habilitar la seguridad de una aplicación, debe establecer un nivel de autenticación distinto de Ninguno. El nivel de autenticación indica a COM cuánta protección de autenticación se requiere y puede abarcar desde la autenticación del cliente en la primera llamada de método hasta el cifrado completo de los estados de parámetro.

**Para establecer el nivel de autenticación de una aplicación**

1.  En la **página de** propiedades Aplicaciones Dcomcnfg.exe, seleccione  la aplicación y haga clic en el botón Propiedades (o haga doble clic en la aplicación seleccionada).

2.  En la **página General,** seleccione un nivel de autenticación distinto **de (Ninguno)** en el cuadro **de lista Nivel** de autenticación .

3.  Si va a establecer otras propiedades para esta aplicación, elija el **botón** Aplicar para aplicar el nuevo nivel de autenticación. Haga **clic en** Aceptar si ha terminado de establecer las propiedades de esta aplicación y desea aplicar los cambios.

## <a name="setting-the-location-for-an-application"></a>Establecer la ubicación de una aplicación

La ubicación establecida para la aplicación determina el equipo en el que se ejecutará la aplicación. Puede optar por ejecutar la aplicación en el equipo donde se encuentran los datos, en el equipo que usa para establecer la ubicación o en un equipo especificado.

**Para establecer la ubicación de una aplicación**

1.  Cuando Dcomcnfg.exe, seleccione la aplicación en  la página  Aplicaciones y elija el botón Propiedades (o haga doble clic en la aplicación seleccionada).

2.  En la **página Ubicación,** active una o varias casillas que correspondan a las ubicaciones en las que desea que se ejecute la aplicación. Si selecciona más de una casilla, COM usa la primera que se aplica. Si Dcomcnfg.exe se ejecuta en el equipo servidor, seleccione siempre **Ejecutar aplicación en este equipo.**

3.  Si va a establecer otras propiedades para esta aplicación, elija el **botón** Aplicar para aplicar la nueva ubicación. Elija **Aceptar** si ha terminado de establecer las propiedades de esta aplicación y desea aplicar los cambios.

## <a name="setting-launch-permissions-for-an-application"></a>Establecer permisos de inicio para una aplicación

Con Dcomcnfg.exe, puede establecer permisos de inicio para controlar la lista de usuarios a los que se les ha concedido o denegado permiso para iniciar un servidor determinado. Puede agregar usuarios o grupos a la lista, especificando si se concede o se deniega el permiso de acceso. También puede quitar usuarios de la lista.

**Para establecer permisos de inicio para una aplicación**

1.  Cuando Dcomcnfg.exe, seleccione la aplicación en  la página  Aplicaciones y elija el botón Propiedades (o haga doble clic en la aplicación seleccionada).

2.  En la **página de** propiedades Seguridad, seleccione el botón de opción Usar permisos de **inicio personalizados** y elija el **botón Editar** en la misma área.

3.  Para quitar usuarios o grupos, seleccione el usuario o grupo que desea quitar y elija el **botón** Quitar. El usuario o grupo seleccionado ya no aparecerá en el cuadro de lista. Cuando haya terminado de quitar usuarios y grupos, elija **Aceptar.**

4.  Si desea agregar usuarios o grupos, elija el **botón** Agregar.

5.  Si conoce el nombre de usuario completo que desea agregar, escriba en el **cuadro de** texto Agregar nombres. Si no conoce el nombre de usuario, puede examinar la base de datos de usuario para encontrarla (consulte Exploración de la base de datos de usuario a continuación). Cuando haya ubicado el nombre de usuario, seleccione el usuario o grupo en el cuadro **de** lista Nombres y elija el **botón** Agregar.

6.  En el **cuadro de lista Tipo** de acceso, seleccione el tipo de acceso **(Permitir inicio** o Denegar **inicio).** Para agregar otros usuarios que tendrán el tipo de acceso seleccionado, repita el paso 5. Cuando haya terminado de agregar usuarios para el tipo de acceso seleccionado, elija el **botón** Aceptar.

7.  Para agregar usuarios que tendrán un tipo de acceso diferente, repita los pasos 5 y 6. De lo contrario, **elija Aceptar** para aplicar los cambios.

## <a name="setting-access-permissions-for-an-application"></a>Establecer permisos de acceso para una aplicación

Con Dcomcnfg.exe, puede administrar la lista de usuarios a los que se concede o deniega el acceso a los métodos de un servidor determinado estableciendo permisos de acceso. Puede agregar usuarios o grupos a la lista, especificando si se concede o se deniega el permiso de acceso. También puede quitar usuarios de la lista.

Al establecer permisos de acceso, debe asegurarse de que SYSTEM se incluye en la lista de usuarios a los que se concede acceso. Si ha concedido permisos de acceso a Todos, SYSTEM se incluye implícitamente.

El proceso de configuración de permisos de acceso para una aplicación es similar a establecer los permisos de inicio. Estos son los pasos.

**Para establecer permisos de acceso para una aplicación**

1.  Cuando Dcomcnfg.exe, seleccione la aplicación en  la página  Aplicaciones y elija el botón Propiedades (o haga doble clic en la aplicación seleccionada).

2.  En la **página de** propiedades Seguridad, seleccione el botón de opción Usar permisos de acceso **personalizados** y **elija el botón Editar** en la misma área.

3.  Para quitar usuarios o grupos, seleccione el usuario o grupo que desea quitar y elija el **botón** Quitar. El usuario o grupo seleccionado ya no aparecerá en el cuadro de lista. Cuando haya terminado de quitar usuarios y grupos, elija **Aceptar.**

4.  Si desea agregar un usuario o un grupo, elija el **botón** Agregar.

5.  Si conoce el nombre de usuario completo que desea agregar, escriba en el **cuadro de** texto Agregar nombres. Si no conoce el nombre de usuario, puede examinar la base de datos de usuario para encontrarlo. Cuando haya ubicado el nombre de usuario, seleccione el usuario o grupo en el cuadro **de** lista Nombres y elija el **botón** Agregar.

6.  En el **cuadro de lista Tipo** de acceso, seleccione el tipo de acceso **(Permitir acceso** o Denegar **acceso).** Para agregar otros usuarios que tendrán el tipo de acceso seleccionado, repita el paso 5. Cuando haya terminado de agregar usuarios para el tipo de acceso seleccionado, elija el **botón** Aceptar.

7.  Para agregar usuarios que tendrán un tipo de acceso diferente, repita los pasos 5 y 6. De lo contrario, **elija Aceptar** para aplicar los cambios.

## <a name="setting-the-identity-for-an-application"></a>Establecer la identidad de una aplicación

La identidad de una aplicación es la cuenta que se usa para ejecutar la aplicación. La identidad puede ser la del usuario que ha iniciado sesión actualmente (el usuario interactivo), la cuenta de usuario del proceso de cliente que inició el servidor, un usuario especificado o un servicio. Puede usar Dcomcnfg.exe para elegir una de estas identidades para la aplicación. Para obtener ayuda para decidir qué identidad establecer para la aplicación, vea [Identidad de aplicación](application-identity.md).

**Para establecer la identidad de una aplicación**

1.  Cuando Dcomcnfg.exe, seleccione la aplicación en  la página  Aplicaciones y elija el botón Propiedades (o haga doble clic en la aplicación seleccionada).

2.  En la **página de** propiedades Identidad, seleccione el botón de opción de la identidad que desee. Si elige **Este usuario**, debe escribir el nombre de usuario, la contraseña y la contraseña confirmada.

3.  Si va a establecer otras propiedades para esta aplicación, elija el **botón** Aplicar para aplicar la nueva identidad. Elija **Aceptar** si ha terminado de establecer las propiedades de esta aplicación y desea aplicar los cambios.

## <a name="browsing-the-user-database"></a>Examinar la base de datos de usuario

Examinaría la base de datos de usuario Dcomcnfg.exe cuando necesite encontrar el nombre de usuario completo de un usuario determinado. Por ejemplo, puede examinar la base de datos de usuario para buscar un usuario que desee agregar para obtener permisos de acceso o de inicio.

**Para examinar la base de datos de usuario**

1.  En el **cuadro de lista Enumerar** nombres desde , seleccione el dominio que contiene el usuario o grupo que desea agregar.

2.  Para ver los usuarios que pertenecen al dominio seleccionado, elija el **botón Mostrar** usuarios.

3.  Para ver los miembros de un grupo determinado, seleccione el grupo en el cuadro de lista **Nombres** y elija el **botón Mostrar** miembros.

4.  Si no encuentra el usuario o grupo que  desea agregar, elija el botón Buscar, que abre el cuadro de diálogo **Buscar** cuenta. Seleccione el dominio que desea buscar (o seleccione Buscar **todo),** escriba el nombre de usuario que desea buscar y elija el **botón** Buscar.

## <a name="dcomcnfgexe-and-64-bit-applications"></a>Dcomcnfg.exe y aplicaciones de 64 bits

En sistemas operativos x64 de Windows XP a Windows Server 2008, la versión de 64 bits de DCOMCNFG.EXE no configura correctamente aplicaciones DCOM de 32 bits para la activación remota. Este comportamiento hace que los componentes que están diseñados para activarse de forma remota se activen localmente. Este comportamiento no se produce en Windows 7 y Windows Server 2008 R2 y versiones posteriores.

La solución alternativa es usar la versión de 32 bits de DCOMCNFG. Ejecute la versión de 32 bits de mmc.exe y cargue la versión de 32 bits del complemento Servicios de componentes mediante la siguiente línea de comandos.

C: \\ WINDOWS \\ SysWOW64>**mmc comexp.msc /32**

La versión de 32 bits de Servicios de componentes registra correctamente aplicaciones DCOM de 32 bits para la activación remota.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de Process-Wide seguridad](setting-processwide-security.md)
</dt> </dl>

 

 




