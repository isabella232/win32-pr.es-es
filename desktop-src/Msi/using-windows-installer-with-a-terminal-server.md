---
description: Lo siguiente puede afectar a Windows instalador cuando se usa un servidor de terminal. Los desarrolladores de instalación siempre deben probar que su paquete Windows Installer se instala según lo previsto cuando los usuarios también usan un servidor terminal.
ms.assetid: deda9efa-a0fc-4b4e-a531-650ac201fd84
title: Uso Windows Installer con terminal server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9aba70bc9430f0bc55c7e234b19764a14b138a4d5053de5c1cc6b9aee37692d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995835"
---
# <a name="using-windows-installer-with-a-terminal-server"></a>Uso Windows Installer con terminal server

Lo siguiente puede afectar a Windows instalador cuando se usa un servidor de terminal. Los desarrolladores de instalación siempre deben probar que su paquete Windows Installer se instala según lo previsto cuando los usuarios también usan un servidor terminal.

-   En sistemas operativos anteriores a Windows Server 2008 y Windows Vista, la directiva del sistema [EnableAdminTSRemote](enableadmintsremote.md) debe establecerse para permitir que los administradores realicen instalaciones en la sesión de cliente. A partir Windows Server 2008 y Windows Vista, la directiva EnableAdminTSRemote ya no tiene ningún efecto. Independientemente de su configuración, los administradores y no administradores pueden realizar una instalación en la sesión de cliente o en la sesión de consola. Los administradores y no administradores siempre pueden realizar instalaciones Windows Installer en la sesión de consola.
-   El Windows de instalación impide la [](installation-context.md) instalación en el contexto de instalación por usuario si la directiva del sistema [DisableUserInstalls](disableuserinstalls.md)[está](system-policy.md) establecida en 1. En este caso, el instalador omite todas las aplicaciones registradas como por usuario y busca solo las aplicaciones registradas como por equipo.
-   Cuando un administrador realiza una instalación en una sesión de cliente de un servidor de terminal server hospedado en Windows 2000, la instalación debe usar una ruta de acceso UNC y no una letra de unidad asignada.

Los desarrolladores deben cumplir las siguientes directrices al desarrollar un Windows Installer que se pueda usar con un servidor terminal.

-   Escriba toda **la información del registro hkcu** en la parte **hkcu** \\ **software** del registro.
-   No se recomienda almacenar información de configuración en archivos INI.
-   Escriba información por usuario en el Registro cuando la aplicación se ejecute por primera vez y no en el momento de la instalación. Si debe escribir información por usuario en el Registro en el momento de la instalación, separe la información por usuario y por equipo en diferentes componentes Windows Installer. Cree el paquete de forma que el instalador no intente validar y reparar los componentes que contienen información por usuario cuando se instala la aplicación.
-   Un paquete usado solo para instalaciones por equipo debe escribir variables de entorno en el entorno del equipo incluyendo en la columna Nombre \* de la tabla de [entorno](environment-table.md). Si el paquete se puede usar para instalaciones por usuario o por máquina, use dos componentes. Incluya el componente por usuario en la tabla [de](condition-table.md) componentes y escriba la configuración del usuario en la tabla de entorno. Incluya el componente por equipo en la tabla de componentes y escriba la configuración del equipo en la Tabla de entorno. Controlar qué componente se instala mediante instrucciones condicionales basadas en la [**propiedad ALLUSERS**](allusers.md) en el campo Condición de la tabla de componentes.
-   Al realizar instalaciones por máquina desde un servidor de terminal Server, el instalador escribe variables de entorno por usuario en **HKCU.** \\ **Entorno** \\ **predeterminado.** Dado que el servidor de terminal no replica esta sección del Registro, la instalación no establece las variables de entorno por usuario.
-   Dado que un servidor se puede configurar para impedir que los usuarios repare aplicaciones, la aplicación debe controlar correctamente el caso de que falte claves del Registro.

Lo siguiente se aplica cuando se instala un paquete de Windows Installer que usa acciones personalizadas dll, EXE o [script](custom-actions.md) en el contexto de instalación por equipo en un servidor de Terminal Server. En este caso, el instalador establece la [**propiedad TerminalServer.**](terminalserver.md)

-   Las acciones personalizadas diferidas se ejecutan en el contexto del sistema local a menos que la acción tenga el **atributo msidbCustomActionTypeTSAware.** Esto es así incluso si la acción personalizada suplanta al usuario en un sistema que no es un servidor terminal. Tenga en cuenta que si una acción personalizada que tiene el atributo **msidbCustomActionTypeTSAware** cambia el registro del usuario, el instalador no garantiza automáticamente que esos cambios también se realicen en el registro de todos los usuarios del equipo.
-   Las operaciones del Registro en una acción personalizada diferida que se leen desde el subárbol del Registro **HKCU** ven el subárbol del Registro predeterminado del sistema y no el subárbol del registro del usuario actual.
-   El instalador detecta todas las operaciones del Registro en una acción personalizada diferida que escriben en **HKCU** Software y se copian en cada usuario del equipo en el siguiente inicio \\  de sesión del usuario.
-   El instalador no detecta ni copia las operaciones del Registro de una acción personalizada diferida que escriben en **HKCU,** pero que no están bajo la clave del Registro **hkcu** \\ **software.**

Para más información, consulte [Terminal Services](../termserv/terminal-services-portal.md) en el Kit de desarrollo de software (SDK) de Microsoft Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EnableAdminTSRemote](enableadmintsremote.md)
</dt> <dt>

[**Propiedad TerminalServer**](terminalserver.md)
</dt> <dt>

[**RemoteAdminTS, propiedad**](remoteadmints.md)
</dt> <dt>

[Terminal Services](../termserv/terminal-services-portal.md)
</dt> </dl>

 

 
