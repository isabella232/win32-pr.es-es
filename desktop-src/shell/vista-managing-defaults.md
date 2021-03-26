---
description: Este tema proporciona a los fabricantes de software independientes (ISV) una guía rápida de los pasos necesarios para registrar y administrar los valores predeterminados de las aplicaciones en Windows Vista y versiones posteriores. Se proporcionan vínculos a artículos más detallados sobre el tema de cada sección.
ms.assetid: 649eb20d-07d3-4209-abff-45fc50f05631
title: Administración de aplicaciones predeterminadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de40d6c80aae4005fc015c08ef7bf2907289e795
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909513"
---
# <a name="managing-default-applications"></a>Administración de aplicaciones predeterminadas

La característica **Configurar acceso y programas predeterminados del equipo** (SPAD) se ha agregado a Windows XP y versiones posteriores de Windows para administrar los valores predeterminados por equipo. Además de SPAD, Windows Vista presentó el concepto de aplicaciones predeterminadas por usuario y el elemento **programas predeterminados** en el panel de control.

> [!IMPORTANT]
> Este tema no se aplica a Windows 10. La forma en que las asociaciones de archivos predeterminadas funcionan en Windows 10. Para obtener más información, consulte la sección **cambios en la forma en que Windows 10 trata las aplicaciones predeterminadas** en [esta publicación](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

La configuración predeterminada por usuario es específica de una cuenta de usuario individual en el sistema. Si los valores predeterminados de cada usuario están presentes, tienen prioridad sobre los valores predeterminados correspondientes por equipo para esa cuenta. A partir de Windows 8, el sistema de extensibilidad para el tipo de archivo y los valores predeterminados del protocolo es estrictamente por usuario y se omiten los valores predeterminados por equipo. SPAD también cambió en Windows 8 para establecer los valores predeterminados por usuario.

-   En los sistemas que ejecutan versiones de Windows anteriores a Windows 8, una cuenta de usuario recién creada recibe los valores predeterminados por equipo hasta que se establecen los valores predeterminados por usuario. En Windows Vista y versiones posteriores, los usuarios pueden usar el elemento **programas predeterminados** del panel de control para establecer o cambiar sus valores predeterminados por usuario. Además, cuando se ejecuta una aplicación por primera vez, se pueden establecer los valores predeterminados por usuario mediante las instrucciones que se indican a continuación en la sección [primera ejecución de la aplicación y valores predeterminados](#application-first-run-and-defaults) .
-   En los sistemas que ejecutan Windows 8, una cuenta de usuario recién creada se basa en los valores predeterminados por usuario del inicio y la configuración de los valores predeterminados en la primera ejecución, tal y como se explica en la sección [primera ejecución de la aplicación y valores predeterminados](#application-first-run-and-defaults) ya no se admite.

Una aplicación debe registrarse con SPAD y la característica programas predeterminados que se va a ofrecer como programa predeterminado en Windows Vista y versiones posteriores.

Este tema proporciona a los fabricantes de software independientes (ISV) una guía rápida de los pasos necesarios para registrar y administrar los valores predeterminados de las aplicaciones en Windows Vista y versiones posteriores. Se proporcionan vínculos a artículos más detallados sobre el tema de cada sección.

-   [Elemento programas predeterminados en el panel de control](#default-programs-item-in-control-panel)
-   [Establecer los valores predeterminados de acceso a programas y del equipo](#set-program-access-and-computer-defaults)
    -   [Establecer valores predeterminados en SPAD](#setting-defaults-in-spad)
    -   [Ocultar acceso en SPAD](#hide-access-in-spad)
-   [Registrar para puntos de entrada de la aplicación](#registering-for-application-entry-points)
    -   [Abrir con](#open-with)
    -   [Menú Inicio y barra de inicio rápido](#start-menu-and-quick-launch-bar)
-   [Instalación y valores predeterminados de la aplicación](#application-installation-and-defaults)
-   [Actualizaciones y valores predeterminados de aplicaciones](#application-upgrades-and-defaults)
-   [Primera ejecución de la aplicación y valores predeterminados](#application-first-run-and-defaults)
-   [Comprobar los valores predeterminados y solicitar el consentimiento del usuario](#verifying-defaults-and-asking-for-user-consent)
-   [Sugerencias de compatibilidad de aplicaciones](#application-compatibility-tips)
    -   [Evite desencadenar la virtualización de Per-User](#avoid-triggering-per-user-virtualization)
    -   [Evitar las advertencias o los bloques de AppCompat del Asistente para la compatibilidad de programas](#avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant)
    -   [Compatibilidad con versiones anteriores del sistema operativo Windows](#support-for-previous-windows-operating-system-versions)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="default-programs-item-in-control-panel"></a>Elemento programas predeterminados en el panel de control

**Programas predeterminados** es una característica introducida en Windows Vista, accesible directamente desde el menú **Inicio** , así como el panel de control. Proporciona una nueva infraestructura que funciona con privilegios de usuario estándar (no elevado) y está diseñado para permitir que los usuarios y las aplicaciones administren los valores predeterminados por usuario. Para los usuarios, programas predeterminados proporciona una forma unificada y fácilmente accesible de administrar valores predeterminados, asociaciones de archivos y configuraciones de reproducción automática en todas las aplicaciones del sistema. En el caso de las aplicaciones, el uso del ámbito por usuario proporcionado por las API de programas predeterminados ofrece las siguientes ventajas:

-   **Sin elevación**

    Una aplicación no tiene que elevar sus privilegios para reclamar los valores predeterminados.

-   **Buena ciudadanía**

    En un equipo con varios usuarios, cada usuario puede seleccionar diferentes aplicaciones predeterminadas.

-   **Administración predeterminada**

    Las API de programas predeterminados ofrecen un mecanismo confiable y coherente para la comprobación automática del estado predeterminado y la recuperación de la configuración perdida sin tener que recurrir a escribir directamente en el registro. Sin embargo, a partir de Windows 8, no se recomienda que las aplicaciones consulten el estado predeterminado, ya que una aplicación ya no puede cambiar la configuración predeterminada, por lo que solo el usuario puede realizar los cambios.

Para permitir que la aplicación administre los valores predeterminados de forma eficaz, debe registrar la aplicación como un posible programa predeterminado. Para obtener más información sobre el registro y el uso de las API de programas predeterminados, consulte [programas predeterminados](default-programs.md).

Programas predeterminados también proporciona estas dos características:

-   **Interfaz de usuario de valores predeterminados reutilizables**

    La interfaz de usuario de los valores predeterminados del programa (**establecer los programas predeterminados**) y las asociaciones de archivo (**asociar un tipo de archivo o protocolo con un programa**) se puede reutilizar y llamar desde dentro de una aplicación. Esto permite a las aplicaciones proporcionar una experiencia de usuario estándar para administrar los valores predeterminados y evita que los ISV tengan que desarrollar una interfaz de usuario personalizada o equivalente.

-   **Inclusión de información de marketing y URL**

    Como parte de la página **establecer programas predeterminados** del elemento **programas predeterminados** en el panel de control, una aplicación puede proporcionar información de marketing y un vínculo al sitio web del proveedor. Esta dirección URL se deriva del certificado Authenticode con el que se ha firmado la aplicación. Esto evita el uso incorrecto y el reemplazo no autorizado de este vínculo. Si una aplicación tiene un certificado Authenticode que incluye una dirección URL incrustada, la interfaz de usuario de Windows muestra esa dirección URL insertada. Los ISV deben aprovechar esta característica para dirigir a los usuarios a su sitio web en busca de actualizaciones y otras descargas.

## <a name="set-program-access-and-computer-defaults"></a>Establecer los valores predeterminados de acceso a programas y del equipo

**Establecer los valores predeterminados de acceso a programas y del equipo** (SPAD) permite a los administradores administrar los valores predeterminados para todo el equipo heredados por todos los nuevos usuarios de ese equipo. Antes de Windows 8, SPAD también permitía a los administradores reparar las asociaciones de archivo en caso de que se interrumpiera cuando se quitaban programas del sistema. Sin embargo, a partir de Windows 8, SPAD solo afecta a los valores predeterminados específicos del usuario.

Para obtener más información sobre el registro de una aplicación en SPAD, vea [trabajar con configurar el acceso y los valores predeterminados del equipo (SPAD)](cpl-setprogramaccess.md) y [registrar programas con tipos de cliente](reg-middleware-apps.md). En las secciones siguientes se describen los cambios específicos y las nuevas recomendaciones.

### <a name="setting-defaults-in-spad"></a>Establecer valores predeterminados en SPAD

Los valores predeterminados por usuario invalidan los valores predeterminados por equipo.

-   **Antes de Windows 8**: los valores predeterminados establecidos en SPAD (que son por equipo) no serán visibles para los usuarios si se establecen los valores predeterminados por usuario correspondientes. Si un usuario no ha establecido un valor predeterminado por usuario, el sistema utiliza el valor predeterminado correspondiente del equipo. Las nuevas cuentas de usuario de un equipo heredan inicialmente los valores predeterminados del equipo. La primera vez que un usuario ejecuta una aplicación, la aplicación debe solicitar al usuario que asigne sus valores predeterminados por usuario. Vea la [primera ejecución de la aplicación y los valores predeterminados](#application-first-run-and-defaults).
-   A **partir de Windows 8**: todos los valores predeterminados son por usuario y se omite cualquier valor predeterminado por equipo. Las aplicaciones ya no pueden establecer las opciones predeterminadas, por lo que no pueden guiar al usuario a través de la asignación de esos valores predeterminados.

Cuando una aplicación anterior a Windows 8 implementa **set como valor predeterminado** en SPAD, se deben seguir estas directrices:

-   Las aplicaciones solo deben solicitar los valores predeterminados de nivel de equipo mediante SPAD.
-   Las aplicaciones *no* deben reclamar los valores predeterminados por usuario a través de SPAD.

Cuando una aplicación de Windows 8 implementa **set como valor predeterminado** en SPAD, deben registrar sus tipos de archivo y protocolos en [programas predeterminados](default-programs.md), con el mismo nombre de aplicación que se usa en SPAD. Esto permite que un cambio en SPAD se refleje como un cambio en la entrada de programas predeterminados correspondiente para el usuario actual.

### <a name="hide-access-in-spad"></a>Ocultar acceso en SPAD

Se tiene acceso a la opción ocultar acceso para cada valor predeterminado posible en SPAD de una de estas dos maneras:

-   Elija la categoría de valores predeterminados que **no sean de Microsoft** , lo que elimina el acceso a todos los valores predeterminados de Microsoft.
-   Elija la categoría **personalizado** y desactive la casilla **Habilitar el acceso a este programa** .

Anteriormente, realizar cualquiera de esas acciones quitaba todos los puntos de entrada de las aplicaciones adecuadas en el sistema. Las instrucciones específicas para esta situación indican quitar accesos directos e iconos de las siguientes ubicaciones:

-   Escritorio
-   Menú Inicio
-   Barra de inicio rápido (solo Windows Vista y versiones anteriores)
-   Área de notificaciones
-   Menús contextuales
-   Banda de tareas de carpeta

Se recomienda a los proveedores que implementen estas instrucciones en la función de devolución de llamada de ocultación de acceso de la aplicación.

### <a name="alternate-hide-access-method-in-spad"></a>Método de acceso de ocultación alternativo en SPAD

En el caso de algunas aplicaciones heredadas, es posible que una implementación completa de ocultar acceso no sea práctica. Un método alternativo que logra el mismo efecto, pero que el usuario no es fácilmente reversible, es desinstalar la aplicación. A continuación se muestra el comportamiento de ejemplo y el código de ejemplo para implementar esto.

La experiencia de usuario recomendada para esta alternativa es la siguiente:

-   Cuando el usuario desactiva la casilla **Habilitar el acceso a este programa** en SPAD, se presenta la siguiente interfaz de usuario.

    ![cuadro de diálogo vista sobre cómo ocultar el acceso al programa](images/hideaccessvista.png)

-   Cuando el usuario hace clic en **Aceptar**, se muestra el elemento **programas y características** del panel de control para que el usuario pueda desinstalar la aplicación.
-   Los usuarios de Windows XP deben aparecer con el siguiente cuadro de diálogo.

    ![cuadro de diálogo de Windows XP acerca de cómo ocultar el acceso al programa](images/hideaccessxp.png)

-   Cuando el usuario de Windows XP hace clic en **Aceptar**, se muestra el elemento **Agregar o quitar programas** del panel de control para que el usuario pueda desinstalar la aplicación.

En el código siguiente se proporciona una implementación reutilizable para la característica de ocultación de acceso, tal y como se ha descrito anteriormente. Se puede usar en Windows XP, Windows Vista y Windows 7.


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



## <a name="registering-for-application-entry-points"></a>Registrar para puntos de entrada de la aplicación

Una aplicación puede tener muchos puntos de entrada en el sistema operativo. A continuación se indican las ubicaciones recomendadas para los puntos de entrada:

-   Escritorio
-   Menú Inicio
-   Barra de inicio rápido (solo Windows Vista y versiones anteriores)
-   Área de notificaciones
-   Menús contextuales
-   Banda de tareas de carpeta

Esta sección se centra en estas áreas específicas:

-   [Abrir con](#open-with)
-   [Menú Inicio y barra de inicio rápido](#start-menu-and-quick-launch-bar)

### <a name="open-with"></a>Abrir con

El menú contextual **abrir con** permite al usuario seleccionar una aplicación que puede controlar un tipo de archivo específico. Aunque **abrir con** puede usarse para abrir un archivo con una aplicación una vez, también puede usarse para establecer el valor predeterminado de esa extensión de nombre de archivo. Por lo tanto, una aplicación siempre debe registrarse para **Open with** , de modo que los usuarios se presenten con esa aplicación como opción. Las aplicaciones pueden registrar los tipos de archivo y protocolos para **abrir con**. Las aplicaciones que registran protocolos en el marco programas predeterminados se agregan automáticamente a las opciones **abrir con** para los protocolos.

Para obtener información sobre el registro para **Open with**, vea [Introducción a las asociaciones de archivo](fa-intro.md).

### <a name="start-menu-and-quick-launch-bar"></a>Menú Inicio y barra de inicio rápido

Para que sea más reconocible para el usuario, las aplicaciones pueden agregar accesos directos a varias ubicaciones en Windows. El lugar más común para agregar un acceso directo es el menú **Inicio** . En Windows Vista y versiones posteriores, una aplicación crea un acceso directo en la carpeta oculta% ProgramData% \\ Microsoft \\ Windows \\ menú Inicio \\ programas para que aparezca en la lista de programas del menú **Inicio** para todos los usuarios. Normalmente, una aplicación agrega una subcarpeta que contiene el acceso directo.

En el caso de los programas de correo electrónico y explorador, el menú **Inicio** de Windows Vista también presenta dos vínculos dedicados fuera de la lista de programas, denominados canonmente **Internet** y **correo electrónico**. Una vez que una aplicación se registra para esas categorías, el marco de trabajo de programas predeterminados puede administrar lo que se inicia a través de esos vínculos.

> [!Note]  
> Los vínculos del menú **Inicio** de **Internet** y el **correo electrónico** dedicado ya no están presentes en Windows 7.

 

Para aumentar la capacidad de detección, las aplicaciones también pueden agregar accesos directos al escritorio y a la barra de inicio rápido. Las aplicaciones deben pedir permiso al usuario (normalmente durante la instalación o en la primera ejecución) antes de agregar un icono al menú **Inicio** , al escritorio o a la barra de inicio rápido.

> [!Note]  
> La barra de inicio rápido ya no está disponible a partir de Windows 7. La alternativa de Windows 7 es que la aplicación esté anclada a la barra de tareas, pero el anclaje no se puede realizar mediante programación, ya que es estrictamente una opción del usuario.

 

Para más información, consulte los temas siguientes:

-   [Cómo registrar un explorador de Internet o un cliente de correo electrónico con el menú Inicio de Windows](start-menu-reg.md)
-   [Registrar programas con tipos de cliente](reg-middleware-apps.md)

## <a name="application-installation-and-defaults"></a>Instalación y valores predeterminados de la aplicación

Los procedimientos de instalación de aplicaciones no han cambiado fundamentalmente desde Windows XP, con la excepción de una nueva directriz para sistemas que ejecutan versiones de Windows anteriores a Windows 8: toman los valores predeterminados por equipo en el momento de la instalación, pero no establecen los valores predeterminados por usuario hasta que el usuario ejecuta la aplicación por primera vez. (Consulte [primera ejecución de la aplicación y valores predeterminados](#application-first-run-and-defaults)). Las aplicaciones no deben establecer los valores predeterminados por usuario durante la instalación porque hay situaciones en las que la persona que instala la aplicación no es el usuario previsto. A partir de Windows 8, no se admiten los valores predeterminados por equipo y las aplicaciones no pueden cambiar la configuración predeterminada por usuario.

Durante la instalación, una aplicación debe copiar sus archivos binarios en el disco duro y escribir sus ProgID en el registro. La aplicación también debe registrarse para programas predeterminados y **abrir con** en este momento para cada Asociación de archivo que sea candidata a administrar. La aplicación puede usar la subclave **OpenWithProgIds** para registrarse con **Open with**.

Para más información, consulte los temas siguientes:

-   [Programas predeterminados](default-programs.md)
-   [Introducción a las asociaciones de archivos](fa-intro.md)

## <a name="application-upgrades-and-defaults"></a>Actualizaciones y valores predeterminados de aplicaciones

Muchas aplicaciones tienen la capacidad de actualizarse a lo largo del tiempo. Este procedimiento de actualización no debe cambiar el estado de los valores predeterminados por usuario, ya que ese cambio sería inesperado para el usuario. Sin embargo, es aceptable que una aplicación Compruebe las asociaciones de archivos de nivel de equipo y las repare si se han dañado.

## <a name="application-first-run-and-defaults"></a>Primera ejecución de la aplicación y valores predeterminados

> [!Note]  
> A partir de Windows 8, el sistema controla este procedimiento en nombre de todas las aplicaciones. Las propias aplicaciones ya no pueden consultar y cambiar los valores predeterminados. Solo el usuario puede hacerlo. Por lo tanto, las aplicaciones no deberían intentar consultar el valor predeterminado actual o cambiarlo de forma predeterminada a través de cualquier mecanismo. Sin embargo, las aplicaciones pueden proporcionar un punto de entrada a los programas predeterminados en el panel de control llamando al método [**LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) de la interfaz [**IApplicationAssociationRegistrationUI**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui) .

 

Con la introducción de los valores predeterminados por usuario en Windows Vista, es importante que las aplicaciones que contratan las extensiones de nombre de archivo más populares proporcionen una experiencia de usuario común para reclamar estas extensiones. Dado que estos valores predeterminados se establecen ahora en el contexto del usuario, deben presentarse como una posibilidad predeterminada solo cuando el usuario ejecuta el programa después de la instalación.

La directriz para establecer los valores predeterminados por usuario es la siguiente: cuando se ejecuta una aplicación por primera vez para un usuario específico, esa aplicación debe solicitar preferencias de usuario para los valores predeterminados y las asociaciones de archivo para sí mismo.

La interfaz de usuario recomendada debe proporcionar dos opciones claras al usuario:

1.  Acepte todos los valores predeterminados a los que la aplicación desea recibir notificaciones. Esta opción también puede establecer otras propiedades predeterminadas de la aplicación, como la privacidad o la configuración de actualización automática. Esta opción permite a la aplicación reclamar todos sus valores predeterminados registrados.
2.  Para personalizar, acepte o no acepte las selecciones predeterminadas y la configuración del programa de forma individual. Esta opción presenta una interfaz de usuario adicional que permite al usuario realizar elecciones pormenorizadas para sus opciones predeterminadas.

Para obtener más información, consulte [programas predeterminados](default-programs.md).

## <a name="verifying-defaults-and-asking-for-user-consent"></a>Comprobar los valores predeterminados y solicitar el consentimiento del usuario

> [!Note]  
> Esto no se admite en Windows 8.

 

Después de que una aplicación se registra con programas predeterminados en Windows Vista y versiones posteriores, algunas API están disponibles para la aplicación. Por ejemplo, es posible que una aplicación necesite comprobar si es el programa predeterminado. La interfaz [**IApplicationAssociationRegistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) proporciona métodos para hacerlo.

Cualquier aplicación que desee reclamar valores predeterminados debe preguntar primero al usuario y nunca reclamar los valores predeterminados sin permiso. Se debe preguntar al usuario si desea que la aplicación sea la predeterminada o dejar el valor predeterminado actual. También debe existir una opción para no volver a preguntar esta pregunta una vez que el usuario ha elegido su elección.

Para obtener más información, consulte [programas predeterminados](default-programs.md).

## <a name="application-compatibility-tips"></a>Sugerencias de compatibilidad de aplicaciones

En esta sección se proporcionan algunas sugerencias de compatibilidad de aplicaciones relacionadas con la experiencia de programas predeterminados en Windows.

### <a name="avoid-triggering-per-user-virtualization"></a>Evite desencadenar la virtualización de Per-User

Con el entorno de control de cuentas de usuario (UAC), las aplicaciones siempre deben ejecutarse con derechos de usuario estándar para la mejor experiencia de cliente. Por motivos de seguridad, las aplicaciones con un nivel de privilegios de usuario estándar no pueden escribir en determinadas partes del registro y en ciertos archivos del sistema. Windows Vista y versiones posteriores de Windows proporcionan una capa de compatibilidad de aplicaciones temporal (AppCompat) para ayudar a las aplicaciones a realizar la transición. Los intentos bloqueados para escribir en el registro o en los archivos del sistema se "virtualizan" para que la aplicación continúe ejecutándose, pero no se modifican las áreas confidenciales del sistema. Sin embargo, las aplicaciones no deben basarse en la tecnología AppCompat como una solución a largo plazo. En su lugar, las aplicaciones deben usar las muchas herramientas disponibles para comprobar que se pueden ejecutar correctamente con derechos de usuario estándar. Es posible que sea necesaria la reprogramación de la aplicación para lograrlo, pero debe hacerse en interés de la compatibilidad a largo plazo.

### <a name="avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant"></a>Evitar las advertencias o los bloques de AppCompat del Asistente para la compatibilidad de programas

El Asistente para la compatibilidad de programas (PCA) se proporciona en Windows Vista y versiones posteriores. Su finalidad es proporcionar un método automatizado para que los programas anteriores con problemas de compatibilidad funcionen mejor. El PCA supervisa los programas en busca de problemas conocidos. Si se detecta un problema, informa al usuario del problema y ofrece la aplicación de soluciones eficaces antes de que el usuario vuelva a ejecutar el programa. Para evitar ver estas advertencias o bloques, los ISV deben usar las muchas herramientas disponibles para asegurarse de que sus aplicaciones son compatibles con Windows Vista, Windows 7 y versiones posteriores.

### <a name="support-for-previous-windows-operating-system-versions"></a>Compatibilidad con versiones anteriores del sistema operativo Windows

La infraestructura programas predeterminados no está disponible en ningún sistema operativo Windows antes de Windows Vista. Por lo tanto, cuando las aplicaciones pasan a la nueva infraestructura de programas predeterminados, deben conservar el código predeterminado de la aplicación anterior para mantener la compatibilidad con versiones anteriores de Windows. Una aplicación debe ejecutar una comprobación de la versión del sistema operativo como parte de la instalación para determinar qué código predeterminado de la aplicación debe ejecutarse.

Para admitir una actualización de Windows XP a Windows Vista o posterior, las aplicaciones deben agregar todas las entradas del registro necesarias para los programas predeterminados incluso cuando se instalan en un equipo que ejecuta Windows XP. El registro no tendrá ningún efecto en un equipo que ejecute Windows XP, pero si el equipo se actualiza posteriormente, la aplicación ya estará registrada y podrá aprovechar el marco de trabajo.

Para obtener más información, consulte [**OSVERSIONINFO**](/windows/win32/api/winnt/ns-winnt-osversioninfoa).

## <a name="additional-resources"></a>Recursos adicionales

-   [Introducción a las asociaciones de archivos](fa-intro.md)
-   [Cómo registrar un explorador de Internet o un cliente de correo electrónico con el menú Inicio de Windows](start-menu-reg.md)
-   [Registrar una aplicación en un esquema de URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Prácticas recomendadas para asociaciones de archivos](fa-best-practices.md)
</dt> <dt>

[Escenario de ejemplo de Asociación de archivos](fa-sample-scenarios.md)
</dt> <dt>

[Programas predeterminados](default-programs.md)
</dt> <dt>

[Trabajar con establecer valores predeterminados de acceso a programas y del equipo (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
