---
description: 'Un conjunto de claves de cadena que se usan con el método IBindCtx:: RegisterObjectParam para especificar un contexto de enlace.'
title: Enlazar claves de cadena de contexto (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d89a0ee1-9a4b-48a4-8965-0d92f09743a6
api_name:
- STR_AVOID_DRIVE_RESTRICTION_POLICY
- STR_BIND_DELEGATE_CREATE_OBJECT
- STR_BIND_FOLDER_ENUM_MODE
- STR_BIND_FOLDERS_READ_ONLY
- STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE
- STR_DONT_PARSE_RELATIVE
- STR_DONT_RESOLVE_LINK
- STR_FILE_SYS_FIND_DATA
- STR_FILE_SYS_BIND_DATA_WIN7_FORMAT
- STR_GET_ASYNC_HANDLER
- STR_GPS_BESTEFFORT
- STR_GPS_DELAYCREATION
- STR_GPS_FASTPROPERTIESONLY
- STR_GPS_HANDLERPROPERTIESONLY
- STR_GPS_NO_OPLOCK
- STR_GPS_OPENSLOWITEM
- STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK
- STR_IFILTER_LOAD_DEFINED_FILTER
- STR_INTERNAL_NAVIGATE
- STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE
- STR_ITEM_CACHE_CONTEXT
- STR_NO_VALIDATE_FILENAME_CHARS
- STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS
- STR_PARSE_AND_CREATE_ITEM
- STR_PARSE_DONT_REQUIRE_VALIDATED_URLS
- STR_PARSE_PARTIAL_IDLIST
- STR_PARSE_PREFER_FOLDER_BROWSING
- STR_PARSE_PREFER_WEB_BROWSING
- STR_PARSE_PROPERTYSTORE
- STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS
- STR_PARSE_SHOW_NET_DIAGNOSTICS_UI
- STR_PARSE_SKIP_NET_CACHE
- STR_PARSE_TRANSLATE_ALIASES
- STR_PARSE_WITH_PROPERTIES
- STR_PROPERTYBAG_PARAM
- STR_SKIP_BINDING_CLSID
- STR_TRACK_CLSID
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b1dcdb3b9199fede88d6f13949cc9276bde17b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986119"
---
# <a name="bind-context-string-keys"></a>Enlazar claves de cadena de contexto

Un conjunto de claves de cadena que se usan con el método [**IBindCtx:: RegisterObjectParam**](/windows/win32/api/objidl/nf-objidl-ibindctx-registerobjectparam) para especificar un contexto de enlace.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_AVOID_DRIVE_RESTRICTION_POLICY"></span><span id="str_avoid_drive_restriction_policy"></span><dl> <dt><strong>STR_AVOID_DRIVE_RESTRICTION_POLICY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows XP SP2</strong>. Especifique este contexto de enlace para permitir que los clientes del origen de datos invaliden la Directiva de Letras de unidad ocultas y habilite el acceso a los objetos de vista para los orígenes de datos en las unidades bloqueadas.<br/> Se usa con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: BindToHandler</strong></a>.<br/> El sistema admite directivas controladas por el administrador que ocultan las letras de unidad especificadas para impedir que los usuarios tengan acceso a esas unidades a través del explorador de Windows. Cuando esta directiva está activa, el resultado es que los objetos de vista y otros controladores creados con el método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject"><strong>IShellFolder:: CreateViewObject</strong></a> producirán un error cuando se llamen en unidades bloqueadas por la Directiva.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_DELEGATE_CREATE_OBJECT"></span><span id="str_bind_delegate_create_object"></span><dl> <dt><strong>STR_BIND_DELEGATE_CREATE_OBJECT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows Vista</strong>. Especifique este contexto de enlace para que el método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> use el objeto especificado por el parámetro <em>PBC</em> para crear el objeto de destino. en este caso, el objeto especificado por el parámetro <em>punk</em> en la llamada <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx:: RegisterObjectParam</strong></a> debe implementar la interfaz <a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>ICreateObject</strong></a> . <br/> Se usa con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: BindToHandler</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FOLDER_ENUM_MODE"></span><span id="str_bind_folder_enum_mode"></span><dl> <dt><strong>STR_BIND_FOLDER_ENUM_MODE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 7</strong>. Se pasa a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> con un valor <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode"><strong>FOLDER_ENUM_MODE</strong></a> para controlar el modo de enumeración del elemento analizado. El valor <strong>FOLDER_ENUM_MODE</strong> se pasa en el contexto de enlace a través de un objeto que implementa <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>IObjectWithFolderEnumMode</strong></a>. <br/> Los elementos con modos de enumeración diferentes se comparan de modo canónico (SHCIDS_CANONICALONLY) diferentes porque enumeran diferentes conjuntos de elementos.<br/> Si un elemento no admite el modo de enumeración (porque no es una carpeta o no proporciona el modo de enumeración), se crea en el modo de enumeración predeterminado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_FOLDERS_READ_ONLY"></span><span id="str_bind_folders_read_only"></span><dl> <dt><strong>STR_BIND_FOLDERS_READ_ONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 7</strong>. Se pasa a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> junto con <strong>STR_FILE_SYS_BIND_DATA</strong>. Esto fuerza el análisis sencillo mientras que también busca archivos Desktop.ini a lo largo de la ruta de acceso desde la que se va a obtener una cadena de nombre traducida. Esto evita el sondeo de carpetas a lo largo de la ruta de acceso, que, en el caso de una carpeta que representa un servidor o un recurso compartido, puede llevar mucho tiempo y recursos. Desktop.ini archivos se almacenan en caché en algunas ubicaciones, por lo que será al menos tan eficaz como el sondeo de los atributos de carpeta y, a continuación, el sondeo de la Desktop.ini si esa carpeta debe hacer que la ou sea de solo lectura.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE"></span><span id="str_bind_force_folder_shortcut_resolve"></span><dl> <dt><strong>STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows XP SP2</strong>. Especifique este contexto de enlace para forzar que un acceso directo a la carpeta resuelva el vínculo que apunta a su destino. <br/> Un acceso directo de carpeta es un elemento de carpeta que apunta a otro elemento de carpeta en el mismo espacio de nombres, mediante un vínculo (acceso directo) que contiene el IDList del destino. El vínculo se resuelve para realizar el seguimiento del destino en caso de que se mueva o cambie de nombre. Por ejemplo, la carpeta <strong>mis sitios de red</strong> de Windows XP y la carpeta <strong>equipo</strong> de Windows Vista pueden contener accesos directos a carpetas creados con el Asistente para <strong>Agregar ubicación de red</strong> . Para mejorar el rendimiento, el método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> no resuelve los vínculos a la carpeta de red de forma predeterminada.<br/> Se usa con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: BindToHandler</strong></a>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_DONT_PARSE_RELATIVE"></span><span id="str_dont_parse_relative"></span><dl> <dt><strong>STR_DONT_PARSE_RELATIVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows XP</strong>. Especifique este contexto de enlace para evitar que una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> de la carpeta <strong>Desktop</strong> trate de tratar las rutas de acceso relativas en relación con el escritorio. en tal caso, se produce un error de análisis cuando se especifica este contexto de enlace.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_DONT_RESOLVE_LINK"></span><span id="str_dont_resolve_link"></span><dl> <dt><strong>STR_DONT_RESOLVE_LINK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows Vista</strong>. Especifique este contexto de enlace para indicar a un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> que no resuelva el destino de vínculo obtenido al usar el GUID de <strong>BHID_LinkTargetItem</strong> en <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: BindToHandler</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_FILE_SYS_FIND_DATA"></span><span id="str_file_sys_find_data"></span><dl> <dt><strong>STR_FILE_SYS_FIND_DATA</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows XP</strong>. Especifique este contexto de enlace para proporcionar metadatos de archivo al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> , que se usa en lugar de intentar recuperar los metadatos de archivo reales. El objeto asociado debe implementar <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a> y, opcionalmente, también puede implementar <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>IFileSystemBindData2</strong></a>. De forma predeterminada, el método <strong>IShellFolder::P arsedisplayname</strong> comprueba que el archivo existe y usa los metadatos reales del archivo para rellenar la lista de identificadores.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_FILE_SYS_BIND_DATA_WIN7_FORMAT"></span><span id="str_file_sys_bind_data_win7_format"></span><dl> <dt><strong>STR_FILE_SYS_BIND_DATA_WIN7_FORMAT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 8.1</strong>. Especifique este contexto de enlace para indicar que los datos proporcionados en el contexto de enlace de <strong>STR_FILE_SYS_FIND_DATA</strong> deben usarse para crear una lista de Itemid en el formato de Windows 7.&quot;<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GET_ASYNC_HANDLER"></span><span id="str_get_async_handler"></span><dl> <dt><strong>STR_GET_ASYNC_HANDLER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 7</strong>. Especifique este contexto de enlace cuando el controlador se recupera en el mismo subproceso que la interfaz de usuario. Se deben evitar las actividades que consumen mucha memoria, como las que implican el acceso al disco o a la red.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_BESTEFFORT"></span><span id="str_gps_besteffort"></span><dl> <dt><strong>STR_GPS_BESTEFFORT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows Vista</strong>. Especifique este contexto de enlace al solicitar un controlador <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Este valor se usa con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Vea la marca de <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_BESTEFFORT</strong></a> para obtener más información.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_DELAYCREATION"></span><span id="str_gps_delaycreation"></span><dl> <dt><strong>STR_GPS_DELAYCREATION</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows Vista</strong>. Especifique este contexto de enlace al solicitar un controlador <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Este valor se usa con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Vea la marca de <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_DELAYCREATION</strong></a> para obtener más información.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_FASTPROPERTIESONLY"></span><span id="str_gps_fastpropertiesonly"></span><dl> <dt><strong>STR_GPS_FASTPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows Vista</strong>. Especifique este contexto de enlace al solicitar un controlador <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Este valor se usa con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Vea la marca de <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_FASTPROPERTIESONLY</strong></a> para obtener más información.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_HANDLERPROPERTIESONLY"></span><span id="str_gps_handlerpropertiesonly"></span><dl> <dt><strong>STR_GPS_HANDLERPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows Vista</strong>. Especifique este contexto de enlace al solicitar un controlador <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Este valor se usa con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Vea la marca de <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_HANDLERPROPERTIESONLY</strong></a> para obtener más información.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_NO_OPLOCK"></span><span id="str_gps_no_oplock"></span><dl> <dt><strong>STR_GPS_NO_OPLOCK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 7</strong>. Especifique este contexto de enlace al solicitar un controlador <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Este valor se usa con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Vea la marca de <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_NO_OPLOCK</strong></a> para obtener más información.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_OPENSLOWITEM"></span><span id="str_gps_openslowitem"></span><dl> <dt><strong>STR_GPS_OPENSLOWITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows Vista</strong>. Especifique este contexto de enlace al solicitar un controlador <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Este valor se usa con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Vea la marca de <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_OPENSLOWITEM</strong></a> para obtener más información.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK"></span><span id="str_ifilter_force_text_filter_fallback"></span><dl> <dt><strong>STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Solo Windows Vista.</strong> Especifique este contexto de enlace para que se produzca una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> que solicita la interfaz de <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> para que un objeto del sistema de archivos devuelva un filtro de texto si no hay ningún otro filtro disponible. Este valor no se define a partir de Windows 7.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_IFILTER_LOAD_DEFINED_FILTER"></span><span id="str_ifilter_load_defined_filter"></span><dl> <dt><strong>STR_IFILTER_LOAD_DEFINED_FILTER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Solo Windows Vista.</strong> Especifique este contexto de enlace para que se produzca una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> que solicita a la interfaz <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> para un objeto de sistema de archivos que no devuelva un filtro de reserva si no se encuentra ningún filtro registrado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_INTERNAL_NAVIGATE"></span><span id="str_internal_navigate"></span><dl> <dt><strong>STR_INTERNAL_NAVIGATE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows Vista</strong>. Especifique este contexto de enlace para habilitar la carga del historial de un flujo para una navegación interna cuando se llama al método <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768216(v=vs.85)"><strong>IPersistHistory:: LoadHistory</strong></a> . Una navegación interna es una navegación dentro de la misma vista.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE"></span><span id="str_internetfolder_parse_only_urlmon_bindable"></span><dl> <dt><strong>STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 7</strong>. Especifique este contexto de enlace con STR_PARSE_PREFER_FOLDER_BROWSING cuando el cliente desea que los controladores de carpetas del shell de Internet generen un IDList para cualquier dirección URL válida si no se puede crear una carpeta de tipo DAV para esa dirección URL. No se comprueba que la dirección URL exista; solo se comprueba su sintaxis y tiene un controlador de protocolo registrado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_ITEM_CACHE_CONTEXT"></span><span id="str_item_cache_context"></span><dl> <dt><strong>STR_ITEM_CACHE_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 7</strong>. Especifique este contexto de enlace para indicar a las implementaciones de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> y <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3:: InitializeEx</strong></a> para almacenar en caché objetos auxiliares que consumen mucha memoria y que pueden existir en las instancias de elementos de Shell en lugar de volver a crear estos objetos cada vez que se crea un elemento de Shell. El objeto asociado es otro objeto de contexto de enlace, inicialmente vacío. Esto debería producir un objeto de contexto de enlace independiente, al que se tiene acceso a través de <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx:: GetObjectParam</strong></a> o <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx:: register. ObjectParam</strong></a>. <br/> Un llamador debe participar en este comportamiento proporcionando este parámetro de contexto de enlace al llamar a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a>. Al hacerlo, se optimiza el comportamiento del enlace a varios nombres de análisis en sucesión. La duración del objeto de contexto de enlace debe abarcar varias instancias de elementos de Shell y sus contextos de enlace individuales.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_NO_VALIDATE_FILENAME_CHARS"></span><span id="str_no_validate_filename_chars"></span><dl> <dt><strong>STR_NO_VALIDATE_FILENAME_CHARS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows Vista</strong>. Especifique este contexto de enlace para permitir que los caracteres de nombre de archivo no válidos aparezcan en los nombres de archivo. De forma predeterminada, una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> rechaza los caracteres que no son válidos en los nombres de archivo. Este contexto de enlace solo es significativo junto con el contexto de enlace STR_FILE_SYS_FIND_DATA.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS"></span><span id="str_parse_allow_internet_shell_folders"></span><dl> <dt><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows Vista</strong>. Especifique este contexto de enlace para habilitar una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> en la carpeta <strong>Desktop</strong> para analizar las direcciones URL. Si se especifica este contexto de enlace, invalida <strong><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_AND_CREATE_ITEM"></span><span id="str_parse_and_create_item"></span><dl> <dt><strong>STR_PARSE_AND_CREATE_ITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 7</strong>. Especifique este contexto de enlace para indicar a la implementación de un origen de datos de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> para optimizar el comportamiento de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a>. <br/> Normalmente, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a> realiza dos operaciones de enlace en el nombre que se va a analizar: una a una y otra a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> y otra para crear el elemento de Shell. Cuando se admite el contexto de enlace de <strong>STR_PARSE_AND_CREATE_ITEM</strong> , el segundo enlace se evita creando el elemento de Shell durante la <strong>IShellFolder::P</strong> enlace de arsedisplayname y almacenando el elemento de Shell a través de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iparseandcreateitem-setitem"><strong>IParseAndCreateItem:: SetItem</strong></a>. A continuación, <strong>SHCreateItemFromParsingName</strong> usa el elemento Shell almacenado en lugar de crear uno.<br/> Este parámetro se aplica al último elemento del nombre que se analiza. Por ejemplo, en el nombre &quot;C:\Folder1\File.txt, los datos se aplican a File.txt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_DONT_REQUIRE_VALIDATED_URLS"></span><span id="str_parse_dont_require_validated_urls"></span><dl> <dt><strong>STR_PARSE_DONT_REQUIRE_VALIDATED_URLS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Solo Windows Vista.</strong> Especifica que, al analizar una dirección URL, este contexto de enlace no debe requerir que la dirección URL exista antes de generar un IDList para ella. Especifique este contexto de enlace junto con <strong><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></strong> cuando el cliente represente que los controladores de carpetas del <strong>Shell de Internet</strong> generan un IDList para la dirección URL si no se puede crear una carpeta DAV para la dirección URL especificada.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PARTIAL_IDLIST"></span><span id="str_parse_partial_idlist"></span><dl> <dt><strong>STR_PARSE_PARTIAL_IDLIST</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows Vista</strong>. Especifique este contexto de enlace para pasar el elemento original que se va a analizar cuando dicho elemento se almacena como un objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> que también implementa la interfaz <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a> . Antes de Windows 7, este valor no se definió en un archivo de encabezado. Puede ser definido por el llamador o pasarse como el valor de cadena <strong>de &quot; L &quot; ParseOriginalItem</strong>. A partir de Windows 7, el valor se define en ShlObj. h. Tenga en cuenta que se trata de un encabezado diferente que las demás constantes STR.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_FOLDER_BROWSING"></span><span id="str_parse_prefer_folder_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows XP</strong>. Especifique este contexto de enlace para habilitar una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> en la carpeta <strong>Desktop</strong> para analizar las direcciones URL como si fueran carpetas. Utilice este contexto de enlace para enlazar con un servidor WebDAV.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_WEB_BROWSING"></span><span id="str_parse_prefer_web_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows Vista</strong>. Especifique este contexto de enlace para evitar una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> en las direcciones URL de análisis del formulario de carpetas de <strong>escritorio</strong> . <strong><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></strong>puede invalidar este contexto de enlace.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PROPERTYSTORE"></span><span id="str_parse_propertystore"></span><dl> <dt><strong>STR_PARSE_PROPERTYSTORE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows Vista</strong>. Especifique este contexto de enlace para invalidar el almacén de propiedades predeterminado que usa el método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> y, en su lugar, use el almacén de propiedades especificado como parámetro BIND. Se aplica a las carpetas delegadas.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS"></span><span id="str_parse_shell_protocol_to_file_objects"></span><dl> <dt><strong>STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows XP SP2</strong>. Especifique este contexto de enlace para habilitar una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> en la carpeta <strong>Desktop</strong> para usar la &quot; notación Shell: &quot; prefix para tener acceso a los archivos.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_SHOW_NET_DIAGNOSTICS_UI"></span><span id="str_parse_show_net_diagnostics_ui"></span><dl> <dt><strong>STR_PARSE_SHOW_NET_DIAGNOSTICS_UI</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows Vista</strong>. Especifique este contexto de enlace para que se produzca una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> para mostrar el cuadro de diálogo diagnósticos de red si se produce un error en el análisis de una ruta de acceso de red.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SKIP_NET_CACHE"></span><span id="str_parse_skip_net_cache"></span><dl> <dt><strong>STR_PARSE_SKIP_NET_CACHE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows Vista</strong>. Especifique este contexto de enlace para que se produzca una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> para omitir la comprobación de la memoria caché de recursos compartidos de red y póngase en contacto directamente con el servidor de red. La información sobre los recursos compartidos de red se almacena en caché para mejorar el rendimiento y <strong>IShellFolder::P arsedisplayname</strong> comprueba esta caché de forma predeterminada.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_TRANSLATE_ALIASES"></span><span id="str_parse_translate_aliases"></span><dl> <dt><strong>STR_PARSE_TRANSLATE_ALIASES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows XP</strong>. Especifique este contexto de enlace para pasar las propiedades analizadas al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> para un espacio de nombres de delegado. El espacio de nombres puede usar las propiedades pasadas en lugar de intentar analizar el propio nombre.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_WITH_PROPERTIES"></span><span id="str_parse_with_properties"></span><dl> <dt><strong>STR_PARSE_WITH_PROPERTIES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Solo Windows Vista.</strong> Contexto de enlace de análisis que se usa para pasar un conjunto de propiedades y el nombre del elemento cuando se llama a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a>. El objeto en el contexto de enlace implementa <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> y se recupera llamando a <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx:: GetObjectParam</strong></a>.<br/> DBFolder es un origen de datos de Shell que representa elementos en los resultados de la búsqueda y en las vistas basadas en consultas. DBFolder recupera estos elementos consultando el sistema de Windows Search. Los elementos de los resultados de la búsqueda se identifican mediante un esquema de protocolo, por ejemplo, &quot; archivo: &quot; o &quot; MAPI: &quot; . DBFolder proporciona el comportamiento de estos elementos mediante la delegación de orígenes de datos de Shell que se crean para estos protocolos. Vea <a href="/previous-versions/bb233544(v=msdn.10)">desarrollar complementos de controlador de protocolo</a> para obtener más información.<br/> Cuando DBFolder delega su operación de análisis en los orígenes de datos de Shell que admiten los protocolos de Windows Search, este contexto de enlace proporciona acceso a los valores que se devolvieron en el resultado de la consulta para ese elemento. Entre estas estructuras se incluyen las siguientes:<br/>
<ul>
<li><a href="/windows/desktop/properties/props-system-itemtype">System. ItemType</a> (PKEY_ItemType)</li>
<li><a href="/windows/desktop/properties/props-system-parsingpath">System. ParsingPath</a> (PKEY_ParsingPath)</li>
<li><a href="/windows/desktop/properties/props-system-itempathdisplay">System. ItemPathDisplay</a> (PKEY_ItemPathDisplay)</li>
<li><a href="/windows/desktop/properties/props-system-itemnamedisplay">System. ItemNameDisplay</a> (PKEY_ItemNameDisplay)</li>
</ul>
<br/> Este contexto de enlace también se puede utilizar para analizar un elemento DBFolder si un cliente tiene un conjunto de propiedades que definen el elemento. En este caso, se debe pasar un nombre vacío a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a>.<br/> Antes de Windows 7, este valor no se definió en un archivo de encabezado. Puede ser definido por el llamador o pasarse como su valor de cadena: <code>L&quot;ParseWithProperties&quot;</code> . A partir de Windows 7, el valor se define en ShlObj. h. Tenga en cuenta que se trata de un encabezado diferente del lugar en el que se definen las demás constantes STR.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PROPERTYBAG_PARAM"></span><span id="str_propertybag_param"></span><dl> <dt><strong>STR_PROPERTYBAG_PARAM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 8</strong>. Especifique este contexto de enlace para indicar que el parámetro de contexto de enlace es un contenedor de propiedades (<a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)"><strong>IPropertyBag</strong></a>) que se usa para pasar valores de variante en el contexto de enlace. Vea la sección Comentarios para obtener más detalles.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_SKIP_BINDING_CLSID"></span><span id="str_skip_binding_clsid"></span><dl> <dt><strong>STR_SKIP_BINDING_CLSID</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows XP</strong>. Especifique este contexto de enlace para que las llamadas a los métodos <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> omitan una extensión de espacio de nombres de Shell determinada al analizar o enlazar. El CLSID del espacio de nombres que se va a omitir lo proporciona el método <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid"><strong>IPersist:: GetClassID</strong></a> del parámetro BIND. <br/>
<blockquote>
[!Note]<br />
Introducido en Windows 2000 SP3, este valor se definió en ShlObj. h hasta Windows XP, cuando se trasladó a shobjidl. h.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_TRACK_CLSID"></span><span id="str_track_clsid"></span><dl> <dt><strong>STR_TRACK_CLSID</strong></dt> </dl></td>
<td style="text-align: left;">No se utiliza.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Observaciones

Los contextos de enlace se usan para pasar parámetros opcionales a las funciones que tienen un \* parámetro IBindCtx. Estos parámetros se expresan como objetos COM y pueden implementar interfaces que se usan para modelar los datos de los parámetros. Algunos contextos de enlace representan un valor booleano, donde **true** indica un objeto que implementa solo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) y False indica que no hay ningún objeto presente.

[**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname), [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) y [**IShellItem:: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) toman un contexto de enlace y se pueden pasar parámetros a través de ese contexto de enlace.

Algunos contextos de enlace son específicos de determinadas implementaciones de orígenes de datos o tipos de controlador.

Los parámetros de contexto de enlace se definen para su uso con una función o un método específicos.

Al solicitar un almacén de propiedades a través de [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), puede especificar el equivalente [**del \_ valor predeterminado de GPS**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags) pasando un parámetro [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) nulo. También puede especificar el equivalente de ReadWrite de GPS \_ pasando un modo de STGM \_ ReadWrite \| STGM \_ exclusivo en el contexto de enlace.

La bolsa de propiedades especificada por el objeto de contexto del enlace de **\_ \_ parámetros PROPERTYBAG de Str** contiene valores adicionales a los que se puede tener acceso con los métodos [**IPropertyBag:: Read**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768197(v=vs.85)) y [**IPropertyBag:: Write**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768198(v=vs.85)) .



| Nombre de propiedad                                 | Tipo     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_marcas de elementos de enumeración Str \_ \_                       | VT \_ UI4  | **Introducido en Windows 8**. Especifica un valor de [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) que se va a pasar a [**IShellFolder:: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) cuando se llama a [**IShellItem:: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) con **BHID \_ EnumItems**.                                                                                                                                                                                                                         |
| la \_ asociación explícita del análisis de Str se \_ \_ \_ realizó correctamente | VT \_ bool | **Introducido en Windows 7**. El método [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) establece esta propiedad para indicar al llamador que el IDList devuelto se ha enlazado al [identificador de programa (ProgID](fa-progids.md) ) especificado con el **\_ análisis de Str con el \_ \_ \_ ProgID explícito** o la aplicación especificada con el **análisis Str \_ \_ con \_ \_ ASSOCAPP explícito**. Cuando no está presente la **\_ \_ asociación explícita del \_ \_ análisis de Str** , el ProgID o la aplicación no se enlazaron a IDList. |
| \_análisis \_ de Str \_ con \_ ASSOCAPP explícitos          | VT \_ BSTR | **Introducido en Windows 7**. Especifique esta propiedad para que se produzca una llamada al método [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) para devolver una IDList enlazada al controlador de asociaciones de tipo de archivo de la aplicación.                                                                                                                                                                                                                                          |
| \_análisis \_ de Str con \_ \_ ProgID explícito            | VT \_ BSTR | **Introducido en Windows 7**. Especifique esta propiedad para que se produzca una llamada al método [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) para devolver una IDList enlazada al controlador de Asociación de archivo del [ProgID](fa-progids.md)proporcionado.                                                                                                                                                                                                                          |



 

Vea el [ejemplo de análisis con parámetros](samples-parsingwithparameters.md) para obtener un ejemplo del uso de valores de contexto de enlace.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 
