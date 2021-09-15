---
description: Describe los métodos para abrir un elemento Panel de control para Windows Vista y sistemas posteriores, así como para abarcar los comandos Panel de control heredados.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Ejecución de Panel de control elementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb941bb7542b0d786d682e6626e8d78faea8bd7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579609"
---
# <a name="executing-control-panel-items"></a>Ejecución de Panel de control elementos

> [!Note]  
> Si busca la lista de nombres canónicos y de módulos para los Panel de control, vea Nombres canónicos [de Panel de control elementos](controlpanel-canonical-names.md).

 

Hay dos maneras de abrir un Panel de control elemento:

-   El usuario puede abrir Panel de control y, a continuación, abrir un elemento haciendo clic o haciendo doble clic en el icono del elemento.
-   El usuario o una aplicación pueden iniciar un Panel de control elemento ejecutándose directamente desde el símbolo de la línea de comandos.

Una aplicación puede abrir el Panel de control mediante programación mediante la [**función WinExec.**](/windows/win32/api/winbase/nf-winbase-winexec)


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



En el ejemplo siguiente se muestra cómo una aplicación puede iniciar el elemento Panel de control denominado **MyCpl.cpl** mediante la [**función WinExec.**](/windows/win32/api/winbase/nf-winbase-winexec)


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



Cuando un Panel de control se abre a través de una línea de comandos, puede indicarle que se abra en una pestaña determinada del elemento. Debido a la adición y eliminación de ciertas pestañas en algunos elementos de Windows Vista Panel de control, es posible que la numeración de las pestañas haya cambiado a partir de Windows XP. Por ejemplo, en el ejemplo siguiente se inicia la cuarta pestaña del elemento Sistema en Windows XP y la tercera pestaña en Windows Vista.


```
control.exe sysdm.cpl,,3
```



Este tema trata lo siguiente:

-   [Windows Nombres canónicos de Vista](#windows-vista-canonical-names)
-   [Nuevos comandos para Windows Vista](#new-commands-for-windows-vista)
-   [Comandos de Panel de control heredados](#legacy-control-panel-commands)
-   [Temas relacionados](#related-topics)

## <a name="windows-vista-canonical-names"></a>Windows Nombres canónicos de Vista

En Windows Vista y versiones posteriores, el método preferido para iniciar un elemento Panel de control desde una línea de comandos es usar el nombre canónico del elemento Panel de control. Un nombre canónico es una cadena no localizada que el elemento Panel de control declara en el Registro. El valor de usar un nombre canónico es que abstrae el nombre del módulo del Panel de control elemento. Un elemento se puede implementar en un .dll y posterior se puede volver a implementar como un .exe o cambiar su nombre de módulo. Siempre que el nombre canónico siga siendo el mismo, no es necesario actualizar ningún programa que lo abra con ese nombre canónico.

Por convención, el nombre canónico se forma como "CorporationName.ControlPanelItemName".

En el ejemplo siguiente se muestra cómo una aplicación puede iniciar el Panel de control de **Windows update** con [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



Para iniciar un Panel de control con su nombre canónico, use: "%systemroot% \\ system32 \\control.exe /name *canonicalName"*

Para abrir una subpáptica específica en un elemento o para abrirla con parámetros adicionales, use: "%systemroot% \\ system32 \\control.exe /name **canonicalName** /page **pageName"**

Una aplicación también puede implementar el método [**IOpenControlPanel::Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) para iniciar Panel de control, incluida la capacidad de abrir una sub página específica.

Para obtener una lista completa de Panel de control de elementos canónicos, vea Nombres canónicos [de Panel de control elementos](controlpanel-canonical-names.md).

## <a name="new-commands-for-windows-vista"></a>Nuevos comandos para Windows Vista

En Windows Vista, algunas opciones a las que se ha accedido mediante un módulo .cpl en Windows XP ahora se implementan como .exe archivos. Esto proporciona mayor seguridad al permitir que se pida a los usuarios estándar que proporcionen credenciales de administrador al intentar iniciar los archivos. Se accede a las opciones que no requieren seguridad adicional mediante las mismas líneas de comandos que se usaron en Windows XP. A continuación se muestra una lista de los comandos que se usan en Windows Vista para acceder a pestañas específicas de Panel de control elementos:

### <a name="personalization"></a>Personalización

-   Tamaño de fuente y PPP: %windir% \\ system32 \\DpiScaling.exe
-   Resolución de pantalla: %windir% \\ system32 \\control.exe desk.cpl,Configuración,@Settings
-   Configuración de visualización: %windir% \\ system32 \\control.exe desk.cpl,Configuración,@Settings
-   Temas: %windir% \\ system32 \\control.exe desk.cpl,Themes,@Themes
-   Protector de pantalla: %windir% \\ system32 \\control.exe desk.cpl,screensaver,@screensaver
-   Varios monitores: %windir% \\ system32 \\control.exe desk.cpl,Monitor,@Monitor
-   Combinación de colores: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /pageColorization
-   Fondo del escritorio: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /pageWallpaper

> [!Note]  
> Las ediciones Starter y Basic no admiten control.exe comando /name Microsoft.Personalization.

 

### <a name="system"></a>Sistema

-   Rendimiento: %windir% \\ system32 \\SystemPropertiesPerformance.exe
-   Acceso remoto: %windir% \\ system32 \\SystemPropertiesRemote.exe
-   Nombre del equipo: %windir% \\ system32 \\SystemPropertiesComputerName.exe
-   Protección del sistema: %windir% \\ system32 \\SystemPropertiesProtection.exe
-   Propiedades avanzadas del sistema: %windir% \\ system32 \\SystemPropertiesAdvanced.exe

### <a name="programs-and-features"></a>Programas y características

-   Agregar o quitar programas: %windir% \\ system32 \\control.exe /name Microsoft.ProgramsAndFeatures
-   Windows características: %windir% \\ system32 \\OptionalFeatures.exe

### <a name="regional-and-language-options"></a>Configuración regional y de idioma

-   Teclado: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"
-   Ubicación: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"
-   Administrativo: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"

### <a name="folder-options"></a>Opciones de carpeta

-   Búsqueda de carpetas: %windir% \\ system32 \\rundll32.exe shell32.dll,Options \_ RunDLL 2
-   Asociaciones de archivo: %windir% \\ system32 \\control.exe /name Microsoft.DefaultPrograms /pageFileAssoc
-   Vista: %windir% \\ system32 \\rundll32.exe shell32.dll,Options \_ RunDLL 7
-   General: %windir% \\ system32 \\rundll32.exe shell32.dll,Options \_ RunDLL 0

### <a name="power-options"></a>Opciones de energía

-   Editar la configuración actual del plan: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /page pagePlanSettings
-   Configuración del sistema: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /pageGlobalSettings
-   Crear un plan de energía: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /pageCreateNewPlan
-   No hay ningún comando canónico para la página advanced Configuración, se accede a él de la manera anterior: %windir% \\ system32 \\control.exe powercfg.cpl,3

## <a name="legacy-control-panel-commands"></a>Comandos de Panel de control heredados

Cuando se usa [**la función WinExec,**](/windows/win32/api/winbase/nf-winbase-winexec) el sistema puede reconocer comandos Panel de control especiales. Estos comandos son anteriores a Windows Vista.




| | | control.exe escritorio | Inicia la ventana <strong>Propiedades de pantalla</strong> ventana.<blockquote>[!Note]<br />Las ediciones Starter y Basic no admiten este comando.</blockquote><br /> | | control.exe color | Inicia la ventana <strong>Propiedades de pantalla</strong> con la <strong>pestaña Apariencia</strong> preseleccionada. | | control.exe fecha y hora | Inicia la ventana <strong>Propiedades de fecha y</strong> hora. | | control.exe internacional | Inicia la ventana <strong>Opciones regionales y de</strong> idioma. | | control.exe del mouse | Inicia la ventana <strong>Propiedades del</strong> mouse. | | control.exe teclado | Inicia la ventana <strong>Propiedades del</strong> teclado. | | control.exe impresoras | Muestra la <strong>carpeta Impresoras y faxes.</strong> | | control.exe fuentes | Muestra la <strong>carpeta Fuentes.</strong> | 




 

Para Windows sistemas 2000 y posteriores:



| Get-Help                    | Descripción                                              |
|----------------------------|----------------------------------------------------------|
| control.exe carpetas        | Inicia la ventana **Opciones de carpeta.**                  |
| control.exe netware        | Inicia la ventana **NetWare de Asíns** (si está instalada).   |
| control.exe telefonía      | Inicia la ventana **Teléfono y opciones de módem.**         |
| control.exe admintools     | Muestra la **carpeta Herramientas administrativas.**            |
| control.exe schedtasks     | Muestra la **carpeta Tareas programadas.**                 |
| control.exe netconnections | Muestra la carpeta **Conexiones de** red.             |
| control.exe de datos       | Inicia la ventana **Monitor de inifijo** (si está instalado). |
| control.exe userpasswords  | Inicia la ventana **Cuentas de** usuario.                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Panel de control elementos](control-panel-applications.md)
</dt> <dt>

[Directrices de la experiencia de usuario](user-experience-guidelines.md)
</dt> <dt>

[Registro de Panel de control elementos](registering-control-panel-items.md)
</dt> <dt>

[Uso de CPLApplet](using-cplapplet.md)
</dt> <dt>

[Panel de control de mensajes](message-processing.md)
</dt> <dt>

[Extender elementos de Panel de control sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Asignación de Panel de control categorías](assigning-control-panel-categories.md)
</dt> <dt>

[Crear vínculos de tareas que se pueden buscar para un elemento Panel de control búsqueda](creating-searchable-task-links.md)
</dt> <dt>

[Acceso al Panel de control en modo Caja fuerte en Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
