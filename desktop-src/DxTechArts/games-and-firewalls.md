---
title: Firewall de Windows para desarrolladores de juegos
description: En este artículo se describe el Firewall de Windows, por qué existe, lo que se consigue y cómo lo hace. Lo más importante es que se describe cómo configurar el juego para que funcione bien con el firewall.
ms.assetid: 2ee9f769-03dc-3661-5d5b-6a4ecd151fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88656fb3f622a847c15544646c333b807f3a0fb2
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104547446"
---
# <a name="windows-firewall-for-game-developers"></a>Firewall de Windows para desarrolladores de juegos

En este artículo se describe el Firewall de Windows, por qué existe, lo que se consigue y cómo lo hace. Lo más importante es que se describe cómo configurar el juego para que funcione bien con el firewall.

Contenido:

-   [¿Qué es un firewall?](#what-is-a-firewall)
-   [¿Cómo se puede saber si se ve afectado mi juego?](#how-can-i-tell-if-my-game-is-affected)
-   [El Firewall antes de Windows XP SP2](#the-firewall-before-windows-xp-sp2)
-   [El Firewall de Windows XP SP2 es mejor](#windows-xp-sp2-firewall-is-better)
-   [Trabajar con el Firewall de Windows](#working-with-the-windows-firewall)
-   [Integración con InstallScript de InstallShield](#integrating-using-installshield-installscript)
-   [Integración en el Windows Installer](#integrating-into-wise-for-windows-installer)
-   [Integrar en Windows Installer](#integrating-into-windows-installer)
-   [Recomendaciones](#recommendations)

## <a name="what-is-a-firewall"></a>¿Qué es un firewall?

El Firewall proporciona una barrera contra las intrusiones basadas en la red. Bloquea el tráfico entrante no solicitado y hace que el sistema sea invisible en Internet mediante el rechazo de las solicitudes del Protocolo de mensajes de control de Internet (ICMP). Esto significa que ping y tracert no funcionarán. El Firewall también busca y rechaza los paquetes no válidos.

Esta barrera evita ataques oportunistas. Los ataques se propagan al encontrar muchos sistemas con la misma vulnerabilidad. El Firewall puede frustrar muchos ataques mediante la introducción de un signo "no molestar" para aquellas características que no se usan actualmente. el ataque se pasa por alto y no Strike Home. La ventaja esencial del firewall de Windows es que las características y aplicaciones que no están en uso no pueden ser vías de ataque.

El usuario configura el sistema para identificar qué aplicaciones y características son necesarias y deben estar abiertas en la red. Esto sucede cuando se instala una aplicación o cuando intenta abrirse en la red.

## <a name="how-can-i-tell-if-my-game-is-affected"></a>¿Cómo se puede saber si se ve afectado mi juego?

Con la llegada de Windows XP SP2, el Firewall de Windows se ha implementado ampliamente. Todos los juegos multijugador de Windows están afectados en cierto grado. Aunque los clientes están normalmente en buen estado, los servidores, los hosts y los equipos del mismo nivel de punto a punto necesitan que el Firewall esté configurado para seguir funcionando. En concreto, se quita el tráfico entrante no solicitado. El Firewall intercepta los paquetes de filtrado del tráfico de red basándose en el contenido del paquete y en la actividad de red reciente. El Firewall utiliza el contenido y la actividad para decidir si desea reenviar o quitar un paquete. Una vez que el Firewall esté configurado correctamente, un juego podrá aceptar tráfico entrante no solicitado como antes.

¿Quién tiene tráfico entrante no solicitado?

-   Cliente/servidor: todos los participantes se conectan a un servidor central. El servidor central es el que tiene tráfico entrante no solicitado. Los clientes que se conectan al servidor solicitan tráfico de devolución, lo que se espera y se le permite pasar a través del firewall si se siguen las reglas para los clientes. El servidor central debe estar configurado para aceptar el tráfico no solicitado y permitir que el tráfico del cliente pase a través del firewall.
-   Multijugador masivo (MMP): todos los participantes están conectados a un centro de datos. Esto se remonta en una relación compleja entre cliente y servidor, ya que el centro de datos tiene el tráfico entrante no solicitado. Los participantes son clientes y, en general, no necesitan aceptar tráfico no solicitado.
-   Punto a punto, donde todos los participantes se conectan entre sí directamente: todos los participantes deben estar preparados para aceptar tráfico no solicitado de cualquier jugador nuevo que se una al grupo. En un sentido, cada participante debe funcionar como un host, por lo que todos deben configurarse como si fueran hosts.

Los clientes suelen estar en buen estado. Sus conexiones salientes del Protocolo de control de transmisión/Protocolo de Internet (TCP/IP) funcionarán correctamente, ya que los mensajes del Protocolo de datagramas de usuario (UDP) salientes junto con las respuestas oportunas a esos mensajes: el Firewall mantiene el puerto abierto durante 90 segundos después de cada mensaje saliente en previsión de una respuesta.

## <a name="the-firewall-before-windows-xp-sp2"></a>El Firewall antes de Windows XP SP2

El Firewall de conexión a Internet (ICF) de Windows XP y Windows Server 2003 es un filtro de paquetes con estado y controla el protocolo de Internet, la versión 4 (IPv4) y el protocolo de Internet, versión 6 (IPv6). Sin embargo, no está activada de forma predeterminada y no admite pilas de red de terceros, de las que hay un número importante en el mundo, como proveedores de Internet de gran tamaño, incluidas las compañías telefónicas nacionales.

Para aquellos que no estén en Windows XP SP2, se recomienda encarecidamente activar ICF. Consulte las instrucciones "uso de un firewall de Internet" en https://www.microsoft.com/security/protect el primer paso para proteger el equipo. El Firewall de conexión a Internet (ICF) proporciona la asignación de puertos para invalidar el filtro de paquetes. En esencia, se especifica el puerto que se va a abrir y permanece abierto hasta que se cierra. Si el usuario se reinicia antes de cerrarse, permanecerá abierto hasta que se cierre de forma específica. El control del firewall y la administración de las asignaciones de puertos se realiza a través de [**INetSharingManager**](/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingmanager) (IPv4) y [**INetFwV6Mgr**](/previous-versions/windows/desktop/ics/inetfwv6mgr) (IPv6).

El Firewall de Windows para Windows XP SP2 es una solución más completa que admite pilas de red de terceros y controla los puertos de forma más inteligente: los puertos solo se mantienen abiertos, siempre y cuando la aplicación que los necesite todavía esté activa.

## <a name="windows-xp-sp2-firewall-is-better"></a>El Firewall de Windows XP SP2 es mejor

Windows XP SP2 pone en primer plano las opciones de seguridad y la configuración. El objetivo es proteger de forma predeterminada y permitir al usuario tomar decisiones informadas sobre qué aplicaciones pueden ejecutarse en su equipo.

El nuevo Firewall de Windows está disponible en Windows XP SP2 y en el Service Pack 1 (SP1) de Windows Server 2003. Al igual que el ICF, es un firewall de software que admite tanto IPv4 como IPv6, pero a diferencia de ICF, el Firewall de Windows:

-   Tiene protección en tiempo de arranque del sistema, eliminando una pequeña ventana de vulnerabilidad durante el arranque.
-   Admite pilas de red de terceros.
-   Tiene un modo "activado sin excepciones" que bloquea todos los paquetes entrantes no solicitados. Esto es muy útil cuando se usa una red pública, como en un aeropuerto o cafetería.

En el modo "activado sin excepciones", todos los huecos estáticos están cerrados. Se permiten llamadas API para abrir un hueco estático, pero se aplazan; es decir, no se aplican hasta que el Firewall vuelve a la operación normal. También se omitirán todas las solicitudes de escucha de las aplicaciones. Las conexiones salientes seguirán siendo correctas.

En el caso de las nuevas aplicaciones, agregue la aplicación a la lista de excepciones durante la instalación. Puede Agregar la aplicación mediante la interfaz [**INetFwAuthorizedApplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) , proporcionando la ruta de acceso completa. Trataremos los detalles en el ejemplo.

Por lo tanto, es posible que se pregunte si se trata de un riesgo de seguridad que las aplicaciones puedan agregar y quitar aplicaciones de la lista de excepciones la intervención del usuario, o quizás piense que el riesgo mayor es que las aplicaciones pueden deshabilitar el Firewall por completo. Para realizar estas operaciones, la aplicación debe tener privilegios de administrador. Si tiene código malintencionado que se ejecuta en modo de administrador en el sistema, el juego ya está por encima y el pirata ya ha ganado. La capacidad del hacker de deshabilitar el Firewall merecería poco más que una nota al pie.

Las aplicaciones heredadas, incluidas las aplicaciones instaladas antes de que el usuario haya actualizado a Windows XP SP2, se controlan con el menú emergente de la lista de excepciones (consulte la figura 1). Este cuadro de diálogo muestra cuando una aplicación intenta abrir un puerto para el tráfico entrante, ya sea al llamar a BIND () con un puerto distinto de cero para UDP o aceptar () para el protocolo TCP/IP. Debe estar ejecutando como administrador para "desbloquear" las aplicaciones, mientras que "preguntar más tarde" no permite este tiempo, pero vuelve a preguntar la próxima vez.

Se trata de un cuadro de diálogo que no es de bloqueo y modal del sistema. Al ejecutar una aplicación de pantalla completa de Microsoft Direct3D, el cuadro de diálogo se incluye en el interior; y el usuario puede controlarlo cuando la aplicación salga del modo de pantalla completa o de las pestañas Alt en el escritorio. Sin embargo, no siempre es obvio para el usuario que este cuadro de diálogo aparece cuando un juego se ejecuta en pantalla completa, por lo que es importante evitar que este cuadro de diálogo aparezca mediante la interfaz [**INetFwAuthorizedApplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) que se describe a continuación.

**Figura 1. Cuadro de diálogo emergente de la lista de excepciones**

![cuadro de diálogo emergente de la lista de excepciones](images/firewalls1.jpg)

Observará que el elemento emergente conoce el nombre y el publicador de la aplicación. Aquí no hay ninguna magia, sino que se extrae de la información de versión del archivo ejecutable. Esta información es una herramienta de administración del sistema importante; se usa incluso para el trabajo de compatibilidad de aplicaciones en curso. Algunas aplicaciones no mantienen actualizada esta información de versión.

Los usuarios también pueden agregar sus aplicaciones a través de la interfaz de usuario (consulte la figura 2).

**Figura 2. Configuración del firewall**

![configuración del firewall](images/firewalls2.jpg)

**Figura 3. Agregar un programa a la lista de excepciones de Firewall**

![Agregar un programa a la lista de excepciones de Firewall](images/firewalls3.jpg)

El mejor de los escenarios es hacer las adiciones y eliminaciones de la lista de excepciones automatizadas. El mejor momento para realizar estas adiciones y eliminaciones es durante el proceso de instalación y desinstalación. La adición o eliminación de la lista de excepciones de Firewall requiere privilegios de administrador, por lo que debe tener esto en cuenta.

## <a name="working-with-the-windows-firewall"></a>Trabajar con el Firewall de Windows

De nuevo, la mayoría de los juegos solo tienen que agregarse a la lista de excepciones de Firewall si pueden funcionar como un servidor o si implementan un protocolo de comunicación punto a punto. El FirewallInstallHelper.dll es un archivo DLL de ejemplo al que se puede llamar desde un instalador. El origen se proporciona si desea integrar el origen directamente en su propia aplicación. El ejemplo se puede encontrar aquí:



|             |                                                                              |
|-------------|------------------------------------------------------------------------------|
| Origen:     | (Raíz del SDK) \\ Ejemplos de \\ C++ \\ varios \\ FirewallInstallHelper                        |
| Ejecutable: | (Raíz del SDK) \\ Ejemplos \\ de \\ \\ \\ <arch> \\FirewallInstallHelper.dll de C++ Misc |



 

Las funciones exportadas por este archivo DLL son las siguientes:

<dl> <dt>

<span id="AddApplicationToExceptionListW"></span><span id="addapplicationtoexceptionlistw"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTW"></span>**AddApplicationToExceptionListW**
</dt> <dd>

Esta función agrega una aplicación a la lista de excepciones. Toma una ruta de acceso completa al archivo ejecutable y un nombre descriptivo que aparecerá en la lista de excepciones de Firewall. Esta función requiere privilegios de administrador.

</dd> <dt>

<span id="AddApplicationToExceptionListA"></span><span id="addapplicationtoexceptionlista"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTA"></span>**AddApplicationToExceptionListA**
</dt> <dd>

Versión ANSI de **AddApplicationToExceptionListW**

</dd> <dt>

<span id="RemoveApplicationFromExceptionListW"></span><span id="removeapplicationfromexceptionlistw"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTW"></span>**RemoveApplicationFromExceptionListW**
</dt> <dd>

Esta función quita la aplicación de la lista de excepciones. Toma una ruta de acceso completa al archivo ejecutable. Esta función requiere privilegios de administrador

</dd> <dt>

<span id="RemoveApplicationFromExceptionListA"></span><span id="removeapplicationfromexceptionlista"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTA"></span>**RemoveApplicationFromExceptionListA**
</dt> <dd>

Versión ANSI de **RemoveApplicationFromExceptionListW**

</dd> <dt>

<span id="CanLaunchMultiplayerGameW"></span><span id="canlaunchmultiplayergamew"></span><span id="CANLAUNCHMULTIPLAYERGAMEW"></span>**CanLaunchMultiplayerGameW**
</dt> <dd>

Esta función notifica si la aplicación se ha deshabilitado o quitado de la lista de excepciones. Se debe llamar a este método cada vez que se ejecute el juego. La función toma una ruta de acceso completa al archivo ejecutable. Esta función no requiere privilegios de administrador.

</dd> <dt>

<span id="CanLaunchMultiplayerGameA"></span><span id="canlaunchmultiplayergamea"></span><span id="CANLAUNCHMULTIPLAYERGAMEA"></span>**CanLaunchMultiplayerGameA**
</dt> <dd>

Versión ANSI de **CanLaunchMultiplayerGameW**

</dd> <dt>

<span id="SetMSIFirewallProperties"></span><span id="setmsifirewallproperties"></span><span id="SETMSIFIREWALLPROPERTIES"></span>**SetMSIFirewallProperties**
</dt> <dd>

Llame a este método solo si está utilizando acciones personalizadas en Windows Installer. Consulte a continuación para más información.

</dd> <dt>

<span id="AddToExceptionListUsingMSI"></span><span id="addtoexceptionlistusingmsi"></span><span id="ADDTOEXCEPTIONLISTUSINGMSI"></span>**AddToExceptionListUsingMSI**
</dt> <dd>

Llame a este método solo si está utilizando acciones personalizadas en Windows Installer. Consulte a continuación para más información.

</dd> <dt>

<span id="RemoveFromExceptionListUsingMSI"></span><span id="removefromexceptionlistusingmsi"></span><span id="REMOVEFROMEXCEPTIONLISTUSINGMSI"></span>**RemoveFromExceptionListUsingMSI**
</dt> <dd>

Llame a este método solo si está utilizando acciones personalizadas en Windows Installer. Consulte a continuación para más información.

</dd> </dl>

En las secciones siguientes se describen los métodos específicos para llamar a las funciones DLL exportadas desde este FirewallInstallHelper desde un paquete InstallShield, Wise o Windows Installer. Todos los métodos representan los mismos resultados y depende del desarrollador determinar el método que se va a implementar.

## <a name="integrating-using-installshield-installscript"></a>Integración con InstallScript de InstallShield

Un método alternativo de usar las API de Firewall es agregar las llamadas de función a un InstallScript de InstallShield. Los pasos necesarios para integrar son bastante sencillos:

1.  Abra un proyecto de InstallScript en el editor de InstallShield.
2.  Agregue el FirewallInstallHelper.dll al proyecto como archivo de compatibilidad.

    1.  En la pestaña Asistente para proyectos, abra la pestaña archivos de aplicación.
    2.  Haga clic en el botón Agregar archivos para agregar archivos a la carpeta de destino de la aplicación.
    3.  Busque el FirewallInstallHelper.dll que ha creado o utilice el que se proporciona en el SDK de DirectX y agréguelo al proyecto.

3.  Agregue InstallScript al proyecto.

    1.  Abra la vista del diseñador de instalación y haga clic en el comportamiento y la lógica \| InstallScript
    2.  Haga clic en el archivo InstallScript (normalmente Setup. RUL) para abrirlo en el editor
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

    4.  Cambie los comentarios TODO con el nombre de la aplicación que se mostrará en la lista de excepciones de firewall y la ruta de acceso al archivo ejecutable del juego en relación con el directorio de instalación.

## <a name="integrating-into-wise-for-windows-installer"></a>Integración en el Windows Installer

Para realizar la integración con la Windows Installer, se deben seguir estos pasos:

1.  Abra el proyecto de Windows Installer.
2.  Seleccione la pestaña "experto en la instalación" en la parte inferior.
3.  Haga clic en archivos y agregue el FirewallInstallHelper.dll desde DXSDK al directorio de instalación del juego.
4.  Seleccione la pestaña "script MSI" en la parte inferior.
5.  Seleccione la pestaña "ejecutar inmediato" cerca de la parte inferior.
6.  Después de CostFinalize, agregue una acción de "establecer propiedad" que establezca FULLPATH en " \[ INSTALLDIR \] ruta de acceso relativa al archivo ejecutable desde el directorio de instalación". Por ejemplo, " \[ INSTALLDIR \]game.exe" sin las comillas
7.  Seleccione la pestaña "Execute diferido" cerca de la parte inferior.
8.  Después de PublishProduct, agregue una instrucción "if" con la condición "no instalada" (distingue mayúsculas de minúsculas).
9.  En el bloque if, agregue una acción "llamar a DLL personalizada desde el destino".

    1.  Establezca el campo archivo DLL en " \[ INSTALLDIR \]FirewallInstallHelper.dll."
    2.  Establezca el campo Nombre de función en "AddApplicationToExceptionListA".
    3.  Agregue un parámetro con el tipo "String Pointer", el origen del valor "Property" y el nombre de propiedad "FULLPATH".
    4.  Agregue un segundo parámetro con el tipo "String Pointer", el origen del valor "Constant" y establezca el valor constante en el nombre descriptivo de la aplicación que desea que se muestre en la lista de excepciones de Firewall.
    5.  Cierre el bloque if agregando una instrucción "End Statement".

10. Justo encima de la acción RemoveFiles cerca de la parte superior, agregue otro bloque if, con la condición de "REMOVE ~ =" ALL "" (distingue mayúsculas de minúsculas y sin las comillas externas).
11. En el segundo bloque if, agregue una acción "llamar a DLL personalizada desde el destino".

    1.  Establezca el campo archivo DLL en " \[ INSTALLDIR \]FirewallInstallHelper.dll."
    2.  Establezca el campo Nombre de función en "RemoveApplicationFromExceptionListA".
    3.  Agregue un parámetro con el tipo "String Pointer", el origen del valor "Property" y el nombre de propiedad "FULLPATH".
    4.  Cierre el segundo bloque if agregando una instrucción "End Statement".

## <a name="integrating-into-windows-installer"></a>Integrar en Windows Installer

Para integrar con Windows Installer en el nivel alto, estos pasos deben realizarse. Se explicarán con más detalle a continuación:

-   Agregue 2 propiedades "FriendlyNameForFirewall" y "RelativePathToExeForFirewall" como se describe a continuación.
-   Después de la acción CostFinalize, llame a "SetMSIFirewallProperties" en una acción personalizada inmediata para establecer las propiedades MSI adecuadas para las demás acciones personalizadas.
-   Durante la instalación después de la acción InstallFiles, llame a una acción personalizada diferida que use la función "AddToExceptionListUsingMSI" de FirewallInstallHelper.
-   Durante la desinstalación después de la acción InstallFiles, llame a una acción personalizada diferida que use la función "RemoveFromExceptionListUsingMSI" de FirewallInstallHelper.
-   Durante la reversión, llame a una acción personalizada diferida que también llame a la función "RemoveFromExceptionListUsingMSI" de FirewallInstallHelper.

A continuación se indican los pasos necesarios para realizar esta tarea mediante un editor MSI como orca que se encuentra en el SDK de la plataforma. Tenga en cuenta que algunos editores tienen asistentes que simplifican algunos de estos pasos:

1.  Abra el paquete MSI en orca.
2.  Agregue lo siguiente a la tabla binaria:

    

    | Nombre     | Datos                                                                                                                                                                          |
    |----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | FIREWALL | Señale a la FirewallInstallHelper.dll. Este archivo se incrustará en el paquete MSI, por lo que tendrá que realizar este paso cada vez que vuelva a compilar FirewallInstallHelper.dll. |

    

     

3.  Agregue lo siguiente a la tabla CustomAction:

    

    | Acción                   | Tipo                                                                                                                                                                                                   | Source   | Destino                          |
    |--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------|
    | FirewallSetMSIProperties | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                                                        | FIREWALL | SetMSIFirewallProperties        |
    | FirewallAdd              | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | FIREWALL | AddToExceptionListUsingMSI      |
    | FirewallRemove           | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | FIREWALL | RemoveFromExceptionListUsingMSI |
    | FirewallRollBackAdd      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | FIREWALL | RemoveFromExceptionListUsingMSI |
    | FirewallRollBackRemove   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | FIREWALL | AddToExceptionListUsingMSI      |

    

     

4.  Agregue lo siguiente a la tabla InstallExecuteSequence:

    

    | Acción                   | Condición     | Secuencia | Notas                                                                                                                                                                      |
    |--------------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | FirewallSetMSIProperties |               | 1010     | Esto se coloca poco después de CostFinalize.                                                                                                                                       |
    | FirewallAdd              | NO instalado | 4021     | Esta acción personalizada solo se producirá durante una instalación nueva. El número de secuencia coloca la acción después de InstallFiles y después de la reversión.                              |
    | FirewallRollBackAdd      | NO instalado | 4020     | Esta acción personalizada solo se producirá cuando se cancele una instalación nueva. El número de secuencia coloca la acción después de InstallFiles y antes de agregar la acción personalizada.          |
    | FirewallRemove           | Instalado     | 3461     | Esta acción personalizada solo se producirá durante la desinstalación. El número de secuencia coloca la acción directamente antes de RemoveFiles y después de la reversión.                           |
    | FirewallRollBackRemove   | NO instalado | 3460     | Esta acción personalizada solo se producirá cuando se cancele una desinstalación. El número de secuencia coloca la acción directamente antes de RemoveFiles y antes de la acción personalizada quitar. |

    

     

5.  Agregue lo siguiente a la tabla de propiedades:

    

    | Propiedad                     | Value                                                                             |
    |------------------------------|-----------------------------------------------------------------------------------|
    | FriendlyNameForFirewall      | Debe ser el nombre que se mostrará en la lista de excepciones. Por ejemplo, "juego de ejemplo" |
    | RelativePathToExeForFirewall | Debe ser el ejecutable instalado del juego. Por ejemplo, "ExampleGame.exe"  |

    

     

Para obtener más información sobre Windows Installer, vea [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="recommendations"></a>Recomendaciones

El Firewall está aquí para quedarse. Estas recomendaciones proporcionarán a sus clientes una buena experiencia de firewall con su juego de Windows:

-   No indique a los usuarios que deshabiliten el firewall para jugar. Esto hace que todo el equipo sea vulnerable incluso cuando no juega el juego.
-   Haga que la configuración del firewall sea perfecta para los usuarios. Agregue la aplicación a la lista de excepciones durante la instalación y quite la aplicación de la lista de excepciones durante la instalación.
-   Enviar comentarios al usuario si el estado del Firewall bloquea el multijugador. Por ejemplo, deshabilite las características de red si no funcionarán porque la aplicación no está permitida o porque el sistema está en el modo "no excepciones".

 

 