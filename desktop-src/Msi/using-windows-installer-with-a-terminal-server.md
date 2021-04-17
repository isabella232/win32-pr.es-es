---
description: Lo siguiente puede afectar a las instalaciones de Windows Installer cuando se usa un servidor de Terminal Server. Los desarrolladores de instalación siempre deben probar que el paquete de Windows Installer se instala según lo esperado cuando los usuarios también utilizan un servidor de Terminal Server.
ms.assetid: deda9efa-a0fc-4b4e-a531-650ac201fd84
title: Usar Windows Installer con un Terminal Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d471fa19b4588a01a2730af44fa5e9d978d18859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497248"
---
# <a name="using-windows-installer-with-a-terminal-server"></a>Usar Windows Installer con un Terminal Server

Lo siguiente puede afectar a las instalaciones de Windows Installer cuando se usa un servidor de Terminal Server. Los desarrolladores de instalación siempre deben probar que el paquete de Windows Installer se instala según lo esperado cuando los usuarios también utilizan un servidor de Terminal Server.

-   En sistemas operativos anteriores a Windows Server 2008 y Windows Vista, se debe establecer la Directiva del sistema [EnableAdminTSRemote](enableadmintsremote.md) para permitir que los administradores realicen instalaciones en la sesión del cliente. A partir de Windows Server 2008 y Windows Vista, la Directiva EnableAdminTSRemote ya no tiene ningún efecto. Independientemente de su configuración, los administradores y los usuarios que no son administradores pueden realizar una instalación en la sesión de cliente o en la sesión de consola. Los administradores y los usuarios que no son administradores siempre pueden realizar instalaciones Windows Installer en la sesión de la consola.
-   El Windows Installer evita la instalación en el contexto de [instalación](installation-context.md) por usuario si la[Directiva del sistema](system-policy.md) [DisableUserInstalls](disableuserinstalls.md)está establecida en 1. En este caso, el instalador omite todas las aplicaciones registradas como por usuario y busca solo las aplicaciones registradas como por equipo.
-   Cuando un administrador realiza una instalación en una sesión de cliente de un servidor de Terminal Server que se hospeda en Windows 2000, la instalación debe utilizar una ruta de acceso UNC y no una letra de unidad asignada.

Los desarrolladores deben cumplir las siguientes directrices al desarrollar un componente de Windows Installer que se pueda usar con un servidor de Terminal Server.

-   Escriba toda la información del registro **HKCU** en la  \\ parte del **software** HKCU del registro.
-   No se recomienda almacenar la información de configuración en archivos INI.
-   Escriba la información por usuario en el registro cuando la aplicación se ejecute por primera vez y no durante la instalación. Si debe escribir información por usuario en el registro durante la instalación, separe la información por usuario y por equipo en diferentes componentes de Windows Installer. Cree el paquete de modo que el instalador no intente validar y reparar los componentes que contienen información de cada usuario cuando se instala la aplicación.
-   Un paquete que se usa solo para instalaciones por equipo debe escribir variables de entorno en el entorno del equipo mediante \* la inclusión de en la columna Nombre de la [tabla de entorno](environment-table.md). Si el paquete se puede usar para instalaciones por usuario o para instalaciones por máquina, use dos componentes. Incluya el componente por usuario en la [tabla de componentes](condition-table.md) y escriba la configuración de usuario en la tabla de entorno. Incluya el componente por equipo en la tabla de componentes y escriba la configuración del equipo en la tabla de entorno. Controlar qué componente se instala mediante instrucciones condicionales basadas en la propiedad [**AllUsers**](allusers.md) en el campo condición de la tabla componente.
-   Al realizar instalaciones por equipo desde un servidor de Terminal Server, el instalador escribe variables de entorno por usuario en **HKCU** \\ **.** \\ **Entorno** predeterminado. Dado que el servidor de Terminal Server no Replica esta sección del registro, la instalación no establece las variables de entorno por usuario.
-   Dado que un servidor se puede configurar para impedir que los usuarios reparen aplicaciones, la aplicación debe controlar el caso de que falten claves del registro correctamente.

Lo siguiente se aplica cuando un paquete de Windows Installer que utiliza [acciones personalizadas](custom-actions.md) de dll, exe o script se instala en el contexto de instalación por equipo en un servidor de Terminal Server. En este caso, el instalador establece la propiedad [**TerminalServer**](terminalserver.md) .

-   Las acciones personalizadas diferidas se ejecutan en el contexto del sistema local, a menos que la acción tenga el atributo **msidbCustomActionTypeTSAware** . Esto es así incluso si la acción personalizada suplanta al usuario en un sistema que no es un servidor de Terminal Server. Tenga en cuenta que si una acción personalizada que tiene el atributo **msidbCustomActionTypeTSAware** cambia el registro del usuario, el instalador no garantiza automáticamente que esos cambios también se realicen en el registro de todos los usuarios del equipo.
-   Cualquier operación del registro en una acción personalizada diferida que se lea desde el subárbol del registro **HKCU** verá el subárbol del registro predeterminado del sistema y no el subárbol del registro del usuario actual.
-   El instalador detecta todas las operaciones del registro en una acción personalizada diferida que escriben en el \\ **software** HKCU y se copian en todos los usuarios del equipo en el siguiente inicio de sesión del usuario.
-   Las operaciones del registro en una acción personalizada diferida que escriben en **HKCU**, pero no en la \\ clave del registro HKCU **software** , no las detecta el instalador ni se copian.

Para obtener más información, vea [Terminal Services](../termserv/terminal-services-portal.md) en el kit de desarrollo de software (SDK) de Microsoft Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EnableAdminTSRemote](enableadmintsremote.md)
</dt> <dt>

[**Propiedad TerminalServer**](terminalserver.md)
</dt> <dt>

[**Propiedad RemoteAdminTS**](remoteadmints.md)
</dt> <dt>

[Terminal Services](../termserv/terminal-services-portal.md)
</dt> </dl>

 

 
