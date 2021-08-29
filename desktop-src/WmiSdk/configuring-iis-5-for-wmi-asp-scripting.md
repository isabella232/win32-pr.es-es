---
description: Toda la configuración de autenticación se realiza a través del Administrador de servicios Internet.
ms.assetid: 9b118120-f0cb-4973-b537-dd3d12a7a6d5
ms.tgt_platform: multiple
title: Configuración de IIS 5.0 y versiones posteriores para el scripting ASP de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ade580408337c2b559ce46f8125e7d639205d8014e288a7a63d9730fde3fba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131627"
---
# <a name="configuring-iis-50-and-later-for-wmi-asp-scripting"></a>Configuración de IIS 5.0 y versiones posteriores para el scripting ASP de WMI

Toda la configuración de autenticación se realiza a través del Administrador de servicios Internet.

Al configurar la seguridad de Internet Information Server (IIS) 5.0 e IIS 6.0 para scripts ASP wmi, tenga en cuenta los siguientes problemas:

-   [Nivel de autenticación](#authentication-level)

    Puede configurar en el nivel de servidor, directorio o archivo.

-   [Configuración de autenticación](#authentication-setting)

    Puede establecer la autenticación en Anonymous, Integrated Windows o ambos.

-   [Protección](#protection)

    Puede establecer el ASP para que se ejecute en proceso (protección baja) o fuera de proceso mediante Dllhost.exe (protección media o alta).

## <a name="authentication-level"></a>Nivel de autenticación

Para mayor seguridad, puede configurar la autenticación en el nivel de directorio o archivo.

Si la autenticación se establece en el nivel de servidor, todos los directorios y archivos posteriores se adhieren a la autenticación del servidor, a menos que se altere explícitamente en el nivel de directorio o archivo. Puede crear una estructura de directorios que contenga todos los scripts ASP de WMI donde las páginas HTML y las ASP específicas de WMI se pueden configurar independientemente del resto del servidor. Realice el procedimiento siguiente para cambiar el nivel de autenticación de un servidor, directorio o archivo.

**Para establecer la autenticación en cualquier nivel**

1.  En Panel de control, haga doble clic en **Herramientas administrativas** y, a continuación, haga doble clic en el complemento IIS.

2.  Busque el icono de página ASP y, a continuación, abra las propiedades del nivel que se va a establecer, que pueden ser servidor, directorio o archivo.

    > [!Note]  
    > La configuración de autenticación se encuentra en la pestaña Seguridad de **directorios** o **Seguridad de** archivos de la **hoja** Propiedades.

     

## <a name="authentication-setting"></a>Configuración de autenticación

En el caso de los scripts ASP de WMI, la combinación de autenticación anónima desactivada (desactivada) y Autenticación Windows integrada activada (activada) proporciona una mayor oportunidad para establecer la seguridad. Para usar la configuración de autenticación de NT LAN Manager (NTLM), Passport o Digest IIS, debe activar los privilegios de habilitación remota, ya que el usuario se trata como una identidad de red y se registra de forma remota. La configuración de habilitación remota no es necesaria para la autenticación anónima y básica. Sin embargo, el sistema es mucho menos seguro cuando se usa la autenticación anónima y básica.

Si la autenticación anónima se usa con o sin la autenticación Windows integrada, el enfoque más seguro es usar un inicio de sesión que requiera que un usuario escriba un nombre de usuario y una contraseña. El inicio de sesión predeterminado es la identidad de IIS, pero se puede crear un inicio de sesión mediante permisos específicos adecuados para los scripts ASP wmi que se pueden usar como cuenta para las conexiones anónimas o de invitado.

Si elige un identificador de inicio de sesión que no sea una identidad de IIS, desactive la casilla Permitir que **IIS controle** la contraseña y escriba la contraseña correcta. Esto obliga a todas las conexiones anónimas o invitadas a usar el identificador de inicio de sesión. Al crear un inicio de sesión independiente de la identidad de IIS, los privilegios de una cuenta que accede a WMI se pueden controlar sin afectar a los demás directorios o archivos del servidor IIS, a menos que la autenticación se establezca en el nivel de servidor.

Realice el procedimiento siguiente para establecer los requisitos de autenticación de la página ASP mediante el complemento IIS en el Panel de control.

**Para llegar a la configuración de la cuenta**

1.  En Panel de control, haga doble  clic en el icono Herramientas administrativas, abra el complemento IIS, busque la página ASP y abra las propiedades del nivel que se va a establecer, que pueden ser servidor, directorio o archivo.

    La configuración de autenticación se puede encontrar en la pestaña **Seguridad** de directorios o **Seguridad de** archivos de la **hoja** Propiedades.

2.  En el área Autenticación anónima, haga clic **en Editar.**

3.  Si se selecciona un identificador de inicio de sesión distinto de la identidad de IIS, desactive la casilla Permitir que **IIS controle** la contraseña y escriba la contraseña correcta. Esto obliga a todas las conexiones anónimas o invitadas a usar el identificador de inicio de sesión.

Mediante un inicio de sesión diferente de la identidad de IIS, los privilegios de la cuenta que accede a WMI se pueden controlar sin afectar a los demás directorios o archivos del servidor IIS, a menos que la autenticación se establezca en el nivel de servidor.

La configuración anterior permite que el servidor IIS use la autenticación anónima en algunas áreas y la autenticación Windows o la autenticación mixta en otras.

## <a name="protection"></a>Protección

La última consideración al configurar el servidor IIS es qué protección usar al ejecutar un ASP.

Puede establecer un ASP para ejecutar lo siguiente:

-   En proceso en IIS (protección baja).

-   Externo a IIS con Dllhost.exe como agrupada o fuera de proceso (protección mediana agrupada).

-   Auto-host fuera de proceso (alta protección).

> [!Note]  
> Para obtener el mejor equilibrio entre seguridad y rendimiento, use el host agrupado.

 

 

 



