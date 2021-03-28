---
description: En esta sección se describen las funciones del shell de Windows.
title: Funciones de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f4d6c0c4-8db3-4721-80f5-2a73bb57cd99
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c8e31bdaac8ec581504326c17d5d37012dd019d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997725"
---
# <a name="shell-functions"></a>Funciones de Shell

\[Esta función ya no se implementa.\]

En esta sección se describen las funciones del shell de Windows.

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="intsafe-h-functions-bumper.md">Intsafe. h (funciones)</a><br/></td>

</tr>
<tr class="even">
<td><a href="library-functions-bumper.md">Funciones de la biblioteca</a><br/></td>

</tr>
<tr class="odd">
<td><a href="path-functions.md">Funciones de ruta de acceso</a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>AssocCreateForClasses</strong></a><br/></td>
<td>Recupera un objeto que implementa una interfaz <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-assocgetdetailsofpropkey"><strong>AssocGetDetailsOfPropKey</strong></a><br/></td>
<td>Recupera el valor de una clave de propiedad determinada mediante la información de Asociación de archivo proporcionada por las <a href="nse-works.md">extensiones de espacio de nombres</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2"><strong>CDefFolderMenu_Create2</strong></a><br/></td>
<td>Crea un menú contextual para un grupo seleccionado de objetos de carpeta de archivos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/ntquery/nf-ntquery-cishutdown"><strong>CIShutdown</strong></a><br/></td>
<td>Cierra el indizador de contenido y cierra todos los catálogos abiertos. <br/>
<blockquote>
[!Note]<br />
Esta función no se admite a partir de Windows 8.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-commandlinetoargvw"><strong>CommandLineToArgvW</strong></a><br/></td>
<td>Analiza una cadena de línea de comandos de Unicode y devuelve una matriz de punteros a los argumentos de la línea de comandos, junto con un recuento de estos argumentos, de una manera similar a los valores de las <em>argc</em> estándar <em>argv</em> y de C en tiempo de ejecución de C.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>APPLET_PROC</strong></a><br/></td>
<td>Sirve como punto de entrada para una aplicación del panel de control. Se trata de una función de devolución de llamada definida por la biblioteca.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-createappcontainerprofile"><strong>CreateAppContainerProfile</strong></a><br/></td>
<td>Crea un perfil por usuario y por aplicación para aplicaciones de la tienda Windows.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock"><strong>CreateEnvironmentBlock</strong></a><br/></td>
<td>Recupera las variables de entorno para el usuario especificado. A continuación, este bloque se puede pasar a la función <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera"><strong>CreateProcessAsUser</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="createmrulist.md"><strong>CreateMRUListW</strong></a><br/></td>
<td>Crea una nueva lista de elementos usados más recientemente (MRU).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-createprofile"><strong>CreateProfile</strong></a><br/></td>
<td>Crea un nuevo perfil de usuario.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-defscreensaverproc"><strong>DefScreenSaverProc</strong></a><br/></td>
<td>Proporciona el procesamiento predeterminado para los mensajes que no procesa una aplicación de protector de pantalla.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-defsubclassproc"><strong>DefSubclassProc</strong></a><br/></td>
<td>Llama al siguiente controlador de la cadena de subclases de una ventana. El último controlador de la cadena de subclase llama al procedimiento de ventana original para la ventana.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-deleteappcontainerprofile"><strong>DeleteAppContainerProfile</strong></a><br/></td>
<td>Elimina el perfil por usuario y por aplicación especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-deleteprofilea"><strong>DeleteProfile</strong></a><br/></td>
<td>Elimina el perfil de usuario y toda la configuración relacionada con el usuario del equipo especificado. El autor de la llamada debe tener privilegios administrativos para eliminar el perfil de un usuario.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock"><strong>DestroyEnvironmentBlock</strong></a><br/></td>
<td>Libera las variables de entorno creadas por la función <a href="/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock"><strong>CreateEnvironmentBlock</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-deriveappcontainersidfromappcontainername"><strong>DeriveAppContainerSidFromAppContainerName</strong></a><br/></td>
<td>Obtiene el SID del perfil especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/userenv/nf-userenv-deriverestrictedappcontainersidfromappcontainersidandrestrictedname"><strong>DeriveRestrictedAppContainerSidFromAppContainerSidAndRestrictedName</strong></a><br/></td>
<td>DeriveRestrictedAppContainerSidFromAppContainerSidAndRestrictedName se reserva para uso futuro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><em>DLLGETVERSIONPROC</em></a><br/></td>
<td>Implementado por muchos de los archivos DLL del shell de Windows para permitir que las aplicaciones obtengan información de versión específica de la DLL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles"><strong>DragAcceptFiles</strong></a><br/></td>
<td>Registra si una ventana acepta archivos colocados.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragfinish"><strong>DragFinish</strong></a><br/></td>
<td>Libera la memoria asignada por el sistema para su uso en la transferencia de nombres de archivo a la aplicación.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea"><strong>DragQueryFile</strong></a><br/></td>
<td>Recupera los nombres de los archivos colocados que son el resultado de una operación de arrastrar y colocar correcta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint"><strong>DragQueryPoint</strong></a><br/></td>
<td>Recupera la posición del puntero del mouse en el momento en que se quitó un archivo durante una operación de arrastrar y colocar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-duplicateicon"><strong>DuplicateIcon</strong></a><br/></td>
<td>Crea un duplicado de un icono especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera"><strong>ExpandEnvironmentStringsForUser</strong></a><br/></td>
<td>Expande la cadena de origen utilizando el bloque de entorno establecido para el usuario especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-extractassociatedicona"><strong>ExtractAssociatedIcon</strong></a><br/></td>
<td>Obtiene un identificador de un icono almacenado como un recurso en un archivo o un icono almacenado en el archivo ejecutable asociado de un archivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona"><strong>ExtractIcon</strong></a><br/></td>
<td>Obtiene un identificador de un icono del archivo ejecutable, DLL o archivo de icono especificado. <br/> Para recuperar una matriz de identificadores para iconos grandes o pequeños, utilice la función <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a><br/></td>
<td>La función <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a> crea una matriz de identificadores para los iconos grandes o pequeños extraídos del archivo ejecutable, el archivo dll o el archivo de icono especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="fileiconinit.md"><strong>FileIconInit</strong></a><br/></td>
<td>Inicializa o reinicializa la lista de imágenes del sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-findexecutablea"><strong>FindExecutable</strong></a><br/></td>
<td>Recupera el nombre y el identificador del archivo ejecutable (. exe) asociado a un archivo de documento específico.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/syncmgr/nf-syncmgr-freeconfirmconflictitem"><strong>FreeConfirmConflictItem</strong></a><br/></td>
<td>Libera los recursos que se han asignado para una estructura de <a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarray"><strong>FreeIDListArray</strong></a><br/></td>
<td>Libera la memoria usada por un puntero a una matriz de listas de identificadores de elementos (PIDL).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarraychild"><strong>FreeIDListArrayChild</strong></a><br/></td>
<td>Libera el espacio de memoria para la matriz de punteros a los identificadores de elemento secundarios. Esto libera el PITEMID_CHILDs dentro de la matriz y la propia matriz.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarrayfull"><strong>FreeIDListArrayFull</strong></a><br/></td>
<td>Libera el espacio de memoria de la matriz PIDL. Esto libera el PIDLIST_ABSOLUTEs dentro de la matriz y la propia matriz.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeknownfolderdefinitionfields"><strong>FreeKnownFolderDefinitionFields</strong></a><br/></td>
<td>Libera los campos asignados en el resultado de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getfolderdefinition"><strong>IKnownFolder:: GetFolderDefinition</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="freemrulist.md"><strong>FreeMRUList</strong></a><br/></td>
<td>Libera el identificador asociado a la lista MRU y escribe los datos almacenados en caché en el registro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya"><strong>GetAllUsersProfileDirectory</strong></a><br/></td>
<td>Recupera la ruta de acceso a la raíz del directorio que contiene los datos de programa compartidos por todos los usuarios.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getappcontainerfolderpath"><strong>GetAppContainerFolderPath</strong></a><br/></td>
<td>Obtiene la ruta de acceso de la carpeta de datos de la aplicación local para el contenedor de la aplicación especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getappcontainerregistrylocation"><strong>GetAppContainerRegistryLocation</strong></a><br/></td>
<td>Obtiene la ubicación del almacenamiento del registro asociado a un contenedor de la aplicación.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/jj152005(v=vs.85)"><strong>GetContractDelegateWindow</strong></a><br/></td>
<td>Recupera una ventana que se ha establecido como delegado de la ventana de primer plano principal de una aplicación con el fin de asociar la ventana de delegado a los contratos de la aplicación. Use esta función si es un desarrollador que está escribiendo una aplicación de la tienda Windows en C++ nativo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid"><strong>GetCurrentProcessExplicitAppUserModelID</strong></a><br/></td>
<td>Recupera el identificador de modelo de usuario de la aplicación (AppUserModelID) explícito definido por la aplicación para el proceso actual.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya"><strong>GetDefaultUserProfileDirectory</strong></a><br/></td>
<td>Recupera la ruta de acceso a la raíz del perfil del usuario predeterminado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiforshelluicomponent"><strong>GetDpiForShellUiComponent</strong></a><br/></td>
<td>Recupera los puntos por pulgada (PPP) ocupados por un <a href="/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-shell_ui_component"><strong>SHELL_UI_COMPONENT</strong></a> basándose en el factor de escala actual y en el <a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness"><strong>PROCESS_DPI_AWARENESS</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid"><strong>GetMenuContextHelpId</strong></a><br/></td>
<td>Recupera el identificador de contexto de ayuda asociado al menú especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya"><strong>GetProfilesDirectory</strong></a><br/></td>
<td>Recupera la ruta de acceso al directorio raíz donde se almacenan los perfiles de usuario.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getprofiletype"><strong>GetProfileType</strong></a><br/></td>
<td>Recupera el tipo de perfil cargado para el usuario actual.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorfordevice"><strong>GetScaleFactorForDevice</strong></a><br/></td>
<td>Obtiene el factor de escala preferido para un dispositivo de pantalla.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorformonitor"><strong>GetScaleFactorForMonitor</strong></a><br/></td>
<td>Obtiene el factor de escala de un monitor específico. Esta función reemplaza a <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorfordevice"><strong>GetScaleFactorForDevice</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya"><strong>GetUserProfileDirectory</strong></a><br/></td>
<td>Recupera la ruta de acceso al directorio raíz del perfil del usuario especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid"><strong>GetWindowContextHelpId</strong></a><br/></td>
<td>Recupera el identificador de contexto de ayuda, si existe, asociado a la ventana especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-getwindowsubclass"><strong>GetWindowSubclass</strong></a><br/></td>
<td>Recupera los datos de referencia para la devolución de llamada de la subclase de ventana especificada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-idlistcontainerisconsistent"><strong>IDListContainerIsConsistent</strong></a><br/></td>
<td>Comprueba que la estructura de contenedor de un IDList es válida.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilappendid"><strong>ILAppendID</strong></a><br/></td>
<td>Anexa o antepone una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> a una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclone"><strong>ILClone</strong></a><br/></td>
<td>Clona una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonechild"><strong>ILCloneChild</strong></a><br/></td>
<td>Clona una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> secundaria.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefirst"><strong>ILCloneFirst</strong></a><br/></td>
<td>Clona la primera estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> en una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefull"><strong>ILCloneFull</strong></a><br/></td>
<td>Clona una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> completa o absoluta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcombine"><strong>ILCombine</strong></a><br/></td>
<td>Combina dos estructuras <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcreatefrompath"><strong>ILCreateFromPath</strong></a><br/></td>
<td>Devuelve la estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> asociada a una ruta de acceso de archivo especificada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindchild"><strong>ILFindChild</strong></a><br/></td>
<td>Determina si una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> especificada es el elemento secundario de otra estructura <strong>ITEMIDLIST</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindlastid"><strong>ILFindLastID</strong></a><br/></td>
<td>Devuelve un puntero a la última estructura de <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> en una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree"><strong>ILFree</strong></a><br/></td>
<td>Libera una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> asignada por el shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilgetnext"><strong>ILGetNext</strong></a><br/></td>
<td>Recupera la siguiente estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> en una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilgetsize"><strong>ILGetSize</strong></a><br/></td>
<td>Devuelve el tamaño, en bytes, de una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisaligned"><strong>ILIsAligned</strong></a><br/></td>
<td>Comprueba si una constante <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> está alineada en un límite de puntero, que es un <strong>valor DWORD</strong> en las arquitecturas de 32 bits y un <strong>QWord</strong> en las arquitecturas de 64 bits.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilischild"><strong>ILIsChild</strong></a><br/></td>
<td>Comprueba si un PIDL es un PIDL secundario, que es un PIDL con exactamente un <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisempty"><strong>ILIsEmpty</strong></a><br/></td>
<td>Comprueba si una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> está vacía.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisequal"><strong>ILIsEqual</strong></a><br/></td>
<td>Comprueba si dos estructuras <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> son iguales en una comparación binaria.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisparent"><strong>ILIsParent</strong></a><br/></td>
<td>Comprueba si una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> es el elemento primario de otra estructura <strong>ITEMIDLIST</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilnext"><strong>ILNext (PCUIDLIST_RELATIVE)</strong></a><br/></td>
<td>Recupera la siguiente estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> en una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb776455(v=vs.85)"><strong>ILNext (PUIDLIST_RELATIVE)</strong></a><br/></td>
<td>Recupera la siguiente estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> en una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilremovelastid"><strong>ILRemoveLastID</strong></a><br/></td>
<td>Quita la última estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> de una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilsavetostream"><strong>ILSaveToStream</strong></a><br/></td>
<td>Guarda una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> en una secuencia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilskip"><strong>ILSkip (PCUIDLIST_RELATIVE, UINT)</strong></a><br/></td>
<td>Omite un número determinado de bytes en una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> constante, no alineada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb776459(v=vs.85)"><strong>ILSkip (PUIDLIST_RELATIVE, UINT)</strong></a><br/></td>
<td>Omite un número determinado de bytes en una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> relativa no alineada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-inetisoffline"><strong>InetIsOffline</strong></a><br/></td>
<td>Determina si el sistema está conectado a Internet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol"><strong>InitNetworkAddressControl</strong></a><br/></td>
<td>Inicializa la clase de ventana de control de dirección de red.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea"><strong>LoadUserProfile</strong></a><br/></td>
<td>Carga el perfil del usuario especificado. El perfil puede ser un perfil de <a href="local-user-profiles.md">usuario local</a> o un <a href="roaming-user-profiles.md">Perfil de usuario móvil</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-mimeassociationdialoga"><strong>MIMEAssociationDialog</strong></a><br/></td>
<td>Ejecuta el cuadro de diálogo tipo de contenido MIME no registrado.<br/>
<blockquote>
[!Note]<br />
Windows XP Service Pack 2 (SP2) o posterior: esta función ya no se admite.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathmakeuniquename"><strong>PathMakeUniqueName</strong></a><br/></td>
<td>Crea un nombre de ruta de acceso único a partir de una plantilla.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathyetanothermakeuniquename"><strong>PathYetAnotherMakeUniqueName</strong></a><br/></td>
<td>Crea un nombre de archivo único basado en un nombre de archivo existente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification"><strong>RegisterAppStateChangeNotification</strong></a><br/></td>
<td>Permite que una aplicación registre una función de devolución de llamada a través de la cual se puede notificar que su biblioteca entra o sale de un estado suspendido. La aplicación puede usar esta información para realizar cualquier operación necesaria, como conservar el estado, que se debe realizar en ese momento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-registerdialogclasses"><strong>RegisterDialogClasses</strong></a><br/></td>
<td>Registra las clases de ventana no estándar que requiere el cuadro de diálogo de configuración de un protector de pantalla.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a><br/></td>
<td>Registra un evento que se desencadena cuando es posible que la escala haya cambiado. Esta función reemplaza a <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangenotifications"><strong>RegisterScaleChangeNotifications</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangenotifications"><strong>RegisterScaleChangeNotifications</strong></a><br/></td>
<td>Registra una ventana para recibir devoluciones de llamada cuando se cambia la escala de la información.<br/>
<blockquote>
[!Note]<br />
Esta función no se admite a partir de Windows 8.1. Use <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a> en su lugar.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass"><strong>RemoveWindowSubclass</strong></a><br/></td>
<td>Quita una devolución de llamada de subclase de una ventana.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-revokescalechangenotifications"><strong>RevokeScaleChangeNotifications</strong></a><br/></td>
<td>Revoca el registro de una ventana, evitando que se reciban devoluciones de llamada al cambiar el escalado de la información.<br/>
<blockquote>
[!Note]<br />
Esta función no se admite a partir de Windows 8.1. Use <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-unregisterscalechangeevent"><strong>UnregisterScaleChangeEvent</strong></a> en su lugar.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-screensaverconfiguredialog"><strong>ScreenSaverConfigureDialog</strong></a><br/></td>
<td>Recibe los mensajes enviados al cuadro de diálogo de configuración de un protector de pantalla. Un protector de pantalla que permite la configuración del usuario debe definir esta función.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-screensaverproc"><strong>ScreenSaverProc</strong></a><br/></td>
<td>Recibe los mensajes enviados a la ventana del protector de pantalla especificada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcontractdelegatewindow"><strong>SetContractDelegateWindow</strong></a><br/></td>
<td>Asocia una ventana de la aplicación que no sea la ventana de primer plano principal con los contratos de una aplicación. Use esta función si es un desarrollador que está escribiendo una aplicación de la tienda Windows en C++ nativo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid"><strong>SetCurrentProcessExplicitAppUserModelID</strong></a><br/></td>
<td>Especifica un AppUserModelID único definido por la aplicación que identifica el proceso actual en la barra de tareas. Este identificador permite a una aplicación agrupar sus procesos y ventanas asociados bajo un solo botón de la barra de tareas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid"><strong>SetMenuContextHelpId</strong></a><br/></td>
<td>Asocia un identificador de contexto de ayuda a un menú.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid"><strong>SetWindowContextHelpId</strong></a><br/></td>
<td>Asocia un identificador de contexto de ayuda a la ventana especificada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass"><strong>SetWindowSubclass</strong></a><br/></td>
<td>Instala o actualiza una devolución de llamada de la subclase de una ventana.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a><br/></td>
<td>Notifica al sistema que se ha accedido a un elemento, con el fin de realizar un seguimiento de los elementos usados más recientemente y con más frecuencia. Esta función también se puede usar para borrar todos los datos de uso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage"><strong>SHAppBarMessage</strong></a><br/></td>
<td>Envía un mensaje de Appbar al sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlers"><strong>SHAssocEnumHandlers</strong></a><br/></td>
<td>Devuelve un objeto de enumeración para un conjunto especificado de controladores de extensión de nombre de archivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlersforprotocolbyapplication"><strong>SHAssocEnumHandlersForProtocolByApplication</strong></a><br/></td>
<td>Obtiene una interfaz de enumeración que proporciona acceso a los controladores asociados a un protocolo determinado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent"><strong>SHBindToFolderIDListParent</strong></a><br/></td>
<td>Dado un elemento de espacio de nombres de Shell especificado en el formulario de una carpeta y una lista de identificadores de elementos relativa a esa carpeta, esta función se enlaza al elemento primario del elemento de espacio de nombres y, opcionalmente, devuelve un puntero al componente final de la lista de identificadores de elementos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparentex"><strong>SHBindToFolderIDListParentEx</strong></a><br/></td>
<td>Extiende la función <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent"><strong>SHBindToFolderIDListParent</strong></a> permitiendo que el llamador especifique un contexto de enlace.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoobject"><strong>SHBindToObject</strong></a><br/></td>
<td>Recupera y enlaza a un objeto especificado mediante el método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> del espacio de nombres de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent"><strong>SHBindToParent</strong></a><br/></td>
<td>Toma un puntero a una lista de identificadores de elemento completo (PIDL) y devuelve un puntero de interfaz especificado en el objeto primario.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>SHBrowseForFolder</strong></a><br/></td>
<td>Muestra un cuadro de diálogo que permite al usuario seleccionar una carpeta de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_lock"><strong>SHChangeNotification_Lock</strong></a><br/></td>
<td>Bloquea la memoria compartida asociada a un evento de notificación de cambio de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_unlock"><strong>SHChangeNotification_Unlock</strong></a><br/></td>
<td>Desbloquea la memoria compartida para una notificación de cambios.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify"><strong>SHChangeNotify</strong></a><br/></td>
<td>Notifica al sistema de un evento que una aplicación ha realizado. Una aplicación debe usar esta función si realiza una acción que puede afectar al shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyderegister"><strong>SHChangeNotifyDeregister</strong></a><br/></td>
<td>Anula el registro del proceso de ventana del cliente para recibir mensajes <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify"><strong>SHChangeNotify</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>SHChangeNotifyRegister</strong></a><br/></td>
<td>Registra una ventana para recibir notificaciones del sistema de archivos o del shell, si el sistema de archivos admite notificaciones.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-shchangenotifyregisterthread"><strong>SHChangeNotifyRegisterThread</strong></a><br/></td>
<td>Habilita el registro asincrónico y la anulación del registro de un subproceso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateassociationregistration"><strong>SHCreateAssociationRegistration</strong></a><br/></td>
<td>Crea un objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a> basado en la implementación estándar de la interfaz proporcionada por Windows.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject"><strong>SHCreateDataObject</strong></a><br/></td>
<td>Crea un objeto de datos en una carpeta primaria.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultContextMenu</strong></a><br/></td>
<td>Crea un objeto que representa la implementación del menú contextual predeterminado del shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreatedefaultextracticon"><strong>SHCreateDefaultExtractIcon</strong></a><br/></td>
<td>Crea un extractor de icono estándar, cuyos valores predeterminados se pueden configurar más a través de la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit"><strong>IDefaultExtractIconInit</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nf-shobjidl-shcreatedefaultpropertiesop"><strong>SHCreateDefaultPropertiesOp</strong></a><br/></td>
<td>Crea una operación de archivo que establece las propiedades predeterminadas en el elemento de Shell que aún no se han establecido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist"><strong>SHCreateItemFromIDList</strong></a><br/></td>
<td>Crea e inicializa un objeto de elemento de Shell a partir de un PIDL. El objeto de elemento de Shell resultante es compatible con la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a><br/></td>
<td>Crea e inicializa un objeto de elemento del Shell a partir de un nombre de análisis.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromrelativename"><strong>SHCreateItemFromRelativeName</strong></a><br/></td>
<td>Crea e inicializa un objeto de elemento de Shell a partir de un nombre de análisis relativo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateiteminknownfolder"><strong>SHCreateItemInKnownFolder</strong></a><br/></td>
<td>Crea un objeto de elemento de Shell para un único archivo que existe dentro de una carpeta conocida.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent"><strong>SHCreateItemWithParent</strong></a><br/></td>
<td>Cree un elemento de Shell, dados una carpeta principal y un identificador de elemento secundario.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a><br/></td>
<td>Crea una nueva instancia del objeto de vista de carpeta de shell predeterminado (DefView).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>SHCreateShellFolderViewEx</strong></a><br/></td>
<td>Crea una nueva instancia del objeto de vista de carpeta del shell predeterminado. Se recomienda usar <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a> en lugar de esta función.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellitem"><strong>SHCreateShellItem</strong></a><br/></td>
<td>Crea un objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> . <br/>
<blockquote>
[!Note]<br />
Se recomienda que use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent"><strong>SHCreateItemWithParent</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist"><strong>SHCreateItemFromIDList</strong></a> en lugar de esta función.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarray"><strong>SHCreateShellItemArray</strong></a><br/></td>
<td>Crea un objeto de matriz de elementos de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject"><strong>SHCreateShellItemArrayFromDataObject</strong></a><br/></td>
<td>Crea un objeto de matriz de elementos de Shell a partir de un objeto de datos. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromidlists"><strong>SHCreateShellItemArrayFromIDLists</strong></a><br/></td>
<td>Crea un objeto de matriz de elementos de Shell a partir de una lista de estructuras <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromshellitem"><strong>SHCreateShellItemArrayFromShellItem</strong></a><br/></td>
<td>Crea una matriz de un elemento a partir de un único elemento de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdefextracticona"><strong>SHDefExtractIcon</strong></a><br/></td>
<td>Proporciona un controlador predeterminado para extraer un icono de un archivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop"><strong>SHDoDragDrop</strong></a><br/></td>
<td>Ejecuta una operación de arrastrar y colocar. Admite la creación de código fuente de arrastre a petición, así como a las imágenes de arrastre.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a><br/></td>
<td>Envía un mensaje al área de estado de la barra de tareas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a><br/></td>
<td>Obtiene las coordenadas de pantalla del rectángulo delimitador de un icono de notificación.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellabouta"><strong>ShellAbout</strong></a><br/></td>
<td>Muestra un cuadro de diálogo <strong>ShellAbout</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="shellddeinit.md"><strong>ShellDDEInit</strong></a><br/></td>
<td>Registra los servicios de Intercambio dinámico de datos de Shell (DDE) en el proceso actual, notificando al sistema que el proceso actual desea hospedar objetos DDE.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a><br/></td>
<td>Realiza una operación en un archivo especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a><br/></td>
<td>Realiza una operación en un archivo especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shemptyrecyclebina"><strong>SHEmptyRecycleBin</strong></a><br/></td>
<td>Vacía la papelera de reciclaje de la unidad especificada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shenumerateunreadmailaccountsa"><strong>SHEnumerateUnreadMailAccounts</strong></a><br/></td>
<td>Enumera las cuentas de usuario que tienen correo electrónico no leído.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shevaluatesystemcommandtemplate"><strong>SHEvaluateSystemCommandTemplate</strong></a><br/></td>
<td>Aplica la validación estricta de los parámetros utilizados en una llamada a <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> o a <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a><br/></td>
<td>Copia, mueve, cambia el nombre o elimina un objeto del sistema de archivos. La función se ha reemplazado en Windows Vista por <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shfreenamemappings"><strong>SHFreeNameMappings</strong></a><br/></td>
<td>Libera un objeto de asignación de nombres de archivo recuperado por la función <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>SHGetDataFromIDList</strong></a><br/></td>
<td>Recupera los datos de propiedad extendida de una lista de identificadores relativos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder"><strong>SHGetDesktopFolder</strong></a><br/></td>
<td>Recupera la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> para la carpeta Desktop, que es la raíz del espacio de nombres del shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetdiskfreespaceexa"><strong>SHGetDiskFreeSpaceEx</strong></a><br/></td>
<td>Recupera información de espacio en disco para un volumen de disco.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetdrivemedia"><strong>SHGetDriveMedia</strong></a><br/></td>
<td>Devuelve el tipo de medio que se encuentra en la unidad especificada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetfileinfoa"><strong>SHGetFileInfo</strong></a><br/></td>
<td>Recupera información acerca de un objeto en el sistema de archivos, como un archivo, una carpeta, un directorio o una raíz de unidad.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/mt757093(v=vs.85)"><strong>SHGetFolderPathEx</strong></a><br/></td>
<td>Recupera la ruta de acceso completa de una carpeta conocida identificada por el <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a>de la carpeta. Esto extiende <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>SHGetKnownFolderPath</strong></a> permitiendo establecer el tamaño inicial del búfer de cadena.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgeticonoverlayindexa"><strong>SHGetIconOverlayIndex</strong></a><br/></td>
<td>Devuelve el índice del icono de superposición en la lista de imágenes del sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetidlistfromobject"><strong>SHGetIDListFromObject</strong></a><br/></td>
<td>Recupera el PIDL de un objeto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetimagelist"><strong>SHGetImageList</strong></a><br/></td>
<td>Recupera una lista de imágenes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetinstanceexplorer"><strong>SHGetInstanceExplorer</strong></a><br/></td>
<td>Recupera una interfaz que permite extensiones de Shell hospedadas y otros componentes para impedir que el proceso de host se cierre prematuramente. El proceso de host suele ser el explorador de Windows o Windows Internet Explorer, pero otras aplicaciones también pueden usar esta función.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromdataobject"><strong>SHGetItemFromDataObject</strong></a><br/></td>
<td>Crea un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> o un objeto relacionado basándose en un elemento especificado por <a href="/windows/desktop/api/objidl/nn-objidl-idataobject"><strong>IDataObject</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromobject"><strong>SHGetItemFromObject</strong></a><br/></td>
<td>Recupera un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> para un objeto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist"><strong>SHGetKnownFolderIDList</strong></a><br/></td>
<td>Recupera la ruta de acceso de una carpeta conocida como una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem"><strong>SHGetKnownFolderItem</strong></a><br/></td>
<td>Recupera un objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> que representa una carpeta conocida.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>SHGetKnownFolderPath</strong></a><br/></td>
<td>Recupera la ruta de acceso completa de una carpeta conocida identificada por el <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a>de la carpeta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetlocalizedname"><strong>SHGetLocalizedName</strong></a><br/></td>
<td>Recupera el nombre localizado de un archivo en una carpeta de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetnamefromidlist"><strong>SHGetNameFromIDList</strong></a><br/></td>
<td>Recupera el nombre para mostrar de un elemento identificado por su IDList.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb762192(v=vs.85)"><strong>SHGetNameFromPropertyKey</strong></a><br/></td>
<td>Recupera el nombre canónico de la propiedad dado su <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetnewlinkinfoa"><strong>SHGetNewLinkInfo</strong></a><br/></td>
<td>Crea un nombre para un nuevo acceso directo basado en el destino propuesto del acceso directo. Esta función no crea el acceso directo, solo el nombre.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista"><strong>SHGetPathFromIDList</strong></a><br/></td>
<td>Convierte una lista de identificadores de elemento en una ruta de acceso del sistema de archivos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlistex"><strong>SHGetPathFromIDListEx</strong></a><br/></td>
<td>Convierte una lista de identificadores de elemento en una ruta de acceso del sistema de archivos. Esta función extiende <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista"><strong>SHGetPathFromIDList</strong></a> permitiendo establecer el tamaño inicial del búfer de cadena y declarar las opciones siguientes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>SHGetSettings</strong></a><br/></td>
<td>Recupera la configuración actual de la opción de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a><br/></td>
<td>Recupera información sobre los iconos de Shell definidos por el sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgettemporarypropertyforitem"><strong>SHGetTemporaryPropertyForItem</strong></a><br/></td>
<td>Recupera la propiedad temporal para el elemento especificado. Una propiedad temporal es un almacén de lectura/escritura que contiene propiedades solo durante el período de duración del objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> , en lugar de volver a almacenarse en el elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetunreadmailcountw"><strong>SHGetUnreadMailCount</strong></a><br/></td>
<td>Recupera el número de mensajes no leídos de un usuario especificado para una o todas las cuentas de correo electrónico.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-shisfileavailableoffline"><strong>SHIsFileAvailableOffline</strong></a><br/></td>
<td>Determina si un archivo o carpeta está disponible para su uso sin conexión. Esta función también determina si el archivo se abriría desde la red, desde la caché de Archivos sin conexión local o desde ambas ubicaciones.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shloadinproc"><strong>SHLoadInProc</strong></a><br/></td>
<td>Crea una instancia de la clase de objeto especificada desde el contexto del proceso del shell. <br/> <strong>Windows Vista</strong> y versiones posteriores: esta función se ha deshabilitado y devuelve E_NOTIMPL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-shloadnonloadediconoverlayidentifiers"><strong>SHLoadNonloadedIconOverlayIdentifiers</strong></a><br/></td>
<td>Indica al shell que, durante la siguiente operación que requiere información de superposición, debe cargar los identificadores de superposición de iconos que no se pudieron crear o que no estaban presentes para su creación en el inicio. Los identificadores que ya se han cargado no se ven afectados.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shlocalstrdupa"><strong>SHLocalStrDup</strong></a><br/></td>
<td>Realiza una copia de una cadena en la memoria recién asignada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-shmultifileproperties"><strong>SHMultiFileProperties</strong></a><br/></td>
<td>Muestra una hoja de propiedades combinada para un conjunto de archivos. Se muestran los valores de propiedad comunes a todos los archivos, mientras que los que difieren muestran la cadena <strong>(varios valores)</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenfolderandselectitems"><strong>SHOpenFolderAndSelectItems</strong></a><br/></td>
<td>Abre una ventana del explorador de Windows con los elementos especificados en una carpeta determinada seleccionada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>SHOpenWithDialog</strong></a><br/></td>
<td>Muestra el cuadro de diálogo <strong>abrir con</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/showsharefolderui"><strong>ShowShareFolderUI</strong></a><br/></td>
<td>Muestra la ficha <strong>compartir carpetas</strong> de la hoja de propiedades de la carpeta especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shparsedisplayname"><strong>SHParseDisplayName</strong></a><br/></td>
<td>Convierte el nombre para mostrar de un objeto de espacio de nombres del shell en una lista de identificadores de elemento y devuelve los atributos del objeto. Esta función es el método preferido para convertir una cadena en un PIDL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shpathprepareforwritea"><strong>SHPathPrepareForWrite</strong></a><br/></td>
<td>Comprueba si existe la ruta de acceso. Esto incluye volver a montar las unidades de red asignadas, pedir que se vuelvan a insertar los medios expulsables, crear las rutas de acceso, solicitar el formato de los medios y proporcionar las interfaces de usuario adecuadas, si es necesario. No se comprueban los permisos de lectura y escritura para el medio.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>SHQueryRecycleBin</strong></a><br/></td>
<td>Recupera el tamaño de la papelera de reciclaje y el número de elementos que hay en ella para una unidad especificada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate"><strong>SHQueryUserNotificationState</strong></a><br/></td>
<td>Comprueba el estado del equipo para el usuario actual con el fin de determinar si el envío de una notificación es adecuado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shremovelocalizedname"><strong>SHRemoveLocalizedName</strong></a><br/></td>
<td>Quita el nombre localizado de un archivo en una carpeta de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-shruncontrolpanel"><strong>SHRunControlPanel</strong></a><br/></td>
<td>Abre un elemento del panel de control. <br/>
<blockquote>
[!Note]<br />
Esta función no es compatible con Windows Vista
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nf-shobjidl-shsetdefaultproperties"><strong>SHSetDefaultProperties</strong></a><br/></td>
<td>Aplica el conjunto predeterminado de propiedades en un elemento de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetinstanceexplorer"><strong>SHSetInstanceExplorer</strong></a><br/></td>
<td>Proporciona una interfaz que permite extensiones de Shell hospedadas y otros componentes para impedir que el proceso de host se cierre prematuramente. Normalmente, el proceso de host es el explorador de Windows o Internet Explorer, pero otras aplicaciones también pueden usar esta función.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath"><strong>SHSetKnownFolderPath</strong></a><br/></td>
<td>Redirige una carpeta conocida a una nueva ubicación.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shsetlocalizedname"><strong>SHSetLocalizedName</strong></a><br/></td>
<td>Establece el nombre localizado de un archivo en una carpeta de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsettemporarypropertyforitem"><strong>SHSetTemporaryPropertyForItem</strong></a><br/></td>
<td>Establece una propiedad temporal para el elemento especificado. Una propiedad temporal se mantiene en un almacén de lectura/escritura que contiene propiedades solo durante el período de duración del objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> , en lugar de volver a escribirlas en el elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shsetunreadmailcountw"><strong>SHSetUnreadMailCount</strong></a><br/></td>
<td>Almacena el número de mensajes no leídos del usuario actual para una cuenta de correo electrónico especificada en el registro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shtesttokenmembership"><strong>SHTestTokenMembership</strong></a><br/></td>
<td>Usa <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembership"><strong>CheckTokenMembership</strong></a> para comprobar si el token especificado es un miembro del grupo local con el RID especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shupdateimagea"><strong>SHUpdateImage</strong></a><br/></td>
<td>Notifica al shell que una imagen de la lista de imágenes del sistema ha cambiado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-softwareupdatemessagebox"><strong>SoftwareUpdateMessageBox</strong></a><br/></td>
<td>Muestra un cuadro de mensaje estándar que se puede usar para notificar a un usuario que se ha actualizado una aplicación.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-stgmakeuniquename"><strong>StgMakeUniqueName</strong></a><br/></td>
<td>Crea un nombre único para un flujo o un objeto de almacenamiento a partir de una plantilla.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstrniw"><strong>StrStrNIW</strong></a><br/></td>
<td>Busca la primera aparición de una subcadena en una cadena. La comparación distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstrnw"><strong>StrStrNW</strong></a><br/></td>
<td>Busca la primera aparición de una subcadena en una cadena. La comparación distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-translateurla"><strong>TranslateURL</strong></a><br/></td>
<td>Aplica traducciones comunes a una cadena de dirección URL determinada y crea una nueva cadena de dirección URL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile"><strong>UnloadUserProfile</strong></a><br/></td>
<td>Descarga el perfil de un usuario cargado por la función <a href="/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea"><strong>LoadUserProfile</strong></a> . El autor de la llamada debe tener privilegios administrativos en el equipo. Para obtener más información, vea la sección Comentarios de la función <strong>LoadUserProfile</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/appnotify/nf-appnotify-unregisterappstatechangenotification"><strong>UnregisterAppStateChangeNotification</strong></a><br/></td>
<td>Cancela una notificación de cambios registrada a través de <a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification"><strong>RegisterAppStateChangeNotification</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-unregisterscalechangeevent"><strong>UnregisterScaleChangeEvent</strong></a><br/></td>
<td>Anula el registro del evento de cambio de escala registrado a través de <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a>. Esta función reemplaza a <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-revokescalechangenotifications"><strong>RevokeScaleChangeNotifications</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-urlassociationdialoga"><strong>URLAssociationDialog</strong></a><br/></td>
<td>Invoca el cuadro de diálogo protocolo de dirección URL no registrado. Este cuadro de diálogo permite al usuario seleccionar una aplicación para asociarla a un protocolo desconocido.<br/>
<blockquote>
[!Note]<br />
Windows XP SP2 o posterior: esta función ya no se admite.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/bb762266(v=vs.85)"><strong>WinExecError</strong></a><br/></td>
<td>Recupera el valor de error generado si la función <a href="/windows/win32/api/winbase/nf-winbase-winexec">WinExec</a> no puede ejecutar una aplicación especificada. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>Salga</strong></a><br/></td>
<td>Inicia la ayuda de Windows (Winhelp.exe) y pasa datos adicionales que indican la naturaleza de la ayuda solicitada por la aplicación.<br/></td>
</tr>
</tbody>
</table>



 

 

 
