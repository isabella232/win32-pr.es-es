---
description: En este tema se describe la característica configurar el acceso y los valores predeterminados del equipo (SPAD) del panel de control.
ms.assetid: 0d706857-5a84-4d68-99dc-bb9aab4197b9
title: Establecer los valores predeterminados de acceso a programas y del equipo (SPAD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f35d9ed70d382e2db6714082ade2d2d76e6ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275240"
---
# <a name="set-program-access-and-computer-defaults-spad"></a>Establecer los valores predeterminados de acceso a programas y del equipo (SPAD)

En este tema se describe la característica **configurar el acceso y los valores predeterminados del equipo (SPAD)** del panel de control. SPAD se encuentra en el elemento [programas predeterminados](default-programs.md) del panel de control en Windows Vista y versiones posteriores de Windows. En Windows XP, se encuentra en el elemento **Agregar o quitar programas** y titulado **establecer acceso y programas predeterminados**.

> [!IMPORTANT]
> Este tema no se aplica a Windows 10. La forma en que las asociaciones de archivos predeterminadas funcionan en Windows 10. Para obtener más información, consulte la sección **cambios en la forma en que Windows 10 trata las aplicaciones predeterminadas** en [esta publicación](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

-   [Usar la herramienta configurar acceso y programas predeterminados del equipo](#using-the-set-program-access-and-computer-defaults-tool)
    -   [Información general sobre cómo establecer el acceso a programas y los valores predeterminados del equipo](#an-overview-of-set-program-access-and-computer-defaults)
    -   [El valor del registro LastUserInitiatedDefaultChange](#the-lastuserinitiateddefaultchange-registry-value)
-   [Filtrar la lista Agregar o quitar programas](#filtering-the-add-or-remove-programs-list)
-   [Recursos adicionales](#filtering-the-add-or-remove-programs-list)
-   [Temas relacionados](#related-topics)

## <a name="using-the-set-program-access-and-computer-defaults-tool"></a>Usar la herramienta configurar acceso y programas predeterminados del equipo

> [!Note]  
> A partir de Windows 8, SPAD configura los valores predeterminados por usuario para el usuario actual. Antes de Windows 8, SPAD estableció valores predeterminados por equipo. Cuando el usuario todavía no ha configurado un valor predeterminado por usuario, el sistema le pedirá que establezca un valor predeterminado por usuario en lugar de revertirlo en un valor predeterminado por equipo. Es posible que los usuarios de Windows Vista y Windows 7 nunca hayan encontrado los valores predeterminados por máquina, si habían establecido previamente valores predeterminados por usuario, ya que los valores predeterminados por usuario invalidan los valores predeterminados por equipo en esos sistemas operativos.

 

En Windows XP, **configurar el acceso y los valores predeterminados de programas** es una herramienta que se encuentra como una opción en el elemento **Agregar o quitar programas** del panel de control. En Windows Vista y versiones posteriores, se encuentra en el elemento [programas predeterminados](default-programs.md) del panel de control. En el caso de los programas [registrados](reg-middleware-apps.md) , realiza las siguientes funciones:

-   Habilita la elección de programas predeterminados para cada tipo de cliente (solo hasta Windows 7).
-   Habilita el control de la presentación de los iconos, accesos directos y entradas de menú del programa.
-   Proporciona un conjunto de opciones preestablecidas de programas predeterminados. (Solo Windows XP Service Pack 1 (SP1))

Esta herramienta se usa para los cinco tipos de cliente siguientes.

-   Browser
-   Correo electrónico
-   Programa messenging instantáneo
-   Reproductor multimedia
-   Máquina virtual para Java

### <a name="an-overview-of-set-program-access-and-computer-defaults"></a>Información general sobre cómo establecer el acceso a programas y los valores predeterminados del equipo

La página **Configurar acceso y valores predeterminados del equipo** de Windows 8 se muestra en la siguiente captura de pantalla.

![captura de pantalla de la vista de entrada configurar acceso y valores predeterminados del equipo](images/spad-initial.png)

Se presentan tres opciones de configuración posibles al usuario, con la opción para que los OEM presenten una cuarta opción titulada "fabricante del equipo".

-   [Microsoft Windows](#microsoft-windows)
-   [Programas que no son de Microsoft](#non-microsoft)
-   [Personalizada](#custom)
-   [Fabricante del equipo](#computer-manufacturer)

### <a name="microsoft-windows"></a>Microsoft Windows

La configuración de **Microsoft Windows** se compone de un conjunto de programas predeterminados que se proporcionan con Windows, tal como se muestra en la siguiente captura de pantalla.

![captura de pantalla de las opciones establecer acceso de programa y valores predeterminados de Microsoft](images/mspage.png)

La selección de la configuración de **Microsoft Windows** también habilita la visualización de iconos, accesos directos o entradas de menú para cada programa registrado para cualquiera de los cinco tipos de cliente. Estos iconos, accesos directos y entradas de menú están disponibles para el usuario en el menú **Inicio** o en la pantalla Inicio, en el escritorio y en todas las demás ubicaciones a las que se agregaron.

### <a name="non-microsoft"></a>Programas que no son de Microsoft

La configuración **que no es de Microsoft** , que se muestra en la siguiente captura de pantalla, se utiliza para las aplicaciones registradas en el sistema del usuario que no produce Microsoft. Estas aplicaciones se pueden preinstalar en el sistema del usuario o pueden ser aplicaciones que no sean de Microsoft y que el usuario tenga instalado.

> [!Note]  
> Las aplicaciones deben registrarse para que aparezcan en esta página. Para obtener instrucciones sobre cómo registrar una aplicación, consulte [registrar programas con tipos de cliente](reg-middleware-apps.md).

 

![captura de pantalla de las opciones establecer acceso de programa y valores predeterminados que no son de Microsoft](images/nonmspage.png)

La selección de la opción **no Microsoft** también quita el acceso a los iconos, accesos directos y entradas de menú de los programas de Microsoft enumerados en la configuración de [Microsoft Windows](#microsoft-windows) para todos los tipos de cliente que los tienen. Estos iconos, accesos directos y entradas de menú de Microsoft se quitan del menú **Inicio** , el escritorio y otras ubicaciones a las que se agregaron.

### <a name="custom"></a>Personalizados

La configuración **personalizada** , que se muestra en la siguiente captura de pantalla, permite a los usuarios personalizar sus sistemas con cualquier combinación de programas de Microsoft y que no sean de Microsoft registrados como posibilidades predeterminadas para los cinco tipos de cliente. Esta es la única de las cuatro opciones disponibles en Windows 2000 Service Pack 3 (SP3).

![captura de pantalla de las opciones personalizadas de establecer acceso y valores predeterminados del programa](images/custompage.png)

Todas las opciones que se presentan en las configuraciones de [Microsoft Windows](#microsoft-windows) y [que no son de Microsoft](#non-microsoft) están disponibles para el usuario en la sección **personalizada** , así como las aplicaciones de Microsoft instaladas de forma adicional que no forman parte de Windows. El botón de radio **usar el explorador Web actual** está preseleccionado, como se muestra en la captura de pantalla anterior. No hay ninguna manera de determinar el explorador predeterminado actual desde la interfaz de usuario. Invocar vínculos Web o archivos en Windows es la única manera de detectar el explorador predeterminado actual.

Cuando un usuario selecciona la casilla **Habilitar el acceso a este programa** para un programa, los iconos, accesos directos y entradas de menú de ese programa se muestran en el menú Inicio o en la pantalla Inicio, en el escritorio o en cualquier otra ubicación donde se instalaron. Si se desactiva esta opción, se deben quitar los iconos, accesos directos y entradas de menú; sin embargo, el comportamiento de estas opciones es totalmente el proveedor de la aplicación. Windows no controla cómo se habilita o se quita el acceso a través de la interfaz de usuario. También es importante entender que no es necesario que las aplicaciones se registren para **establecer el acceso a programas y los valores predeterminados del equipo**.

### <a name="computer-manufacturer"></a>Fabricante del equipo

Una cuarta categoría titulada "Computer manufacturer" puede aparecer en la ventana de SPAD en algunos sistemas. Los fabricantes de equipos pueden optar por preconfigurar sus equipos con un conjunto personalizado de valores predeterminados y elegir entre las mismas selecciones disponibles en la configuración [personalizada](#custom) . (A efectos ilustrativos, un conjunto ficticio de aplicaciones denominado LitWare se registra para su uso con todos los tipos de cliente). Un usuario puede volver a la configuración predeterminada del fabricante del equipo en cualquier momento; para ello, elija la opción **fabricante del equipo** , tal como se muestra en la siguiente captura de pantalla de Windows XP.

> [!Note]  
> Esta configuración no aparece en todos los sistemas. Para obtener más información, consulte el kit de preinstalación OEM (OPK).

 

![captura de pantalla de las opciones establecer acceso de programa y fabricante de equipos predeterminados](images/oempage.jpg)

### <a name="the-lastuserinitiateddefaultchange-registry-value"></a>El valor del registro LastUserInitiatedDefaultChange

El valor LastUserInitiatedDefaultChange se ha agregado al registro para ayudar a las aplicaciones a reconocer y respetar las opciones predeterminadas del usuario. El valor contiene \_ datos binarios de registro en forma de una estructura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que contiene la fecha y hora (en hora universal coordinada (UTC)) de la última vez que el usuario cambió una opción predeterminada mediante la herramienta **establecer los valores predeterminados de acceso a programas y del equipo** . Este valor se encuentra en la subclave siguiente.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         ClientTypeName
            LastUserInitiatedDefaultChange = FILETIME
```

En el escenario siguiente se usa este valor para una aplicación que supervisa las asociaciones de archivo.

1.  Una aplicación registra internamente la hora en que se estableció por última vez como programa predeterminado para su tipo de cliente (ya sea en la instalación o en un momento posterior).
2.  La aplicación detecta que el programa predeterminado para su tipo de cliente se ha cambiado a un programa distinto de sí mismo o a la aplicación que representa (en el caso de los programas auxiliares en segundo plano). No se admite en Windows 8.
3.  La aplicación lee el valor de LastUserInitiatedDefaultChange (la marca de tiempo del último cambio predeterminado Iniciado por el usuario) y lo compara con el valor de marca de tiempo que ha almacenado para su propia opción como valor predeterminado.
4.  Si LastUserInitiatedDefaultChange es posterior al valor almacenado de la aplicación, la aplicación no debe realizar ninguna acción porque el usuario solicitó explícitamente el cambio a través de la herramienta **establecer acceso y valores predeterminados del programa** .
5.  La aplicación ya no supervisa la Asociación de archivos hasta que se elige de nuevo como valor predeterminado. No se admite en Windows 8.

Al adherirse a este tipo de esquema, se respetan los deseos del usuario y se mantiene la propiedad definitiva de sus sistemas.

## <a name="filtering-the-add-or-remove-programs-list"></a>Filtrar la lista Agregar o quitar programas

> [!Note]  
> Esta sección se aplica a Windows XP Service Pack 2 (SP2) y versiones posteriores, y a Windows Server 2003 y versiones posteriores.

 

En Windows XP y Windows Server 2003, la lista de aplicaciones mostradas en la pestaña **cambiar o quitar programas** de **Agregar o quitar programas** se puede filtrar por el usuario para excluir las entradas de las actualizaciones de la aplicación. En estas versiones de Windows, esto se logra mediante una casilla **Mostrar actualizaciones** en la parte superior de la ventana. La opción **Mostrar actualizaciones** no está seleccionada de forma predeterminada, por lo que *no* se muestran las actualizaciones a menos que el usuario elija mostrarlas. Los cambios en el estado de la casilla se conservan al cerrar **Agregar o quitar programas** ; Si un usuario elige mostrar las actualizaciones, se siguen mostrando hasta que el usuario desactive la casilla.

> [!Note]  
> La propia actualización de Windows XP SP2 es una excepción al filtrado. Siempre se muestra independientemente del estado de la casilla.

 

En Windows Vista y versiones posteriores, las actualizaciones de la aplicación se muestran en una página independiente en el panel de control dedicado solo a las actualizaciones. Esta página se muestra cuando el usuario hace clic en el vínculo de la tarea **ver actualizaciones instaladas** . No hay ninguna opción seleccionable por el usuario para mostrar las actualizaciones en la misma página que los programas instalados. A pesar del cambio en la interfaz de usuario, el mecanismo para registrarse como una actualización de un programa instalado sigue siendo el mismo que en versiones anteriores de Windows.

Las aplicaciones de Microsoft y que no son de Microsoft que usan el Windows Installer no necesitan hacer nada más para que las actualizaciones se reconozcan como actualizaciones. Las aplicaciones que no son de Microsoft que no usan Windows Installer deben declarar ciertos valores en el registro como parte de la instalación para que se reconozcan como una actualización de un programa existente.

En el ejemplo siguiente se muestran los valores del registro que se van a declarar para que una instalación se reconozca como una actualización de un programa existente.

1.  La aplicación primaria debe agregar su información de desinstalación en una subclave de la subclave **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Uninstall** . Vea el tema de [instalación](/previous-versions/ms997548(v=msdn.10)) para obtener más información sobre el uso de la subclave **Uninstall** .
2.  Cada actualización de la aplicación primaria también debe agregar su información como subclave de la subclave **Uninstall** . Debe utilizar una Convención de nomenclatura determinada de su elección, intentando evitar posibles conflictos con otros programas. Las siguientes convenciones están reservadas como nombres de subclaves de Microsoft para su uso con actualizaciones de Windows.
    -   IEUpdate
    -   OEUpdate
    -   "KB" seguido de seis dígitos, por ejemplo "KB123456"
    -   "Q" seguido de seis dígitos, por ejemplo "Q123456"
    -   Seis dígitos, por ejemplo "123456"
3.  Además de la información de desinstalación estándar agregada para la aplicación primaria, las subclaves de cada actualización deben incluir además dos de las tres entradas siguientes. Sus valores son de tipo REG \_ SZ.
    -   **ParentKeyName**. Este valor es necesario. Es el nombre de la subclave del elemento primario declarado en el paso 1. Esto asocia la actualización con el programa.
    -   **ParentDisplayName**. Este valor es necesario. Si ninguna subclave coincide con la denominada en ParentKeyName, este valor se utiliza como un programa primario de marcador de posición que se mostrará en **Agregar o quitar programas**.
    -   **InstallDate**. Este valor es opcional. Debe usar el formulario `yyyymmdd` para especificar la fecha. Esta fecha se usa para la información **instalada en** que se muestra junto a la entrada de la actualización en la interfaz de usuario. Si no hay ninguna entrada **InstallDate** o está presente pero no tiene ningún valor asignado, ocurre lo siguiente:
        -   Versiones de sistema operativo distintas de Windows Vista y Windows 7: no se ha **instalado** ninguna información.
        -   Windows Vista y versiones posteriores: se utiliza una fecha predeterminada. Esta es la fecha de "última modificación" para cualquiera de las entradas de la subclave de la actualización. Suele ser el día en que se agregó la actualización al registro. Sin embargo, dado que se trata de una fecha de "última modificación", cualquier cambio subsiguiente en cualquiera de las entradas de la subclave hace que el valor de InstallDate se cambie a la fecha de ese cambio.

En el ejemplo siguiente se muestran las entradas del registro pertinentes para una actualización de la aplicación LitWare Deluxe.

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

Las aplicaciones que no son de Microsoft y que no proporcionan la información de registro adecuada, como las actualizaciones generadas antes de que esta opción estuvieran disponibles, se siguen mostrando normalmente en la lista de programas instalados y no se filtran.

El filtrado de actualizaciones en versiones de sistema operativo distintas de Windows Vista y Windows 7 es normalmente una configuración controlada por el usuario y debe respetarse como tal por las aplicaciones. Sin embargo, en un entorno empresarial, los administradores pueden controlar si los usuarios tienen la opción de filtrar las actualizaciones mediante el valor del registro DontGroupPatches, como se muestra en el ejemplo siguiente.

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

Este valor es de tipo REG \_ DWORD y se interpreta de la siguiente manera.



| Valor DontGroupPatches             | Significado                                                                                                                                                                                                             |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                  | La casilla **Mostrar actualizaciones** se muestra al usuario. El filtrado depende de si el usuario ha activado o no esta casilla.                                                                                         |
| 1                                  | La casilla **Mostrar actualizaciones** se ha quitado de la interfaz de usuario. Las actualizaciones no se filtran de la lista. Este valor se revierte esencialmente al comportamiento de Windows XP SP1, antes de que se introdujera la funcionalidad de **Mostrar actualizaciones** . |
| La entrada DontGroupPatches no está presente | Esto es equivalente a establecer el valor en 0.                                                                                                                                                                       |



 

DontGroupPatches no tiene ningún efecto en Windows Vista y Windows 7, donde la interfaz de usuario no contiene ninguna casilla y las actualizaciones registradas siempre se filtran.

> [!Note]  
> Las directivas las establecen únicamente los administradores. Las aplicaciones no deben modificar este valor. Para obtener más información sobre cómo establecer un directiva de grupo basado en el registro, consulte [Directiva de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page) o [Windows Server Directiva de grupo](/windows/deployment/deploy-whats-new).

 

## <a name="additional-resources"></a>Recursos adicionales

-   [Registrar programas con tipos de cliente](reg-middleware-apps.md)
-   [Instalación](/previous-versions/ms997548(v=msdn.10))
-   [Configuración de agregar o quitar programas con Windows Installer](../msi/configuring-add-remove-programs-with-windows-installer.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Prácticas recomendadas para asociaciones de archivos](fa-best-practices.md)
</dt> <dt>

[Escenario de ejemplo de Asociación de archivos](fa-sample-scenarios.md)
</dt> <dt>

[Directrices para administrar aplicaciones predeterminadas en Windows Vista y versiones posteriores](vista-managing-defaults.md)
</dt> <dt>

[Programas predeterminados](default-programs.md)
</dt> </dl>

 

 
