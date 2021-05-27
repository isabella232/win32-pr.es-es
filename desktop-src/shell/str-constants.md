---
description: Conjunto de claves de cadena que se usan con el método IBindCtx::RegisterObjectParam para especificar un contexto de enlace.
title: Enlazar claves de cadena de contexto (Shobjidl.h)
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
ms.openlocfilehash: 2bf8dc681718e64bf8aea059027a50148650635e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549250"
---
# <a name="bind-context-string-keys"></a>Enlazar claves de cadena de contexto

Conjunto de claves de cadena que se usan con [**el método IBindCtx::RegisterObjectParam**](/windows/win32/api/objidl/nf-objidl-ibindctx-registerobjectparam) para especificar un contexto de enlace.



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
<td style="text-align: left;"><strong>Introducido en Windows XP SP2.</strong> Especifique este contexto de enlace para permitir que los clientes del origen de datos invaliden la directiva de letra de unidad oculta y habiliten el acceso a los objetos de vista para los orígenes de datos en las unidades bloqueadas.<br/> Se usa <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>con IShellFolder::BindToObject</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler</strong></a>.<br/> El sistema admite directivas controladas por el administrador que ocultan las letras de unidad especificadas para impedir que los usuarios accedan a esas unidades Explorador de Windows. Cuando esta directiva está activa, el resultado es que los objetos de vista y otros controladores creados con el método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject"><strong>IShellFolder::CreateViewObject</strong></a> producirán un error cuando se llame a en unidades bloqueadas por la directiva.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_DELEGATE_CREATE_OBJECT"></span><span id="str_bind_delegate_create_object"></span><dl> <dt><strong>STR_BIND_DELEGATE_CREATE_OBJECT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Se introdujo en Windows Vista</strong>. Especifique este contexto de enlace para que el método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> use el objeto especificado por el parámetro <em>parameter parameter</em> para crear el objeto de destino; En este caso, el objeto especificado por el parámetro <em>parameter de la</em> llamada <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx::RegisterObjectParam</strong></a> debe implementar la <a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>interfaz ICreateObject.</strong></a> <br/> Se usa <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>con IShellFolder::BindToObject</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FOLDER_ENUM_MODE"></span><span id="str_bind_folder_enum_mode"></span><dl> <dt><strong>STR_BIND_FOLDER_ENUM_MODE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 7.</strong> Se pasa <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>a IShellFolder::P arseDisplayName</strong></a> con un valor <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode"><strong>FOLDER_ENUM_MODE</strong></a> para controlar el modo de enumeración del elemento analizada. El <strong>FOLDER_ENUM_MODE</strong> se pasa en el contexto de enlace a través de un objeto que implementa <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>IObjectWithFolderEnumMode</strong></a>. <br/> Los elementos con distintos modos de enumeración se comparan canónicamente (SHCIDS_CANONICALONLY) diferentes porque enumeran distintos conjuntos de elementos.<br/> Si un elemento no admite el modo de enumeración (porque no es una carpeta o no proporciona el modo de enumeración), se crea en el modo de enumeración predeterminado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_FOLDERS_READ_ONLY"></span><span id="str_bind_folders_read_only"></span><dl> <dt><strong>STR_BIND_FOLDERS_READ_ONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 7.</strong> Se pasa <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>a IShellFolder::P arseDisplayName</strong></a> junto con <strong>STR_FILE_SYS_BIND_DATA</strong>. Esto fuerza un análisis simple al mismo tiempo que busca archivos Desktop.ini a lo largo de la ruta de acceso de la que se obtiene una cadena de nombre localizada. Esto evita el sondeo de carpetas a lo largo de la ruta de acceso, lo que, en un caso de una carpeta que representa un servidor o un recurso compartido, podría tardar mucho tiempo y recursos. Desktop.ini archivos se almacenan en caché en algunas ubicaciones, por lo que será al menos tan eficaz como sonding para los atributos de carpetas y, a continuación, sondeando para el Desktop.ini si esa carpeta debe volver ou tot ser de solo lectura.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE"></span><span id="str_bind_force_folder_shortcut_resolve"></span><dl> <dt><strong>STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows XP SP2.</strong> Especifique este contexto de enlace para forzar un acceso directo de carpeta para resolver el vínculo que apunta a su destino. <br/> Un acceso directo de carpeta es un elemento de carpeta que apunta a otro elemento de carpeta en el mismo espacio de nombres, mediante un vínculo (acceso directo) para contener el IDList del destino. El vínculo se resuelve para realizar el seguimiento del destino en caso de que se mueve o se cambia el nombre. Por ejemplo, la carpeta Mis lugares de red de Windows <strong>XP</strong> y la carpeta Equipo de Windows <strong>Vista</strong> pueden contener accesos directos de carpeta creados con el Asistente para agregar <strong>ubicación de</strong> red. Para mejorar el rendimiento, el <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>método IShellFolder::BindToObject</strong></a> no resuelve los vínculos a la carpeta de red de forma predeterminada.<br/> Se usa <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>con IShellFolder::BindToObject</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler</strong></a>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_DONT_PARSE_RELATIVE"></span><span id="str_dont_parse_relative"></span><dl> <dt><strong>STR_DONT_PARSE_RELATIVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows XP.</strong> Especifique este contexto de enlace para evitar que una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> de la carpeta <strong>Desktop</strong> trate las rutas de acceso relativas como relativas al escritorio. En tal caso, se produce un error al analizar cuando se especifica este contexto de enlace.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_DONT_RESOLVE_LINK"></span><span id="str_dont_resolve_link"></span><dl> <dt><strong>STR_DONT_RESOLVE_LINK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Se introdujo en Windows Vista</strong>. Especifique este contexto de enlace para indicar a <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>un IShellItem</strong></a> que no resuelva el destino del vínculo obtenido <strong>al</strong> usar el GUID de BHID_LinkTargetItem en <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_FILE_SYS_FIND_DATA"></span><span id="str_file_sys_find_data"></span><dl> <dt><strong>STR_FILE_SYS_FIND_DATA</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows XP.</strong> Especifique este contexto de enlace para proporcionar metadatos de archivo al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName,</strong></a> que se usa en lugar de intentar recuperar los metadatos de archivo reales. El objeto asociado debe implementar <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a> y, opcionalmente, también puede implementar <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>IFileSystemBindData2.</strong></a> De forma predeterminada, el método <strong>IShellFolder::P arseDisplayName</strong> comprueba que el archivo existe y usa los metadatos reales del archivo para rellenar la lista de identificadores.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_FILE_SYS_BIND_DATA_WIN7_FORMAT"></span><span id="str_file_sys_bind_data_win7_format"></span><dl> <dt><strong>STR_FILE_SYS_BIND_DATA_WIN7_FORMAT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 8.1</strong>. Especifique este contexto de enlace para indicar que los datos proporcionados en <strong>el</strong> STR_FILE_SYS_FIND_DATA de enlace deben usarse para crear una lista ItemID en el formato de Windows 7.&quot;<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GET_ASYNC_HANDLER"></span><span id="str_get_async_handler"></span><dl> <dt><strong>STR_GET_ASYNC_HANDLER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 7.</strong> Especifique este contexto de enlace cuando el controlador se recupere en el mismo subproceso que la interfaz de usuario. Se deben evitar las actividades que consumen mucha memoria, como las que implican el acceso a disco o red.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_BESTEFFORT"></span><span id="str_gps_besteffort"></span><dl> <dt><strong>STR_GPS_BESTEFFORT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Se introdujo en Windows Vista</strong>. Especifique este contexto de enlace al solicitar un <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>controlador IPropertySetStorage</strong></a> <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>o IPropertyStore.</strong></a> Este valor se usa con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a>. Consulte la <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_BESTEFFORT</strong></a> para obtener más información.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_DELAYCREATION"></span><span id="str_gps_delaycreation"></span><dl> <dt><strong>STR_GPS_DELAYCREATION</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Se introdujo en Windows Vista</strong>. Especifique este contexto de enlace al solicitar un <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>controlador IPropertySetStorage</strong></a> <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>o IPropertyStore.</strong></a> Este valor se usa con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a>. Consulte la <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_DELAYCREATION</strong></a> para obtener más información.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_FASTPROPERTIESONLY"></span><span id="str_gps_fastpropertiesonly"></span><dl> <dt><strong>STR_GPS_FASTPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Se introdujo en Windows Vista</strong>. Especifique este contexto de enlace al solicitar un <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>controlador IPropertySetStorage</strong></a> <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>o IPropertyStore.</strong></a> Este valor se usa con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a>. Consulte la <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_FASTPROPERTIESONLY</strong></a> para obtener más información.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_HANDLERPROPERTIESONLY"></span><span id="str_gps_handlerpropertiesonly"></span><dl> <dt><strong>STR_GPS_HANDLERPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Se introdujo en Windows Vista</strong>. Especifique este contexto de enlace al solicitar un <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>controlador IPropertySetStorage</strong></a> <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>o IPropertyStore.</strong></a> Este valor se usa con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a>. Consulte la <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_HANDLERPROPERTIESONLY</strong></a> para obtener más información.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_NO_OPLOCK"></span><span id="str_gps_no_oplock"></span><dl> <dt><strong>STR_GPS_NO_OPLOCK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 7.</strong> Especifique este contexto de enlace al solicitar un <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>controlador IPropertySetStorage</strong></a> <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>o IPropertyStore.</strong></a> Este valor se usa con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a>. Consulte la <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_NO_OPLOCK</strong></a> para obtener más información.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_OPENSLOWITEM"></span><span id="str_gps_openslowitem"></span><dl> <dt><strong>STR_GPS_OPENSLOWITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Se introdujo en Windows Vista</strong>. Especifique este contexto de enlace al solicitar un <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>controlador IPropertySetStorage</strong></a> <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>o IPropertyStore.</strong></a> Este valor se usa con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a>. Consulte la <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_OPENSLOWITEM</strong></a> para obtener más información.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK"></span><span id="str_ifilter_force_text_filter_fallback"></span><dl> <dt><strong>STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Solo Windows Vista.</strong> Especifique este contexto de enlace para provocar una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> que solicita a la interfaz <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> que un objeto del sistema de archivos devuelva un filtro de texto si no hay ningún otro filtro disponible. Este valor no se define a partir de Windows 7.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_IFILTER_LOAD_DEFINED_FILTER"></span><span id="str_ifilter_load_defined_filter"></span><dl> <dt><strong>STR_IFILTER_LOAD_DEFINED_FILTER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Solo Windows Vista.</strong> Especifique este contexto de enlace para provocar una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> que solicita a la interfaz <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> que un objeto del sistema de archivos no devuelva un filtro de reserva si no se encuentra ningún filtro registrado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_INTERNAL_NAVIGATE"></span><span id="str_internal_navigate"></span><dl> <dt><strong>STR_INTERNAL_NAVIGATE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Se introdujo en Windows Vista</strong>. Especifique este contexto de enlace para habilitar la carga del historial desde una secuencia para una navegación interna cuando se llama al método <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768216(v=vs.85)"><strong>IPersistHistory::LoadHistory.</strong></a> Una navegación interna es una navegación dentro de la misma vista.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE"></span><span id="str_internetfolder_parse_only_urlmon_bindable"></span><dl> <dt><strong>STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 7.</strong> Especifique este contexto de enlace con STR_PARSE_PREFER_FOLDER_BROWSING cuando el cliente desee que los controladores de carpetas de Shell de Internet generen un IDList para cualquier dirección URL válida si no se puede crear una carpeta de tipo DAV para esa dirección URL. No se comprueba que la dirección URL exista; solo se comprueba su sintaxis y que tiene un controlador de protocolo registrado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_ITEM_CACHE_CONTEXT"></span><span id="str_item_cache_context"></span><dl> <dt><strong>STR_ITEM_CACHE_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 7.</strong> Especifique este contexto de enlace para indicar a las implementaciones de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3::InitializeEx</strong></a> almacenar en caché objetos auxiliares de uso intensivo de memoria que pueden existir en las instancias de elementos de Shell en lugar de volver a crear estos objetos cada vez que se crea un elemento de Shell. El objeto asociado es otro objeto de contexto de enlace, inicialmente vacío. Esto debería dar lugar a un objeto de contexto de enlace independiente al que se accede a través de <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx::GetObjectParam</strong></a> o <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx::Register.ObjectParam</strong></a>. <br/> Un llamador debe participar en este comportamiento proporcionando este parámetro de contexto de enlace al llamar a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a>. Al hacerlo, optimiza el comportamiento del enlace a varios nombres de análisis en sucesión. La duración del objeto de contexto de enlace debe abarcar varias instancias de elementos de Shell y sus contextos de enlace individuales.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_NO_VALIDATE_FILENAME_CHARS"></span><span id="str_no_validate_filename_chars"></span><dl> <dt><strong>STR_NO_VALIDATE_FILENAME_CHARS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Se introdujo en Windows Vista</strong>. Especifique este contexto de enlace para permitir que aparezcan caracteres de nombre de archivo no válidos en los nombres de archivo. De forma predeterminada, una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> rechaza los caracteres que no son válidos en los nombres de archivo. Este contexto de enlace solo es significativo junto con el STR_FILE_SYS_FIND_DATA de enlace.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS"></span><span id="str_parse_allow_internet_shell_folders"></span><dl> <dt><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Se introdujo en Windows Vista</strong>. Especifique este contexto de enlace para habilitar una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> en la carpeta <strong>Desktop</strong> para analizar direcciones URL. Si se especifica este contexto de enlace, invalida <strong><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_AND_CREATE_ITEM"></span><span id="str_parse_and_create_item"></span><dl> <dt><strong>STR_PARSE_AND_CREATE_ITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 7.</strong> Especifique este contexto de enlace para indicar a la implementación de un origen de datos <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>de IShellFolder::P arseDisplayName</strong></a> que optimice el comportamiento de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a>. <br/> Normalmente, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a> realiza dos operaciones de enlace en el nombre que se va a analizar: una a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>iShellFolder::P arseDisplayName</strong></a> y otra para crear el elemento de Shell. Cuando se <strong>admite</strong> el contexto de enlace de STR_PARSE_AND_CREATE_ITEM, el segundo enlace se evita mediante la creación del elemento de Shell durante el enlace <strong>IShellFolder::P arseDisplayName</strong> y el almacenamiento del elemento de Shell mediante <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iparseandcreateitem-setitem"><strong>IParseAndCreateItem::SetItem</strong></a>. <strong>SHCreateItemFromParsingName</strong> usa el elemento de Shell almacenado en lugar de crear uno.<br/> Este parámetro se aplica al último elemento del nombre que se analiza. Por ejemplo, en el nombre &quot;C:\Folder1\File.txt, los datos se aplican a File.txt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_DONT_REQUIRE_VALIDATED_URLS"></span><span id="str_parse_dont_require_validated_urls"></span><dl> <dt><strong>STR_PARSE_DONT_REQUIRE_VALIDATED_URLS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Solo Windows Vista.</strong> Especifique que, al analizar una dirección URL, este contexto de enlace no debe requerir que exista la dirección URL antes de generar un IDList para ella. Especifique este contexto de enlace junto con <strong><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></strong> cuando el cliente desee que los controladores de carpetas de Shell de <strong>Internet</strong> generen un IDList para la dirección URL si no se puede crear una carpeta DAV para la dirección URL especificada.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PARTIAL_IDLIST"></span><span id="str_parse_partial_idlist"></span><dl> <dt><strong>STR_PARSE_PARTIAL_IDLIST</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Se introdujo en Windows Vista</strong>. Especifique este contexto de enlace para pasar el elemento original que se vuelve a analizar cuando ese elemento se almacena como un objeto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> que también implementa la <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>interfaz IParentAndItem.</strong></a> Antes de Windows 7, este valor no se definió en un archivo de encabezado. El autor de la llamada podría definirlo o pasarlo como su valor de cadena <strong>de L &quot; ParseOriginalItem &quot; </strong>. A partir de Windows 7, el valor se define en Shlobj.h. Tenga en cuenta que se trata de un encabezado diferente al de las otras constantes STR.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_FOLDER_BROWSING"></span><span id="str_parse_prefer_folder_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows XP.</strong> Especifique este contexto de enlace para habilitar una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> en la carpeta <strong>Desktop</strong> para analizar las direcciones URL como si fueran carpetas. Use este contexto de enlace para enlazar a un servidor WebDAV.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_WEB_BROWSING"></span><span id="str_parse_prefer_web_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Se introdujo en Windows Vista</strong>. Especifique este contexto de enlace para evitar una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> en el formulario carpeta Desktop analizando direcciones URL. <strong></strong> Este contexto de enlace se puede invalidar mediante <strong><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PROPERTYSTORE"></span><span id="str_parse_propertystore"></span><dl> <dt><strong>STR_PARSE_PROPERTYSTORE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Se introdujo en Windows Vista</strong>. Especifique este contexto de enlace para invalidar el almacén de propiedades predeterminado que usa el método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> y, en su lugar, use el almacén de propiedades especificado como parámetro de enlace. Se aplica a las carpetas de delegado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS"></span><span id="str_parse_shell_protocol_to_file_objects"></span><dl> <dt><strong>STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows XP SP2.</strong> Especifique este contexto de enlace para habilitar una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> en la carpeta <strong>Desktop</strong> para usar la notación de prefijo shell: para acceder a los &quot; &quot; archivos.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_SHOW_NET_DIAGNOSTICS_UI"></span><span id="str_parse_show_net_diagnostics_ui"></span><dl> <dt><strong>STR_PARSE_SHOW_NET_DIAGNOSTICS_UI</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Se introdujo en Windows Vista</strong>. Especifique este contexto de enlace para que se haga una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> para mostrar el cuadro de diálogo de diagnóstico de red si se produce un error en el análisis de una ruta de acceso de red.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SKIP_NET_CACHE"></span><span id="str_parse_skip_net_cache"></span><dl> <dt><strong>STR_PARSE_SKIP_NET_CACHE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Se introdujo en Windows Vista</strong>. Especifique este contexto de enlace para que una llamada al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> omita la comprobación de la caché de recursos compartidos de red y póngase en contacto directamente con el servidor de red. La información sobre los recursos compartidos de red se almacena en caché para mejorar el rendimiento y <strong>IShellFolder::P arseDisplayName</strong> comprueba esta memoria caché de forma predeterminada.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_TRANSLATE_ALIASES"></span><span id="str_parse_translate_aliases"></span><dl> <dt><strong>STR_PARSE_TRANSLATE_ALIASES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows XP.</strong> Especifique este contexto de enlace para pasar propiedades analizadas al método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> para un espacio de nombres delegado. El espacio de nombres puede usar las propiedades pasadas en lugar de intentar analizar el propio nombre.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_WITH_PROPERTIES"></span><span id="str_parse_with_properties"></span><dl> <dt><strong>STR_PARSE_WITH_PROPERTIES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Solo Windows Vista.</strong> Contexto de enlace de análisis que se usa para pasar un conjunto de propiedades y el nombre del elemento al llamar a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a>. El objeto del contexto de enlace implementa <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> y se recupera mediante una llamada <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>a IBindCtx::GetObjectParam</strong></a>.<br/> DBFolder es un origen de datos de Shell que representa los elementos de los resultados de búsqueda y las vistas basadas en consultas. DBFolder recupera estos elementos consultando el Windows Search sistema. Los elementos de los resultados de la búsqueda se identifican a través de un esquema de protocolo, por &quot; ejemplo, file: &quot; o &quot; mapi: &quot; . DBFolder proporciona el comportamiento de estos elementos delegando en orígenes de datos de Shell creados para estos protocolos. Vea <a href="/previous-versions/bb233544(v=msdn.10)">Developing Protocol Handler Add-ins</a> (Desarrollo de complementos de controlador de protocolos) para obtener más información.<br/> Cuando DBFolder delega su operación de análisis en los orígenes de datos de Shell que admiten protocolos Windows Search, este contexto de enlace proporciona acceso a los valores devueltos en el resultado de la consulta para ese elemento. Incluye lo siguiente:<br/>
<ul>
<li><a href="/windows/desktop/properties/props-system-itemtype">System.ItemType</a> (PKEY_ItemType)</li>
<li><a href="/windows/desktop/properties/props-system-parsingpath">System.ParsingPath</a> (PKEY_ParsingPath)</li>
<li><a href="/windows/desktop/properties/props-system-itempathdisplay">System.ItemPathDisplay</a> (PKEY_ItemPathDisplay)</li>
<li><a href="/windows/desktop/properties/props-system-itemnamedisplay">System.ItemNameDisplay</a> (PKEY_ItemNameDisplay)</li>
</ul>
<br/> Este contexto de enlace también se puede usar para analizar un elemento DBFolder si un cliente tiene un conjunto de propiedades que definen el elemento. En este caso, se debe pasar un nombre vacío a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a>.<br/> Antes de Windows 7, este valor no se definió en un archivo de encabezado. El autor de la llamada podría definirlo o pasarlo como su valor de cadena: <code>L&quot;ParseWithProperties&quot;</code> . A partir de Windows 7, el valor se define en Shlobj.h. Tenga en cuenta que se trata de un encabezado diferente de donde se definen las otras constantes STR.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PROPERTYBAG_PARAM"></span><span id="str_propertybag_param"></span><dl> <dt><strong>STR_PROPERTYBAG_PARAM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows 8</strong>. Especifique este contexto de enlace para indicar que el parámetro de contexto de enlace es un bolsa de propiedades (<a href="/windows/win32/api/oaidl/nn-oaidl-ipropertybag"><strong>IPropertyBag</strong></a>) que se usa para pasar valores VARIANT en el contexto de enlace. Consulte la sección Comentarios para obtener más detalles.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_SKIP_BINDING_CLSID"></span><span id="str_skip_binding_clsid"></span><dl> <dt><strong>STR_SKIP_BINDING_CLSID</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introducido en Windows XP.</strong> Especifique este contexto de enlace para que las llamadas a los métodos <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> omitan una extensión de espacio de nombres de Shell determinada al analizar o enlazar. El método <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid"><strong>IPersist::GetClassID</strong></a> del parámetro bind proporciona el CLSID del espacio de nombres que se va a omitir. <br/>
<blockquote>
[!Note]<br />
Introducido en Windows 2000 SP3, este valor se definió en Shlobj.h hasta Windows XP, cuando se movió a Shobjidl.h.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_TRACK_CLSID"></span><span id="str_track_clsid"></span><dl> <dt><strong>STR_TRACK_CLSID</strong></dt> </dl></td>
<td style="text-align: left;">No se usa.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentarios

Los contextos de enlace se usan para pasar parámetros opcionales a funciones que tienen un parámetro \* IBindCtx. Esos parámetros se expresan como objetos COM y pueden implementar interfaces que se usan para modelar los datos de parámetros. Algunos contextos de enlace representan un valor booleano, donde **TRUE** indica un objeto que implementa solo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) y FALSE indica que no hay ningún objeto presente.

[**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname), [**IShellFolder::BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) e [**IShellItem::BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) toman un contexto de enlace y se pueden pasar parámetros a través de ese contexto de enlace.

Algunos contextos de enlace son específicos de determinadas implementaciones de origen de datos o tipos de controlador.

Los parámetros de contexto de enlace se definen para su uso con una función o un método específicos.

Al solicitar un almacén de propiedades a través de [**IShellFolder,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)puede especificar el equivalente de DEFAULT de [**GPS \_**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags) pasando un parámetro [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) nulo. También puede especificar el equivalente de READWRITE gps pasando un modo \_ de STGM \_ READWRITE STGM EXCLUSIVE en el \| contexto de \_ enlace.

El bolsa de propiedades especificado por el objeto de contexto de enlace **STR \_ PROPERTYBAG \_ PARAM** contiene valores adicionales a los que se puede acceder con los métodos [**IPropertyBag::Read**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768197(v=vs.85)) e [**IPropertyBag::Write.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768198(v=vs.85))



| Nombre de propiedad                                 | Tipo     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MARCAS \_ DE ELEMENTOS DE \_ \_ ENUMERACIÓN STR                       | VT \_ UI4  | **Introducido en Windows 8**. Especifica un [**valor SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) que se va a pasar a [**IShellFolder::EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) cuando se llama a [**IShellItem::BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) con **ELID \_ EnumItems**.                                                                                                                                                                                                                         |
| STR \_ PARSE \_ EXPLICIT \_ ASSOCIATION \_ SUCCESSFUL | VT \_ BOOL | **Introducido en Windows 7.** El método [**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) establece esta propiedad para decir al autor de la llamada que el IDList devuelto estaba enlazado al [ProgID](fa-progids.md) especificado con **STR \_ PARSE \_ WITH EXPLICIT \_ \_ PROGID** o a la aplicación especificada con **STR \_ PARSE WITH EXPLICIT \_ \_ \_ ASSOCAPP**. Cuando **STR \_ PARSE EXPLICIT ASSOCIATION \_ \_ \_ SUCCESSFUL** no está presente, el ProgID o la aplicación no se enlazan a IDList. |
| STR \_ PARSE \_ WITH \_ EXPLICIT \_ ASSOCAPP          | VT \_ BSTR | **Introducido en Windows 7.** Especifique esta propiedad para hacer que una llamada al método [**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) devuelva un IDList enlazado al controlador de asociación de tipo de archivo para la aplicación.                                                                                                                                                                                                                                          |
| STR \_ PARSE \_ WITH \_ EXPLICIT \_ PROGID            | VT \_ BSTR | **Introducido en Windows 7.** Especifique esta propiedad para que una llamada al método [**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) devuelva un IDList enlazado al controlador de asociación de archivos del [ProgID proporcionado.](fa-progids.md)                                                                                                                                                                                                                          |



 

Consulte el [ejemplo de análisis con parámetros](samples-parsingwithparameters.md) para obtener un ejemplo del uso de valores de contexto de enlace.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 
