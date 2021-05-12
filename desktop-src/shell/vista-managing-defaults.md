---
description: En este tema se proporcionan proveedores de software independientes (ISV) con una guía rápida de los pasos necesarios para registrar y administrar los valores predeterminados de la aplicación en Windows Vista y versiones posteriores. Se proporcionan vínculos a artículos más exhaustivos sobre el tema de cada sección.
ms.assetid: 649eb20d-07d3-4209-abff-45fc50f05631
title: Administración de aplicaciones predeterminadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc146858d197b96229edda49ac2e7249db51bf4c
ms.sourcegitcommit: 4d639170c06864e47ef66b2cfe6ca3d07cce0b02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109812830"
---
# <a name="managing-default-applications"></a>Administración de aplicaciones predeterminadas

La **característica Establecer acceso a** programas y valores predeterminados de equipo (SPAD) se agregó a Windows XP y versiones posteriores de Windows para administrar los valores predeterminados por equipo. Además de SPAD, Windows Vista introdujo el concepto de aplicaciones predeterminadas por usuario y el elemento **Programas** predeterminados en Panel de control.

> [!IMPORTANT]
> Este tema no se aplica a Windows 10. La forma en que funcionan las asociaciones de archivos predeterminadas ha cambiado Windows 10. Para obtener más información, vea la sección Sobre los cambios en Windows 10 **controla las aplicaciones predeterminadas** en [esta entrada](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

La configuración predeterminada por usuario es específica de una cuenta de usuario individual en el sistema. Si la configuración predeterminada por usuario está presente, tiene prioridad sobre los valores predeterminados por equipo correspondientes para esa cuenta. A Windows 8, el sistema de extensibilidad para los valores predeterminados de protocolo y tipo de archivo es estrictamente por usuario y se omiten los valores predeterminados por equipo. SPAD también ha cambiado en Windows 8 para establecer los valores predeterminados por usuario.

-   En sistemas que ejecutan versiones de Windows anteriores a Windows 8, una cuenta de usuario recién creada recibe los valores predeterminados por equipo hasta que se establecen los valores predeterminados por usuario. En Windows Vista y versiones  posteriores, los usuarios pueden usar el elemento Programas predeterminados de Panel de control establecer o cambiar sus valores predeterminados por usuario. Además, cuando se ejecuta una aplicación por primera vez, los valores predeterminados por usuario se pueden establecer siguiendo las directrices que se de la sección [Application First Run and Defaults](#application-first-run-and-defaults) (Primera ejecución de la aplicación y valores predeterminados).
-   En los sistemas que ejecutan Windows 8, una cuenta de usuario recién creada se basa en los valores predeterminados por usuario desde el principio y la configuración de esos valores predeterminados en la primera ejecución, como se explica en la sección Application [First Run and Defaults](#application-first-run-and-defaults) (Primera ejecución de la aplicación y valores predeterminados) ya no se admite.

Una aplicación debe registrarse tanto con SPAD como con la característica Programas predeterminados para ofrecerse como el programa predeterminado en Windows Vista y versiones posteriores.

En este tema se proporcionan proveedores de software independientes (ISV) con una guía rápida de los pasos necesarios para registrar y administrar los valores predeterminados de la aplicación en Windows Vista y versiones posteriores. Se proporcionan vínculos a artículos más exhaustivos sobre el tema de cada sección.

-   [Elemento de programas predeterminado en Panel de control](#default-programs-item-in-control-panel)
-   [Establecer el acceso al programa y los valores predeterminados del equipo](#set-program-access-and-computer-defaults)
    -   [Establecer valores predeterminados en SPAD](#setting-defaults-in-spad)
    -   [Ocultar el acceso en SPAD](#hide-access-in-spad)
-   [Registro para puntos de entrada de la aplicación](#registering-for-application-entry-points)
    -   [Abrir con](#open-with)
    -   [Menú Inicio y barra inicio rápido inicio](#start-menu-and-quick-launch-bar)
-   [Instalación de la aplicación y valores predeterminados](#application-installation-and-defaults)
-   [Actualizaciones de aplicaciones y valores predeterminados](#application-upgrades-and-defaults)
-   [Ejecución de la primera aplicación y valores predeterminados](#application-first-run-and-defaults)
-   [Comprobar los valores predeterminados y solicitar el consentimiento del usuario](#verifying-defaults-and-asking-for-user-consent)
-   [Sugerencias de compatibilidad de aplicaciones](#application-compatibility-tips)
    -   [Evitar desencadenar la virtualización Per-User virtualización](#avoid-triggering-per-user-virtualization)
    -   [Evitar advertencias o bloques de AppCompat desde el Asistente para compatibilidad de programas](#avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant)
    -   [Compatibilidad con versiones anteriores del sistema operativo Windows](#support-for-previous-windows-operating-system-versions)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="default-programs-item-in-control-panel"></a>Elemento de programas predeterminado en Panel de control

**Programas predeterminados** es una característica introducida en Windows Vista, accesible directamente desde el **menú** Inicio y Panel de control. Proporciona una nueva infraestructura que funciona con privilegios de usuario estándar (no elevados) y está diseñada para permitir que los usuarios y las aplicaciones administren los valores predeterminados por usuario. Para los usuarios, los programas predeterminados proporcionan una manera unificada y fácil de acceder para administrar valores predeterminados, asociaciones de archivos y configuración de reproducción automática en todas las aplicaciones del sistema. Para las aplicaciones, el uso del ámbito por usuario proporcionado por las API de programas predeterminados ofrece las siguientes ventajas:

-   **Sin elevación**

    Una aplicación no tiene que elevar sus privilegios para reclamar los valores predeterminados.

-   **Buena educación**

    En un equipo de varios usuarios, cada usuario puede seleccionar diferentes aplicaciones predeterminadas.

-   **Administración predeterminada**

    Las API de programas predeterminadas ofrecen un mecanismo confiable y coherente para comprobar el estado predeterminado y reclamar la configuración perdida sin tener que escribir directamente en el registro. Sin embargo, a Windows 8, no se recomienda que las aplicaciones consulten el estado predeterminado porque una aplicación ya no puede cambiar la configuración predeterminada: esos cambios solo los puede realizar el usuario.

Para permitir que la aplicación administre los valores predeterminados de forma eficaz, debe registrar la aplicación como un programa predeterminado potencial. Para obtener más información sobre el registro y el uso de las API de programas predeterminados, vea [Programas predeterminados.](default-programs.md)

Los programas predeterminados también proporcionan estas dos características:

-   **Interfaz de usuario de valores predeterminados reutilizables**

    La interfaz de usuario de los valores predeterminados del programa **(Establecer** los programas predeterminados) y las asociaciones de archivo (Asociar un tipo de archivo o protocolo **a** un programa) se pueden reutilizar y llamar desde dentro de una aplicación. Esto permite a las aplicaciones proporcionar una experiencia de usuario estándar para administrar los valores predeterminados y evitar que los ISV tengan que desarrollar una interfaz de usuario personalizada o equivalente.

-   **Inclusión de la dirección URL y la información de marketing**

    Como parte  de la página Establecer  los programas predeterminados del elemento Programas predeterminados de Panel de control, una aplicación puede proporcionar información de marketing y un vínculo al sitio web del proveedor. Esta dirección URL se deriva del certificado Authenticode con el que se ha firmado la aplicación. Esto evita el uso indebido y el reemplazo no autorizado de este vínculo. Si una aplicación tiene un certificado Authenticode que incluye una dirección URL insertada, la interfaz de usuario de Windows muestra esa dirección URL insertada. Los ISV deben aprovechar esta característica para dirigir a los usuarios a su sitio web para actualizaciones y otras descargas.

## <a name="set-program-access-and-computer-defaults"></a>Establecer el acceso al programa y los valores predeterminados del equipo

**Establecer el acceso a** programas y los valores predeterminados del equipo (SPAD) permite a los administradores administrar los valores predeterminados de todo el equipo heredados por todos los nuevos usuarios de ese equipo. Antes de Windows 8, SPAD también permitía a los administradores reparar asociaciones de archivos en caso de que se rompían cuando se quitaban programas del sistema. Sin embargo, a Windows 8, SPAD solo afecta a los valores predeterminados específicos del usuario.

Para obtener más información sobre el registro de una aplicación en SPAD, vea Trabajar con establecer el acceso a programas y los valores predeterminados del equipo [(SPAD)](cpl-setprogramaccess.md) y Registrar programas con [tipos de cliente](reg-middleware-apps.md). Los cambios específicos y las nuevas recomendaciones se analizan en las secciones siguientes.

### <a name="setting-defaults-in-spad"></a>Establecer valores predeterminados en SPAD

Los valores predeterminados por usuario invalidan los valores predeterminados por equipo.

-   **Antes Windows 8:** los valores predeterminados establecidos en SPAD (que son por equipo) no los verán los usuarios si se establecen los valores predeterminados por usuario correspondientes. Si un usuario no ha establecido un valor predeterminado por usuario, el sistema usa el valor predeterminado del equipo correspondiente. Las nuevas cuentas de usuario de un equipo heredan inicialmente los valores predeterminados del equipo. La primera vez que un usuario ejecuta una aplicación, la aplicación debe pedir al usuario que asigne sus valores predeterminados por usuario. Vea [Application First Run (Primera ejecución de la aplicación) y Defaults (Valores predeterminados).](#application-first-run-and-defaults)
-   **A Windows 8:** todos los valores predeterminados son por usuario y se omite cualquier configuración predeterminada por equipo. Las aplicaciones ya no pueden establecer opciones predeterminadas, por lo que no pueden guían al usuario a través de la asignación de esos valores predeterminados.

Cuando una aplicación de Windows 8 implementa **Establecer** como predeterminado en SPAD, se deben seguir estas directrices:

-   Las aplicaciones solo deben reclamar valores predeterminados de nivel de equipo a través de SPAD.
-   Las aplicaciones *no deben* reclamar valores predeterminados por usuario a través de SPAD.

Cuando una Windows 8 implementa **Establecer** como predeterminado en SPAD, debe registrar sus tipos de archivo y protocolos en Programas predeterminados [,](default-programs.md)con el mismo nombre de aplicación que se usa en SPAD. Esto permite que un cambio en SPAD se refleje como un cambio en la entrada Programas predeterminados correspondiente para el usuario actual.

### <a name="hide-access-in-spad"></a>Ocultar el acceso en SPAD

Se tiene acceso a la opción ocultar acceso para cada posible valor predeterminado en SPAD de una de estas dos maneras:

-   Elija la categoría de valores predeterminados que no son de **Microsoft,** que quita el acceso a todos los valores predeterminados de Microsoft.
-   Elija la **categoría** Personalizado y desactive la **casilla Habilitar el** acceso a este programa.

Anteriormente, al realizar cualquiera de esas acciones se quitaba todos los puntos de entrada a las aplicaciones adecuadas del sistema. Las directrices específicas para esta situación indican quitar accesos directos e iconos de las siguientes ubicaciones:

-   Escritorio
-   Menú Inicio
-   inicio rápido (solo Windows Vista y versiones anteriores)
-   Área de notificaciones
-   Menús contextuales
-   Banda de tareas de carpeta

Se recomienda a los proveedores implementar estas directrices en la función de devolución de llamada Ocultar acceso de la aplicación.

### <a name="alternate-hide-access-method-in-spad"></a>Método de acceso hide alternativo en SPAD

Para algunas aplicaciones heredadas, una implementación completa de Ocultar acceso puede no ser práctica. Un método alternativo que logra el mismo efecto, pero que el usuario no puede reversibler fácilmente, es desinstalar la aplicación. A continuación se muestra el comportamiento de ejemplo y el código de ejemplo para implementarlo.

La experiencia de usuario recomendada para esta alternativa es la siguiente:

-   Cuando el usuario desactive la casilla Habilitar acceso a **este programa** en SPAD, se presenta la siguiente interfaz de usuario.

    ![vista dialog box about hiding access to program (Cuadro de diálogo de vista sobre cómo ocultar el acceso al programa)](images/hideaccessvista.png)

-   Cuando el usuario hace  clic en **Aceptar,** se muestra el elemento Programas y características Panel de control para que el usuario pueda desinstalar la aplicación.
-   Los usuarios de Windows XP deben presentar el siguiente cuadro de diálogo.

    ![cuadro de diálogo de Windows XP sobre cómo ocultar el acceso al programa](images/hideaccessxp.png)

-   Cuando el usuario de Windows  XP hace clic en **Aceptar,** se muestra el elemento Agregar o quitar programas de Panel de control para que el usuario pueda desinstalar la aplicación.

El código siguiente proporciona una implementación reutilizable para la característica Ocultar acceso como se ha descrito anteriormente. Se puede usar en Windows XP, Windows Vista y Windows 7.


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



## <a name="registering-for-application-entry-points"></a>Registro para puntos de entrada de la aplicación

Una aplicación puede tener muchos puntos de entrada dentro del sistema operativo. A continuación se recomiendan ubicaciones para los puntos de entrada:

-   Escritorio
-   Menú Inicio
-   inicio rápido (solo Windows Vista y versiones anteriores)
-   Área de notificaciones
-   Menús contextuales
-   Banda de tareas de carpeta

Esta sección se centra en estas áreas específicas:

-   [Abrir con](#open-with)
-   [Menú Inicio y barra inicio rápido inicio](#start-menu-and-quick-launch-bar)

### <a name="open-with"></a>Abrir con

El **menú contextual Abrir con** permite al usuario seleccionar una aplicación que pueda controlar un tipo de archivo específico. Aunque **Abrir con** se puede usar para abrir un archivo con una aplicación una vez, también se puede usar para establecer el valor predeterminado para esa extensión de nombre de archivo. Por lo tanto, una aplicación siempre debe registrarse **para Abrir con** para que los usuarios se presenten con esa aplicación como opción. Las aplicaciones pueden registrar tipos de archivo y protocolos para **Abrir con**. Las aplicaciones que registran protocolos en el marco programas predeterminados se agregan automáticamente a las opciones **Abrir** con para los protocolos.

Para obtener información sobre cómo registrarse **para Abrir con**, vea Introducción a las asociaciones de [archivos](fa-intro.md).

### <a name="start-menu-and-quick-launch-bar"></a>Menú Inicio y barra inicio rápido inicio

Para que el usuario sea más reconocible, las aplicaciones pueden agregar accesos directos a varias ubicaciones de Windows. El lugar más común para agregar un acceso directo es el **menú** Inicio. En Windows Vista y versiones posteriores, una aplicación crea un acceso directo en la carpeta oculta %ProgramData% Programas del menú Inicio de Microsoft Windows para que aparezca en la lista de programas del menú Inicio para todos los \\ \\ \\ \\ usuarios.  Normalmente, una aplicación agrega una subcarpeta que contiene el acceso directo.

Para los programas de explorador y correo electrónico, el menú Inicio de Windows **Vista** también presenta dos vínculos dedicados fuera de la lista de programas, con el título de **Internet** y **correo electrónico.** Una vez que una aplicación se registra para esas categorías, el marco programas predeterminados puede administrar lo que se inicia a través de esos vínculos.

> [!Note]  
> Los **vínculos** de  **menú** Inicio dedicados de Internet y correo electrónico ya no están presentes a partir de Windows 7.

 

Para aumentar aún más la detectabilidad, las aplicaciones también pueden agregar accesos directos al escritorio y a la inicio rápido configuración. Las aplicaciones deben pedir permiso al usuario (normalmente durante la instalación  o en la primera ejecución) antes de agregar un icono al menú Inicio, al escritorio o a inicio rápido barra.

> [!Note]  
> La inicio rápido ya no está disponible a partir de Windows 7. La alternativa de Windows 7 es que la aplicación esté anclada a la barra de tareas, pero la anclación no se puede realizar mediante programación, ya que es estrictamente una opción del usuario.

 

Para más información, consulte los temas siguientes:

-   [Cómo registrar un explorador de Internet o un cliente de correo electrónico con el menú Inicio de Windows](start-menu-reg.md)
-   [Registro de programas con tipos de cliente](reg-middleware-apps.md)

## <a name="application-installation-and-defaults"></a>Instalación de la aplicación y valores predeterminados

Los procedimientos de instalación de aplicaciones no han cambiado fundamentalmente desde Windows XP, a excepción de una nueva guía para los sistemas que ejecutan versiones de Windows anteriores a Windows 8: tome los valores predeterminados por equipo en el momento de la instalación, pero no establezca ningún valor predeterminado por usuario hasta que ese usuario ejecute la aplicación por primera vez. (Vea [Application First Run (Primera ejecución de la aplicación) y Defaults (Valores predeterminados).](#application-first-run-and-defaults) Las aplicaciones no deben establecer valores predeterminados por usuario durante la instalación porque hay situaciones en las que la persona que instala la aplicación no es el usuario previsto. A Windows 8, no se admiten los valores predeterminados por equipo y las aplicaciones no pueden cambiar la configuración predeterminada por usuario.

Durante la instalación, una aplicación debe copiar sus archivos binarios en el disco duro y escribir sus ProgID en el Registro. La aplicación también debe registrarse en Programas predeterminados y **Abrir** con en este momento para cada asociación de archivos que sea candidata para controlar. La aplicación puede usar la subclave **OpenWithProgIds** para registrarse con **Open With**.

Para más información, consulte los temas siguientes:

-   [Programas predeterminados](default-programs.md)
-   [Introducción a las asociaciones de archivos](fa-intro.md)

## <a name="application-upgrades-and-defaults"></a>Actualizaciones de aplicaciones y valores predeterminados

Muchas aplicaciones tienen la capacidad de actualizarse a sí mismas a lo largo del tiempo. Este procedimiento de actualización no debe cambiar el estado de los valores predeterminados por usuario porque ese cambio sería inesperado para el usuario. Sin embargo, es aceptable que una aplicación compruebe las asociaciones de archivos de nivel de equipo y las repare si se han dañado.

## <a name="application-first-run-and-defaults"></a>Ejecución de la primera aplicación y valores predeterminados

> [!Note]  
> A Windows 8, el sistema controla este procedimiento en nombre de todas las aplicaciones. Las aplicaciones ya no pueden consultar ni cambiar los valores predeterminados. Solo el usuario puede hacerlo. Por lo tanto, las aplicaciones no deben intentar consultar el valor predeterminado actual ni cambiar ese valor predeterminado mediante ningún mecanismo. Sin embargo, las aplicaciones pueden proporcionar un punto de entrada a Programas predeterminados en el Panel de control llamando al método [**LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) de la interfaz [**IApplicationAssociationRegistrationUI.**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

 

Con la introducción de los valores predeterminados por usuario en Windows Vista, es importante que las aplicaciones que concursan por extensiones de nombre de archivo populares proporcionen una experiencia de usuario común para reclamar estas extensiones. Dado que estos valores predeterminados ahora se establecen en el contexto del usuario, deben presentarse como una posibilidad predeterminada solo cuando el usuario ejecuta el programa después de la instalación.

La guía para establecer los valores predeterminados por usuario es esta: cuando una aplicación se ejecuta por primera vez para un usuario específico, esa aplicación debe solicitar preferencias de usuario para los valores predeterminados y las asociaciones de archivo para sí misma.

La interfaz de usuario recomendada debe proporcionar dos opciones claras al usuario:

1.  Acepte todos los valores predeterminados que la aplicación desea reclamar. Esta opción también puede establecer otras propiedades predeterminadas de la aplicación, como la privacidad o la configuración de actualización automática. Esta opción permite que la aplicación reclame todos sus valores predeterminados registrados.
2.  Personalice aceptando o no las selecciones predeterminadas y la configuración del programa individualmente. Esta opción presenta una interfaz de usuario adicional que permite al usuario tomar opciones pormenorizados para sus opciones predeterminadas.

Para obtener más información, vea [Programas predeterminados.](default-programs.md)

## <a name="verifying-defaults-and-asking-for-user-consent"></a>Comprobar los valores predeterminados y solicitar el consentimiento del usuario

> [!Note]  
> Esto no se admite a Windows 8.

 

Una vez que una aplicación se registra con programas predeterminados en Windows Vista y versiones posteriores, ciertas API estarán disponibles para la aplicación. Por ejemplo, es posible que una aplicación tenga que comprobar si es el programa predeterminado. La [**interfaz IApplicationAssociationRegistration proporciona**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) métodos para ello.

Cualquier aplicación que quiera reclamar valores predeterminados debe preguntar primero al usuario y nunca reclamar los valores predeterminados sin permiso. Se debe preguntar al usuario si quiere que la aplicación sea el valor predeterminado o dejar el valor predeterminado actual en su lugar. También debe haber una opción para no volver a hacer esta pregunta después de que el usuario haya elegido.

Para obtener más información, vea [Programas predeterminados.](default-programs.md)

## <a name="application-compatibility-tips"></a>Sugerencias de compatibilidad de aplicaciones

En esta sección se proporcionan algunas sugerencias de compatibilidad de aplicaciones relacionadas con la experiencia programas predeterminados en Windows.

### <a name="avoid-triggering-per-user-virtualization"></a>Evitar desencadenar la virtualización Per-User virtualización

Con el entorno de control de cuentas de usuario (UAC), las aplicaciones siempre deben ejecutarse con solo derechos de usuario estándar para obtener la mejor experiencia del cliente. Por motivos de seguridad, las aplicaciones con un nivel de privilegio de usuario estándar no pueden escribir en determinadas partes del Registro y en determinados archivos del sistema. Windows Vista y versiones posteriores de Windows proporcionan una capa de compatibilidad temporal de aplicaciones (AppCompat) para ayudar a las aplicaciones a realizar la transición. Los intentos bloqueados de escribir en el Registro o en los archivos del sistema se "virtualizan" para que la aplicación siga en ejecución, pero no se modifican las áreas confidenciales del sistema. Sin embargo, las aplicaciones no deben basarse en la tecnología AppCompat como una solución a largo plazo. En su lugar, las aplicaciones deben usar las muchas herramientas disponibles para comprobar que se pueden ejecutar correctamente con derechos de usuario estándar. Es posible que sea necesario realizar alguna reprogramación de la aplicación para lograr esto, pero debe realizarse en a favor de la compatibilidad a largo plazo.

### <a name="avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant"></a>Evitar advertencias o bloques de AppCompat desde el Asistente para compatibilidad de programas

El Asistente para la compatibilidad de programas (PCA) se proporciona en Windows Vista y versiones posteriores. Su propósito es proporcionar un método automatizado para mejorar el funcionamiento de los programas antiguos con problemas de compatibilidad. El PCA supervisa los programas en busca de problemas conocidos. Si se detecta un problema, notifica al usuario el problema y le ofrece que aplique soluciones eficaces antes de que el usuario ejecute de nuevo el programa. Para evitar ver estas advertencias o bloques, los ISV deben usar las muchas herramientas disponibles para asegurarse de que sus aplicaciones son compatibles con Windows Vista, Windows 7 y versiones posteriores.

### <a name="support-for-previous-windows-operating-system-versions"></a>Compatibilidad con versiones anteriores del sistema operativo Windows

La infraestructura programas predeterminados no está disponible en ningún sistema operativo Windows antes de Windows Vista. Por lo tanto, cuando las aplicaciones se mueven a la nueva infraestructura de programas predeterminados, deben conservar su código anterior de los valores predeterminados de la aplicación para mantener la compatibilidad con versiones anteriores de Windows. Una aplicación debe ejecutar una comprobación de versión del sistema operativo como parte de su instalación para determinar qué código predeterminado de la aplicación se debe ejecutar.

Para admitir una actualización de Windows XP a Windows Vista o posterior, las aplicaciones deben agregar todas las entradas del Registro necesarias para los programas predeterminados incluso cuando se instalan en un equipo que ejecuta Windows XP. El registro no tendrá ningún efecto en un equipo que ejecuta Windows XP, pero si el equipo se actualiza más adelante, la aplicación ya estará registrada y podrá aprovechar el marco.

Para obtener más información, [**vea OSVERSIONINFO**](/windows/win32/api/winnt/ns-winnt-osversioninfoa).

## <a name="additional-resources"></a>Recursos adicionales

-   [Introducción a las asociaciones de archivos](fa-intro.md)
-   [Cómo registrar un explorador de Internet o un cliente de correo electrónico con el menú Inicio de Windows](start-menu-reg.md)
-   [Registro de una aplicación en un esquema uri](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos recomendados para asociaciones de archivos](fa-best-practices.md)
</dt> <dt>

[Escenario de ejemplo de asociación de archivos](fa-sample-scenarios.md)
</dt> <dt>

[Programas predeterminados](default-programs.md)
</dt> <dt>

[Trabajar con establecer el acceso al programa y los valores predeterminados del equipo (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
