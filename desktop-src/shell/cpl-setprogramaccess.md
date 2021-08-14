---
description: En este tema se describe la característica Set Program Access and Computer Defaults (SPAD) que se encuentra en Panel de control.
ms.assetid: 0d706857-5a84-4d68-99dc-bb9aab4197b9
title: Establecer el acceso al programa y los valores predeterminados del equipo (SPAD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 978749171366e3091738ac22c78e04cd92123a75d2288f7c83200ee8532d232c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861476"
---
# <a name="set-program-access-and-computer-defaults-spad"></a>Establecer el acceso al programa y los valores predeterminados del equipo (SPAD)

En este tema se describe la **característica Set Program Access and Computer Defaults (SPAD)** que se encuentra en Panel de control. SPAD se encuentra en el elemento [Panel de control](default-programs.md) programas predeterminados de Windows Vista y versiones posteriores de Windows. En Windows XP, se encuentra  en el elemento Agregar o quitar programas y se ha titulado Establecer el acceso al programa **y los valores predeterminados.**

> [!IMPORTANT]
> Este tema no se aplica a Windows 10. La forma en que funcionan las asociaciones de archivos predeterminadas ha cambiado en Windows 10. Para obtener más información, vea la sección Sobre los cambios en Windows 10 **controla las aplicaciones predeterminadas** en [esta entrada](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

-   [Usar la herramienta Establecer el acceso al programa y los valores predeterminados del equipo](#using-the-set-program-access-and-computer-defaults-tool)
    -   [Información general sobre cómo establecer el acceso al programa y los valores predeterminados del equipo](#an-overview-of-set-program-access-and-computer-defaults)
    -   [Valor del Registro LastUserInitiatedDefaultChange](#the-lastuserinitiateddefaultchange-registry-value)
-   [Filtrado de la lista Agregar o quitar programas](#filtering-the-add-or-remove-programs-list)
-   [Recursos adicionales](#filtering-the-add-or-remove-programs-list)
-   [Temas relacionados](#related-topics)

## <a name="using-the-set-program-access-and-computer-defaults-tool"></a>Usar la herramienta Establecer el acceso al programa y los valores predeterminados del equipo

> [!Note]  
> A partir Windows 8, SPAD configura los valores predeterminados por usuario para el usuario actual. Antes de Windows 8, SPAD establece los valores predeterminados por equipo. Cuando el usuario aún no haya configurado un valor predeterminado por usuario, el sistema le pedirá que establezca un valor predeterminado por usuario en lugar de volver a un valor predeterminado por equipo. Es posible que los usuarios de Windows Vista y Windows 7 nunca vean los valores predeterminados por equipo si previamente habían establecido valores predeterminados por usuario, ya que los valores predeterminados por usuario invalidan los valores predeterminados por equipo en esos sistemas operativos.

 

En Windows XP, **Establecer** acceso a programas y valores predeterminados es una herramienta que se encuentra como una opción en el elemento Agregar o quitar **programas** de Panel de control. En Windows Vista y versiones posteriores, se encuentra en el [elemento Panel de control](default-programs.md) programas predeterminados. En [el caso](reg-middleware-apps.md) de los programas registrados, realiza las siguientes funciones:

-   Habilita la elección de programas predeterminados para cada tipo de cliente (hasta Windows 7 solo).
-   Habilita el control de la presentación de los iconos, accesos directos y entradas de menú del programa.
-   Proporciona un conjunto de opciones de programa predeterminadas preestablecidas. (Windows XP Service Pack 1 (SP1) solamente)

Esta herramienta se usa para los cinco tipos de cliente siguientes.

-   Browser
-   Correo electrónico
-   Programa de creación instantánea
-   Reproductor multimedia
-   Máquina virtual para Java

### <a name="an-overview-of-set-program-access-and-computer-defaults"></a>Información general sobre cómo establecer el acceso al programa y los valores predeterminados del equipo

La Windows 8 **establecer el acceso al programa y los** valores predeterminados del equipo se muestra en la siguiente captura de pantalla.

![captura de pantalla del conjunto de acceso al programa y la vista de entrada predeterminada del equipo](images/spad-initial.png)

El usuario presenta tres opciones de configuración posibles, con la opción de que los OEM presenten una cuarta opción titulada "Fabricante del equipo".

-   [Microsoft Windows](#microsoft-windows)
-   [Programas que no son de Microsoft](#non-microsoft)
-   [Personalizada](#custom)
-   [Fabricante del equipo](#computer-manufacturer)

### <a name="microsoft-windows"></a>Microsoft Windows

La **configuración Windows** microsoft consta de un conjunto de programas predeterminados proporcionados con Windows, como se muestra en la siguiente captura de pantalla.

![captura de pantalla del acceso al programa establecido y las opciones predeterminadas de Microsoft](images/mspage.png)

Al seleccionar la configuración **Windows** microsoft también se permite mostrar los iconos, los accesos directos o las entradas de menú de cada programa registrado para cualquiera de los cinco tipos de cliente. Esos iconos, accesos directos y entradas de  menú están disponibles para el usuario en el menú Inicio o pantalla Inicio, en el escritorio y en todas las demás ubicaciones a las que se agregaron.

### <a name="non-microsoft"></a>Programas que no son de Microsoft

La configuración que no es de **Microsoft,** que se muestra en la siguiente captura de pantalla, se usa para las aplicaciones registradas en el sistema del usuario que no son producidas por Microsoft. Estas aplicaciones se pueden preinstalar en el sistema del usuario o pueden ser aplicaciones que no sean de Microsoft que el usuario haya instalado.

> [!Note]  
> Las aplicaciones deben registrarse para que aparezcan en esta página. Para obtener instrucciones sobre cómo registrar una aplicación, vea [Registrar programas con tipos de cliente.](reg-middleware-apps.md)

 

![captura de pantalla del acceso al programa establecido y las opciones predeterminadas que no son de Microsoft](images/nonmspage.png)

Al seleccionar la opción Que no es de **Microsoft** también se quita el acceso a los iconos, accesos directos y entradas de menú de los programas de Microsoft enumerados en la configuración de [Microsoft Windows](#microsoft-windows) para todos los tipos de cliente que los tienen. Estos iconos, accesos directos y entradas  de menú de Microsoft se quitan del menú Inicio, el escritorio y otras ubicaciones a las que se agregaron.

### <a name="custom"></a>Personalizado

La **configuración** personalizada, que se muestra en la siguiente captura de pantalla, permite a los usuarios personalizar sus sistemas con cualquier combinación de programas de Microsoft y que no son de Microsoft registrados como posibilidades predeterminadas para los cinco tipos de cliente. Esta es la única de las cuatro opciones disponibles en Windows 2000 Service Pack 3 (SP3).

![captura de pantalla del acceso al programa establecido y opciones personalizadas predeterminadas](images/custompage.png)

Todas las opciones que se presentan en las configuraciones microsoft [Windows](#microsoft-windows)  y no de [Microsoft](#non-microsoft) están disponibles para el usuario en la sección Personalizado, así como cualquier aplicación de Microsoft instalada adicionalmente que no forma parte de Windows. El **botón de radio** Usar mi explorador web actual está preseleccionado, como se muestra en la captura de pantalla anterior. No hay ninguna manera de determinar el explorador predeterminado actual desde la interfaz de usuario. Invocar vínculos web o archivos en Windows es la única manera de detectar el explorador predeterminado actual.

Cuando un usuario  activa la casilla Habilitar acceso a este programa para un programa, los iconos, accesos directos y entradas de menú de ese programa se muestran en menú Inicio o pantalla Inicio, en el escritorio o en cualquier otra ubicación donde se instalaron. Desactivar esta opción debe quitar esos iconos, accesos directos y entradas de menú; sin embargo, el comportamiento de estas opciones es totalmente del proveedor de la aplicación. Windows no controla cómo se habilita o quita el acceso en toda la interfaz de usuario. También es importante comprender que no es necesario que las aplicaciones se registren para establecer el acceso al programa y **los valores predeterminados del equipo.**

### <a name="computer-manufacturer"></a>Fabricante del equipo

Puede aparecer una cuarta categoría titulada "Fabricante del equipo" en la ventana de SPAD en algunos sistemas. Los fabricantes de equipos pueden optar por preconfigurar sus equipos con un conjunto personalizado de valores predeterminados, eligiendo entre las mismas selecciones disponibles en la [configuración](#custom) personalizada. (Para fines ilustrativos, se registra un conjunto ficticio de aplicaciones denominada LitWare para su uso con todos los tipos de cliente). Un usuario puede volver a la configuración predeterminada del fabricante  del equipo en cualquier momento si elige la opción Fabricante del equipo, como se muestra en la siguiente captura de pantalla Windows XP.

> [!Note]  
> Esta configuración no aparece en todos los sistemas. Para más información, consulte el Kit de preinstalación (OPK) de OEM.

 

![captura de pantalla de la configuración del acceso al programa y las opciones predeterminadas del fabricante del equipo](images/oempage.jpg)

### <a name="the-lastuserinitiateddefaultchange-registry-value"></a>Valor del Registro LastUserInitiatedDefaultChange

El valor LastUserInitiatedDefaultChange se ha agregado al Registro para ayudar a las aplicaciones a reconocer y respetar las opciones predeterminadas del usuario. El valor contiene datos REG BINARY en forma de una estructura FILETIME que contiene la fecha y hora (en hora universal coordinada (UTC)) de la última vez que el usuario cambió una opción predeterminada mediante la herramienta Establecer acceso al programa y Valores predeterminados \_ **del equipo.** [](/windows/win32/api/minwinbase/ns-minwinbase-filetime) Este valor se encuentra en la subclave siguiente.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         ClientTypeName
            LastUserInitiatedDefaultChange = FILETIME
```

En el escenario siguiente se usa este valor para una aplicación que supervisa las asociaciones de archivo.

1.  Una aplicación registra internamente la hora en que se estableció por última vez como el programa predeterminado para su tipo de cliente (ya sea en la instalación o en un momento posterior).
2.  La aplicación detecta que el programa predeterminado para su tipo de cliente se ha cambiado a un programa distinto de sí mismo o a la aplicación que representa (en el caso de los programas auxiliares en segundo plano). No se admite en Windows 8.
3.  La aplicación lee el valor de LastUserInitiatedDefaultChange (la marca de tiempo del último cambio predeterminado iniciado por el usuario) y lo compara con el valor de marca de tiempo que ha almacenado para su propia elección como valor predeterminado.
4.  Si LastUserInitiatedDefaultChange es posterior al valor almacenado de la aplicación, esa aplicación no debe realizar ninguna acción porque el usuario solicitó explícitamente el cambio a través de la herramienta Establecer acceso al programa y valores **predeterminados.**
5.  La aplicación ya no supervisa esa asociación de archivos hasta que se elige de nuevo como valor predeterminado. No se admite en Windows 8.

Al cumplir este esquema, se respetan los deseo del usuario y se mantiene su propiedad final de sus sistemas.

## <a name="filtering-the-add-or-remove-programs-list"></a>Filtrado de la lista Agregar o quitar programas

> [!Note]  
> Esta sección se aplica a Windows XP Service Pack 2 (SP2) y versiones posteriores y Windows Server 2003 y versiones posteriores.

 

En Windows XP y Windows Server 2003, el usuario puede filtrar  la lista de  aplicaciones que se muestran en la pestaña Cambiar o quitar programas en Agregar o quitar programas para excluir las entradas de las actualizaciones de la aplicación. En estas versiones de Windows, esto se logra mediante una casilla **Mostrar** actualizaciones en la parte superior de la ventana. La **opción Mostrar actualizaciones** no está seleccionada  de forma predeterminada, por lo que las actualizaciones no se muestran a menos que el usuario decida mostrarlas. Los cambios en el estado de la casilla persisten **cuando se cierra Agregar** o quitar programas; Si un usuario decide mostrar las actualizaciones, se seguirán mostrando hasta que el usuario desactive la casilla.

> [!Note]  
> La Windows XP SP2 propiamente dicha es una excepción al filtrado. Siempre se muestra independientemente del estado de la casilla.

 

En Windows Vista y versiones posteriores, las actualizaciones de aplicaciones se muestran en una página independiente de Panel de control dedicadas a las actualizaciones por sí solas. Esta página se muestra cuando el usuario hace clic en el **vínculo De la tarea Ver actualizaciones** instaladas. No hay ninguna opción seleccionable por el usuario para mostrar actualizaciones en la misma página que los programas instalados. A pesar del cambio en la interfaz de usuario, el mecanismo para registrarse como una actualización en un programa instalado sigue siendo el mismo que en versiones anteriores de Windows.

Las aplicaciones de Microsoft y que no son de Microsoft que usan Windows Installer no necesitan hacer nada más para que sus actualizaciones se reconozcan como actualizaciones. Las aplicaciones que no son de Microsoft que no usan Windows Installer deben declarar determinados valores en el Registro como parte de su instalación para que se reconozcan como una actualización de un programa existente.

En el ejemplo siguiente se muestran los valores del Registro que se deben declarar para que una instalación se reconozca como una actualización de un programa existente.

1.  La aplicación primaria debe agregar su información de desinstalación en una subclave bajo la subclave **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Uninstall.** Vea el [tema Instalación](/previous-versions/ms997548(v=msdn.10)) para obtener más información sobre el uso de la subclave **Uninstall.**
2.  Cada actualización de esa aplicación primaria también debe agregar su información como subclave de la subclave **Desinstalar.** Debe usar una convención de nomenclatura determinada de su elección, intentando evitar posibles conflictos con otros programas. Microsoft reserva las convenciones siguientes como nombres de subclave para su uso con Windows actualizaciones.
    -   IEUpdate
    -   OEUpdate
    -   "KB" seguido de seis dígitos, por ejemplo, "KB123456"
    -   "Q" seguido de seis dígitos, por ejemplo, "Q123456"
    -   Seis dígitos, por ejemplo , "123456"
3.  Además de la información de desinstalación estándar agregada para la aplicación primaria, las subclaves de cada actualización deben incluir además dos de las tres entradas siguientes. Sus valores son de tipo REG \_ SZ.
    -   **ParentKeyName**. Este valor es necesario. Este es el nombre de la subclave del elemento primario declarada en el paso 1. Esto asocia la actualización al programa.
    -   **ParentDisplayName**. Este valor es necesario. Si ninguna subclave coincide con la denominada en ParentKeyName, este valor se usa como un programa primario de marcador de posición que se mostrará en Agregar o **quitar programas.**
    -   **InstallDate**. Este valor es opcional. Debe usar el formulario `yyyymmdd` para especificar la fecha. Esta fecha se usa para la **información instalada en** que se muestra junto a la entrada de la actualización en la interfaz de usuario. Si no hay ninguna **entrada InstallDate** o si está presente pero no tiene ningún valor asignado, ocurre lo siguiente:
        -   Se muestran versiones de sistema operativo distintas de Windows Vista y Windows 7: no **se muestra** información instalada sobre .
        -   Windows Vista y versiones posteriores: se usa una fecha predeterminada. Esta es la fecha de "última modificación" de cualquiera de las entradas de la subclave de esa actualización. Este es normalmente el día en que se agregó la actualización al Registro. Sin embargo, dado que es una fecha de "última modificación", cualquier cambio posterior en cualquiera de las entradas de la subclave hace que el valor InstallDate cambie a la fecha de ese cambio.

En el ejemplo siguiente se muestran las entradas pertinentes del Registro para una actualización de la aplicación LitWare Suite.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Uninstall
                  LitWare
                     DisplayName = LitWare Deluxe
                     UninstallString = "C:\Program Files\LitWare\LitWare Deluxe\litware.exe" /uninstall
                  LitWare_Update123456
                     DisplayName = LitWare Deluxe Update 123456. Fixes printing problems.
                     UninstallString = "C:\Program Files\LitWare\LitWare Deluxe\Updates\123456.exe" /uninstall
                     ParentKeyName = LitWare
                     ParentDisplayName = LitWare Deluxe
                     InstallDate = 20050513
```

Las aplicaciones que no son de Microsoft que no suministran la información del Registro adecuada, como las actualizaciones producidas antes de que esta opción estaba disponible, se seguirán mostrando normalmente en la lista de programas instalados y no se filtran.

El filtrado de actualizaciones en versiones de sistema operativo distintas de Windows Vista y Windows 7 es normalmente una configuración controlada por el usuario y las aplicaciones deben respetarlas como tales. Sin embargo, en un entorno empresarial, los administradores pueden controlar si los usuarios tienen la opción de filtrar las actualizaciones a través del valor del Registro DontGroupPatches, como se muestra en el ejemplo siguiente.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               policies
                  Uninstall
                     DontGroupPatches = 0 or 1
```

Este valor es de tipo REG \_ DWORD y se interpreta de la manera siguiente.



| Valor dontGroupPatches             | Significado                                                                                                                                                                                                             |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                  | La **casilla Mostrar** actualizaciones se muestra al usuario. El filtrado depende de si el usuario ha activado esta casilla o no.                                                                                         |
| 1                                  | La **casilla Mostrar actualizaciones** se quita de la interfaz de usuario. Las actualizaciones no se filtran de la lista. Este valor básicamente se revierte al Windows XP SP1, antes de que se introdujese **la** funcionalidad Mostrar actualizaciones. |
| La entrada DontGroupPatches no está presente | Esto equivale a establecer el valor en 0.                                                                                                                                                                       |



 

DontGroupPatches no tiene ningún efecto en Windows Vista y Windows 7, donde la interfaz de usuario no contiene ninguna casilla y las actualizaciones registradas siempre se filtran.

> [!Note]  
> Solo los administradores establecen las directivas. Las aplicaciones no deben modificar este valor. Para obtener más información sobre cómo establecer un servidor basado en directiva de grupo, vea directiva de grupo [o](/previous-versions/windows/desktop/Policy/group-policy-start-page) Windows [Server directiva de grupo](/windows/deployment/deploy-whats-new).

 

## <a name="additional-resources"></a>Recursos adicionales

-   [Registro de programas con tipos de cliente](reg-middleware-apps.md)
-   [Instalación](/previous-versions/ms997548(v=msdn.10))
-   [Configuración de Agregar o quitar programas con Windows Instalador](../msi/configuring-add-remove-programs-with-windows-installer.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos recomendados para asociaciones de archivos](fa-best-practices.md)
</dt> <dt>

[Escenario de ejemplo de asociación de archivos](fa-sample-scenarios.md)
</dt> <dt>

[Directrices para administrar aplicaciones predeterminadas en Windows Vista y versiones posteriores](vista-managing-defaults.md)
</dt> <dt>

[Programas predeterminados](default-programs.md)
</dt> </dl>

 

 
