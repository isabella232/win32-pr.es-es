---
title: Cuadros de diálogo abrir y guardar como
description: El cuadro de diálogo Abrir permite al usuario especificar la unidad, el directorio y el nombre de un archivo o un conjunto de archivos que se van a abrir.
ms.assetid: 5676ca9d-daca-40bf-8881-def2ff841c58
keywords:
- Biblioteca de cuadros de diálogo comunes
- cuadros de diálogo comunes
- Cuadro de diálogo Abrir
- Guardar como, cuadro de diálogo
- personalizar el cuadro de diálogo abrir
- personalizar el cuadro de diálogo Guardar como
- cuadros de diálogo, abrir
- cuadros de diálogo, guardar como
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: bc2977a5f91abde32a78c722a7a7c7b6b4a23ffd
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105698467"
---
# <a name="open-and-save-as-dialog-boxes"></a>Cuadros de diálogo abrir y guardar como

> [!NOTE]
> La función [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) se muestra en el [ejemplo el archivo está en uso](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse).

\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)). Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]

El cuadro de diálogo **abrir** permite al usuario especificar la unidad, el directorio y el nombre de un archivo o un conjunto de archivos que se van a abrir. Puede crear y mostrar un cuadro de diálogo **abierto** inicializando una estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) y pasando la estructura a la función [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) .

El cuadro de diálogo **Guardar como** permite al usuario especificar la unidad, el directorio y el nombre de un archivo que se va a guardar. Puede crear y mostrar un cuadro de diálogo **Guardar como** inicializando una estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) y pasando la estructura a la función [**getSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) .

Los cuadros de diálogo **abrir** y **Guardar como** del explorador proporcionan características de la interfaz de usuario similares al explorador de Windows. Sin embargo, el sistema sigue siendo compatible con los cuadros de diálogo **abrir** y **Guardar como** de estilo antiguo para las aplicaciones que deben ser coherentes con la interfaz de usuario de estilo antiguo.

Además de la diferencia en la apariencia, los cuadros de diálogo estilo del explorador y estilo antiguo difieren en el uso de plantillas personalizadas y procedimientos de enlace para personalizar los cuadros de diálogo. Sin embargo, los cuadros de diálogo estilo del explorador y estilo antiguo tienen el mismo comportamiento para la mayoría de las operaciones básicas, como la especificación de un filtro de nombre de archivo, la validación de la entrada del usuario y la obtención del nombre de archivo especificado por el usuario. Para obtener más información acerca de los cuadros de diálogo estilo del explorador y estilo antiguo, vea el apartado sobre la [Personalización del cuadro de diálogo abrir y guardar como](#open-and-save-as-dialog-box-customization).

En la ilustración siguiente se muestra un cuadro de diálogo de **apertura** de estilo de explorador típico.

![Abrir archivo (cuadro de diálogo)](images/opendialogboxxp.png)

En la ilustración siguiente se muestra un cuadro de diálogo **Guardar como** de estilo de explorador típico.

![cuadro de diálogo Guardar archivo](images/saveasdialogboxxp.png)

Si el usuario especifica un nombre de archivo y hace clic en el botón **Aceptar** , [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) o [**getSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) devuelve **true**. El búfer señalado por el miembro **lpstrFile** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) contiene la ruta de acceso completa y el nombre de archivo especificado por el usuario.

Si el usuario cancela el cuadro de diálogo **abrir** o **Guardar como** o se produce un error, la función devuelve **false**. Para determinar la causa del error, llame a la función [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar el valor de error extendido. Si el búfer de **lpstrFile** es demasiado pequeño para recibir el nombre completo, **CommDlgExtendedError** devuelve **FNERR \_ BUFFERTOOSMALL** y los primeros 2 bytes del búfer al que apunta el miembro **lpstrFile** se establecen en un valor entero que especifica el tamaño necesario para recibir el nombre completo.

Los temas siguientes se describen en esta sección.

-   [Nombres de archivo y directorios](#file-names-and-directories)
-   [Filtros](#filters)
-   [Validación de archivos y directorios](#file-and-directory-validation)
-   [Abrir y guardar como personalización del cuadro de diálogo](#open-and-save-as-dialog-box-customization)
-   [Procedimientos de enlace de estilo del explorador](#explorer-style-hook-procedures)
-   [Plantillas personalizadas de estilo Explorador](#explorer-style-custom-templates)
-   [Identificadores de control de estilo del explorador](#explorer-style-control-identifiers)
-   [Personalización de Old-Style cuadros de diálogo](#customizing-old-style-dialog-boxes)

## <a name="file-names-and-directories"></a>Nombres de archivo y directorios

La información de esta sección se aplica a los cuadros de diálogo de estilo de explorador y de estilo antiguo **abrir** y **Guardar como** .

Antes de llamar a las funciones [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) o [**getSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) , el miembro **lpstrFile** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) debe apuntar al búfer para recibir el nombre de archivo. El miembro **nMaxFile** debe especificar el tamaño, en caracteres, del búfer **lpstrFile** . Para una función ANSI, es el número de bytes, pero para una función Unicode es el número de caracteres.

Si el usuario especifica un nombre de archivo y hace clic en el botón **Aceptar** , el cuadro de diálogo copia la unidad, el directorio y el nombre de archivo seleccionados en el búfer de **lpstrFile** . La función también establece los miembros **nFileOffset** y **nFileExtension** en los desplazamientos, en caracteres, desde el inicio del búfer hasta el nombre de archivo y la extensión de nombre de archivo, respectivamente.

Para recuperar solo el nombre de archivo y la extensión, establezca el miembro **lpstrFileTitle** para que apunte a un búfer y establezca el miembro **nMaxFileTitle** en el tamaño, en caracteres, del búfer. Como alternativa, puede pasar el búfer de **lpstrFile** en una llamada a la función [**GetFileTitle**](/windows/desktop/api/Commdlg/nf-commdlg-getfiletitlea) para obtener el nombre para mostrar del archivo seleccionado. Sin embargo, tenga en cuenta que el nombre de archivo que devuelve **GetFileTitle** solo incluye una extensión si es la preferencia del usuario para mostrar los nombres de archivo.

El cuadro de diálogo utiliza el directorio actual para el proceso de llamada como directorio inicial desde el que se muestran los archivos y directorios. Use las funciones [**GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) y [**SetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) para obtener y cambiar el directorio actual de un proceso. Para especificar un directorio inicial diferente sin cambiar el directorio actual, use el miembro **lpstrInitialDir** para especificar el nombre de un directorio. El cuadro de diálogo cambia automáticamente el directorio actual cuando el usuario selecciona una unidad o un directorio diferente. Para evitar que el cuadro de diálogo cambie el directorio actual, establezca la marca **OFN \_ NOCHANGEDIR** . Esta marca no impide que el usuario cambie los directorios para buscar un archivo.

Para especificar una extensión de nombre de archivo predeterminada, use el miembro **lpstrDefExt** . Si el usuario especifica un nombre de archivo que no tiene una extensión, el cuadro de diálogo agrega la extensión predeterminada. Si especifica una extensión predeterminada y el usuario especifica un nombre de archivo con una extensión diferente, el cuadro de diálogo establece la marca **\_ EXTENSIONDIFFERENT de OFN** .

Para permitir al usuario seleccionar más de un archivo de un directorio, establezca la marca **OFN \_ ALLOWMULTISELECT** . Por compatibilidad con las aplicaciones anteriores, el cuadro de diálogo selección múltiple predeterminada utiliza la interfaz de usuario de estilo antiguo. Para mostrar un cuadro de diálogo de selección múltiple de estilo del explorador, también debe establecer la marca **OFN \_ Explorer** .

Si el usuario selecciona más de un archivo, el búfer señalado por el miembro **lpstrFile** devuelve la ruta de acceso al directorio actual seguido de los nombres de archivo de los archivos seleccionados. El miembro **nFileOffset** es el desplazamiento del primer nombre de archivo y no se utiliza el miembro **nFileExtension** . En la tabla siguiente se describe la diferencia entre los cuadros de diálogo de estilo de explorador y de estilo antiguo al devolver varios nombres de archivo.



| Estilo de cuadro de diálogo            | Descripción                                                                                                                                                                                                               |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cuadros de diálogo de estilo del explorador | Las cadenas de nombre de archivo y directorio se separan con **valores NULL** , con un carácter **nulo** adicional después del último nombre de archivo. Este formato permite a los cuadros de diálogo de estilo del explorador devolver nombres de archivo largos que incluyen espacios. |
| Cuadros de diálogo de estilo antiguo      | Las cadenas de nombre de archivo y directorio se separan mediante espacios. En el caso de los nombres de archivo con espacios, la función usa nombres de archivo cortos.                                                                                              |



 

Puede utilizar la función [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) para realizar la conversión entre nombres de archivo largos y cortos.

Si especifica **OFN \_ ALLOWMULTISELECT** y el usuario selecciona un solo archivo, la cadena **lpstrFile** no tiene un separador entre la ruta de acceso y el nombre de archivo.

## <a name="filters"></a>Filtros

La información de esta sección se aplica a los cuadros de diálogo de estilo de explorador y antiguo **abrir** y **Guardar como** .

Puede proporcionar filtros de nombre de archivo para ayudar al usuario a limitar los nombres de archivo que muestra el cuadro de diálogo. Un filtro de nombre de archivo consta de un par de cadenas terminadas en null, una descripción y un patrón, una concatenada con la otra. El cuadro de diálogo muestra la descripción para permitir que el usuario elija el filtro que se va a usar. y usa el patrón para seleccionar los archivos que se van a mostrar.

Para especificar los filtros, establezca el miembro **lpstrFilter** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) para que apunte a un búfer que contenga una matriz de pares de cadenas de filtro. La última cadena de la matriz debe ir seguida de un carácter nulo adicional.

Una cadena de patrón puede ser una combinación de caracteres de nombre de archivo válidos y el asterisco ( \* ). El asterisco es un carácter comodín que representa cualquier combinación de caracteres de nombre de archivo válidos. En el cuadro de diálogo solo se muestran los archivos que coinciden con el patrón. Para especificar varios patrones para la misma descripción, debe usar un punto y coma (;) para separar los patrones. Tenga en cuenta que los caracteres de espacio de la cadena de patrón pueden producir resultados inesperados.

En el fragmento de código siguiente se especifican dos filtros. El filtro con la descripción "origen" tiene dos patrones. Si el usuario selecciona este filtro, el cuadro de diálogo muestra solo los archivos que tienen el. C y. Extensiones de CXX. Tenga en cuenta que, en el lenguaje de programación C, una cadena entre comillas dobles está terminada en NULL.


```
OPENFILENAME ofn;       // common dialog box structure

ofn.lpstrFilter = "Source\0*.C;*.CXX\0All\0*.*\0"
ofn.nFilterIndex = 1;
```



El miembro **nFilterIndex** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) especifica un índice que indica qué filtro utiliza inicialmente el cuadro de diálogo. El primer filtro del búfer tiene el índice 1, el segundo 2, y así sucesivamente. Si el usuario cambia el filtro mientras se usa el cuadro de diálogo, el miembro **nFilterIndex** se establece en el índice del filtro seleccionado al devolverse.

Puede crear un filtro personalizado estableciendo el miembro **lpstrCustomFilter** en la dirección de un búfer que contenga un filtro único y estableciendo el miembro **nMaxCustFilter** en el tamaño del búfer, en caracteres o bytes. El cuadro de diálogo siempre coloca el filtro personalizado al principio de la lista de filtros y, en la devolución, siempre actualiza la parte del patrón del filtro con el patrón del filtro seleccionado por el usuario.

En los cuadros de diálogo de estilo del explorador, la extensión predeterminada puede cambiar si el usuario selecciona un filtro diferente. Si el usuario selecciona un filtro cuyo primer patrón tiene el formato \* .*XXX* (es decir, la extensión no incluye un carácter comodín), el cuadro de diálogo utiliza *XXX* como extensión predeterminada. Esto solo ocurre si especificó una extensión predeterminada en el miembro **lpstrDefExt** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . Por ejemplo, si el usuario selecciona "origen \\ 0" \* . C; \* . CXX \\ 0 ", la extensión predeterminada cambia a" C ". Sin embargo, si ha definido el filtro como "origen \\ 0" \* . C \* \\ 0 ", la extensión predeterminada no cambiaría porque la extensión incluye un carácter comodín.

El mensaje de notificación [**\_ INCLUDEITEM de CDN**](cdn-includeitem.md) proporciona otra manera de filtrar los nombres que muestra el cuadro de diálogo. Para usar este mensaje, proporcione un procedimiento de enlace [**OFNHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) y especifique la marca **\_ ENABLEINCLUDENOTIFY de OFN** en la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) al crear el cuadro de diálogo. Cada vez que el usuario abre una carpeta, el cuadro de diálogo envía una notificación **\_ INCLUDEITEM de CDN** al procedimiento de enlace para cada elemento de la carpeta que se acaba de abrir. El valor devuelto del procedimiento de enlace indica si el cuadro de diálogo debe mostrar el elemento en la lista de elementos de la carpeta.

## <a name="file-and-directory-validation"></a>Validación de archivos y directorios

A menos que se indique lo contrario, la información de esta sección se aplica a los cuadros de diálogo de estilo de explorador y de estilo antiguo **abrir** y **Guardar como** .

El cuadro de diálogo valida automáticamente los nombres de archivo especificados por el usuario para asegurarse de que los nombres solo contienen caracteres válidos. Para invalidar la validación de caracteres de nombre de archivo, establezca la marca **OFN \_ novalidate** .

Para forzar que el cuadro de diálogo Compruebe que el usuario especificó el nombre de un archivo existente, establezca la marca **OFN \_ FILEMUSTEXIST** . Para forzar la comprobación de que existe la ruta de acceso especificada, establezca la marca **OFN \_ PATHMUSTEXIST** . Si establece la marca **OFN \_ CREATEPROMPT** , el cuadro de diálogo le pedirá permiso al usuario para crear un archivo inexistente. Si se establece esta marca y el usuario elige crear un nuevo archivo, el cuadro de diálogo se cierra y la función devuelve el nombre especificado. De lo contrario, el cuadro de diálogo permanece abierto.

Al usar el cuadro de diálogo **Guardar como** , puede dirigir el cuadro de diálogo para pedir permiso al usuario para sobrescribir un archivo existente estableciendo la marca **\_ OVERWRITEPROMPT de OFN** .

De forma predeterminada, el cuadro de diálogo crea un archivo de prueba de longitud cero para determinar si se puede crear un nuevo archivo en el directorio seleccionado. Para evitar la creación de este archivo de prueba, establezca la marca **OFN \_ NOTESTFILECREATE** .

Si habilita un procedimiento de enlace, el cuadro de diálogo notifica al procedimiento de enlace cuando se produce una infracción de uso compartido de red para el nombre de archivo especificado por el usuario. Si establece la marca **del \_ Explorador de OFN** , el cuadro de diálogo envía el mensaje [**\_ SHAREVIOLATION de la red CDN**](cdn-shareviolation.md) al procedimiento de enlace. Si no establece **OFN \_ Explorer**, el cuadro de diálogo envía el mensaje [**SHAREVISTRING**](sharevistring.md) registrado al procedimiento de enlace. Para evitar que el cuadro de diálogo envíe notificaciones de infracciones de uso compartido, establezca la marca **OFN \_ SHAREAWARE** .

Si el usuario selecciona la casilla de solo lectura, el cuadro de diálogo establece la **marca \_ ReadOnly de OFN** en la devolución. Para ocultar la casilla **Abrir como solo lectura** , establezca la marca **OFN \_ HIDEREADONLY** . Para evitar que el cuadro de diálogo devuelva nombres de archivos existentes que tengan el atributo de solo lectura, establezca la marca **OFN \_ NOREADONLYRETURN** .

Para evitar que el cuadro de diálogo desreferencia los archivos de vínculo, establezca el valor de **\_ NODEREFERENCELINKS de OFN** . En este caso, el cuadro de diálogo devuelve el nombre del archivo de vínculo en lugar del nombre del archivo al que hace referencia el archivo de vínculo.

## <a name="open-and-save-as-dialog-box-customization"></a>Abrir y guardar como personalización del cuadro de diálogo

Puede personalizar un cuadro de diálogo **abrir** o **Guardar como** si proporciona un procedimiento de enlace, una plantilla personalizada o ambos. Sin embargo, las versiones de estilo de explorador y de estilo anterior de los cuadros de diálogo difieren en el uso de plantillas personalizadas y procedimientos de enlace.

Para obtener información sobre cómo personalizar un cuadro de diálogo de estilo del explorador, vea [procedimientos de enlace de estilo](#explorer-style-hook-procedures)del explorador, [plantillas personalizadas de estilo del](#explorer-style-custom-templates)explorador y [identificadores de controles de estilo del explorador](#explorer-style-control-identifiers). Para obtener información sobre cómo personalizar un cuadro de diálogo de estilo antiguo, vea [personalizar Old-Style cuadros de diálogo](#customizing-old-style-dialog-boxes).

En la tabla siguiente se resumen las diferencias entre los dos estilos.



| Personalización                  | Descripción                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Procedimiento de enlace de estilo del explorador  | El procedimiento de enlace recibe mensajes de notificación enviados desde el cuadro de diálogo común y mensajes para cualquier control adicional que haya definido especificando una plantilla de diálogo secundaria. El procedimiento de enlace no recibe mensajes para los controles estándar del cuadro de diálogo predeterminado. |
| Plantilla personalizada de estilo de explorador | El sistema utiliza la plantilla personalizada para crear un cuadro de diálogo secundario. La plantilla puede definir controles adicionales y puede especificar la ubicación del clúster de controles estándar. La plantilla personalizada no reemplaza la plantilla predeterminada.                                          |
| Procedimiento de enlace de estilo antiguo       | El procedimiento de enlace recibe todos los mensajes enviados al cuadro de diálogo, incluidos los mensajes de los controles estándar y los controles personalizados. El procedimiento de enlace recibe también mensajes registrados enviados desde el cuadro de diálogo común.                                                         |
| Plantilla personalizada de estilo antiguo      | La plantilla personalizada reemplaza la plantilla predeterminada. Cree la plantilla personalizada modificando la plantilla predeterminada especificada en el archivo FileOpen. Dlg.                                                                                                                                  |



 

El título predeterminado para los cuadros de diálogo estilo del explorador y estilo antiguo es "**abrir**" o "**Guardar como**". Para cambiar el título, especifique el nuevo título en el miembro **lpstrTitle** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .

El subárbol del registro de **\_ \_ usuario actual de HKEY** puede contener valores que personalicen el contenido de los cuadros de diálogo **abrir** y **Guardar como** del explorador. Estas entradas del registro solo afectan a los cuadros de diálogo que se muestran para el usuario asociado al subárbol del registro.

Para ocultar características de los cuadros de diálogo **abrir** y **Guardar como** del explorador, un administrador puede establecer los valores de la tabla siguiente bajo esta subclave:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Comdlg32
```



| Nombre del valor       | Valor | Significado                                  |
|------------------|-------|------------------------------------------|
| **NoPlacesBar**  | 1     | Oculta la barra de ubicaciones.                    |
| **NoFileMRU**    | 1     | Oculta la lista de elementos usados más recientemente (MRU). |
| **NoBackButton** | 1     | Oculta el botón **atrás** .               |



 

El contenido de la barra de **ubicaciones** viene determinado por el contenido de la siguiente subclave:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Comdlg32
                     Placesbar
```

Actualmente, solo puede haber cinco entradas bajo esta clave y el índice de valor/nombre está basado en cero. Los nombres de las entradas deben ser Place0, Place1, Place2, Place3 y Place4. Los valores de las entradas pueden ser los valores **reg \_ DWORD**, **reg \_ SZ** o **reg \_ Expand \_ SZ** que identifiquen las ubicaciones que se van a incluir en la barra de ubicaciones.



| Tipo de valor                         | Significado                                                                                                   |
|------------------------------------|-----------------------------------------------------------------------------------------------------------|
| **\_valor DWORD reg**                     | Valor CSIDL que identifica una carpeta. Para obtener una lista de valores de CSIDL, consulte [**valores de CSIDL**](../shell/csidl.md). |
| **Reg \_ . SZ** o **reg \_ Expand \_ SZ** | Una cadena terminada en null que especifica una ruta de acceso válida.                                                     |



 

## <a name="explorer-style-hook-procedures"></a>Explorer-Style procedimientos de enlace

Puede personalizar un cuadro de diálogo para **abrir** o **Guardar como** estilo del explorador proporcionando un procedimiento de enlace, una plantilla personalizada o ambos. Si proporciona un procedimiento de enlace para un cuadro de diálogo de estilo Explorador, el sistema crea un cuadro de diálogo que es un elemento secundario del cuadro de diálogo predeterminado. El procedimiento de enlace actúa como el procedimiento de diálogo para el cuadro de diálogo secundario. Este cuadro de diálogo secundario se basa en la plantilla personalizada o en una plantilla predeterminada si no se proporciona ninguno. Para obtener más información, vea [plantillas personalizadas de estilo de explorador](#explorer-style-custom-templates).

Para habilitar un procedimiento de enlace para un cuadro de diálogo para **abrir** o **Guardar como** estilo del explorador, use la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) al crear el cuadro de diálogo. Establezca las **marcas OFN \_ ENABLEHOOK** y **OFN \_ Explorer** en el miembro **Flags** y especifique la dirección de un procedimiento de enlace [**OFNHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) en el miembro **lpfnHook** . Si proporciona un procedimiento de enlace y omite la marca del **\_ Explorador de OFN** , debe usar un procedimiento de enlace de [**OFNHookProcOldStyle**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) y obtendrá la interfaz de usuario de estilo antiguo. Para obtener más información, vea [personalizar Old-Style cuadros de diálogo](#customizing-old-style-dialog-boxes).

Un procedimiento de enlace de estilo del explorador recibe una variedad de mensajes mientras el cuadro de diálogo está abierto. Entre ellas, figuran:

-   Mensaje [**de \_ INITDIALOG de WM**](wm-initdialog.md) y otros mensajes del cuadro de diálogo estándar, como el mensaje de color de control de [**\_ CTLCOLORDLG de WM**](wm-ctlcolordlg.md) .
-   Un conjunto de mensajes de notificación de [**\_ notificaciones de WM**](../controls/wm-notify.md) que indican las acciones realizadas por el usuario u otros eventos del cuadro de diálogo.
-   Mensajes para cualquier control adicional que haya definido especificando una plantilla de cuadro de diálogo secundaria.

Además, hay un conjunto de mensajes que se pueden enviar a un cuadro de diálogo de estilo Explorador para obtener información o para controlar el comportamiento y la apariencia del cuadro de diálogo.

Si proporciona un procedimiento de enlace para un cuadro de diálogo de estilo Explorador, el procedimiento de cuadro de diálogo predeterminado crea un cuadro de diálogo secundario cuando el procedimiento de diálogo predeterminado está procesando su mensaje de [**WM \_ INITDIALOG**](wm-initdialog.md) . El procedimiento de enlace actúa como el procedimiento de diálogo para el cuadro de diálogo secundario. En este momento, el procedimiento de enlace recibe su propio mensaje de **WM \_ INITDIALOG** con el parámetro *lParam* establecido en la dirección de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) usada para inicializar el cuadro de diálogo. Después de que el cuadro de diálogo secundario finaliza el procesamiento de su propio mensaje de **\_ INITDIALOG de WM** , el procedimiento de cuadro de diálogo predeterminado mueve los controles estándar, si es necesario, para dejar espacio a los controles adicionales del cuadro de diálogo secundario. Después, el procedimiento de cuadro de diálogo predeterminado envía el mensaje de notificación [**\_ INITDONE de la red CDN**](cdn-initdone.md) al procedimiento de enlace.

El procedimiento de enlace recibe mensajes de notificación de [**\_ notificaciones de WM**](../controls/wm-notify.md) que indican las acciones realizadas por el usuario en el cuadro de diálogo. Puede usar algunos de estos mensajes para controlar el comportamiento del cuadro de diálogo. Por ejemplo, el procedimiento de enlace recibe el mensaje [**\_ FILEOK de la red CDN**](cdn-fileok.md) cuando el usuario elige un nombre de archivo y hace clic en el botón **Aceptar** . En respuesta a este mensaje, el procedimiento de enlace puede utilizar la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para rechazar el nombre seleccionado y forzar que el cuadro de diálogo permanezca abierto.

El parámetro *lParam* de cada mensaje de [**\_ notificación de WM**](../controls/wm-notify.md) es un puntero a una estructura de [**Notify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) o [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) que define la acción. El miembro de **código** en el encabezado de esta estructura contiene uno de los siguientes mensajes de notificación.



| Mensaje                                           | Significado                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FILEOK de CDN \_**](cdn-fileok.md)                 | El usuario hizo clic en el botón **Aceptar** ; el cuadro de diálogo está a punto de cerrarse.                                                                                                                                                                                                                          |
| [**FOLDERCHANGE de CDN \_**](cdn-folderchange.md)     | El usuario ha abierto una nueva carpeta o directorio.                                                                                                                                                                                                                                                     |
| [**ayuda de CDN \_**](cdn-help.md)                     | El usuario hizo clic en el botón **ayuda** .                                                                                                                                                                                                                                                          |
| [**INCLUDEITEM de CDN \_**](cdn-includeitem.md)       | Determina si se debe mostrar un elemento. Cuando el usuario abre una nueva carpeta o directorio, el sistema envía esta notificación para cada elemento de la carpeta o directorio. El sistema envía esta notificación solo si se estableció la marca **OFN \_ ENABLEINCLUDENOTIFY** .                          |
| [**INITDONE de CDN \_**](cdn-initdone.md)             | El sistema ha terminado de inicializar el cuadro de diálogo y el cuadro de diálogo ha terminado de procesar el mensaje de [**\_ INITDIALOG de WM**](wm-initdialog.md) . Además, el sistema ha terminado de organizar los controles en el cuadro de diálogo común para dejar espacio a los controles del cuadro de diálogo secundario (si hay alguno). |
| [**SELCHANGE de CDN \_**](cdn-selchange.md)           | El usuario seleccionó un nuevo archivo o carpeta en la lista de archivos.                                                                                                                                                                                                                                     |
| [**SHAREVIOLATION de CDN \_**](cdn-shareviolation.md) | El cuadro de diálogo común encontró una infracción de uso compartido en el archivo que se va a devolver.                                                                                                                                                                                                        |
| [**TYPECHANGE de CDN \_**](cdn-typechange.md)         | El usuario seleccionó un nuevo tipo de archivo en la lista de tipos de archivo.                                                                                                                                                                                                                                 |



 

Estos mensajes de [**\_ notificación de WM**](../controls/wm-notify.md) sustituyen a los mensajes registrados [**FILEOKSTRING**](fileokstring.md), [**LBSELCHSTRING**](lbselchstring.md), [**SHAREVISTRING**](sharevistring.md)y [**HELPMSGSTRING**](helpmsgstring.md) utilizados por versiones anteriores de los cuadros de diálogo **abrir** y **Guardar como** . Sin embargo, el procedimiento de enlace recibe también el mensaje reemplazado después del mensaje de **\_ notificación de WM** si el procesamiento de **\_ notificaciones de WM** no usa [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para establecer un valor **\_ MSGRESULT de DWL** distinto de cero.

Para recuperar información sobre el estado del cuadro de diálogo o para controlar el comportamiento y la apariencia del cuadro de diálogo, el procedimiento de enlace puede enviar los siguientes mensajes al cuadro de diálogo.



| Mensaje                                             | Significado                                                                                                                                                                                                                  |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CDM \_ GETFILEPATH**](cdm-getfilepath.md)         | Recupera la ruta de acceso y el nombre de archivo del archivo seleccionado.                                                                                                                                                                   |
| [**CDM \_ GETFOLDERIDLIST**](cdm-getfolderidlist.md) | Recupera la lista de identificadores de elemento correspondiente a la carpeta actual que el cuadro de diálogo tiene abierto. Para obtener más información sobre las listas de identificadores de elementos, vea [Introducción al espacio de nombres del shell](/windows/desktop/shell/namespace-intro). |
| [**GETFOLDERPATH de CDM \_**](cdm-getfolderpath.md)     | Recupera la ruta de acceso de la carpeta o directorio actual para el cuadro de diálogo.                                                                                                                                                |
| [**CDM \_ GETSPEC**](cdm-getspec.md)                 | Recupera el nombre de archivo (sin incluir la ruta de acceso) del archivo seleccionado actualmente en el cuadro de diálogo.                                                                                                                       |
| [**CDM \_ HIDECONTROL**](cdm-hidecontrol.md)         | Oculta el control especificado.                                                                                                                                                                                             |
| [**CDM \_ SETCONTROLTEXT**](cdm-setcontroltext.md)   | Establece el texto en el control especificado.                                                                                                                                                                                  |
| [**CDM \_ SETDEFEXT**](cdm-setdefext.md)             | Establece la extensión de nombre de archivo predeterminada para el cuadro de diálogo.                                                                                                                                                                 |



 

## <a name="explorer-style-custom-templates"></a>Explorer-Style plantillas personalizadas

Para definir controles adicionales para un cuadro de diálogo para **abrir** o **Guardar como** estilo del explorador, use la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) para especificar una plantilla para un cuadro de diálogo secundario que contenga los controles adicionales. Si la plantilla de cuadro de diálogo secundaria es un recurso de una biblioteca de vínculos dinámicos o de aplicación, establezca la marca **OFN \_ ENABLETEMPLATE** en el miembro **Flags** y use los miembros **hInstance** y **lpTemplateName** de la estructura para identificar el nombre del módulo y del recurso. Si la plantilla ya está en memoria, establezca la marca **OFN \_ ENABLETEMPLATEHANDLE** y use el miembro **hInstance** para identificar el objeto de memoria que contiene la plantilla. Al proporcionar una plantilla de diálogo secundaria para un cuadro de diálogo de estilo Explorador, también debe establecer la marca **OFN \_ Explorer** ; de lo contrario, el sistema supone que está proporcionando una plantilla de reemplazo para un cuadro de diálogo de estilo antiguo. Normalmente, si proporciona controles adicionales, también debe proporcionar un procedimiento de [enlace de estilo del explorador](#explorer-style-hook-procedures) para procesar los mensajes para los nuevos controles.

Puede crear la plantilla del cuadro de diálogo secundario como lo haría con cualquier otra plantilla, salvo que debe especificar los estilos **WS \_ secundario** y **WS \_ CLIPSIBLINGS** y debe especificar los estilos de **\_ control** DS **\_ 3DLOOK** y DS. El sistema requiere el **estilo \_ secundario WS** porque la plantilla define un cuadro de diálogo secundario del cuadro de diálogo **abrir** o **Guardar como** predeterminado. El estilo **WS \_ CLIPSIBLINGS** garantiza que el cuadro de diálogo secundario no pinte los controles del cuadro de diálogo predeterminado. El **estilo \_ 3DLOOK de DS** garantiza que la apariencia de los controles del cuadro de diálogo secundario es coherente con los controles del cuadro de diálogo predeterminado. El estilo de **\_ control DS** se asegura de que el usuario puede usar la pestaña y otras teclas de navegación para desplazarse entre todos los controles, predeterminado o personalizado, en el cuadro de diálogo personalizado.

Para dejar espacio a los nuevos controles, el sistema expande el cuadro de diálogo predeterminado en el ancho y el alto del cuadro de diálogo personalizado. De forma predeterminada, todos los controles del cuadro de diálogo personalizado se colocan debajo de los controles del cuadro de diálogo predeterminado. Sin embargo, puede invalidar esta posición predeterminada si incluye un control de texto estático en la plantilla de cuadro de diálogo personalizado y le asigna el valor de identificador de control de **stc32**. (Este valor se define en el archivo de encabezado Dlgs. h). En este caso, el sistema utiliza el control como punto de referencia para determinar dónde colocar los nuevos controles. Todos los controles nuevos situados encima y a la izquierda del control **stc32** se colocan en la misma cantidad anterior y a la izquierda de los controles del cuadro de diálogo predeterminado. Los nuevos controles situados debajo y a la derecha del control **stc32** se colocan debajo y a la derecha de los controles predeterminados. En general, cada nuevo control se coloca para que tenga la misma posición con respecto a los controles predeterminados que tenía en el control **stc32** . Para dejar espacio a estos nuevos controles, el sistema agrega espacio a la izquierda, derecha, inferior y superior del cuadro de diálogo predeterminado según sea necesario.

El sistema requiere que el procedimiento de enlace procese todos los mensajes destinados al cuadro de diálogo personalizado y, por tanto, envía los mismos mensajes de ventana al procedimiento de enlace que a cualquier otro procedimiento de cuadro de diálogo. Por ejemplo, el procedimiento de enlace recibe mensajes de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) cuando el usuario hace clic en los controles de botón en el cuadro de diálogo personalizado. El procedimiento de enlace es responsable de inicializar estos controles y recuperar los valores de los controles cuando se cierra el cuadro de diálogo. Tenga en cuenta que cuando el procedimiento de enlace recibe el mensaje de [**\_ INITDIALOG de WM**](wm-initdialog.md) , el sistema aún no ha pasado los controles a sus posiciones finales.

El procedimiento de cuadro de diálogo predeterminado controla los mensajes de todos los controles del cuadro de diálogo predeterminado, pero el procedimiento de enlace recibe los mensajes de notificación para las acciones del usuario en estos controles, tal y como se describe en [procedimientos de enlace de estilo del explorador](#explorer-style-hook-procedures).

## <a name="explorer-style-control-identifiers"></a>Identificadores de control de Explorer-Style

El kit de desarrollo de software (SDK) de Windows proporciona la plantilla de cuadro de diálogo predeterminada para los cuadros de diálogo de estilo antiguo, pero no incluye la plantilla predeterminada para los cuadros de diálogo de estilo del explorador. Esto se debe a que los cuadros de diálogo del estilo del explorador permiten agregar sus propios controles pero no admiten la modificación de la plantilla para los controles estándar. Sin embargo, en algunos casos, puede que necesite conocer los identificadores de control que se usan en las plantillas predeterminadas. Por ejemplo, los mensajes [**CDM \_ HIDECONTROL**](cdm-hidecontrol.md) y [**CDM \_ SETCONTROLTEXT**](cdm-setcontroltext.md) requieren un identificador de control.

En la tabla siguiente se muestran los identificadores de los controles estándar en los cuadros de diálogo **abrir** y **Guardar como** del estilo del explorador. Los identificadores son constantes que se definen en Dlgs. h y Winuser. h.



| Identificador de control | Descripción del control                                                                                                                                                                                                                                                                        |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **chx1**           | Casilla de solo lectura                                                                                                                                                                                                                                                                    |
| **cmb1**           | Cuadro combinado desplegable que muestra la lista de filtros de tipo de archivo                                                                                                                                                                                                                            |
| **stc2**           | Etiqueta para el cuadro combinado **cmb1**                                                                                                                                                                                                                                                           |
| **cmb2**           | Cuadro combinado desplegable que muestra la unidad o carpeta actual, y que permite al usuario seleccionar una unidad o carpeta para abrir                                                                                                                                                                |
| **stc4**           | Etiqueta para el cuadro combinado **CMB2**                                                                                                                                                                                                                                                           |
| **cmb13**          | Cuadro combinado desplegable que muestra el nombre del archivo actual, permite al usuario escribir el nombre de un archivo que se va a abrir y seleccionar un archivo que se ha abierto o guardado recientemente. Se trata de aplicaciones compatibles con el explorador anteriores sin enlazar o plantilla de cuadro de diálogo. Comparar con **edt1**. |
| **edt1**           | Control de edición que muestra el nombre del archivo actual o permite al usuario escribir el nombre del archivo que se va a abrir. Comparar con **cmb13**.                                                                                                                                                  |
| **stc3**           | Etiqueta para el cuadro combinado **cmb13** y el control de edición edt1                                                                                                                                                                                                                                |
| **lst1**           | Cuadro de lista que muestra el contenido de la unidad o carpeta actual                                                                                                                                                                                                                         |
| **stc1**           | Etiqueta del cuadro de lista **lst1**                                                                                                                                                                                                                                                            |
| **IDOK**           | Botón de comando **Aceptar** (botón de comando)                                                                                                                                                                                                                                                    |
| **IDCANCEL**       | Botón **Cancelar** (botón de comando)                                                                                                                                                                                                                                                |
| **pshHelp**        | Botón de comando **ayuda** (botón de comando)                                                                                                                                                                                                                                                  |



 

## <a name="customizing-old-style-dialog-boxes"></a>Personalización de Old-Style cuadros de diálogo

Puede personalizar un cuadro de diálogo **abrir** o **Guardar como** de estilo antiguo si proporciona un procedimiento de enlace [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) que recibe mensajes o notificaciones destinados al procedimiento de cuadro de diálogo predeterminado. También puede proporcionar una plantilla personalizada que se usará en lugar de la plantilla predeterminada. Los procedimientos de enlace y las plantillas utilizados con los cuadros de diálogo de estilo antiguo son similares a los que se usan con los otros cuadros de diálogo comunes. Para obtener más información, vea [procedimientos de enlace para cuadros de diálogo comunes](customizing-common-dialog-boxes.md) y [plantillas personalizadas](customizing-common-dialog-boxes.md).

Para habilitar un procedimiento de enlace para un cuadro de diálogo **abrir** o **Guardar como** de estilo antiguo, use la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) al crear el cuadro de diálogo. Establezca la **marca OFN \_ ENABLEHOOK** en el miembro **Flags** y especifique la dirección de un procedimiento de enlace [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) en el miembro **lpfnHook** . El procedimiento de cuadro de diálogo envía un mensaje de [**WM \_ INITDIALOG**](wm-initdialog.md) al procedimiento de enlace con el parámetro *param* establecido en la dirección de la estructura **OPENFILENAME** usada para inicializar el cuadro de diálogo.

Puede usar la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) para especificar una plantilla personalizada para el cuadro de diálogo **abrir** o **Guardar como** que se usará en lugar de la plantilla predeterminada. Si la plantilla personalizada es un recurso de una aplicación o biblioteca de vínculos dinámicos, establezca la marca **OFN \_ ENABLETEMPLATE** en el miembro **Flags** y use los miembros **hInstance** y **lpTemplateName** de la estructura para identificar el módulo y el nombre del recurso. Si la plantilla personalizada ya está en la memoria, establezca la marca **OFN \_ ENABLETEMPLATEHANDLE** y use el miembro **hInstance** para identificar el objeto de memoria que contiene la plantilla. Cree la plantilla personalizada modificando la plantilla predeterminada especificada en el archivo FileOpen. Dlg. Los identificadores de control que se usan en las plantillas de cuadro de diálogo Buscar y reemplazar predeterminados se definen en el archivo Dlgs. h.

De forma predeterminada, las funciones [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) y [**getSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) muestran los cuadros de diálogo de estilo del explorador. Si desea mostrar un cuadro de diálogo de estilo anterior, debe proporcionar un procedimiento de enlace [**OFNHookProcOldStyle**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) y asegurarse de que la marca del **\_ Explorador OFN** no esté establecida en el miembro **Flags** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .

Si establece la marca **del \_ Explorador de OFN** , el sistema trata un procedimiento de enlace o una plantilla personalizada como una personalización de estilo del explorador. Para obtener información sobre cómo personalizar un cuadro de diálogo de estilo Explorador, consulte [plantillas personalizadas de estilo de explorador](#explorer-style-custom-templates).

## <a name="see-also"></a>Vea también

* [El archivo está en uso en el ejemplo](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse)
