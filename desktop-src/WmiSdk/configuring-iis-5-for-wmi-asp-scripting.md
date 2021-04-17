---
description: Toda la configuración de autenticación se realiza a través del Administrador de servicios Internet.
ms.assetid: 9b118120-f0cb-4973-b537-dd3d12a7a6d5
ms.tgt_platform: multiple
title: Configuración de IIS 5,0 y versiones posteriores para el scripting de ASP de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4b5ddde139b3eef32fd7c80f4cca4e10fd816a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715851"
---
# <a name="configuring-iis-50-and-later-for-wmi-asp-scripting"></a>Configuración de IIS 5,0 y versiones posteriores para el scripting de ASP de WMI

Toda la configuración de autenticación se realiza a través del Administrador de servicios Internet.

Al configurar Internet Information Server (IIS) 5,0 y la seguridad de IIS 6,0 para los scripts ASP de WMI, tenga en cuenta los siguientes problemas:

-   [Nivel de autenticación](#authentication-level)

    Puede configurar en el nivel de servidor, directorio o archivo.

-   [Configuración de autenticación](#authentication-setting)

    Puede establecer la autenticación en las ventanas anónimas, integradas o en ambas.

-   [Protección](#protection)

    Puede configurar el ASP para que se ejecute en proceso (protección baja) o fuera de proceso mediante Dllhost.exe (protección media o alta).

## <a name="authentication-level"></a>Nivel de autenticación

Para mayor seguridad, puede configurar la autenticación en el nivel de directorio o de archivo.

Si la autenticación se establece en el nivel de servidor, todos los archivos y directorios posteriores se adhieren a la autenticación del servidor, a menos que se modifiquen explícitamente en el nivel de directorio o archivo. Puede crear una estructura de directorios que contenga todos los scripts ASP de WMI donde las páginas HTML y los ASP específicos de WMI se pueden configurar independientemente del resto del servidor. Realice el procedimiento siguiente para cambiar el nivel de autenticación de un servidor, directorio o archivo.

**Para establecer la autenticación en cualquier nivel**

1.  En el panel de control, haga doble clic en **herramientas administrativas** y, a continuación, haga doble clic en el complemento IIS.

2.  Busque el icono de la página ASP y, a continuación, abra las propiedades del nivel que se va a establecer, que puede ser servidor, directorio o archivo.

    > [!Note]  
    > La configuración de autenticación se encuentra en la pestaña **seguridad de directorios** o **seguridad de archivos** de la hoja de **propiedades**.

     

## <a name="authentication-setting"></a>Configuración de autenticación

En el caso de los scripts ASP de WMI, la combinación de autenticación anónima desactivada (desactivada) y la autenticación integrada de Windows activada (activada) proporciona una mayor oportunidad para establecer la seguridad. Para usar las opciones de autenticación de NT LAN Manager (NTLM), Passport o Digest de IIS, debe activar los privilegios de habilitación remota, ya que el usuario se trata como una identidad de red y se registra de forma remota. La configuración de habilitación remota no es necesaria para la autenticación anónima y básica. Sin embargo, el sistema es mucho menos seguro cuando se utiliza la autenticación anónima y la autenticación básica.

Si se usa la autenticación anónima con o sin la autenticación integrada de Windows, el enfoque más seguro consiste en usar un inicio de sesión que requiera que un usuario escriba un nombre de usuario y una contraseña. El inicio de sesión predeterminado es la identidad de IIS, pero se puede crear un inicio de sesión con permisos específicos adecuados para los scripts ASP de WMI que se pueden usar como cuenta para las conexiones anónimas o de invitado.

Si elige un identificador de inicio de sesión que no sea una identidad de IIS, desactive la casilla **permitir que IIS controle la contraseña** y escriba la contraseña correcta. Esto obliga a todas las conexiones anónimas o de invitado a usar el identificador de inicio de sesión. Al crear un inicio de sesión independiente de la identidad de IIS, se pueden controlar los privilegios de una cuenta que tenga acceso a WMI sin que afecte a los demás directorios o archivos del servidor IIS, a menos que la autenticación se establezca en el nivel de servidor.

Realice el procedimiento siguiente para establecer los requisitos de autenticación para la página ASP con el complemento IIS en el panel de control.

**Para acceder a la configuración de la cuenta**

1.  En el panel de control, haga doble clic en el icono **herramientas administrativas** , abra el complemento IIS, busque la página ASP y abra las propiedades del nivel que se va a establecer, que puede ser servidor, directorio o archivo.

    La configuración de autenticación se puede encontrar en la pestaña **seguridad de directorios** o **seguridad de archivos** de la hoja de **propiedades** .

2.  En el área autenticación anónima, haga clic en **Editar**.

3.  Si se selecciona un identificador de inicio de sesión distinto de la identidad de IIS, desactive la casilla **permitir que IIS controle la contraseña** y escriba la contraseña correcta. Esto obliga a todas las conexiones anónimas o de invitado a usar el identificador de inicio de sesión.

Al usar un inicio de sesión diferente de la identidad de IIS, se pueden controlar los privilegios de la cuenta que tiene acceso a WMI sin que afecte a los demás directorios o archivos del servidor IIS, a menos que la autenticación se establezca en el nivel de servidor.

La configuración anterior permite que el servidor IIS use la autenticación anónima en algunas áreas, y la autenticación mixta o integrada de Windows en otros.

## <a name="protection"></a>Protección

La última consideración al configurar el servidor IIS es la protección que se debe usar al ejecutar un ASP.

Puede establecer un ASP para ejecutar lo siguiente:

-   En curso a IIS (protección baja).

-   Externo a IIS con Dllhost.exe como agrupado o fuera de proceso (protección mediana agrupada).

-   Self-of-Process-host (protección alta).

> [!Note]  
> Para obtener el mejor equilibrio de seguridad y rendimiento, use el host agrupado.

 

 

 



