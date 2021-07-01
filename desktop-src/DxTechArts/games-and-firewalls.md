---
title: Firewall de Windows para desarrolladores de juegos
description: 'En este artículo se describe el Firewall de Windows: por qué existe, lo que logra y cómo lo hace. Lo más importante es que describe cómo configurar el juego para que funcione bien con el firewall.'
ms.assetid: 2ee9f769-03dc-3661-5d5b-6a4ecd151fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c7ff3c9b651b6264703732f0eec57054784034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120240"
---
# <a name="windows-firewall-for-game-developers"></a>Firewall de Windows para desarrolladores de juegos

En este artículo se describe el Firewall de Windows: por qué existe, lo que logra y cómo lo hace. Lo más importante es que describe cómo configurar el juego para que funcione bien con el firewall.

Contenido:

-   [¿Qué es un firewall?](#what-is-a-firewall)
-   [¿Cómo puedo saber si mi juego se ve afectado?](#how-can-i-tell-if-my-game-is-affected)
-   [Firewall anterior a Windows XP SP2](#the-firewall-before-windows-xp-sp2)
-   [Firewall de Windows XP SP2 es mejor](#windows-xp-sp2-firewall-is-better)
-   [Trabajar con firewall de Windows](#working-with-the-windows-firewall)
-   [Integración mediante InstallShield InstallScript](#integrating-using-installshield-installscript)
-   [Integración en Wise for Windows Installer](#integrating-into-wise-for-windows-installer)
-   [Integración en Windows Installer](#integrating-into-windows-installer)
-   [Recomendaciones](#recommendations)

## <a name="what-is-a-firewall"></a>¿Qué es un firewall?

El firewall proporciona una barrera contra las intrusiones basadas en red. Bloquea el tráfico entrante no solicitado y hace que el sistema sea prácticamente invisible en Internet al rechazar las solicitudes icmp (Protocolo de mensajes de control de Internet). Esto significa que ping y tracert no funcionarán. El firewall también busca y rechaza paquetes no válidos.

Esta barrera evita ataques oportunistas. Los ataques se propagan mediante la búsqueda de muchos sistemas con la misma vulnerabilidad. El firewall puede impedir muchos ataques mediante la colocación de un signo de "no molestar" para esas características que no se están utilizando actualmente. el ataque se omite y no se realiza en casa. La ventaja esencial del Firewall de Windows es que las características y aplicaciones que no están en uso no pueden ser vías de ataque.

El usuario configura el sistema para identificar qué aplicaciones y características son necesarias y deben estar abiertas a la red. Esto sucede cuando se instala una aplicación o cuando intenta abrirse a la red.

## <a name="how-can-i-tell-if-my-game-is-affected"></a>¿Cómo puedo saber si mi juego se ve afectado?

Con la llegada de Windows XP SP2, el Firewall de Windows se ha implementado ampliamente. Todos los juegos multijugador de Windows se ven afectados hasta cierto punto. Aunque los clientes suelen estar en buen estado, los servidores, hosts y pares del mismo nivel necesitan que el firewall esté configurado para seguir funcionando. En concreto, se descarta el tráfico entrante no solicitado. El firewall intercepta los paquetes de filtro de tráfico de red en función del contenido de los paquetes y la actividad de red reciente. El firewall usa el contenido y la actividad para decidir reenviar o quitar un paquete. Una vez configurado correctamente el firewall, un juego podrá aceptar el tráfico entrante no solicitado como antes.

¿Quién tiene tráfico entrante no solicitado?

-   Cliente/servidor: todos los participantes se conectan a un servidor central. El servidor central es el que tiene tráfico entrante no solicitado. Los clientes que se conectan al servidor solicitan tráfico de retorno, que se espera y puede pasar a través del firewall si se siguen las reglas para los clientes. El servidor central debe configurarse para aceptar el tráfico no solicitado para permitir que el tráfico del cliente pase a través del firewall.
-   Multijugador masivo (MMP): todos los participantes están conectados a un centro de datos. Esto equivale a una relación compleja entre cliente y servidor, ya que el centro de datos tiene el tráfico entrante no solicitado. Los participantes son clientes y, en general, no necesitan aceptar tráfico no solicitado.
-   Punto a punto, donde todos los participantes están conectados entre sí directamente: todos los participantes deben estar listos para aceptar el tráfico no solicitado de cualquier nuevo jugador que se una al grupo. En cierto sentido, cada uno de los participantes debe funcionar como un host, por lo que todos deben configurarse como si fueran hosts.

Por lo general, los clientes están en buen estado. Sus conexiones salientes del Protocolo de control de transmisión/Protocolo de Internet (TCP/IP) funcionarán correctamente, al igual que los mensajes salientes del Protocolo de datagramas de usuario (UDP) junto con las respuestas a tiempo a esos mensajes: el firewall mantiene el puerto abierto durante 90 segundos después de cada mensaje saliente en previsión de una respuesta.

## <a name="the-firewall-before-windows-xp-sp2"></a>Firewall anterior a Windows XP SP2

El Firewall de conexiones a Internet (ICF) en Windows XP y Windows Server 2003 es un filtro de paquetes con estado y controla tanto protocolo de Internet, versión 4 (IPv4) como protocolo de Internet, versión 6 (IPv6). Sin embargo, no está en on de forma predeterminada y no admite pilas de red de terceros, de las que hay un número significativo en el mundo, como grandes proveedores de Internet, incluidas las compañías telefónicas nacionales.

Para aquellos que no están en Windows XP SP2, se recomienda encarecidamente activar el ICF. Vea las instrucciones "Usar un firewall de Internet" como https://www.microsoft.com/security/protect primer paso para proteger el equipo. El Firewall de conexión a Internet (ICF) proporciona la asignación de puertos para invalidar el filtro de paquetes. Básicamente, especifique el puerto que se va a abrir y permanecerá abierto hasta que lo cierre. Si el usuario se reinicia antes de cerrarse, permanecerá abierto hasta que se cierre específicamente. El control del firewall y la administración de las asignaciones de puertos se realiza a través de [**INetSharingManager**](/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingmanager) (IPv4) e [**INetFwV6Mgr**](/previous-versions/windows/desktop/ics/inetfwv6mgr) (IPv6).

Firewall de Windows para Windows XP SP2 es una solución más completa que admite pilas de red de terceros y controla los puertos de forma más inteligente: los puertos se mantienen abiertos solo mientras la aplicación que los necesite esté aún activa.

## <a name="windows-xp-sp2-firewall-is-better"></a>Firewall de Windows XP SP2 es mejor

Windows XP SP2 coloca las opciones de seguridad y la configuración por adelantado. El objetivo es proteger de forma predeterminada y permitir al usuario tomar decisiones informadas sobre qué aplicaciones se pueden ejecutar en su equipo.

El nuevo Firewall de Windows está disponible en Windows XP SP2 y Windows Server 2003 Service Pack 1 (SP1). Al igual que el ICF, es un firewall de software que admite IPv4 e IPv6, pero a diferencia de ICF firewall de Windows:

-   Tiene protección en tiempo de arranque del sistema, lo que elimina una pequeña ventana de vulnerabilidad durante el arranque.
-   Admite pilas de red de terceros.
-   Tiene un modo "on sin excepciones" que bloquea todos los paquetes entrantes no solicitados. Esto es excelente cuando se usa una red pública, como en un aeropuerto o una cafetería.

En el modo "on with no exceptions" (en sin excepciones), se cierran todos los huecos estáticos. Las llamadas API para abrir un hueco estático se permiten, pero se aplazan; Es decir, no se aplican hasta que el firewall vuelve al funcionamiento normal. También se omitirán todas las solicitudes de escucha de las aplicaciones. Las conexiones salientes seguirán siendo correctas.

Para las nuevas aplicaciones, agregue la aplicación a la "Lista de excepciones" durante la instalación. Puede agregar la aplicación mediante la [**interfaz INetFwAuthorizedApplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) y proporcionar la ruta de acceso completa. Vamos a cubrir los detalles del ejemplo.

Como nota adicional, es posible que se pregunte si es un riesgo de seguridad que las aplicaciones puedan agregar y quitar aplicaciones de la lista de excepciones de cualquier intervención del usuario, o quizás piense que el mayor riesgo es que las aplicaciones puedan deshabilitar el firewall por completo. Para realizar estas hazañas, la aplicación debe tener privilegios de administrador. Si tiene código malintencionado que se ejecuta en modo de administrador en el sistema, el juego ya ha terminado y el hacker ya ha ganado. La capacidad del hacker para deshabilitar el firewall sería poco más que una nota al pie.

Las aplicaciones heredadas, incluidas las instaladas antes de que el usuario actualizara a Windows XP SP2, se controlan con el menú emergente Lista de excepciones (consulte la figura 1). Este cuadro de diálogo muestra cuándo una aplicación intenta abrir un puerto para el tráfico entrante, ya sea al llamar a bind() con un puerto distinto de cero para UDP o accept() para el protocolo TCP/IP. Debe ejecutarse como administrador para "Desbloquear" aplicaciones, mientras que "Pregúnteme más tarde" no permite esta vez, pero vuelve a preguntar la próxima vez.

Se trata de un cuadro de diálogo modal del sistema sin bloqueo. Al ejecutar una aplicación de Microsoft Direct3D de pantalla completa, el cuadro de diálogo aparece debajo; y el usuario puede controlarlo cuando la aplicación salga del modo de pantalla completa o de las pestañas alt al escritorio. Sin embargo, no siempre es obvio para el usuario que este diálogo haya aparecido cuando se ejecuta un juego en pantalla completa, por lo que es importante evitar que este diálogo aparezca mediante la interfaz [**INetFwAuthorizedApplications,**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) como se describe a continuación.

**Figura 1. Cuadro de diálogo emergente Lista de excepciones**

![cuadro de diálogo emergente de lista de excepciones](images/firewalls1.jpg)

Observará que el elemento emergente conoce el nombre y el publicador de la aplicación. No hay ninguna magia aquí: se extrayó de la información de versión del archivo ejecutable. Esta información es una herramienta de administración del sistema importante; incluso se usa para el trabajo continuo de compatibilidad de aplicaciones. Algunas aplicaciones no mantienen actualizada esta información de versión.

Los usuarios también pueden agregar sus aplicaciones a través de la interfaz de usuario (IU) (consulte la figura 2)

**Figura 2. Configuración del firewall**

![configuración del firewall](images/firewalls2.jpg)

**Figura 3. Agregar un programa a la lista de excepciones de firewall**

![agregar un programa a la lista de excepciones de firewall](images/firewalls3.jpg)

El mejor escenario es automatizar las adiciones y eliminaciones de la lista de excepciones. El mejor momento para realizar estas adiciones y eliminaciones es durante el proceso de instalación y desinstalación. La adición o eliminación de la lista de excepciones de firewall requiere privilegios de administrador, por lo que debe tener esto en cuenta.

## <a name="working-with-the-windows-firewall"></a>Trabajar con firewall de Windows

De nuevo, la mayoría de los juegos solo deben agregarse a la lista de excepciones del firewall si pueden funcionar como un servidor o si implementan un protocolo de comunicación punto a punto. El FirewallInstallHelper.dll es un archivo DLL de ejemplo al que se puede llamar desde un instalador. El origen se proporciona si desea integrar el origen directamente en su propia aplicación. El ejemplo se puede encontrar aquí:



|             | Archivo                                                                             |
|-------------|------------------------------------------------------------------------------|
| **Origen:**     | (raíz del SDK) \\ Ejemplos \\ de firewall de C++ \\ \\ miscInstallHelper                        |
| **Ejecutable:** | (raíz del SDK) \\ Ejemplos \\ de errores de \\ C++ \\ \\ <arch> \\FirewallInstallHelper.dll |



 

Las funciones exportadas por este archivo DLL son las siguientes:

<dl> <dt>

<span id="AddApplicationToExceptionListW"></span><span id="addapplicationtoexceptionlistw"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTW"></span>**AddApplicationToExceptionListW**
</dt> <dd>

Esta función agrega una aplicación a la lista de excepciones. Toma una ruta de acceso completa al ejecutable y un nombre descriptivo que aparecerá en la lista de excepciones del firewall. Esta función requiere privilegios de administrador.

</dd> <dt>

<span id="AddApplicationToExceptionListA"></span><span id="addapplicationtoexceptionlista"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTA"></span>**AddApplicationToExceptionListA**
</dt> <dd>

Versión ANSI de **AddApplicationToExceptionListW**

</dd> <dt>

<span id="RemoveApplicationFromExceptionListW"></span><span id="removeapplicationfromexceptionlistw"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTW"></span>**RemoveApplicationFromExceptionListW**
</dt> <dd>

Esta función quita la aplicación de la lista de excepciones. Toma una ruta de acceso completa al ejecutable. Esta función requiere privilegios de administrador

</dd> <dt>

<span id="RemoveApplicationFromExceptionListA"></span><span id="removeapplicationfromexceptionlista"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTA"></span>**RemoveApplicationFromExceptionListA**
</dt> <dd>

Versión ANSI de **RemoveApplicationFromExceptionListW**

</dd> <dt>

<span id="CanLaunchMultiplayerGameW"></span><span id="canlaunchmultiplayergamew"></span><span id="CANLAUNCHMULTIPLAYERGAMEW"></span>**CanLaunchMultiplayerGameW**
</dt> <dd>

Esta función notifica si la aplicación se ha deshabilitado o quitado de la lista de excepciones. Debe llamarse cada vez que se ejecute el juego. La función toma una ruta de acceso completa al ejecutable. Esta función no requiere privilegios de administrador.

</dd> <dt>

<span id="CanLaunchMultiplayerGameA"></span><span id="canlaunchmultiplayergamea"></span><span id="CANLAUNCHMULTIPLAYERGAMEA"></span>**CanLaunchMultiplayerGameA**
</dt> <dd>

Versión ANSI de **CanLaunchMultiplayerGameW**

</dd> <dt>

<span id="SetMSIFirewallProperties"></span><span id="setmsifirewallproperties"></span><span id="SETMSIFIREWALLPROPERTIES"></span>**SetMSIFirewallProperties**
</dt> <dd>

Llame a esto solo si usa acciones personalizadas en Windows Installer. Consulte a continuación para más información.

</dd> <dt>

<span id="AddToExceptionListUsingMSI"></span><span id="addtoexceptionlistusingmsi"></span><span id="ADDTOEXCEPTIONLISTUSINGMSI"></span>**AddToExceptionListUsingMSI**
</dt> <dd>

Llame a esto solo si usa acciones personalizadas en Windows Installer. Consulte a continuación para más información.

</dd> <dt>

<span id="RemoveFromExceptionListUsingMSI"></span><span id="removefromexceptionlistusingmsi"></span><span id="REMOVEFROMEXCEPTIONLISTUSINGMSI"></span>**RemoveFromExceptionListUsingMSI**
</dt> <dd>

Llame a esto solo si usa acciones personalizadas en Windows Installer. Consulte a continuación para más información.

</dd> </dl>

En las secciones siguientes se describen métodos específicos para llamar a las funciones DLL exportadas desde este FirewallInstallHelper desde un paquete InstallShield, Wise o Windows Installer paquete. Todos los métodos representan los mismos resultados y es el desarrollador quien debe determinar qué método implementar.

## <a name="integrating-using-installshield-installscript"></a>Integración mediante InstallShield InstallScript

Un método alternativo para usar las API de firewall es agregar las llamadas de función a installShield InstallScript. Los pasos necesarios para la integración son bastante sencillos:

1.  Abra un proyecto de InstallScript en el editor de InstallShield.
2.  Agregue el FirewallInstallHelper.dll al proyecto como archivo de soporte técnico.

    1.  En la pestaña Asistente de proyectos, abra la pestaña Archivos de aplicación.
    2.  Haga clic en el botón Agregar archivos para agregar archivos a la carpeta de destino de la aplicación.
    3.  Vaya a la FirewallInstallHelper.dll que ha creado o use la proporcionada en el SDK de DirectX y agrécela al proyecto.

3.  Agregue InstallScript al proyecto.

    1.  Abra la vista Diseñador de instalación y haga clic en Behavior and Logic InstallScript (Comportamiento e instalación \| lógica)
    2.  Haga clic en el archivo InstallScript (normalmente setup.rul) para abrirlo en el editor.
    3.  Pegue el código siguiente en el archivo InstallScript:

    ``` syntax
    #include "ifx.h"

    prototype BOOL FirewallInstallHelper.AddApplicationToExceptionListW( WSTRING, WSTRING );
    prototype BOOL FirewallInstallHelper.RemoveApplicationFromExceptionListW( WSTRING );

    function OnMoved()
        WSTRING path[256];
    begin
        // The DLL has been installed into the TARGETDIR
        if !MAINTENANCE then // TRUE when installing
            UseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
            path = TARGETDIR ^ "TODO: change to relative path to executable from install directory";
            FirewallInstallHelper.AddApplicationToExceptionListW( path, "TODO: change to friendly app name" );
            UnUseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
        endif;
    end;
          

    function OnMoving()
        WSTRING path[256];
    begin
        // The DLL is about to be removed from TARGETDIR
        if MAINTENANCE && UNINST != "" then // TRUE when uninstalling
            UseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
            path = TARGETDIR ^ "TODO: change to relative path to executable from install directory";
            FirewallInstallHelper.RemoveApplicationFromExceptionListW( path );
            UnUseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
        endif;
    end;
    ```

    4.  Cambie los comentarios todo por el nombre de la aplicación que se mostrará en la lista de excepciones del firewall y la ruta de acceso al archivo ejecutable del juego en relación con el directorio de instalación.

## <a name="integrating-into-wise-for-windows-installer"></a>Integración en Wise for Windows Installer

Para integrar con Wise for Windows Installer, deben realizarse estos pasos:

1.  Abra el proyecto Wise for Windows Installer.
2.  Seleccione la pestaña "Installation Expert" (Experto en instalación) en la parte inferior.
3.  Haga clic en Archivos y agregue la FirewallInstallHelper.dll del DXSDK al directorio de instalación del juego.
4.  Seleccione la pestaña "Script MSI" en la parte inferior.
5.  Seleccione la pestaña "Ejecutar inmediato" cerca de la parte inferior.
6.  Después de CostFinalize, agregue una acción "Set Property" que establezca FULLPATH en \[ "InstallDIR relative path to executable from install directory" (Ruta de acceso relativa de INSTALLDIR al ejecutable \] desde el directorio de instalación). Por ejemplo, \[ "INSTALLDIR \]game.exe" sin comillas
7.  Seleccione la pestaña "Ejecutar aplazado" cerca de la parte inferior.
8.  Después de PublishProduct, agregue una instrucción "If" con la condición "NOT Installed" (distingue mayúsculas de minúsculas).
9.  Dentro del bloque If, agregue una acción "Llamar a un archivo DLL personalizado desde el destino".

    1.  Establezca el campo Archivo DLL en \[ "INSTALLDIR \]FirewallInstallHelper.dll".
    2.  Establezca el campo Nombre de función en "AddApplicationToExceptionListA".
    3.  Agregue un parámetro con el tipo "puntero de cadena", el origen de valor "Property" y el nombre de propiedad "FULLPATH".
    4.  Agregue un segundo parámetro con el tipo "puntero de cadena", el origen de valor "Constant" y establezca el valor constante en el nombre descriptivo de la aplicación que desea mostrar en la lista de excepciones del firewall.
    5.  Cierre el bloque If agregando una instrucción "End".

10. Justo encima de la acción RemoveFiles cerca de la parte superior, agregue otro bloque If, con la condición "REMOVE~="ALL"" (distingue mayúsculas de minúsculas y sin las comillas externas).
11. Dentro del segundo bloque If, agregue una acción "Llamar a un archivo DLL personalizado desde el destino".

    1.  Establezca el campo Archivo DLL en \[ "INSTALLDIR \]FirewallInstallHelper.dll".
    2.  Establezca el campo Nombre de función en "RemoveApplicationFromExceptionListA".
    3.  Agregue un parámetro con el tipo "puntero de cadena", el origen de valor "Property" y el nombre de propiedad "FULLPATH".
    4.  Cierre el segundo bloque If agregando una instrucción "End".

## <a name="integrating-into-windows-installer"></a>Integración en Windows Installer

Para integrar con Windows Installer en el nivel alto, estos pasos deben realizarse. Se explicarán con detalle a continuación:

-   Agregue 2 propiedades "FriendlyNameForFirewall" y "RelativePathToExeForFirewall" como se describe a continuación.
-   Después de la acción CostFinalize, llame a "SetMSIFirewallProperties" en una acción personalizada inmediata para establecer las propiedades MSI adecuadas para las demás acciones personalizadas.
-   Durante la instalación después de la acción InstallFiles, llame a una acción personalizada diferida que use la función "AddToExceptionListUsingMSI" de FirewallInstallHelper.
-   Durante la desinstalación después de la acción InstallFiles, llame a una acción personalizada diferida que use la función "RemoveFromExceptionListUsingMSI" de FirewallInstallHelper.
-   Durante la reversión, llame a una acción personalizada diferida que también llame a la función "RemoveFromExceptionListUsingMSI" del FirewallInstallHelper.

A continuación se indican los pasos necesarios para hacerlo mediante un editor msi como Orca que se encuentra en el SDK de plataforma. Tenga en cuenta que algunos editores tienen asistentes que simplifican algunos de estos pasos:

1.  Abra el paquete MSI en Orca.
2.  Agregue lo siguiente a la tabla Binaria:

    

    | Nombre     | Datos                                                                                                                                                                          |
    |----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Firewall | Apunte al FirewallInstallHelper.dll. Este archivo se incrustará en el paquete MSI, por lo que tendrá que realizar este paso cada vez que vuelva a compilar FirewallInstallHelper.dll. |

    

     

3.  Agregue lo siguiente a la tabla CustomAction:

    

    | Acción                   | Tipo                                                                                                                                                                                                   | Source   | Destino                          |
    |--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------|
    | FirewallSetMSIProperties | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                                                        | Firewall | SetMSIFirewallProperties        |
    | FirewallAgregue              | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | Firewall | AddToExceptionListUsingMSI      |
    | FirewallRemove           | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | Firewall | RemoveFromExceptionListUsingMSI |
    | FirewallRollBackAgrego      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | Firewall | RemoveFromExceptionListUsingMSI |
    | FirewallRollBackRemove   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | Firewall | AddToExceptionListUsingMSI      |

    

     

4.  Agregue lo siguiente a la tabla InstallExecuteSequence:

    

    | Acción                   | Condición     | Secuencia | Notas                                                                                                                                                                      |
    |--------------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | FirewallSetMSIProperties |               | 1010     | Esto se coloca poco después de CostFinalize.                                                                                                                                       |
    | FirewallAgregue              | NO instalado | 4021     | Esta acción personalizada solo se realizará durante una instalación nueva. El número de secuencia coloca la acción después de InstallFiles y después de las reversión.                              |
    | FirewallRollBackAgrego      | NO instalado | 4020     | Esta acción personalizada solo se realizará cuando se cancele una instalación nueva. El número de secuencia coloca la acción después de InstallFiles y antes de la acción Agregar personalizada.          |
    | FirewallRemove           | Instalado     | 3461     | Esta acción personalizada solo se realizará durante la desinstalación. El número de secuencia coloca la acción directamente antes de RemoveFiles y después de las reversión.                           |
    | FirewallRollBackRemove   | NO instalado | 3460     | Esta acción personalizada solo se realizará cuando se cancele una desinstalación. El número de secuencia coloca la acción directamente antes de RemoveFiles y antes de la acción personalizada Quitar. |

    

     

5.  Agregue lo siguiente a la tabla Property:

    

    | Propiedad                     | Valor                                                                             |
    |------------------------------|-----------------------------------------------------------------------------------|
    | FriendlyNameForFirewall      | Debe ser el nombre que mostrará la lista de excepciones. Por ejemplo, "Ejemplo de juego" |
    | RelativePathToExeForFirewall | Debe ser el ejecutable instalado del juego. Por ejemplo, "ExampleGame.exe"  |

    

     

Para obtener más información sobre Windows Installer, [vea Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="recommendations"></a>Recomendaciones

El firewall está aquí para permanecer. Estas recomendaciones darán a los clientes una buena experiencia de firewall con el juego de Windows:

-   No le diga a los usuarios que deshabilite el firewall para jugar. Esto hace que toda la máquina sea vulnerable incluso cuando no están reproduciendo el juego.
-   Haga que la configuración del firewall sea perfecta para los usuarios. Agregue la aplicación a la lista de excepciones durante la instalación y quite la aplicación de la lista de excepciones durante la instalación.
-   Enviar comentarios al usuario si el estado del firewall bloquea el modo multijugador. Por ejemplo, deshabilite las características de red si no funcionan porque la aplicación no está permitido o porque el sistema está en modo "sin excepciones".

 

 