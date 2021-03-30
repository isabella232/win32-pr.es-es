---
description: Describe los métodos para abrir un elemento del panel de control para Windows Vista y sistemas posteriores, así como para abarcar los comandos heredados del panel de control.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Ejecutar elementos del panel de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaaac4b782273e0b4444fb2b5b6d3cab0b3599ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997833"
---
# <a name="executing-control-panel-items"></a>Ejecutar elementos del panel de control

> [!Note]  
> Si busca la lista de nombres canónicos y de módulos para los elementos del panel de control, consulte [nombres canónicos de elementos del panel de control](controlpanel-canonical-names.md).

 

Hay dos maneras de abrir un elemento del panel de control:

-   El usuario puede abrir el panel de control y, a continuación, abrir un elemento haciendo clic o haciendo doble clic en el icono del elemento.
-   El usuario o una aplicación puede iniciar un elemento del panel de control si lo ejecuta directamente desde el símbolo de la línea de comandos.

Una aplicación puede abrir el panel de control mediante programación con la función [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) .


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



En el ejemplo siguiente se muestra cómo una aplicación puede iniciar el elemento del panel de control denominado **MyCpl.cpl** mediante la función [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) .


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



Cuando un elemento del panel de control se abre a través de una línea de comandos, puede indicarle que se abra en una pestaña determinada del elemento. Debido a la adición y eliminación de ciertas pestañas en algunos elementos del panel de control de Windows Vista, es posible que la numeración de las pestañas haya cambiado en Windows XP. Por ejemplo, en el ejemplo siguiente se inicia la cuarta pestaña en el elemento del sistema en Windows XP y la tercera pestaña en Windows Vista.


```
control.exe sysdm.cpl,,3
```



Este tema trata lo siguiente:

-   [Nombres canónicos de Windows Vista](#windows-vista-canonical-names)
-   [Nuevos comandos para Windows Vista](#new-commands-for-windows-vista)
-   [Comandos del panel de control heredado](#legacy-control-panel-commands)
-   [Temas relacionados](#related-topics)

## <a name="windows-vista-canonical-names"></a>Nombres canónicos de Windows Vista

En Windows Vista y versiones posteriores, el método preferido para iniciar un elemento del panel de control desde una línea de comandos es usar el nombre canónico del elemento del panel de control. Un nombre canónico es una cadena no localizada que el elemento del panel de control declara en el registro. El valor de usar un nombre canónico es que abstrae el nombre del módulo del elemento del panel de control. Un elemento se puede implementar en un archivo. dll y, posteriormente, volver a implementarse como un archivo. exe o cambiar su nombre de módulo. Siempre que el nombre canónico siga siendo el mismo, no es necesario actualizar ningún programa que lo abra con ese nombre canónico.

Por Convención, el nombre canónico tiene el formato "CorporationName. ControlPanelItemName".

En el ejemplo siguiente se muestra cómo una aplicación puede iniciar el elemento del panel de control **Windows Update** con [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



Para iniciar un elemento del panel de control con su nombre canónico, use: "% SystemRoot% \\ system32 \\control.exe/name *canonicalName*"

Para abrir una subpágina específica de un elemento, o para abrirla con parámetros adicionales, use: "% SystemRoot% \\ system32 \\control.exe/name **canonicalName** /Page **pagename**"

Una aplicación también puede implementar el método [**IOpenControlPanel:: Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) para iniciar elementos del panel de control, incluida la capacidad de abrir una subpágina concreta.

Para obtener una lista completa de los nombres canónicos de los elementos del panel de control, consulte [nombres canónicos de elementos del panel de control](controlpanel-canonical-names.md).

## <a name="new-commands-for-windows-vista"></a>Nuevos comandos para Windows Vista

En Windows Vista, algunas de las opciones a las que tenía acceso un módulo. cpl en Windows XP se implementan ahora como archivos. exe. Esto proporciona seguridad adicional al permitir que se pida a los usuarios estándar que proporcionen credenciales de administrador al intentar iniciar los archivos. Las opciones que no requieren seguridad adicional tienen acceso a las mismas líneas de comandos que se usaron en Windows XP. A continuación se muestra una lista de comandos usados en Windows Vista para tener acceso a pestañas específicas de elementos del panel de control:

### <a name="personalization"></a>Personalización

-   Tamaño de fuente y PPP:% WINDIR% \\ system32 \\DpiScaling.exe
-   Resolución de pantalla:% WINDIR% \\ system32 \\control.exe desk.cpl, configuración@Settings
-   Configuración de pantalla:% WINDIR% \\ system32 \\control.exe desk.cpl, configuración@Settings
-   Temas:% WINDIR% \\ system32 \\control.exe desk.cpl, temas@Themes
-   Protector de la:% WINDIR% \\ system32 \\control.exe desk.cpl, protector de la@screensaver
-   Varios monitores:% WINDIR% \\ system32 \\control.exe desk.cpl, monitor,@Monitor
-   Combinación de colores:% WINDIR% \\ system32 \\control.exe/Name Microsoft. Personalization/Page pageColorization
-   Fondo de escritorio:% WINDIR% \\ system32 \\control.exe/Name Microsoft. Personalization/Page pageWallpaper

> [!Note]  
> Las ediciones Starter y Basic no admiten el comando control.exe/Name Microsoft. Personalization.

 

### <a name="system"></a>Sistema

-   Rendimiento:% WINDIR% \\ system32 \\SystemPropertiesPerformance.exe
-   Acceso remoto:% WINDIR% \\ system32 \\SystemPropertiesRemote.exe
-   Nombre de equipo:% WINDIR% \\ system32 \\SystemPropertiesComputerName.exe
-   Protección del sistema:% WINDIR% \\ system32 \\SystemPropertiesProtection.exe
-   Propiedades avanzadas del sistema:% WINDIR% \\ system32 \\SystemPropertiesAdvanced.exe

### <a name="programs-and-features"></a>Programas y características

-   Agregar o quitar programas:% WINDIR% \\ system32 \\control.exe/Name Microsoft. ProgramsAndFeatures
-   Características de Windows:% WINDIR% \\ system32 \\OptionalFeatures.exe

### <a name="regional-and-language-options"></a>Configuración regional y de idioma

-   Teclado:% SystemRoot% \\ system32 \\control.exe/Name Microsoft. RegionalAndLanguageOptions/Page/p: "Keyboard"
-   Ubicación:% SystemRoot% \\ system32 \\control.exe/Name Microsoft. RegionalAndLanguageOptions/Page/p: "Location"
-   Administrativo:% SystemRoot% \\ system32 \\control.exe/Name Microsoft. RegionalAndLanguageOptions/Page/p: "Administrative"

### <a name="folder-options"></a>Opciones de carpeta

-   Búsqueda de carpetas:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, opciones \_ RunDLL 2
-   Asociaciones de archivo:% WINDIR% \\ system32 \\control.exe/Name Microsoft. DefaultPrograms/Page pageFileAssoc
-   Vista:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, opciones \_ RunDLL 7
-   General:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, opciones \_ RunDLL 0

### <a name="power-options"></a>Opciones de energía

-   Editar la configuración del plan actual:% WINDIR% \\ system32 \\control.exe/Name Microsoft. PowerOptions/Page pagePlanSettings
-   Configuración del sistema:% WINDIR% \\ system32 \\control.exe/Name Microsoft. PowerOptions/Page pageGlobalSettings
-   Crear un plan de energía:% WINDIR% \\ system32 \\control.exe/Name Microsoft. PowerOptions/Page pageCreateNewPlan
-   No hay ningún comando canónico para la página Configuración avanzada, se tiene acceso a ella de la manera más antigua:% WINDIR% \\ system32 \\control.exe powercfg.cpl,, 3

## <a name="legacy-control-panel-commands"></a>Comandos del panel de control heredado

Cuando se usa la función [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) , el sistema puede reconocer comandos especiales del panel de control. Estos comandos preparan Windows Vista.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Escritorio control.exe</td>
<td>Inicia la ventana <strong>propiedades de pantalla</strong> .
<blockquote>
[!Note]<br />
Las ediciones Starter y Basic no admiten este comando.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Color de control.exe</td>
<td>Inicia la ventana <strong>propiedades de pantalla</strong> con la pestaña <strong>apariencia</strong> preseleccionada.</td>
</tr>
<tr class="odd">
<td>control.exe fecha y hora</td>
<td>Inicia la ventana <strong>propiedades de fecha y hora</strong> .</td>
</tr>
<tr class="even">
<td>control.exe internacional</td>
<td>Inicia la ventana <strong>Opciones regionales y de idioma</strong> .</td>
</tr>
<tr class="odd">
<td>Mouse control.exe</td>
<td>Inicia la ventana <strong>propiedades del mouse</strong> .</td>
</tr>
<tr class="even">
<td>Teclado control.exe</td>
<td>Inicia la ventana <strong>propiedades del teclado</strong> .</td>
</tr>
<tr class="odd">
<td>control.exe impresoras</td>
<td>Muestra la carpeta <strong>impresoras y faxes</strong> .</td>
</tr>
<tr class="even">
<td>Fuentes de control.exe</td>
<td>Muestra la carpeta <strong>fuentes</strong> .</td>
</tr>
</tbody>
</table>



 

Para sistemas Windows 2000 y versiones posteriores:



|                            |                                                          |
|----------------------------|----------------------------------------------------------|
| Carpetas de control.exe        | Inicia la ventana **Opciones de carpeta** .                  |
| control.exe NetWare        | Inicia la ventana de **Novell NetWare** (si está instalado).   |
| Telefonía control.exe      | Inicia la ventana **Opciones de teléfono y módem** .         |
| control.exe AdminTools     | Muestra la carpeta **herramientas administrativas** .            |
| control.exe schedtasks     | Muestra la carpeta **tareas programadas** .                 |
| control.exe netconnections | Muestra la carpeta **conexiones de red** .             |
| control.exe infrarrojos       | Inicia la ventana **monitor de infrarrojos** (si está instalado). |
| control.exe userpasswords  | Inicia la ventana **cuentas de usuario** .                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos del panel de control](control-panel-applications.md)
</dt> <dt>

[Directrices de la experiencia de usuario](user-experience-guidelines.md)
</dt> <dt>

[Registrar elementos del panel de control](registering-control-panel-items.md)
</dt> <dt>

[Usar CPLApplet](using-cplapplet.md)
</dt> <dt>

[Procesamiento de mensajes del panel de control](message-processing.md)
</dt> <dt>

[Extender elementos del panel de control del sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Asignar categorías del panel de control](assigning-control-panel-categories.md)
</dt> <dt>

[Crear vínculos de tarea que se pueden buscar para un elemento del panel de control](creating-searchable-task-links.md)
</dt> <dt>

[Acceder al panel de control en modo seguro en Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
