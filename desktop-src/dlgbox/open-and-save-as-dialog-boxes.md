---
title: Abrir y guardar como cuadros de diálogo
description: El cuadro de diálogo Abrir permite al usuario especificar la unidad, el directorio y el nombre de un archivo o conjunto de archivos que se va a abrir.
ms.assetid: 5676ca9d-daca-40bf-8881-def2ff841c58
keywords:
- Biblioteca común de cuadros de diálogo
- cuadros de diálogo comunes
- Cuadro de diálogo Abrir
- Guardar como, cuadro de diálogo
- personalizar el cuadro de diálogo Abrir
- personalizar el cuadro de diálogo Guardar como
- cuadros de diálogo, Abrir
- cuadros de diálogo,Guardar como
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 57f1986f950650840ff3acfc9ee19191088e0dcbe099fc4cb8b21690fa0646c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606314"
---
# <a name="open-and-save-as-dialog-boxes"></a>Abrir y guardar como cuadros de diálogo

> [!NOTE]
> La [**función GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) se muestra en el [ejemplo File is in use](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse).

\[A partir Windows Vista,  los  cuadros de diálogo Abrir y Guardar como comunes se han reemplazado por el cuadro [de diálogo Elemento común](../shell/common-file-dialog.md). Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo común.\]

El **cuadro** de diálogo Abrir permite al usuario especificar la unidad, el directorio y el nombre de un archivo o conjunto de archivos que se va a abrir. Para crear y mostrar un **cuadro de** diálogo Abrir, inicialice una estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) y pase la estructura a la [**función GetOpenFileName.**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)

El **cuadro de diálogo** Guardar como permite al usuario especificar la unidad, el directorio y el nombre de un archivo que se guardará. Para crear y mostrar un cuadro de **diálogo** Guardar como, inicialice una estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) y pase la estructura a la [**función GetSaveFileName.**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)

Los cuadros de diálogo **Abrir y** Guardar **como** de estilo explorador proporcionan características de interfaz de usuario similares al Explorador Windows explorador. Sin embargo, el sistema sigue  siendo compatible con los cuadros de diálogo Abrir y Guardar **como** de estilo antiguo para las aplicaciones que deben ser coherentes con la interfaz de usuario de estilo anterior.

Además de la diferencia de apariencia, los cuadros de diálogo estilo Explorador y estilo antiguo difieren en su uso de plantillas personalizadas y procedimientos de enlace para personalizar los cuadros de diálogo. Sin embargo, los cuadros de diálogo Estilo explorador y Estilo antiguo tienen el mismo comportamiento para la mayoría de las operaciones básicas, como especificar un filtro de nombre de archivo, validar la entrada del usuario y obtener el nombre de archivo especificado por el usuario. Para obtener más información sobre los cuadros de diálogo estilo explorador y estilo antiguo, vea Abrir y guardar como personalización [de cuadro de diálogo](#open-and-save-as-dialog-box-customization).

En la ilustración siguiente se muestra un cuadro de diálogo Abrir **típico** de estilo explorador.

![cuadro de diálogo abrir archivo](images/opendialogboxxp.png)

En la ilustración siguiente se muestra un cuadro de diálogo Guardar **como** de estilo explorador típico.

![cuadro de diálogo guardar archivo](images/saveasdialogboxxp.png)

Si el usuario especifica un nombre  de archivo y hace clic en el botón Aceptar, [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) u [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) devuelve **TRUE.** El búfer al que apunta el **miembro lpstrFile** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) contiene la ruta de acceso completa y el nombre de archivo especificados por el usuario.

Si el usuario cancela el **cuadro** de diálogo Abrir o Guardar **como** o se produce un error, la función devuelve **FALSE.** Para determinar la causa del error, llame a la [**función CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar el valor de error extendido. Si el búfer **lpstrFile** es demasiado pequeño para recibir el nombre completo, **CommDlgExtendedError** devuelve **FNERR \_ BUFFERTOOSMALL** y los dos primeros bytes del búfer al que apunta el miembro **lpstrFile** se establecen en un valor entero que especifica el tamaño necesario para recibir el nombre completo.

En esta sección se tratan los temas siguientes.

-   [Nombres de archivo y directorios](#file-names-and-directories)
-   [Filtros](#filters)
-   [Validación de archivos y directorios](#file-and-directory-validation)
-   [Personalización del cuadro de diálogo Abrir y guardar como](#open-and-save-as-dialog-box-customization)
-   [Procedimientos de enlace de estilo explorador](#explorer-style-hook-procedures)
-   [Plantillas personalizadas de estilo explorador](#explorer-style-custom-templates)
-   [Identificadores de control de estilo explorador](#explorer-style-control-identifiers)
-   [Personalización de Old-Style diálogos](#customizing-old-style-dialog-boxes)

## <a name="file-names-and-directories"></a>Nombres de archivo y directorios

La información de esta sección se aplica a  los cuadros de diálogo Abrir y Guardar **como** de estilo anterior.

Antes de llamar a las funciones [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) o [**GetSaveFileName,**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) el miembro **lpstrFile** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) debe apuntar al búfer para recibir el nombre de archivo. El **miembro nMaxFile** debe especificar el tamaño, en caracteres, del **búfer lpstrFile.** Para una función ANSI, este es el número de bytes, pero para una función Unicode es el número de caracteres.

Si el usuario especifica un nombre  de archivo y hace clic en el botón Aceptar, el cuadro de diálogo copia la unidad, el directorio y el nombre de archivo seleccionados en el búfer **lpstrFile.** La función también establece los miembros **nFileOffset** y **nFileExtension** en los desplazamientos, en caracteres, desde el inicio del búfer hasta el nombre de archivo y la extensión de nombre de archivo, respectivamente.

Para recuperar solo el nombre de archivo y la extensión, establezca el miembro **lpstrFileTitle** para que apunte a un búfer y establezca el **miembro nMaxFileTitle** en el tamaño, en caracteres, del búfer. Como alternativa, puede pasar el búfer **lpstrFile** en una llamada a la función [**GetFileTitle**](/windows/desktop/api/Commdlg/nf-commdlg-getfiletitlea) para obtener el nombre para mostrar del archivo seleccionado. Sin embargo, tenga en cuenta que el nombre de archivo que **GetFileTitle** devuelve incluye una extensión solo si esa es la preferencia del usuario para mostrar los nombres de archivo.

El cuadro de diálogo usa el directorio actual para el proceso de llamada como directorio inicial desde el que se muestran los archivos y directorios. Use las [**funciones GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) [**y SetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) para obtener y cambiar el directorio actual de un proceso. Para especificar un directorio inicial diferente sin cambiar el directorio actual, use el **miembro lpstrInitialDir** para especificar el nombre de un directorio. El cuadro de diálogo cambia automáticamente el directorio actual cuando el usuario selecciona otra unidad o directorio. Para evitar que el cuadro de diálogo cambie el directorio actual, establezca la **marca OFN \_ NOCHANGEDIR.** Esta marca no impide que el usuario cambie los directorios para buscar un archivo.

Para especificar una extensión de nombre de archivo predeterminada, use el **miembro lpstrDefExt.** Si el usuario especifica un nombre de archivo que no tiene una extensión, el cuadro de diálogo agrega la extensión predeterminada. Si especifica una extensión predeterminada y el usuario especifica un nombre de archivo con una extensión diferente, el cuadro de diálogo establece la marca **OFN \_ EXTENSIONDIFFERENT.**

Para permitir que el usuario seleccione más de un archivo de un directorio, establezca la **marca \_ ALLOWMULTISELECT de OFN.** Para la compatibilidad con aplicaciones anteriores, el cuadro de diálogo de selección múltiple predeterminada usa la interfaz de usuario de estilo anterior. Para mostrar un cuadro de diálogo de selección múltiple de estilo explorador, también debe establecer la **marca OFN \_ EXPLORER.**

Si el usuario selecciona más de un archivo, el búfer al que apunta el miembro **lpstrFile** devuelve la ruta de acceso al directorio actual seguido de los nombres de archivo de los archivos seleccionados. El **miembro nFileOffset** es el desplazamiento al primer nombre de archivo y no se usa el miembro **nFileExtension.** En la tabla siguiente se describe la diferencia entre los cuadros de diálogo de estilo explorador y de estilo antiguo al devolver varios nombres de archivo.



| Estilo de cuadro de diálogo            | Descripción                                                                                                                                                                                                               |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cuadros de diálogo de estilo explorador | Las cadenas de nombre de archivo y directorio están **separadas por NULL,** con un carácter **NULL** adicional después del último nombre de archivo. Este formato permite que los cuadros de diálogo de estilo explorador devuelvan nombres de archivo largos que incluyen espacios. |
| Cuadros de diálogo de estilo antiguo      | Las cadenas de nombre de archivo y directorio están separadas por espacios. Para los nombres de archivo con espacios, la función usa nombres de archivo cortos.                                                                                              |



 

Puede usar la función [**FindFirstFile para**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) convertir nombres de archivo largos y cortos.

Si especifica **OFN \_ ALLOWMULTISELECT** y el usuario selecciona solo un archivo, la cadena **lpstrFile** no tiene un separador entre la ruta de acceso y el nombre de archivo.

## <a name="filters"></a>Filtros

La información de esta sección se aplica a los cuadros de diálogo Estilo explorador y Estilo **antiguo** Abrir **y** Guardar como.

Puede proporcionar filtros de nombre de archivo para ayudar al usuario a limitar los nombres de archivo que muestra el cuadro de diálogo. Un filtro de nombre de archivo consta de un par de cadenas terminadas en NULL, una descripción y un patrón, una concatenada a la otra. El cuadro de diálogo muestra la descripción para permitir que el usuario elija el filtro que se va a usar; y usa el patrón para seleccionar los archivos que se mostrarán.

Para especificar los filtros, establezca el miembro **lpstrFilter** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) para que apunte a un búfer que contenga una matriz de pares de cadenas de filtro. La última cadena de la matriz debe ir seguida de un carácter null adicional.

Una cadena de patrón puede ser una combinación de caracteres de nombre de archivo válidos y el asterisco ( \* ). El asterisco es un carácter comodín que representa cualquier combinación de caracteres de nombre de archivo válidos. El cuadro de diálogo muestra solo los archivos que coinciden con el patrón. Para especificar varios patrones para la misma descripción, debe usar un punto y coma (;) para separar los patrones. Tenga en cuenta que los caracteres de espacio de la cadena de patrón pueden producir resultados inesperados.

El fragmento de código siguiente especifica dos filtros. El filtro con la descripción "Origen" tiene dos patrones. Si el usuario selecciona este filtro, el cuadro de diálogo muestra solo los archivos que tienen . C y . Extensiones CXX. Tenga en cuenta que, en el lenguaje de programación C, una cadena entre comillas dobles termina en null.


```
OPENFILENAME ofn;       // common dialog box structure

ofn.lpstrFilter = "Source\0*.C;*.CXX\0All\0*.*\0"
ofn.nFilterIndex = 1;
```



El **miembro nFilterIndex** de la [**estructura OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) especifica un índice que indica qué filtro usa inicialmente el cuadro de diálogo. El primer filtro del búfer tiene el índice 1, el segundo 2, y así sucesivamente. Si el usuario cambia el filtro mientras usa el cuadro de diálogo, el **miembro nFilterIndex** se establece en el índice del filtro seleccionado en la devolución.

Puede crear un filtro personalizado estableciendo el miembro **lpstrCustomFilter** en la dirección de un búfer que contiene un único filtro y estableciendo el miembro **nMaxCustFilter** en el tamaño del búfer, en caracteres o bytes. El cuadro de diálogo siempre coloca el filtro personalizado al principio de la lista de filtros y, al devolverlo, siempre actualiza la parte del patrón del filtro con el patrón del filtro seleccionado por el usuario.

En el caso de los cuadros de diálogo de estilo explorador, la extensión predeterminada puede cambiar si el usuario selecciona otro filtro. Si el usuario selecciona un filtro cuyo primer patrón tiene el formato \* .*xxx* (es decir, la extensión no incluye un carácter comodín), el cuadro de diálogo usa *xxx* como extensión predeterminada. Esto solo se produce si especificó una extensión predeterminada en el **miembro lpstrDefExt** de la [**estructura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) Por ejemplo, si el usuario selecciona "Source \\ 0 \* . C; \* . Filtro CXX \\ 0", la extensión predeterminada cambia a "C". Sin embargo, si ha definido el filtro como "Origen \\ 0 \* . C \* \\ 0", la extensión predeterminada no cambiaría porque la extensión incluye un carácter comodín.

El [**CDN de notificación \_ INCLUDEITEM**](cdn-includeitem.md) proporciona otra manera de filtrar los nombres que muestra el cuadro de diálogo. Para usar este mensaje, proporcione un procedimiento de enlace [**OFNHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) y especifique la marca **OFN \_ ENABLEINCLUDENOTIFY** en la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) al crear el cuadro de diálogo. Cada vez que el usuario abre una carpeta, el cuadro de diálogo envía una CDN **\_ INCLUDEITEM** al procedimiento de enlace para cada elemento de la carpeta recién abierta. El valor devuelto del procedimiento de enlace indica si el cuadro de diálogo debe mostrar el elemento en la lista de elementos de la carpeta.

## <a name="file-and-directory-validation"></a>Validación de archivos y directorios

Excepto como se indicó, la información de esta sección  se aplica tanto a los cuadros de diálogo De estilo explorador como De apertura y Guardar **como** de estilo anterior.

El cuadro de diálogo valida automáticamente los nombres de archivo especificados por el usuario para asegurarse de que los nombres contienen solo caracteres válidos. Para invalidar la validación de caracteres de nombre de archivo, establezca la **marca OFN \_ NOVALIDATE.**

Para forzar que el cuadro de diálogo compruebe que el usuario especificó el nombre de un archivo existente, establezca la marca **\_ OFN FILEMUSTEXIST.** Para forzar la comprobación de que existe la ruta de acceso especificada, establezca la **marca OFN \_ PATHMUSTEXIST.** Si establece la marca **OFN \_ CREATEPROMPT,** el cuadro de diálogo solicita permiso al usuario para crear un archivo inexistente. Si se establece esta marca y el usuario elige crear un nuevo archivo, se cierra el cuadro de diálogo y la función devuelve el nombre especificado. De lo contrario, el cuadro de diálogo permanece abierto.

Al usar el **cuadro de diálogo** Guardar como , puede dirigir el cuadro de diálogo para solicitar al usuario permiso para sobrescribir un archivo existente estableciendo la marca **OFN \_ OVERWRITEPROMPT.**

De forma predeterminada, el cuadro de diálogo crea un archivo de prueba de longitud cero para determinar si se puede crear un nuevo archivo en el directorio seleccionado. Para evitar la creación de este archivo de prueba, establezca la **marca OFN \_ NOTESTFILECREATE.**

Si habilita un procedimiento de enlace, el cuadro de diálogo notifica al procedimiento de enlace cuando se produce una infracción de uso compartido de red para el nombre de archivo especificado por el usuario. Si establece la marca **OFN \_ EXPLORER,** el cuadro de diálogo envía el CDN [**\_ SHAREVIOLATION**](cdn-shareviolation.md) al procedimiento de enlace. Si no establece **OFN \_ EXPLORER**, el cuadro de diálogo envía el mensaje [**registrado de SHAREVISTRING**](sharevistring.md) al procedimiento de enlace. Para evitar que el cuadro de diálogo envíe notificaciones de infracciones de uso compartido, establezca la **marca OFN \_ SHAREAWARE.**

Si el usuario selecciona la casilla de solo lectura, el cuadro de diálogo establece la marca **OFN \_ READONLY** en la devolución. Para ocultar la **casilla Abrir como solo** lectura, establezca la marca **OFN \_ HIDEREADONLY.** Para evitar que el cuadro de diálogo devuelva nombres de archivos existentes que tienen el atributo de solo lectura, establezca la marca **OFN \_ NOREADONLYRETURN.**

Para evitar que el cuadro de diálogo desreferencia los archivos de vínculo, establezca el **valor DE OFN \_ NODEREFERENCELINKS.** En este caso, el cuadro de diálogo devuelve el nombre del archivo de vínculo en lugar del nombre del archivo al que hace referencia el archivo de vínculo.

## <a name="open-and-save-as-dialog-box-customization"></a>Personalización del cuadro de diálogo Abrir y guardar como

Puede personalizar un cuadro **de diálogo** Abrir o Guardar **como** proporcionando un procedimiento de enlace, una plantilla personalizada o ambos. Sin embargo, las versiones de estilo explorador y de estilo antiguo de los cuadros de diálogo difieren en su uso de plantillas personalizadas y procedimientos de enlace.

Para obtener información sobre cómo personalizar un cuadro de diálogo de estilo explorador, vea [Explorer-Style Hook Procedures](#explorer-style-hook-procedures), [Explorer-Style Custom Templates](#explorer-style-custom-templates)e [Explorer-Style Control Identifiers](#explorer-style-control-identifiers). Para obtener información sobre cómo personalizar un cuadro de diálogo de estilo antiguo, vea [Personalizar Old-Style cuadros de diálogo](#customizing-old-style-dialog-boxes).

En la tabla siguiente se resumen las diferencias entre los dos estilos.



| Personalización                  | Descripción                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Procedimiento de enlace de estilo explorador  | El procedimiento de enlace recibe mensajes de notificación enviados desde el cuadro de diálogo común y mensajes para los controles adicionales definidos mediante la especificación de una plantilla de diálogo secundaria. El procedimiento de enlace no recibe mensajes para los controles estándar del cuadro de diálogo predeterminado. |
| Plantilla personalizada de estilo explorador | El sistema usa la plantilla personalizada para crear un cuadro de diálogo secundario. La plantilla puede definir controles adicionales y puede especificar la ubicación del clúster de controles estándar. La plantilla personalizada no reemplaza la plantilla predeterminada.                                          |
| Procedimiento de enlace de estilo antiguo       | El procedimiento de enlace recibe todos los mensajes enviados al cuadro de diálogo, incluidos los mensajes para los controles estándar y los controles personalizados. El procedimiento de enlace también recibe mensajes registrados enviados desde el cuadro de diálogo común.                                                         |
| Plantilla personalizada de estilo antiguo      | La plantilla personalizada reemplaza a la plantilla predeterminada. Cree la plantilla personalizada modificando la plantilla predeterminada especificada en el archivo Fileopen.dlg.                                                                                                                                  |



 

El título predeterminado de los cuadros de diálogo de estilo explorador y de estilo antiguo es **"Abrir"** o **"Guardar como".** Para cambiar el título, especifique el nuevo título en el **miembro lpstrTitle** de la [**estructura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)

El subárbol del Registro **HKEY \_ CURRENT \_ USER** de un usuario  puede contener valores que personalizan el contenido de los cuadros de diálogo Abrir y Guardar **como** de estilo explorador. Estas entradas del Registro solo afectan a los cuadros de diálogo que se muestran para el usuario asociado al subárbol del Registro.

Para ocultar las características  de los cuadros de diálogo Abrir y Guardar **como** de estilo Explorador, un administrador puede establecer los valores de la tabla siguiente en esta subclave:

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
| **NoPlacesBar**  | 1     | Oculta la barra de lugares.                    |
| **NoFileMRU**    | 1     | Oculta la lista Usados más recientemente (MRU). |
| **NoBackButton** | 1     | Oculta el **botón** Atrás.               |



 

El contenido de la **barra Lugares** viene determinado por el contenido de la subclave siguiente:

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

Actualmente, solo puede haber cinco entradas en esta clave y el índice de valor/nombre es de base cero. Los nombres de las entradas deben ser Place0, Place1, Place2, Place3 y Place4. Los valores de las entradas pueden ser **REG \_ DWORD,** **REG \_ SZ** o **REG EXPAND \_ \_ SZ** que identifican las ubicaciones que se incluirán en la barra de lugares.



| Tipo de valor                         | Significado                                                                                                   |
|------------------------------------|-----------------------------------------------------------------------------------------------------------|
| **REG \_ DWORD**                     | Valor CSIDL que identifica una carpeta. Para obtener una lista de valores CSIDL, vea [**Valores CSIDL**](../shell/csidl.md). |
| **REG \_ SZ** o **REG EXPAND \_ \_ SZ** | Cadena terminada en NULL que especifica una ruta de acceso válida.                                                     |



 

## <a name="explorer-style-hook-procedures"></a>Explorer-Style de enlace de datos

Puede personalizar un cuadro  de diálogo Abrir o Guardar **como** de estilo explorador proporcionando un procedimiento de enlace, una plantilla personalizada o ambos. Si proporciona un procedimiento de enlace para un cuadro de diálogo de estilo Explorador, el sistema crea un cuadro de diálogo que es un elemento secundario del cuadro de diálogo predeterminado. El procedimiento de enlace actúa como procedimiento de diálogo para el cuadro de diálogo secundario. Este cuadro de diálogo secundario se basa en la plantilla personalizada o en una plantilla predeterminada si no se proporciona ninguna. Para obtener más información, vea [Plantillas personalizadas de estilo explorador.](#explorer-style-custom-templates)

Para habilitar un procedimiento de  enlace  para un cuadro de diálogo Abrir o Guardar como de estilo explorador, use la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) al crear el cuadro de diálogo. Establezca las **marcas OFN \_ ENABLEHOOK** y **OFN \_ EXPLORER** en el miembro **Flags** y especifique la dirección de un procedimiento de enlace [**OFNHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) en el miembro **lpfnHook.** Si proporciona un procedimiento de enlace y omite la marca **OFN \_ EXPLORER,** debe usar un procedimiento de enlace [**OFNHookProcOldStyle**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) y se obtiene la interfaz de usuario de estilo anterior. Para obtener más información, vea [Personalizar Old-Style cuadros de diálogo](#customizing-old-style-dialog-boxes).

Un procedimiento de enlace de estilo explorador recibe una variedad de mensajes mientras el cuadro de diálogo está abierto. que incluyen la siguiente información:

-   El [**mensaje \_ WM INITDIALOG**](wm-initdialog.md) y otros mensajes de cuadro de diálogo estándar, como el mensaje de color del control [**WM \_ CTLCOLORDLG.**](wm-ctlcolordlg.md)
-   Conjunto de mensajes de [**\_ notificación WM NOTIFY**](../controls/wm-notify.md) que indican las acciones realizadas por el usuario u otros eventos de cuadro de diálogo.
-   Mensajes para los controles adicionales definidos mediante la especificación de una plantilla de diálogo secundaria.

Además, hay un conjunto de mensajes que puede enviar a un cuadro de diálogo de estilo Explorador para obtener información o para controlar el comportamiento y la apariencia del cuadro de diálogo.

Si proporciona un procedimiento de enlace para un cuadro de diálogo de estilo Explorador, el procedimiento de cuadro de diálogo predeterminado crea un cuadro de diálogo secundario cuando el procedimiento de diálogo predeterminado está procesando su [**mensaje \_ WM INITDIALOG.**](wm-initdialog.md) El procedimiento de enlace actúa como procedimiento de diálogo para el cuadro de diálogo secundario. En este momento, el procedimiento de enlace recibe su propio mensaje **\_ WM INITDIALOG** con el parámetro *lParam* establecido en la dirección de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) utilizada para inicializar el cuadro de diálogo. Una vez que el diálogo secundario termina de procesar su propio mensaje **\_ INITDIALOG** de WM, el procedimiento de diálogo predeterminado mueve los controles estándar, si es necesario, para dar espacio a los controles adicionales del cuadro de diálogo secundario. A continuación, el procedimiento de diálogo predeterminado CDN mensaje de notificación [**\_ INITDONE**](cdn-initdone.md) al procedimiento de enlace.

El procedimiento de enlace recibe [**mensajes de notificación WM \_ NOTIFY**](../controls/wm-notify.md) que indican las acciones realizadas por el usuario en el cuadro de diálogo. Puede usar algunos de estos mensajes para controlar el comportamiento del cuadro de diálogo. Por ejemplo, el procedimiento de enlace recibe el [**CDN \_ FILEOK**](cdn-fileok.md) cuando el usuario elige un nombre de archivo y hace clic en el **botón** Aceptar. En respuesta a este mensaje, el procedimiento de enlace puede usar la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para rechazar el nombre seleccionado y forzar que el cuadro de diálogo permanezca abierto.

El *parámetro lParam* para cada [**mensaje WM \_ NOTIFY**](../controls/wm-notify.md) es un puntero a una estructura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) o [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) que define la acción. El **miembro** de código del encabezado de esta estructura contiene uno de los siguientes mensajes de notificación.



| Mensaje                                           | Significado                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CDN FILEOK**](cdn-fileok.md)                 | El usuario hizo clic en **el botón** Aceptar; el cuadro de diálogo está a punto de cerrarse.                                                                                                                                                                                                                          |
| [**\_CDN FOLDERCHANGE**](cdn-folderchange.md)     | El usuario abrió una nueva carpeta o directorio.                                                                                                                                                                                                                                                     |
| [**\_CDN Ayuda**](cdn-help.md)                     | El usuario hizo clic en el **botón Ayuda.**                                                                                                                                                                                                                                                          |
| [**\_CDN INCLUDEITEM**](cdn-includeitem.md)       | Determina si se debe mostrar un elemento. Cuando el usuario abre una nueva carpeta o directorio, el sistema envía esta notificación para cada elemento de la carpeta o directorio. El sistema envía esta notificación solo si se ha establecido la marca **\_ ENABLEINCLUDENOTIFY de OFN.**                          |
| [**\_CDN INITDONE**](cdn-initdone.md)             | El sistema ha terminado de inicializar el cuadro de diálogo y el cuadro de diálogo ha terminado de procesar el [**mensaje \_ WM INITDIALOG.**](wm-initdialog.md) Además, el sistema ha terminado de organizar los controles en el cuadro de diálogo común para hacer espacio para los controles del cuadro de diálogo secundario (si los hay). |
| [**\_CDN SELCHANGE**](cdn-selchange.md)           | El usuario seleccionó un nuevo archivo o carpeta de la lista de archivos.                                                                                                                                                                                                                                     |
| [**\_CDN SHAREVIOLATION**](cdn-shareviolation.md) | El cuadro de diálogo común encontró una infracción de uso compartido en el archivo que se va a devolver.                                                                                                                                                                                                        |
| [**\_CDN TYPECHANGE**](cdn-typechange.md)         | El usuario seleccionó un nuevo tipo de archivo de la lista de tipos de archivo.                                                                                                                                                                                                                                 |



 

Estos [**mensajes WM \_ NOTIFY**](../controls/wm-notify.md) reemplazan a los mensajes [**registrados FILEOKSTRING,**](fileokstring.md) [**LBSELCHSTRING,**](lbselchstring.md) [**SHAREVISTRING**](sharevistring.md)y [**HELPMSGSTRING**](helpmsgstring.md) usados por versiones anteriores de los cuadros de diálogo Abrir y Guardar como.   Sin embargo, el procedimiento de enlace también recibe el mensaje reemplazado después del mensaje **WM \_ NOTIFY** si el procesamiento DE **WM \_ NOTIFY** no usa [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para establecer un valor **\_ MSGRESULT de DWL** distinto de cero.

Para recuperar información sobre el estado del cuadro de diálogo o para controlar el comportamiento y la apariencia del cuadro de diálogo, el procedimiento de enlace puede enviar los siguientes mensajes al cuadro de diálogo.



| Mensaje                                             | Significado                                                                                                                                                                                                                  |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GETFILEPATH de CDM \_**](cdm-getfilepath.md)         | Recupera la ruta de acceso y el nombre de archivo del archivo seleccionado.                                                                                                                                                                   |
| [**GETFOLDERIDLIST de CDM \_**](cdm-getfolderidlist.md) | Recupera la lista de identificadores de elemento correspondiente a la carpeta actual que el cuadro de diálogo tiene abierta. Para obtener más información sobre las listas de identificadores de elementos, vea [Introducción al espacio de nombres del shell](/windows/desktop/shell/namespace-intro). |
| [**GETFOLDERPATH de CDM \_**](cdm-getfolderpath.md)     | Recupera la ruta de acceso de la carpeta o directorio actual del cuadro de diálogo.                                                                                                                                                |
| [**GETSPEC de CDM \_**](cdm-getspec.md)                 | Recupera el nombre de archivo (sin incluir la ruta de acceso) del archivo seleccionado actualmente en el cuadro de diálogo.                                                                                                                       |
| [**HIDECONTROL de CDM \_**](cdm-hidecontrol.md)         | Oculta el control especificado.                                                                                                                                                                                             |
| [**SETCONTROLTEXT de CDM \_**](cdm-setcontroltext.md)   | Establece el texto del control especificado.                                                                                                                                                                                  |
| [**CDM \_ SETDEFEXT**](cdm-setdefext.md)             | Establece la extensión de nombre de archivo predeterminada para el cuadro de diálogo.                                                                                                                                                                 |



 

## <a name="explorer-style-custom-templates"></a>Explorer-Style personalizadas

Para definir controles adicionales  para  un cuadro de diálogo Abrir o Guardar como de estilo explorador, use la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) para especificar una plantilla para un cuadro de diálogo secundario que contenga los controles adicionales. Si la plantilla de diálogo secundaria es un recurso de una aplicación o biblioteca de vínculos dinámicos, establezca la marca **OFN \_ ENABLETEMPLATE** en el miembro **Flags** y use los miembros **hInstance** y **lpTemplateName** de la estructura para identificar el módulo y el nombre del recurso. Si la plantilla ya está en memoria, establezca la marca **\_ ENABLETEMPLATEHANDLE** de OFN y use el **miembro hInstance** para identificar el objeto de memoria que contiene la plantilla. Al proporcionar una plantilla de diálogo secundaria para un cuadro de diálogo de estilo Explorador, también debe establecer la marca **OFN \_ EXPLORER;** de lo contrario, el sistema da por supuesto que está proporcionando una plantilla de reemplazo para un cuadro de diálogo de estilo antiguo. Normalmente, si proporciona controles adicionales, también debe proporcionar un procedimiento de enlace de estilo [explorador](#explorer-style-hook-procedures) para procesar los mensajes de los nuevos controles.

Puede crear la plantilla de cuadro de diálogo secundaria como hace con cualquier otra plantilla, excepto que debe especificar los estilos **WS \_ CHILD** y **WS \_ CLIPSIBLINGS** y debe especificar los estilos **DS \_ 3DLOOK** y **DS \_ CONTROL.** El sistema requiere el **estilo WS \_ CHILD** porque la plantilla define un cuadro de diálogo secundario del **cuadro** de diálogo Predeterminado Abrir o **Guardar** como. El **estilo WS \_ CLIPSIBLINGS** garantiza que el cuadro de diálogo secundario no pinta ninguno de los controles del cuadro de diálogo predeterminado. El **estilo DS \_ 3DLOOK** se asegura de que la apariencia de los controles en el cuadro de diálogo secundario sea coherente con los controles del cuadro de diálogo predeterminado. El **estilo \_ DS CONTROL** se asegura de que el usuario puede usar la tecla TAB y otras teclas de navegación para moverse entre todos los controles, predeterminados o personalizados, en el cuadro de diálogo personalizado.

Para dar espacio a los nuevos controles, el sistema expande el cuadro de diálogo predeterminado por el ancho y alto del cuadro de diálogo personalizado. De forma predeterminada, todos los controles del cuadro de diálogo personalizado se sitúan debajo de los controles del cuadro de diálogo predeterminado. Sin embargo, puede invalidar este posicionamiento predeterminado si incluye un control de texto estático en la plantilla de cuadro de diálogo personalizado y le asigna el valor del identificador de control **de stc32**. (Este valor se define en el archivo de encabezado Dlgs.h). En este caso, el sistema usa el control como punto de referencia para determinar dónde colocar los nuevos controles. Todos los controles nuevos situados encima y a la izquierda del control **stc32** se sitúan en la misma cantidad por encima y a la izquierda de los controles en el cuadro de diálogo predeterminado. Los nuevos controles situados a continuación y a la derecha del control **stc32** se sitúan a continuación y a la derecha de los controles predeterminados. En general, cada nuevo control se coloca para que tenga la misma posición con respecto a los controles predeterminados que tenía con el control **stc32.** Para dejar espacio para estos nuevos controles, el sistema agrega espacio a la parte izquierda, derecha, inferior y superior del cuadro de diálogo predeterminado según sea necesario.

El sistema requiere que el procedimiento de enlace procese todos los mensajes destinados al cuadro de diálogo personalizado y, por tanto, envía los mismos mensajes de ventana al procedimiento de enlace que a cualquier otro procedimiento de cuadro de diálogo. Por ejemplo, el procedimiento de enlace recibe mensajes [**\_ WM COMMAND**](/windows/desktop/menurc/wm-command) cuando el usuario hace clic en los controles de botón en el cuadro de diálogo personalizado. El procedimiento de enlace es responsable de inicializar estos controles y recuperar valores de los controles cuando se cierra el cuadro de diálogo. Tenga en cuenta que cuando el procedimiento de enlace recibe el [**mensaje \_ WM INITDIALOG,**](wm-initdialog.md) el sistema aún no ha movido los controles a sus posiciones finales.

El procedimiento de cuadro de diálogo predeterminado controla los mensajes de todos los controles del cuadro de diálogo predeterminado, pero el procedimiento de enlace recibe los mensajes de notificación de las acciones del usuario en estos controles, como se describe en Procedimientos de enlace de estilo [explorador](#explorer-style-hook-procedures).

## <a name="explorer-style-control-identifiers"></a>Explorer-Style identificadores de control

El Kit de desarrollo de software (SDK) de Windows proporciona la plantilla de cuadro de diálogo predeterminada para los cuadros de diálogo de estilo anterior, pero no incluye la plantilla predeterminada para los cuadros de diálogo de estilo explorador. Esto se debe a que los cuadros de diálogo de estilo explorador permiten agregar sus propios controles, pero no admiten la modificación de la plantilla para los controles estándar. Sin embargo, en algunos casos, puede que necesite conocer los identificadores de control usados en las plantillas predeterminadas. Por ejemplo, los [**mensajes \_ HIDECONTROL y**](cdm-hidecontrol.md) [**\_ SETCONTROLTEXT de CDM**](cdm-setcontroltext.md) requieren un identificador de control.

En la tabla siguiente se muestran los identificadores  de los controles estándar en los cuadros de diálogo Abrir y Guardar **como** de estilo explorador. Los identificadores son constantes definidas en Dlgs.h y Winuser.h.



| Identificador de control | Descripción del control                                                                                                                                                                                                                                                                        |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **chx1**           | Casilla de verificación de solo lectura                                                                                                                                                                                                                                                                    |
| **cmb1**           | Cuadro combinado desplegable que muestra la lista de filtros de tipo de archivo                                                                                                                                                                                                                            |
| **stc2**           | Etiqueta del **cuadro combinado cmb1**                                                                                                                                                                                                                                                           |
| **cmb2**           | Cuadro combinado desplegable que muestra la unidad o carpeta actual y que permite al usuario seleccionar una unidad o carpeta para abrirla.                                                                                                                                                                |
| **stc4**           | Etiqueta del **cuadro combinado cmb2**                                                                                                                                                                                                                                                           |
| **cmb13**          | Cuadro combinado desplegable que muestra el nombre del archivo actual, permite al usuario escribir el nombre de un archivo para abrirlo y seleccionar un archivo que se ha abierto o guardado recientemente. Esto es para aplicaciones anteriores compatibles con el Explorador sin plantilla de enlace o diálogo. Compare con **edt1**. |
| **edt1**           | Control de edición que muestra el nombre del archivo actual o permite al usuario escribir el nombre del archivo que se abre. Compare con **cmb13**.                                                                                                                                                  |
| **stc3**           | Etiqueta del **cuadro combinado cmb13** y el control de edición edt1                                                                                                                                                                                                                                |
| **lst1**           | Cuadro de lista que muestra el contenido de la unidad o carpeta actuales                                                                                                                                                                                                                         |
| **stc1**           | Etiqueta del **cuadro de lista lst1**                                                                                                                                                                                                                                                            |
| **IDOK**           | El **botón de** comando Aceptar (botón de inserción)                                                                                                                                                                                                                                                    |
| **IDCANCEL**       | Botón **Cancelar** comando (botón de inserción)                                                                                                                                                                                                                                                |
| **pshHelp**        | Botón **de** comando Ayuda (botón de inserción)                                                                                                                                                                                                                                                  |



 

## <a name="customizing-old-style-dialog-boxes"></a>Personalización de Old-Style diálogos

Puede personalizar un cuadro  de  diálogo Abrir o Guardar como de estilo anterior proporcionando un procedimiento de enlace [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) que recibe mensajes o notificaciones diseñados para el procedimiento de cuadro de diálogo predeterminado. También puede proporcionar una plantilla personalizada para usarla en lugar de la plantilla predeterminada. Los procedimientos de enlace y las plantillas que se usan con los cuadros de diálogo de estilo antiguo son similares a los usados con los otros cuadros de diálogo comunes. Para obtener más información, vea [Procedimientos de enlace para cuadros de diálogo comunes y](customizing-common-dialog-boxes.md) plantillas [personalizadas.](customizing-common-dialog-boxes.md)

Para habilitar un procedimiento de  enlace  para un cuadro de diálogo Abrir o Guardar como de estilo antiguo, use la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) al crear el cuadro de diálogo. Establezca la **marca OFN \_ ENABLEHOOK** en el miembro **Flags** y especifique la dirección de un procedimiento de enlace [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) en el **miembro lpfnHook.** El procedimiento de cuadro de diálogo envía un mensaje [**\_ WM INITDIALOG**](wm-initdialog.md) al procedimiento de enlace con el parámetro *Param* establecido en la dirección de la estructura **OPENFILENAME** utilizada para inicializar el cuadro de diálogo.

Puede usar la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) para especificar  una  plantilla personalizada para el cuadro de diálogo Abrir o Guardar como que se va a usar en lugar de la plantilla predeterminada. Si la plantilla personalizada es un recurso de una aplicación o biblioteca de vínculos **dinámicos,** establezca la marca **\_ ENABLETEMPLATE** de OFN en el miembro Flags y use los miembros **hInstance** y **lpTemplateName** de la estructura para identificar el módulo y el nombre del recurso. Si la plantilla personalizada ya está en memoria, establezca la marca **OFN \_ ENABLETEMPLATEHANDLE** y use el **miembro hInstance** para identificar el objeto de memoria que contiene la plantilla. Cree la plantilla personalizada modificando la plantilla predeterminada especificada en el archivo Fileopen.dlg. Los identificadores de control usados en las plantillas de diálogo Buscar y Reemplazar predeterminadas se definen en el archivo Dlgs.h.

De forma predeterminada, [**las funciones GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) y [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) muestran los cuadros de diálogo estilo Explorador. Si desea mostrar un cuadro de diálogo de estilo antiguo, debe proporcionar un procedimiento de enlace [**OFNHookProcOldStyle**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) y asegurarse de que la marca **OFN \_ EXPLORER** no está establecida en el miembro **Flags** de la estructura [**OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)

Si establece la marca **OFN \_ EXPLORER,** el sistema trata un procedimiento de enlace o una plantilla personalizada como una personalización de estilo Explorador. Para obtener información sobre cómo personalizar un cuadro de diálogo de estilo explorador, vea [Plantillas personalizadas de estilo explorador](#explorer-style-custom-templates).

## <a name="see-also"></a>Vea también

* [Ejemplo de archivo en uso](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse)