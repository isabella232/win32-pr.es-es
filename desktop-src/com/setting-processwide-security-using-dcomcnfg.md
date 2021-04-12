---
title: Establecer la seguridad de Process-Wide mediante DCOMCNFG
description: Es posible que desee habilitar la seguridad para una aplicación en particular si una aplicación tiene necesidades de seguridad diferentes de las requeridas por otras aplicaciones del equipo.
ms.assetid: 04a7f688-78a3-490a-bcfa-862824a05422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03174dd66e83a88724ff5d421d7b0dcb0c17699e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357798"
---
# <a name="setting-process-wide-security-using-dcomcnfg"></a>Establecer la seguridad de Process-Wide mediante DCOMCNFG

Es posible que desee habilitar la seguridad para una aplicación en particular si una aplicación tiene necesidades de seguridad diferentes de las requeridas por otras aplicaciones del equipo. Por ejemplo, puede decidir usar la configuración de todo el sistema para las aplicaciones que requieran un nivel bajo de seguridad al mismo tiempo que se establece un mayor nivel de seguridad para una aplicación determinada.

Sin embargo, a veces no se usa la configuración de seguridad del registro que se aplica a una aplicación determinada. Por ejemplo, la configuración de todo el proceso que se establece en el registro mediante Dcomcnfg.exe se invalidará si un cliente llama a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) para establecer la seguridad de un proxy de interfaz determinado. Del mismo modo, si un cliente o un servidor (o ambos) llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer la seguridad de un proceso, se omitirá la configuración del registro y se usarán los parámetros especificados para **CoInitializeSecurity** .

Al habilitar la seguridad de una aplicación, es posible que sea necesario modificar varias configuraciones. Esto incluye el nivel de autenticación, la ubicación, los permisos de inicio, los permisos de acceso y la identidad. Para conocer los procedimientos paso a paso, consulte lo siguiente:

-   [Establecer el nivel de autenticación para una aplicación](#setting-the-authentication-level-for-an-application)
-   [Establecimiento de la ubicación de una aplicación](#setting-the-location-for-an-application)
-   [Establecer permisos de inicio para una aplicación](#setting-launch-permissions-for-an-application)
-   [Establecer permisos de acceso para una aplicación](#setting-access-permissions-for-an-application)
-   [Establecimiento de la identidad de una aplicación](#setting-the-identity-for-an-application)
-   [Examinar la base de datos de usuario](#browsing-the-user-database)
-   [ Aplicaciones deDcomcnfg.exe y 64 bits](#dcomcnfgexe-and-64-bit-applications)
-   [Temas relacionados](#related-topics)

## <a name="setting-the-authentication-level-for-an-application"></a>Establecer el nivel de autenticación para una aplicación

Para habilitar la seguridad de una aplicación, debe establecer un nivel de autenticación distinto de ninguno. El nivel de autenticación indica a COM Cuánta protección de autenticación se requiere y puede abarcar desde la autenticación del cliente en la primera llamada al método para cifrar los Estados de los parámetros por completo.

**Para establecer el nivel de autenticación de una aplicación**

1.  En la página de propiedades **aplicaciones** de Dcomcnfg.exe, seleccione la aplicación y haga clic en el botón **propiedades** (o haga doble clic en la aplicación seleccionada).

2.  En la página **General** , seleccione un nivel de autenticación distinto de **(ninguno)** en el cuadro de lista **nivel de autenticación** .

3.  Si va a establecer otras propiedades para esta aplicación, elija el botón **aplicar** para aplicar el nuevo nivel de autenticación. Haga clic en **Aceptar** si ha terminado de establecer las propiedades de esta aplicación y desea aplicar los cambios.

## <a name="setting-the-location-for-an-application"></a>Establecimiento de la ubicación de una aplicación

La ubicación que se establece para la aplicación determina el equipo en el que se ejecutará la aplicación. Puede elegir ejecutar la aplicación en el equipo donde se encuentran los datos, en el equipo que usa para establecer la ubicación o en un equipo especificado.

**Para establecer la ubicación de una aplicación**

1.  Con Dcomcnfg.exe en ejecución, seleccione la aplicación en la página **aplicaciones** y elija el botón **propiedades** (o haga doble clic en la aplicación seleccionada).

2.  En la página **Ubicación** , active una o varias casillas de verificación que se correspondan con las ubicaciones en las que desea que se ejecute la aplicación. Si selecciona más de una casilla, COM usa la primera que se aplica. Si Dcomcnfg.exe se está ejecutando en el equipo servidor, seleccione siempre **Ejecutar aplicación en este equipo**.

3.  Si va a establecer otras propiedades para esta aplicación, elija el botón **aplicar** para aplicar la nueva ubicación. Elija **Aceptar** si ha terminado de establecer las propiedades de esta aplicación y desea aplicar los cambios.

## <a name="setting-launch-permissions-for-an-application"></a>Establecer permisos de inicio para una aplicación

Con Dcomcnfg.exe, puede establecer permisos de inicio para controlar la lista de usuarios a los que se concede o deniega el permiso para iniciar un servidor determinado. Puede Agregar usuarios o grupos a la lista, especificando si se concede o se deniega el permiso de acceso. También puede quitar usuarios de la lista.

**Para establecer los permisos de inicio de una aplicación**

1.  Con Dcomcnfg.exe en ejecución, seleccione la aplicación en la página **aplicaciones** y elija el botón **propiedades** (o haga doble clic en la aplicación seleccionada).

2.  En la página de propiedades **seguridad** , seleccione el botón de opción **usar permisos de inicio personalizados** y elija el botón **Editar** en la misma área.

3.  Para quitar usuarios o grupos, seleccione el usuario o grupo que desea quitar y elija el botón **quitar** . El usuario o grupo seleccionado ya no aparecerá en el cuadro de lista. Cuando haya terminado de quitar usuarios y grupos, elija **Aceptar**.

4.  Si desea agregar usuarios o grupos, elija el botón **Agregar** .

5.  Si conoce el nombre de usuario completo que desea agregar, escríbalo en el cuadro de texto **Agregar nombres** . Si no conoce el nombre de usuario, puede examinar la base de datos de usuario para encontrarlo (vea examinar la base de datos de usuario a continuación). Cuando haya encontrado el nombre de usuario, seleccione el usuario o grupo en el cuadro de lista **nombres** y elija el botón **Agregar** .

6.  En el cuadro **de lista tipo de acceso** , seleccione el tipo de acceso ( **permitir** iniciar o **denegar el inicio**). Para agregar otros usuarios que tendrán el tipo de acceso seleccionado, repita el paso 5. Cuando haya terminado de agregar usuarios para el tipo de acceso seleccionado, elija el botón **Aceptar** .

7.  Para agregar usuarios que tengan un tipo de acceso diferente, repita los pasos 5 y 6. De lo contrario, elija **Aceptar** para aplicar los cambios.

## <a name="setting-access-permissions-for-an-application"></a>Establecer permisos de acceso para una aplicación

Con Dcomcnfg.exe, puede administrar la lista de usuarios a los que se concede o deniega el acceso a los métodos de un servidor determinado mediante el establecimiento de los permisos de acceso. Puede Agregar usuarios o grupos a la lista, especificando si se concede o se deniega el permiso de acceso. También puede quitar usuarios de la lista.

Al establecer los permisos de acceso, debe asegurarse de que el sistema está incluido en la lista de usuarios a los que se concede acceso. Si ha concedido permisos de acceso a todos, el sistema se incluye implícitamente.

El proceso de establecimiento de los permisos de acceso para una aplicación es similar al establecimiento de los permisos de inicio. Estos son los pasos.

**Para establecer permisos de acceso para una aplicación**

1.  Con Dcomcnfg.exe en ejecución, seleccione la aplicación en la página **aplicaciones** y elija el botón **propiedades** (o haga doble clic en la aplicación seleccionada).

2.  En la página de propiedades **seguridad** , seleccione el botón de opción **usar permisos de acceso personalizados** y elija el botón **Editar** en la misma área.

3.  Para quitar usuarios o grupos, seleccione el usuario o grupo que desea quitar y elija el botón **quitar** . El usuario o grupo seleccionado ya no aparecerá en el cuadro de lista. Cuando haya terminado de quitar usuarios y grupos, elija **Aceptar**.

4.  Si desea agregar un usuario o un grupo, elija el botón **Agregar** .

5.  Si conoce el nombre de usuario completo que desea agregar, escríbalo en el cuadro de texto **Agregar nombres** . Si no conoce el nombre de usuario, puede examinar la base de datos de usuario para buscarlo. Cuando haya encontrado el nombre de usuario, seleccione el usuario o grupo en el cuadro de lista **nombres** y elija el botón **Agregar** .

6.  En el cuadro **de lista tipo de acceso** , seleccione el tipo de acceso ( **permitir acceso** o **denegar acceso**). Para agregar otros usuarios que tendrán el tipo de acceso seleccionado, repita el paso 5. Cuando haya terminado de agregar usuarios para el tipo de acceso seleccionado, elija el botón **Aceptar** .

7.  Para agregar usuarios que tengan un tipo de acceso diferente, repita los pasos 5 y 6. De lo contrario, elija **Aceptar** para aplicar los cambios.

## <a name="setting-the-identity-for-an-application"></a>Establecimiento de la identidad de una aplicación

La identidad de una aplicación es la cuenta que se usa para ejecutar la aplicación. La identidad puede ser la del usuario que ha iniciado sesión actualmente (el usuario interactivo), la cuenta de usuario del proceso de cliente que inició el servidor, un usuario especificado o un servicio. Puede usar Dcomcnfg.exe para elegir una de estas identidades para la aplicación. Para obtener ayuda a la hora de decidir qué identidad establecer para la aplicación, consulte [Application Identity](application-identity.md).

**Para establecer la identidad de una aplicación**

1.  Con Dcomcnfg.exe en ejecución, seleccione la aplicación en la página **aplicaciones** y elija el botón **propiedades** (o haga doble clic en la aplicación seleccionada).

2.  En la página de propiedades **identidad** , seleccione el botón de opción correspondiente a la identidad que desee. Si elige **este usuario**, debe escribir el nombre de usuario, la contraseña y la contraseña confirmada.

3.  Si va a establecer otras propiedades para esta aplicación, elija el botón **aplicar** para aplicar la nueva identidad. Elija **Aceptar** si ha terminado de establecer las propiedades de esta aplicación y desea aplicar los cambios.

## <a name="browsing-the-user-database"></a>Examinar la base de datos de usuario

Examinaría la base de datos de usuario en Dcomcnfg.exe cuando necesite buscar el nombre de usuario completo de un usuario determinado. Por ejemplo, puede examinar la base de datos de usuario para buscar el usuario que desea agregar para los permisos de acceso o de inicio.

**Para examinar la base de datos de usuario**

1.  En el cuadro de lista **nombres de lista** , seleccione el dominio que contiene el usuario o el grupo que desea agregar.

2.  Para ver los usuarios que pertenecen al dominio seleccionado, elija el botón **Mostrar usuarios** .

3.  Para ver los miembros de un grupo determinado, seleccione el grupo en el cuadro de lista **nombres** y elija el botón **Mostrar miembros** .

4.  Si no encuentra el usuario o grupo que desea agregar, elija el botón **Buscar** , que abre el cuadro de diálogo **Buscar cuenta** . Seleccione el dominio que desea buscar (o seleccione **buscar todo**), escriba el nombre de usuario que desea buscar y elija el botón **Buscar** .

## <a name="dcomcnfgexe-and-64-bit-applications"></a>Aplicaciones de Dcomcnfg.exe y 64 bits

En los sistemas operativos x64 de Windows XP a Windows Server 2008, la versión de 64 bits de DCOMCNFG.EXE no configura correctamente las aplicaciones DCOM de 32 bits para la activación remota. Este comportamiento hace que los componentes que están diseñados para activarse de forma remota se activen localmente. Este comportamiento no se produce en Windows 7 y Windows Server 2008 R2 y versiones posteriores.

La solución consiste en usar la versión de 32 bits de DCOMCNFG. Ejecute la versión de 32 bits de mmc.exe y cargue la versión de 32 bits del complemento Servicios de componentes mediante la siguiente línea de comandos.

C: \\ Windows \\ SysWOW64>**MMC comexp. msc/32**

La versión de 32 bits de servicios de componentes registra correctamente las aplicaciones DCOM de 32 bits para la activación remota.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la seguridad de Process-Wide](setting-processwide-security.md)
</dt> </dl>

 

 




