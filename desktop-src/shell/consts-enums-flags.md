---
description: En esta sección se describen las constantes, las enumeraciones y las marcas del shell de Windows.
title: Constantes, enumeraciones y marcas de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 638beaa7-a065-4ab3-8eb5-286a306a8f24
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2070ef1acc37262a526186862f46afa002c47343
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104279711"
---
# <a name="shell-constants-enumerations-and-flags"></a>Constantes, enumeraciones y marcas de Shell

En esta sección se describen las constantes, las enumeraciones y las marcas del shell de Windows.

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
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_svgio"><strong>_SVGIO</strong></a><br/></td>
<td>Se utiliza con los métodos <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-items"><strong>IFolderView:: items</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-itemcount"><strong>IFolderView:: ItemCount</strong></a>y <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getitemobject"><strong>IShellView:: GetItemObject</strong></a> para restringir o controlar los elementos de sus colecciones.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_svsif"><strong>_SVSIF</strong></a><br/></td>
<td>Indica las marcas usadas por <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>IFolderView</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2"><strong>IFolderView2</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a> para especificar el tipo de selección que se va a aplicar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-appactionflags"><strong>APPACTIONFLAGS</strong></a><br/></td>
<td>Especifica las acciones de administración de aplicaciones admitidas por un publicador de aplicaciones. Estas marcas son las máscaras de máscara que se pasan a <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ishellapp-getpossibleactions"><strong>IShellApp:: GetPossibleActions</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-appinfodataflags"><strong>APPINFODATAFLAGS</strong></a><br/></td>
<td>Especifica la información de la aplicación que se va a devolver de <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ishellapp-getappinfo"><strong>IShellApp:: GetAppInfo</strong></a>. Estas marcas son las máscaras de las que se usan en el miembro <a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>dwMask</strong></a> de la estructura <strong>APPINFODATA</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-application_view_orientation"><strong>APPLICATION_VIEW_ORIENTATION</strong></a><br/></td>
<td>Define el conjunto de modos de orientación de la pantalla para una ventana (vista de la aplicación). Usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-getapplicationvieworientation"><strong>IApplicationDesignModeSettings2:: GetApplicationViewOrientation</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-setapplicationvieworientation"><strong>IApplicationDesignModeSettings2:: SetApplicationViewOrientation</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-application_view_size_preference"><strong>APPLICATION_VIEW_SIZE_PREFERENCE</strong></a><br/></td>
<td>Define el conjunto de preferencias de tamaño posibles de la ventana general (vista de aplicaciones). Usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ilaunchsourceviewsizepreference-getsourceviewsizepreference"><strong>ILaunchSourceViewSizePreference:: GetSourceViewSizePreference</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ilaunchtargetviewsizepreference-gettargetviewsizepreference"><strong>ILaunchTargetViewSizePreference:: GetTargetViewSizePreference</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-application_view_state"><strong>APPLICATION_VIEW_STATE</strong></a><br/></td>
<td>Indica el estado de vista actual de una aplicación de la tienda Windows. Usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setapplicationviewstate"><strong>IApplicationDesignModeSettings:: SetApplicationViewState</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-isapplicationviewstatesupported"><strong>IApplicationDesignModeSettings:: IsApplicationViewStateSupported</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assocdata"><strong>ASSOCDATA</strong></a><br/></td>
<td>Usado por <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getdata"><strong>IQueryAssociations:: GetData</strong></a> para definir el tipo de datos que se van a devolver.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/shell/assocf_str"><strong>ASSOCF</strong></a><br/></td>
<td>Proporciona información a los métodos de la interfaz <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel"><strong>ASSOCIATIONLEVEL</strong></a><br/></td>
<td>Especifica el origen de la Asociación predeterminada para una extensión de nombre de archivo. Lo usan los métodos de la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype"><strong>ASSOCIATIONTYPE</strong></a><br/></td>
<td>Especifica el tipo de Asociación de una aplicación. Lo usan los métodos de la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assockey"><strong>ASSOCKEY</strong></a><br/></td>
<td>Especifica el tipo de clave que va a ser devuelto por <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getkey"><strong>IQueryAssociations:: GetKey</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr"><strong>ASSOCSTR</strong></a><br/></td>
<td>Usado por <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getstring"><strong>IQueryAssociations:: GetString</strong></a> para definir el tipo de cadena que se va a devolver.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_action"><strong>ATTACHMENT_ACTION</strong></a><br/></td>
<td>Proporciona un conjunto de marcas que se van a usar con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt"><strong>IAttachmentExecute::P reguntar</strong></a> para indicar la acción que se realizará tras la confirmación del usuario.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_prompt"><strong>ATTACHMENT_PROMPT</strong></a><br/></td>
<td>Proporciona un conjunto de marcas que se van a usar con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt"><strong>IAttachmentExecute::P reguntar</strong></a> para indicar el tipo de interfaz de usuario del mensaje que se va a mostrar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ne-shlobj_core-autocompletelistoptions"><strong>AUTOCOMPLETELISTOPTIONS</strong></a><br/></td>
<td>Especifica los objetos que se enumeran para las listas de finalización automática.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shldisp/ne-shldisp-autocompleteoptions"><strong>AUTOCOMPLETEOPTIONS</strong></a><br/></td>
<td>Especifica los valores usados por <a href="/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-getoptions"><strong>IAutoComplete2:: GetOptions</strong></a> y <a href="/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions"><strong>IAutoComplete2:: SetOptions</strong></a> para las opciones que rodean a Autocompletar.<br/></td>
</tr>
<tr class="even">
<td><a href="str-constants.md"><strong>Enlazar claves de cadena de contexto</strong></a><br/></td>
<td>Un conjunto de claves de cadena que se usan con el método <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx:: RegisterObjectParam</strong></a> para especificar un contexto de enlace.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shdeprecated/ne-shdeprecated-bnstate"><strong>BNSTATE</strong></a><br/></td>
<td>En desuso. Usado por <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice-setnavigatestate"><strong>IBrowserService:: SetNavigateState</strong></a> y <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice-getnavigatestate"><strong>IBrowserService:: GetNavigateState</strong></a> para especificar los Estados de navegación.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-_browserframeoptions"><strong>BROWSERFRAMEOPTIONS</strong></a><br/></td>
<td>Se usa con el método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibrowserframeoptions-getframeoptions"><strong>IBrowserFrameOptions:: GetFrameOptions</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-categoryinfo_flags"><strong>CATEGORYINFO_FLAGS</strong></a><br/></td>
<td>Proporciona un conjunto de marcas para su uso con la estructura de <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-catsort_flags"><strong>CATSORT_FLAGS</strong></a><br/></td>
<td>Especifica los métodos para ordenar los datos de categoría.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb762483(v=vs.85)"><strong>CDCONTROLSTATE</strong></a><br/></td>
<td>Especifica los valores que indican si un control está visible y habilitado. Lo usan los miembros de la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize"><strong>IFileDialogCustomize</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_enum_flags"><strong>CM_ENUM_FLAGS</strong></a><br/></td>
<td>Lo usan los miembros de la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a> para especificar qué conjunto de columnas se están solicitando, o solo las que están visibles actualmente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_mask"><strong>CM_MASK</strong></a><br/></td>
<td>Indica qué valores de la estructura de <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> se deben establecer durante las llamadas a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icolumnmanager-setcolumninfo"><strong>IColumnManager:: SetColumnInfo</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_set_width_value"><strong>CM_SET_WIDTH_VALUE</strong></a><br/></td>
<td>Especifica valores de ancho en píxeles e incluye compatibilidad especial para el valor predeterminado y el tamaño automático. Lo usan los miembros de la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a> a través de la estructura <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_state"><strong>CM_STATE</strong></a><br/></td>
<td>Especifica valores de estado de columna. Lo usan los miembros de la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a> a través de la estructura <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/CredentialProvider/ne-credentialprovider-credential_provider_account_options"><strong>CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS</strong></a><br/></td>
<td>Indica el tipo de credencial que debe devolver un proveedor de credenciales para asociarla con el &quot; otro usuario &quot; . Utilizado por <a href="/windows/desktop/api/CredentialProvider/nf-credentialprovider-icredentialprovideruserarray-getaccountoptions"><strong>ICredentialProviderUserArray_GetAccountOptions</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/ne-credentialprovider-credential_provider_credential_field_options"><strong>CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS</strong></a><br/></td>
<td>Proporciona opciones de personalización para un solo campo en una interfaz de usuario de credenciales o de inicio de sesión.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_interactive_state"><strong>CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE</strong></a><br/></td>
<td>Describe el estado de un campo y el modo en que un usuario puede interactuar con él. Los campos se pueden mostrar mediante un proveedor de credenciales en distintos Estados interactivos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_state"><strong>CREDENTIAL_PROVIDER_FIELD_STATE</strong></a><br/></td>
<td>Especifica el estado de un solo campo en la interfaz de usuario de credenciales.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_type"><strong>CREDENTIAL_PROVIDER_FIELD_TYPE</strong></a><br/></td>
<td>Especifica un tipo de campo de credencial. Utilizado por <a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_field_descriptor"><strong>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_get_serialization_response"><strong>CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE</strong></a><br/></td>
<td>Describe la respuesta cuando un proveedor de credenciales intenta serializar las credenciales.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_status_icon"><strong>CREDENTIAL_PROVIDER_STATUS_ICON</strong></a><br/></td>
<td>Indica el icono de estado que se debe mostrar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_usage_scenario"><strong>CREDENTIAL_PROVIDER_USAGE_SCENARIO</strong></a><br/></td>
<td>Declara los escenarios en los que se admite un proveedor de credenciales. Un escenario de uso del proveedor de credenciales (CPU) permite que el proveedor de credenciales proporcione un comportamiento de enumeración distinto y una configuración de campos de interfaz de usuario entre escenarios.<br/></td>
</tr>
<tr class="even">
<td><a href="csidl.md"><strong>CSIDL</strong></a><br/></td>
<td><blockquote>
<p><b>Nota: </b> A partir de Windows Vista, estos valores se han sustituido por valores <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a> . Consulte ese tema para obtener una lista de las nuevas constantes y sus valores de CSIDL correspondientes. Para mayor comodidad, los valores de <strong>KNOWNFOLDERID</strong> correspondientes también se indican aquí para cada valor de CSIDL.</p>
<p>El sistema CSIDL es compatible con Windows Vista por motivos de compatibilidad. Sin embargo, el nuevo desarrollo debe usar valores <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a> en lugar de los valores CSIDL.<br/></p>
</blockquote>
<br/> Los valores de CSIDL (lista de ID. de elemento especial constante) proporcionan una manera única independiente del sistema para identificar carpetas especiales usadas con frecuencia por aplicaciones, pero que pueden no tener el mismo nombre o ubicación en ningún sistema determinado. Por ejemplo, la carpeta del sistema puede ser &quot; C:\Windows &quot; en un sistema y &quot; C:\WINNT &quot; en otro. Estas constantes se definen en ShlObj. h.<br/></td>
</tr>
<tr class="odd">
<td><a href="ctf.md"><strong>Marcas de CTF</strong></a><br/></td>
<td>Marcas que controlan el comportamiento de la función de llamada. Usado por <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread"><strong>SHCreateThread</strong></a> y <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadwithhandle"><strong>SHCreateThreadWithHandle</strong></a>. En esas funciones, estos valores se definen como de tipo SHCT_FLAGS.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-dataobj_get_item_flags"><strong>DATAOBJ_GET_ITEM_FLAGS</strong></a><br/></td>
<td>Valores utilizados por la función <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromdataobject"><strong>SHGetItemFromDataObject</strong></a> para especificar las opciones relativas al procesamiento del objeto de origen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-tagdeskbandcid"><strong>Indicadores del comando DBID</strong></a><br/></td>
<td>Estos identificadores de comando se pueden enviar al contenedor del objeto de banda con <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-exec"><strong>IOLECommandTarget:: exec</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-def_share_id"><strong>DEF_SHARE_ID</strong></a><br/></td>
<td>Valores que especifican la carpeta en la que actúan los métodos de la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isharingconfigurationmanager"><strong>ISharingConfigurationManager</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype"><strong>DEFAULTSAVEFOLDERTYPE</strong></a><br/></td>
<td>Especifica la ubicación de almacenamiento predeterminada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-default_folder_menu_restrictions"><strong>DEFAULT_FOLDER_MENU_RESTRICTIONS</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-desktop_wallpaper_position"><strong>DESKTOP_WALLPAPER_POSITION</strong></a><br/></td>
<td>Especifica cómo debe mostrarse el papel tapiz del escritorio.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ne-shtypes-device_scale_factor"><strong>DEVICE_SCALE_FACTOR</strong></a><br/></td>
<td>Indica un factor de escala de dispositivo falsificado, en forma de porcentaje. Usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setapplicationviewstate"><strong>IApplicationDesignModeSettings:: SetApplicationViewState</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-isapplicationviewstatesupported"><strong>IApplicationDesignModeSettings:: IsApplicationViewStateSupported</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/ne-shellscalingapi-display_device_type"><strong>DISPLAY_DEVICE_TYPE</strong></a><br/></td>
<td>Indica si el dispositivo es un tipo de pantalla principal o envolvente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype"><strong>DROPIMAGETYPE</strong></a><br/></td>
<td>Valores utilizados con la estructura <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>DROPDESCRIPTION</strong></a> para especificar la imagen de colocación.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_expcmdstate"><strong>EXPCMDSTATE</strong></a><br/></td>
<td>Los valores de <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_expcmdstate"><strong>EXPCMDSTATE</strong></a> representan el estado de comando de un elemento de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_fill_flags"><strong>EXPLORER_BROWSER_FILL_FLAGS</strong></a><br/></td>
<td>Estas marcas se usan con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-fillfromobject"><strong>IExplorerBrowser:: FillFromObject</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_options"><strong>EXPLORER_BROWSER_OPTIONS</strong></a><br/></td>
<td>Estas marcas se usan con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-getoptions"><strong>IExplorerBrowser:: GetOptions</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-setoptions"><strong>IExplorerBrowser:: SetOptions</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_explorerpanestate"><strong>EXPLORERPANESTATE</strong></a><br/></td>
<td>Indicar las marcas usadas por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate"><strong>IExplorerPaneVisibility:: GetPaneState</strong></a> para obtener el estado actual del panel del explorador de Windows determinado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fdap"><strong>FDAP</strong></a><br/></td>
<td>Especifica la ubicación de la lista.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fde_overwrite_response"><strong>FDE_OVERWRITE_RESPONSE</strong></a><br/></td>
<td>Especifica los valores que usa el método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onoverwrite"><strong>IFileDialogEvents:: OnOverwrite</strong></a> para indicar la respuesta de una aplicación a una solicitud de sobrescritura durante una operación de guardar mediante el cuadro de diálogo de archivo común.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fde_shareviolation_response"><strong>FDE_SHAREVIOLATION_RESPONSE</strong></a><br/></td>
<td>Especifica los valores que usa el método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onshareviolation"><strong>IFileDialogEvents:: OnShareViolation</strong></a> para indicar la respuesta de una aplicación a una infracción de uso compartido que se produce cuando se abre o se guarda un archivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fffp_mode"><strong>FFFP_MODE</strong></a><br/></td>
<td>Describe los criterios de coincidencia. Lo usan los métodos de la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager"><strong>IKnownFolderManager</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-file_usage_type"><strong>FILE_USAGE_TYPE</strong></a><br/></td>
<td>Constantes usadas por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileisinuse-getusage"><strong>IFileIsInUse:: GetUsage</strong></a> para indicar cómo se usa un archivo en uso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_fileopendialogoptions"><strong>FILEOPENDIALOGOPTIONS</strong></a><br/></td>
<td>Define el conjunto de opciones disponibles para un cuadro de diálogo para abrir o guardar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a><br/></td>
<td>Indica las constantes <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> que se usan en el valor marcas de una clave del registro <a href="fa-progids.md">ProgID</a> de la Asociación de archivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode"><strong>FOLDER_ENUM_MODE</strong></a><br/></td>
<td>Lo usan los métodos <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithfolderenummode-getmode"><strong>IObjectWithFolderEnumMode:: GetMode</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithfolderenummode-setmode"><strong>IObjectWithFolderEnumMode:: SetMode</strong></a> para obtener y establecer los modos de presentación de las carpetas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags"><strong>FOLDERFLAGS</strong></a><br/></td>
<td>Conjunto de marcas que especifican las opciones de la vista de carpetas. Las marcas son independientes entre sí y se pueden usar en cualquier combinación.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderlogicalviewmode"><strong>FOLDERLOGICALVIEWMODE</strong></a><br/></td>
<td>Usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderviewsettings-getviewmode"><strong>IFolderViewSettings:: GetViewMode</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setfolderlogicalviewmode"><strong>ISearchFolderItemFactory:: SetFolderLogicalViewMode</strong></a> para describir el modo de vista.<br/></td>
</tr>
<tr class="odd">
<td><a href="foldertypeid.md"><strong>FOLDERTYPEID</strong></a><br/></td>
<td>Los valores de <a href="foldertypeid.md"><strong>FOLDERTYPEID</strong></a> representan una plantilla de vista que se aplica a una carpeta, normalmente en función de su contenido y uso previsto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode"><strong>FOLDERVIEWMODE</strong></a><br/></td>
<td>Especifica el tipo de vista de la carpeta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-folderviewoptions"><strong>FOLDERVIEWOPTIONS</strong></a><br/></td>
<td>Lo usan los métodos de la interfaz <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewoptions"><strong>IFolderViewOptions</strong></a> para activar las opciones de Windows Vista que no se admiten de forma predeterminada en los sistemas Windows 7 y versiones posteriores, así como para desactivar las nuevas opciones de Windows 7.<br/></td>
</tr>
<tr class="even">
<td><a href="iactivedesktop-flags.md"><strong>Marcas de IActiveDesktop</strong></a><br/></td>
<td>En esta sección se describen las marcas usadas por los métodos de la interfaz <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>IActiveDesktop</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ne-shlobj_core-ieshortcutflags"><strong>IESHORTCUTFLAGS</strong></a><br/></td>
<td>Especifica cómo debe controlar un acceso directo el explorador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category"><strong>KF_CATEGORY</strong></a><br/></td>
<td>Valor que representa una categoría por la que se puede clasificar una carpeta registrada con el sistema de carpetas conocido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_definition_flags"><strong>KF_DEFINITION_FLAGS</strong></a><br/></td>
<td>Marcas que especifican ciertos comportamientos de carpeta conocidos. Se usa con la estructura <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_redirect_flags"><strong>KF_REDIRECT_FLAGS</strong></a><br/></td>
<td>Marcas usadas por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-redirect"><strong>IKnownFolderManager:: redirect</strong></a> para especificar detalles de una redirección de carpeta conocida, como los permisos y la propiedad de la carpeta redirigida.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_redirection_capabilities"><strong>KF_REDIRECTION_CAPABILITIES</strong></a><br/></td>
<td>Marcas que especifican las capacidades de redirección actuales de una carpeta conocida. Usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities"><strong>IKnownFolder:: GetRedirectionCapabilities</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag"><strong>KNOWN_FOLDER_FLAG</strong></a><br/></td>
<td>Especifique opciones de recuperación especiales para carpetas conocidas. Estos valores reemplazan a los valores <a href="csidl.md"><strong>CSIDL</strong></a> , que tienen significados en paralelo.<br/></td>
</tr>
<tr class="odd">
<td><a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a><br/></td>
<td>Las constantes <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a> representan los GUID que identifican las carpetas estándar registradas con el sistema como <a href="known-folders.md">carpetas conocidas</a>. Estas carpetas se instalan con Windows Vista y sistemas operativos posteriores, y un equipo solo tendrá las carpetas adecuadas para su instalación. Para obtener descripciones de estas carpetas, consulte <a href="csidl.md"><strong>CSIDL</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryfolderfilter"><strong>LIBRARYFOLDERFILTER</strong></a><br/></td>
<td>Define las opciones para filtrar elementos de carpeta. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarymanagedialogoptions"><strong>LIBRARYMANAGEDIALOGOPTIONS</strong></a><br/></td>
<td>Usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shshowmanagelibraryui"><strong>SHShowManageLibraryUI</strong></a> para definir las opciones de control de un conflicto de nombres al guardar una biblioteca.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags"><strong>LIBRARYOPTIONFLAGS</strong></a><br/></td>
<td>Especifica las opciones de la biblioteca.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarysaveflags"><strong>LIBRARYSAVEFLAGS</strong></a><br/></td>
<td>Especifica las opciones para controlar un conflicto de nombres al guardar una biblioteca. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-mimeassociationdialog_in_flags"><strong>MIMEASSOCIATIONDIALOG_IN_FLAGS</strong></a><br/></td>
<td>Se usa con la función <a href="/windows/desktop/api/Intshcut/nf-intshcut-mimeassociationdialoga"><strong>MIMEAssociationDialog</strong></a> para determinar cómo se ejecuta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-monitor_app_visibility"><strong>MONITOR_APP_VISIBILITY</strong></a><br/></td>
<td>Especifica si una pantalla muestra las ventanas de escritorio en lugar de las aplicaciones de la tienda Windows.<br/></td>
</tr>
<tr class="even">
<td><a href="mp-popupflags.md"><strong>Constantes de MP_POPUPFLAGS</strong></a><br/></td>
<td>Representa las opciones disponibles cuando se muestra un menú emergente.<br/></td>
</tr>
<tr class="odd">
<td><a href="net-string.md"><strong>NET_STRING</strong></a><br/></td>
<td>Representan los tipos de dirección de red. Use una o varias (como una combinación bit a bit) de las constantes siguientes para crear una máscara de dirección de red que se usará con la macro <a href="/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype"><strong>NetAddr_SetAllowType</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nstcfoldercapabilities"><strong>NSTCFOLDERCAPABILITIES</strong></a><br/></td>
<td>Especifica el estado de un elemento de árbol. Estos valores los usan los métodos de la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrolfoldercapabilities"><strong>INameSpaceTreeControlFolderCapabilities</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate"><strong>NSTCITEMSTATE</strong></a><br/></td>
<td>Especifica el estado de un elemento de árbol. Estos valores los usan los métodos de la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_nstcstyle"><strong>NSTCSTYLE</strong></a><br/></td>
<td>Describe las características de un control de árbol de espacios de nombres determinado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-nstcstyle2"><strong>NSTCSTYLE2</strong></a><br/></td>
<td>Lo usan los métodos de <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrol2"><strong>INameSpaceTreeControl2</strong></a> para especificar los estilos de presentación extendidos en una vista de árbol de espacios de nombres de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nwmf"><strong>NWMF</strong></a><br/></td>
<td>Marcas usadas por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inewwindowmanager-evaluatenewwindow"><strong>INewWindowManager:: EvaluateNewWindow</strong></a>. Estos valores son factores en la decisión de si se va a mostrar una ventana emergente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-package_execution_state"><strong>PACKAGE_EXECUTION_STATE</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ne-shtypes-perceived"><strong>PERCIBA</strong></a><br/></td>
<td>Especifica el tipo percibido de un archivo. Este conjunto de constantes se usa en la función <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype"><strong>AssocGetPerceivedType</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-pubappinfoflags"><strong>PUBAPPINFOFLAGS</strong></a><br/></td>
<td>Especifica los miembros de la estructura <a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>PUBAPPINFO</strong></a> que son válidos. Estas marcas se establecen en el miembro <strong>dwMask</strong> y se pasan a <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ipublishedapp-getpublishedappinfo"><strong>IPublishedApp:: GetPublishedAppInfo</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ne-shellapi-query_user_notification_state"><strong>QUERY_USER_NOTIFICATION_STATE</strong></a><br/></td>
<td>Especifica el estado del equipo para el usuario actual en relación con la decoro del envío de una notificación. Usado por <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate"><strong>SHQueryUserNotificationState</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="hkey-type.md"><strong>Tipos de datos del registro</strong></a><br/></td>
<td>Estos tipos de datos se pueden utilizar para especificar el tipo de un valor del registro.<br/></td>
</tr>
<tr class="even">
<td><a href="regsam.md"><strong>REGSAM</strong></a><br/></td>
<td>Un tipo de datos que se usa para especificar los atributos de acceso de seguridad en el registro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions"><strong>CONOCER</strong></a><br/></td>
<td>Estas marcas se usan con la función <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shrestricted"><strong>SHRestricted</strong></a> . <strong>SHRestricted</strong> se usa para determinar si una directiva de administrador especificada está en vigor. En muchos casos, las aplicaciones deben modificar ciertos comportamientos para cumplir con las directivas aprobadas por los administradores del sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/ne-shellscalingapi-scale_change_flags"><strong>SCALE_CHANGE_FLAGS</strong></a><br/></td>
<td>Marcas que se usan para indicar el cambio de escala que se ha producido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-scnrt_status"><strong>SCNRT_STATUS</strong></a><br/></td>
<td>Indica si se habilita o deshabilita el registro asincrónico y se anula el registro para <a href="/windows/desktop/api/Shlobj/nf-shlobj-shchangenotifyregisterthread"><strong>SHChangeNotifyRegisterThread</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-tagsfbs_flags"><strong>SFBS_FLAGS</strong></a><br/></td>
<td>Especifica cómo la función <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a> debe controlar el redondeo de dígitos no mostrados.<br/></td>
</tr>
<tr class="odd">
<td><a href="sfgao.md"><strong>SFGAO</strong></a><br/></td>
<td>Atributos que se pueden recuperar en un elemento (archivo o carpeta) o conjunto de elementos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-shard"><strong>PARTICIÓN</strong></a><br/></td>
<td>Indica la interpretación de los datos pasados por <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> en su parámetro <em>PV</em> para identificar el elemento cuyas estadísticas de uso se están realizando.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-share_role"><strong>SHARE_ROLE</strong></a><br/></td>
<td>Especifica los permisos de acceso asignados a los <strong>usuarios</strong> o a la carpeta <strong>pública</strong> . Se usa en <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-createshare"><strong>CreateShare</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-getsharepermissions"><strong>GetSharePermissions</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ne-shtypes-shcolstate"><strong>SHCOLSTATE</strong></a><br/></td>
<td>Describe cómo se debe tratar una propiedad. Estos valores se definen en Shtypes. h.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_shcontf"><strong>SHCONTF</strong></a><br/></td>
<td>Determina los tipos de elementos incluidos en una enumeración. Estos valores se usan con el método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder:: EnumObjects</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-shell_link_data_flags"><strong>SHELL_LINK_DATA_FLAGS</strong></a><br/></td>
<td>Especifica la configuración de las opciones. Se usa con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinkdatalist-getflags"><strong>IShellLinkDataList:: GetFlags</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinkdatalist-setflags"><strong>IShellLinkDataList:: SetFlags</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-shell_ui_component"><strong>SHELL_UI_COMPONENT</strong></a><br/></td>
<td>Identifica el tipo de componente de interfaz de usuario que se necesita en el shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions"><strong>ShellFolderViewOptions</strong></a><br/></td>
<td>Especifica las opciones de vista devueltas por la propiedad <a href="shellfolderview-viewoptions.md"><strong>ViewOptions</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants"><strong>ShellSpecialFolderConstants</strong></a><br/></td>
<td>Especifica valores únicos, independientes del sistema, que identifican carpetas especiales. Las aplicaciones suelen usar estas carpetas, pero es posible que no tengan el mismo nombre o ubicación en ningún sistema determinado. Por ejemplo, la carpeta del sistema puede ser &quot; C:\Windows &quot; en un sistema y &quot; C:\WINNT &quot; en otro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ExDisp/ne-exdisp-shellwindowfindwindowoptions"><strong>ShellWindowFindWindowOptions</strong></a><br/></td>
<td>Especifica las opciones de búsqueda de la ventana en la colección de Windows de Shell. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Exdisp/ne-exdisp-shellwindowtypeconstants"><strong>ShellWindowTypeConstants</strong></a><br/></td>
<td>Especifica los tipos de ventanas de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_shgdnf"><strong>SHGDNF</strong></a><br/></td>
<td>Define los valores que se usan con los métodos <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-setnameof"><strong>IShellFolder:: SetNameOf</strong></a> para especificar el tipo de nombres de archivo o carpeta que usan esos métodos. <br/>
<blockquote>
<b>Nota:</b><br />
Antes de Windows 7, estos valores se empaquetaban como la enumeración SHGNO.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shglobalcounter"><strong>SHGLOBALCOUNTER</strong></a><br/></td>
<td>Identificadores para varios contadores globales o variables compartidas. Cada contador global se puede incrementar o reducir mediante <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shglobalcounterincrement"><strong>SHGlobalCounterIncrement</strong></a> y <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shglobalcounterdecrement"><strong>SHGlobalCounterDecrement</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shregdel_flags"><strong>SHREGDEL_FLAGS</strong></a><br/></td>
<td>Proporciona un conjunto de valores que indican de qué clave base se va a eliminar un elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shregenum_flags"><strong>SHREGENUM_FLAGS</strong></a><br/></td>
<td>Proporciona un conjunto de valores que indican la clave base que se utilizará para una enumeración.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ne-shellapi-shstockiconid"><strong>SHSTOCKICONID</strong></a><br/></td>
<td>Usado por <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a> para identificar qué icono de sistema de existencias se va a recuperar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_sichintf"><strong>SICHINTF</strong></a><br/></td>
<td>Se utiliza para determinar cómo comparar dos elementos de Shell. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-compare"><strong>IShellItem:: Compare</strong></a> usa este tipo enumerado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sigdn"><strong>SIGDN</strong></a><br/></td>
<td>Solicita la forma del nombre para mostrar de un elemento que se va a recuperar a través de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname"><strong>IShellItem:: getDisplayName</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetnamefromidlist"><strong>SHGetNameFromIDList</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-spaction"><strong>SPACTION</strong></a><br/></td>
<td>Describe una acción que se está llevando a cabo y que requiere que se muestre el progreso al usuario mediante una interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>IActionProgress</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_spbeginf"><strong>SPBEGINF</strong></a><br/></td>
<td>Usado por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-begin"><strong>IActionProgress:: Begin</strong></a>, estas constantes especifican ciertas operaciones de la interfaz de usuario que se van a habilitar o deshabilitar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sptext"><strong>SPTEXT</strong></a><br/></td>
<td>Especifica el tipo de texto descriptivo que se proporciona a una interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>IActionProgress</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="srrf.md"><strong>SRRF</strong></a><br/></td>
<td>Marcas que restringen los datos que se van a establecer o devolver.<br/></td>
</tr>
<tr class="odd">
<td><a href="ssf-constants.md"><strong>Constantes de SSF</strong></a><br/></td>
<td>Lo utiliza la función <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>SHGetSetSettings</strong></a> para especificar qué miembros de su estructura <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>SHELLSTATE</strong></a> se deben establecer o recuperar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-stpflag"><strong>STPFLAG</strong></a><br/></td>
<td>Lo usa el método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties"><strong>ITaskbarList4:: SetTabProperties</strong></a> para especificar las propiedades de la ficha.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-svuia_status"><strong>SVUIA_STATUS</strong></a><br/></td>
<td>Se usa con el método <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-_uiactivateview"><strong>IBrowserService2:: _UIActivateView</strong></a> para establecer el estado de una vista de explorador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_cancel_request"><strong>SYNCMGR_CANCEL_REQUEST</strong></a><br/></td>
<td>Describe una solicitud del usuario para cancelar una sincronización.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_conflict_item_type"><strong>SYNCMGR_CONFLICT_ITEM_TYPE</strong></a><br/></td>
<td>Describe el tipo de elemento de conflicto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_control_flags"><strong>SYNCMGR_CONTROL_FLAGS</strong></a><br/></td>
<td>Especifica cómo debe realizarse una operación solicitada en ciertos métodos de <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>ISyncMgrControl</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_event_flags"><strong>SYNCMGR_EVENT_FLAGS</strong></a><br/></td>
<td>Especifica marcas para un evento de sincronización.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_event_level"><strong>SYNCMGR_EVENT_LEVEL</strong></a><br/></td>
<td>Especifica el tipo de evento del que se va a informar al centro de sincronización.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_capabilities"><strong>SYNCMGR_HANDLER_CAPABILITIES</strong></a><br/></td>
<td>Especifica las capacidades de un controlador con respecto a las acciones que se pueden realizar con él.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_policies"><strong>SYNCMGR_HANDLER_POLICIES</strong></a><br/></td>
<td>Enumera las directivas especificadas por un controlador de sincronización que se desvían de la directiva predeterminada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_type"><strong>SYNCMGR_HANDLER_TYPE</strong></a><br/></td>
<td>Especifica el tipo de un controlador. Usado por <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrhandlerinfo-gettype"><strong>ISyncMgrHandlerInfo:: GetType</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_item_capabilities"><strong>SYNCMGR_ITEM_CAPABILITIES</strong></a><br/></td>
<td>Especifica las acciones que se pueden realizar en un elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_item_policies"><strong>SYNCMGR_ITEM_POLICIES</strong></a><br/></td>
<td>Especifica las directivas de un elemento para controlar cómo pueden habilitarse o deshabilitarse mediante la Directiva de grupo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_presenter_choice"><strong>SYNCMGR_PRESENTER_CHOICE</strong></a><br/></td>
<td>Describe la opción que realiza un usuario acerca de una resolución de conflictos del administrador de sincronización. Usado por <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>ISyncMgrConflictPresenter</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_presenter_next_step"><strong>SYNCMGR_PRESENTER_NEXT_STEP</strong></a><br/></td>
<td>Describe el siguiente paso que debe producirse en la resolución de conflictos del administrador de sincronización. Usado por <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>ISyncMgrConflictPresenter</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_progress_status"><strong>SYNCMGR_PROGRESS_STATUS</strong></a><br/></td>
<td>Especifica el estado de progreso actual de un proceso de sincronización. Usado por <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsynccallback-reportprogress"><strong>ISyncMgrSyncCallback:: ReportProgress</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_resolution_abilities"><strong>SYNCMGR_RESOLUTION_ABILITIES</strong></a><br/></td>
<td>Indica las capacidades y la actividad de resolución de conflictos que se va a seguir. Se usa con <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrresolutionhandler-queryabilities"><strong>ISyncMgrResolutionHandler:: QueryAbilities</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_resolution_feedback"><strong>SYNCMGR_RESOLUTION_FEEDBACK</strong></a><br/></td>
<td>Describe los comentarios de Administrador de sincronización resolución. Usado por <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrresolutionhandler"><strong>ISyncMgrResolutionHandler</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_sync_control_flags"><strong>SYNCMGR_SYNC_CONTROL_FLAGS</strong></a><br/></td>
<td>Indica las marcas usadas por <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync"><strong>ISyncMgrControl:: StartHandlerSync</strong></a> y <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync"><strong>ISyncMgrControl:: StartItemSync</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrflag"><strong>SYNCMGRFLAG</strong></a><br/></td>
<td>Los valores de enumeración <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrflag"><strong>SYNCMGRFLAG</strong></a> se usan en el método <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize"><strong>ISyncMgrSynchronize:: Initialize</strong></a> para indicar cómo se inició el evento de sincronización.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrhandlerflags"><strong>SYNCMGRHANDLERFLAGS</strong></a><br/></td>
<td>Se usa en la estructura <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>SYNCMGRHANDLERINFO</strong></a> como marcas que se aplican al controlador actual.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrinvokeflags"><strong>SYNCMGRINVOKEFLAGS</strong></a><br/></td>
<td>El valor de enumeración <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrinvokeflags"><strong>SYNCMGRINVOKEFLAGS</strong></a> especifica cómo se va a invocar el administrador de sincronización en el método <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizeinvoke-updateitems"><strong>ISyncMgrSynchronizeInvoke:: UpdateItems</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgritemflags"><strong>SYNCMGRITEMFLAGS</strong></a><br/></td>
<td>Especifica información del elemento actual en la estructura <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrloglevel"><strong>SYNCMGRLOGLEVEL</strong></a><br/></td>
<td>Los valores de enumeración <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrloglevel"><strong>SYNCMGRLOGLEVEL</strong></a> especifican un nivel de error para su uso en el método <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>ISyncMgrSynchronizeCallback:: LogError</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrregisterflags"><strong>SYNCMGRREGISTERFLAGS</strong></a><br/></td>
<td>Los valores de enumeración <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrregisterflags"><strong>SYNCMGRREGISTERFLAGS</strong></a> se usan en métodos de la interfaz <a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>ISyncMgrRegister</strong></a> para identificar los eventos para los que el controlador está registrado para recibir notificaciones.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrstatus"><strong>SYNCMGRSTATUS</strong></a><br/></td>
<td>Se usa en el método <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setitemstatus"><strong>ISyncMgrSynchronize:: SetItemStatus</strong></a> para especificar el estado actualizado del elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonflags"><strong>THUMBBUTTONFLAGS</strong></a><br/></td>
<td>Usado por <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>THUMBBUTTON</strong></a> para controlar los Estados y comportamientos específicos del botón.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonmask"><strong>THUMBBUTTONMASK</strong></a><br/></td>
<td>Lo utiliza la estructura <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>THUMBBUTTON</strong></a> para especificar qué miembros de esa estructura contienen datos válidos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/thumbnailstreamcache/ne-thumbnailstreamcache-thumbnailstreamcacheoptions"><strong>ThumbnailStreamCacheOptions</strong></a><br/></td>
<td>Define las opciones de caché usadas por la interfaz <a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache"><strong>IThumbnailStreamCache</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags"><strong>TRANSFER_SOURCE_FLAGS</strong></a><br/></td>
<td>Lo usan los métodos de las interfaces <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>ITransferSource</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>ITransferDestination</strong></a> para controlar sus operaciones de archivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-translateurl_in_flags"><strong>TRANSLATEURL_IN_FLAGS</strong></a><br/></td>
<td>Los valores enumerados de <a href="/windows/desktop/api/Intshcut/ne-intshcut-translateurl_in_flags"><strong>TRANSLATEURL_IN_FLAGS</strong></a> se usan con la función <a href="/windows/desktop/api/Intshcut/nf-intshcut-translateurla"><strong>TRANSLATEURL</strong></a> para determinar cómo se ejecutará.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-undock_reason"><strong>UNDOCK_REASON</strong></a><br/></td>
<td>Valores que indican la razón por la que se ha desacoplado una ventana de aplicación de accesibilidad acoplada. Usado por <a href="/windows/desktop/api/shobjidl/nf-shobjidl-iaccessibilitydockingservicecallback-undocked"><strong>IAccessibilityDockingServiceCallback:: undocked</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-url_scheme"><strong>URL_SCHEME</strong></a><br/></td>
<td>Se usa para especificar los esquemas de dirección URL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-urlassociationdialog_in_flags"><strong>URLASSOCIATIONDIALOG_IN_FLAGS</strong></a><br/></td>
<td>Los valores enumerados de <a href="/windows/desktop/api/Intshcut/ne-intshcut-urlassociationdialog_in_flags"><strong>URLASSOCIATIONDIALOG_IN_FLAGS</strong></a> se usan con <a href="/windows/desktop/api/Intshcut/nf-intshcut-urlassociationdialoga"><strong>URLASSOCIATIONDIALOG</strong></a> para determinar cómo se ejecuta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-vpcolorflags"><strong>VPCOLORFLAGS</strong></a><br/></td>
<td>Especifica el uso de un color. Lo usan los métodos <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ivisualproperties"><strong>IVisualProperties</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-vpwatermarkflags"><strong>VPWATERMARKFLAGS</strong></a><br/></td>
<td>Especifica marcas de marca de agua. Usado por <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-ivisualproperties-setwatermark"><strong>IVisualProperties:: SetWatermark</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

 

 
