---
description: Atributos que se pueden recuperar en un elemento (archivo o carpeta) o en un conjunto de elementos.
ms.assetid: 4cb85995-cdc8-4474-8c4d-c783ac91c759
title: SFGAO (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a5ae5dca355b7c22e3075a0ced7640a5bd45a54
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359667"
---
# <a name="sfgao"></a>SFGAO

Atributos que se pueden recuperar en un elemento (archivo o carpeta) o en un conjunto de elementos.




| Constante o valor | Descripción | 
|----------------|-------------|
| <span id="SFGAO_CANCOPY"></span><span id="sfgao_cancopy"></span><dl><dt><strong>SFGAO_CANCOPY</strong></dt><dt>0x00000001</dt></dl> | Se pueden copiar los elementos especificados.<br /> | 
| <span id="SFGAO_CANMOVE"></span><span id="sfgao_canmove"></span><dl><dt><strong>SFGAO_CANMOVE</strong></dt><dt>0x00000002</dt></dl> | Se pueden mover los elementos especificados.<br /> | 
| <span id="SFGAO_CANLINK"></span><span id="sfgao_canlink"></span><dl><dt><strong>SFGAO_CANLINK</strong></dt><dt>0x00000004</dt></dl> | Se pueden crear accesos directos para los elementos especificados. Este atributo tiene el mismo valor que <a href="/windows/desktop/com/dropeffect-constants"><strong>DROPEFFECT_LINK</strong></a>. <br /> Si una extensión de espacio <strong></strong> de nombres devuelve este atributo, se agrega una entrada Crear acceso directo con un controlador predeterminado al menú contextual que se muestra durante las operaciones de arrastrar y colocar. La extensión también puede implementar su propio controlador para el verbo <em>de</em> vínculo en lugar del predeterminado. Si la extensión lo hace, es responsable de crear el acceso directo.<br /> También <strong>se agrega un</strong> elemento Create Shortcut (Crear acceso directo) al menú Windows Explorer <strong>File</strong> (Archivo del explorador) y a los menús contextuales normales.<br /> Si se selecciona el elemento, se invoca el método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu::InvokeCommand</strong></a> de la aplicación con el <strong>miembro lpVerb</strong> de la estructura <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a> establecida para vincular <em>.</em> La aplicación es responsable de crear el vínculo.<br /> | 
| <span id="SFGAO_STORAGE"></span><span id="sfgao_storage"></span><dl><dt><strong>SFGAO_STORAGE</strong></dt><dt>0x00000008</dt></dl> | Los elementos especificados se pueden enlazar a un <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>objeto IStorage</strong></a> a través <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>de IShellFolder::BindToObject</strong></a>. Para obtener más información sobre las funcionalidades de manipulación de espacios de nombres, <strong>vea IStorage</strong>.<br /> | 
| <span id="SFGAO_CANRENAME"></span><span id="sfgao_canrename"></span><dl><dt><strong>SFGAO_CANRENAME</strong></dt><dt>0x00000010</dt></dl> | Se puede cambiar el nombre de los elementos especificados. Tenga en cuenta que este valor es básicamente una sugerencia; No todos los clientes de espacio de nombres permiten cambiar el nombre de los elementos. Sin embargo, los que sí deben tener este atributo establecido.<br /> | 
| <span id="SFGAO_CANDELETE"></span><span id="sfgao_candelete"></span><dl><dt><strong>SFGAO_CANDELETE</strong></dt><dt>0x00000020</dt></dl> | Se pueden eliminar los elementos especificados.<br /> | 
| <span id="SFGAO_HASPROPSHEET"></span><span id="sfgao_haspropsheet"></span><dl><dt><strong>SFGAO_HASPROPSHEET</strong></dt><dt>0x00000040</dt></dl> | Los elementos especificados tienen hojas de propiedades.<br /> | 
| <span id="SFGAO_DROPTARGET"></span><span id="sfgao_droptarget"></span><dl><dt><strong>SFGAO_DROPTARGET</strong></dt><dt>0x00000100</dt></dl> | Los elementos especificados son destinos de colocación.<br /> | 
| <span id="SFGAO_CAPABILITYMASK"></span><span id="sfgao_capabilitymask"></span><dl><dt><strong>SFGAO_CAPABILITYMASK</strong></dt><dt>0x00000177</dt></dl> | Esta marca es una máscara para los atributos de funcionalidad: SFGAO_CANCOPY, SFGAO_CANMOVE, SFGAO_CANLINK, SFGAO_CANRENAME, SFGAO_CANDELETE, SFGAO_HASPROPSHEET y SFGAO_DROPTARGET. Normalmente, los llamadores no usan este valor.<br /> | 
| <span id="SFGAO_SYSTEM"></span><span id="sfgao_system"></span><dl><dt><strong>SFGAO_SYSTEM</strong></dt><dt>0x00001000</dt></dl> | <strong>Windows 7 y versiones posteriores.</strong> Los elementos especificados son elementos del sistema.<br /> | 
| <span id="SFGAO_ENCRYPTED"></span><span id="sfgao_encrypted"></span><dl><dt><strong>SFGAO_ENCRYPTED</strong></dt><dt>0x00002000</dt></dl> | Los elementos especificados están cifrados y pueden requerir una presentación especial.<br /> | 
| <span id="SFGAO_ISSLOW"></span><span id="sfgao_isslow"></span><dl><dt><strong>SFGAO_ISSLOW</strong></dt><dt>0x00004000</dt></dl> | Se espera que el acceso al elemento (a través <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>de IStream</strong></a> u otras interfaces de almacenamiento) sea una operación lenta. Las aplicaciones deben evitar el acceso a los elementos marcados con SFGAO_ISSLOW. <br /><blockquote>[!Note]<br />La apertura de una secuencia para un elemento suele ser una operación lenta en todo momento. SFGAO_ISSLOW indica que se espera que sea especialmente lento, por ejemplo, en el caso de conexiones de red lentas o archivos sin conexión (FILE_ATTRIBUTE_OFFLINE). Sin embargo, la consulta SFGAO_ISSLOW a sí misma es una operación lenta. Las aplicaciones deben consultar SFGAO_ISSLOW solo en un subproceso en segundo plano. Un método alternativo, como recuperar la propiedad <a href="/windows/desktop/properties/props-system-fileattributes"><strong>PKEY_FileAttributes</strong></a> y probar FILE_ATTRIBUTE_OFFLINE, podría usarse en lugar de una llamada al método que implica SFGAO_ISSLOW.</blockquote><br /> | 
| <span id="SFGAO_GHOSTED"></span><span id="sfgao_ghosted"></span><dl><dt><strong>SFGAO_GHOSTED</strong></dt><dt>0x00008000</dt></dl> | Los elementos especificados se muestran atenuados y no están disponibles para el usuario.<br /> | 
| <span id="SFGAO_LINK"></span><span id="sfgao_link"></span><dl><dt><strong>SFGAO_LINK</strong></dt><dt>0x00010000</dt></dl> | Los elementos especificados son accesos directos.<br /> | 
| <span id="SFGAO_SHARE"></span><span id="sfgao_share"></span><dl><dt><strong>SFGAO_SHARE</strong></dt><dt>0x00020000</dt></dl> | Los objetos especificados se comparten.<br /> | 
| <span id="SFGAO_READONLY"></span><span id="sfgao_readonly"></span><dl><dt><strong>SFGAO_READONLY</strong></dt><dt>0x00040000</dt></dl> | Los elementos especificados son de solo lectura. En el caso de las carpetas, esto significa que no se pueden crear nuevos elementos en esas carpetas. Esto no debe confundirse con el comportamiento especificado por la marca FILE_ATTRIBUTE_READONLY recuperada por <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider::GetItemData</strong></a> en una <a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>estructura SHCOLUMNDATA.</strong></a> FILE_ATTRIBUTE_READONLY no tiene ningún significado para las carpetas del sistema de archivos Win32.<br /> | 
| <span id="SFGAO_HIDDEN"></span><span id="sfgao_hidden"></span><dl><dt><strong>SFGAO_HIDDEN</strong></dt><dt>0x00080000</dt></dl> | El elemento está oculto y no debe mostrarse a menos que la opción Mostrar archivos <strong>y</strong> carpetas ocultos esté habilitada <strong>en Carpeta Configuración</strong>.<br /> | 
| <span id="SFGAO_DISPLAYATTRMASK"></span><span id="sfgao_displayattrmask"></span><dl><dt><strong>SFGAO_DISPLAYATTRMASK</strong></dt><dt>0x000FC000</dt></dl> | No debe usarse.<br /> | 
| <span id="SFGAO_NONENUMERATED"></span><span id="sfgao_nonenumerated"></span><dl><dt><strong>SFGAO_NONENUMERATED</strong></dt><dt>0x00100000</dt></dl> | Los elementos son elementos no con formato y deben estar ocultos. No se devuelven a través de un enumerador como el creado por el <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>método IShellFolder::EnumObjects.</strong></a><br /> | 
| <span id="SFGAO_NEWCONTENT"></span><span id="sfgao_newcontent"></span><dl><dt><strong>SFGAO_NEWCONTENT</strong></dt><dt>0x00200000</dt></dl> | Los elementos contienen contenido nuevo, tal como se define en la aplicación en particular.<br /> | 
| <span id="SFGAO_CANMONIKER"></span><span id="sfgao_canmoniker"></span><dl><dt><strong>SFGAO_CANMONIKER</strong></dt></dl> | No compatible.<br /> | 
| <span id="SFGAO_HASSTORAGE"></span><span id="sfgao_hasstorage"></span><dl><dt><strong>SFGAO_HASSTORAGE</strong></dt></dl> | No compatible.<br /> | 
| <span id="SFGAO_STREAM"></span><span id="sfgao_stream"></span><dl><dt><strong>SFGAO_STREAM</strong></dt><dt>0x00400000</dt></dl> | Indica que el elemento tiene una secuencia asociada. Se puede acceder a esa secuencia mediante una llamada a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler</strong></a> con IID_IStream en el <em>parámetro riid.</em><br /> | 
| <span id="SFGAO_STORAGEANCESTOR"></span><span id="sfgao_storageancestor"></span><dl><dt><strong>SFGAO_STORAGEANCESTOR</strong></dt><dt>0x00800000</dt></dl> | Los elementos secundarios de este elemento son accesibles a <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>través de IStream</strong></a> <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>o IStorage</strong></a>. Esos secundarios se marcan con SFGAO_STORAGE o SFGAO_STREAM.<br /> | 
| <span id="SFGAO_VALIDATE"></span><span id="sfgao_validate"></span><dl><dt><strong>SFGAO_VALIDATE</strong></dt><dt>0x01000000</dt></dl> | Cuando se especifica como entrada, SFGAO_VALIDATE indica a la carpeta que valide que existen los elementos contenidos en una carpeta o una matriz de elementos de Shell. Si uno o varios de esos elementos no existen, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof"><strong>IShellFolder::GetAttributesOf</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes"><strong>IShellItemArray::GetAttributes</strong></a> devuelven un código de error. Esta marca nunca se devuelve como un valor [out].<br /> Cuando se usa con la carpeta del sistema de archivos, SFGAO_VALIDATE indica a la carpeta que descarte las propiedades almacenadas en caché recuperadas por los clientes de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex"><strong>IShellFolder2::GetDetailsEx</strong></a> que podrían haber acumulado para los elementos especificados.<br /> | 
| <span id="SFGAO_REMOVABLE"></span><span id="sfgao_removable"></span><dl><dt><strong>SFGAO_REMOVABLE</strong></dt><dt>0x02000000</dt></dl> | Los elementos especificados están en medios extraíbles o son ellos mismos dispositivos extraíbles.<br /> | 
| <span id="SFGAO_COMPRESSED"></span><span id="sfgao_compressed"></span><dl><dt><strong>SFGAO_COMPRESSED</strong></dt><dt>0x04000000</dt></dl> | Los elementos especificados están comprimidos.<br /> | 
| <span id="SFGAO_BROWSABLE"></span><span id="sfgao_browsable"></span><dl><dt><strong>SFGAO_BROWSABLE</strong></dt><dt>0x08000000</dt></dl> | Los elementos especificados se pueden hospedar dentro de un explorador web o Windows explorer.<br /> | 
| <span id="SFGAO_FILESYSANCESTOR"></span><span id="sfgao_filesysancestor"></span><dl><dt><strong>SFGAO_FILESYSANCESTOR</strong></dt><dt>0x10000000</dt></dl> | Las carpetas especificadas son carpetas del sistema de archivos o contienen al menos un descendiente (secundario, secundario o posterior) que es una carpeta del sistema de archivos (SFGAO_FILESYSTEM).<br /> | 
| <span id="SFGAO_FOLDER"></span><span id="sfgao_folder"></span><dl><dt><strong>SFGAO_FOLDER</strong></dt><dt>0x20000000</dt></dl> | Los elementos especificados son carpetas. Algunos elementos se pueden marcar con SFGAO_STREAM y SFGAO_FOLDER, como un archivo comprimido con una .zip de nombre de archivo. Algunas aplicaciones pueden incluir esta marca al probar los elementos que son archivos y contenedores.<br /> | 
| <span id="SFGAO_FILESYSTEM"></span><span id="sfgao_filesystem"></span><dl><dt><strong>SFGAO_FILESYSTEM</strong></dt><dt>0x40000000</dt></dl> | Las carpetas o archivos especificados forman parte del sistema de archivos (es decir, son archivos, directorios o directorios raíz). Se puede suponer que los nombres analizados de los elementos son rutas de acceso del sistema de archivos Win32 válidas. Estas rutas de acceso pueden basarse en UNC o en letra de unidad.<br /> | 
| <span id="SFGAO_STORAGECAPMASK"></span><span id="sfgao_storagecapmask"></span><dl><dt><strong>SFGAO_STORAGECAPMASK</strong></dt><dt>0x70C50008</dt></dl> | Esta marca es una máscara para los atributos de funcionalidad de almacenamiento: SFGAO_STORAGE, SFGAO_LINK, SFGAO_READONLY, SFGAO_STREAM, SFGAO_STORAGEANCESTOR, SFGAO_FILESYSANCESTOR, SFGAO_FOLDER y SFGAO_FILESYSTEM. Normalmente, los llamadores no usan este valor.<br /> | 
| <span id="SFGAO_HASSUBFOLDER"></span><span id="sfgao_hassubfolder"></span><dl><dt><strong>SFGAO_HASSUBFOLDER</strong></dt><dt>0x80000000</dt></dl> | Las carpetas especificadas tienen subcarpetas. El SFGAO_HASSUBFOLDER solo es un aviso y es posible que lo devuelvan las implementaciones de carpetas de Shell incluso si no contienen subcarpetas. Sin embargo, tenga en cuenta que la inversa(no devolver SFGAO_HASSUBFOLDER) indica definitivamente que los objetos de carpeta no tienen subcarpetas.<br /> La SFGAO_HASSUBFOLDER se recomienda siempre que se requiera una cantidad significativa de tiempo para determinar si existen subcarpetas. Por ejemplo, el Shell siempre devuelve SFGAO_HASSUBFOLDER cuando una carpeta se encuentra en una unidad de red.<br /> | 
| <span id="SFGAO_CONTENTSMASK"></span><span id="sfgao_contentsmask"></span><dl><dt><strong>SFGAO_CONTENTSMASK</strong></dt><dt>0x80000000</dt></dl> | Esta marca es una máscara para los atributos de contenido, actualmente solo SFGAO_HASSUBFOLDER. Normalmente, los llamadores no usan este valor.<br /> | 
| <span id="SFGAO_PKEYSFGAOMASK"></span><span id="sfgao_pkeysfgaomask"></span><dl><dt><strong>SFGAO_PKEYSFGAOMASK</strong></dt><dt>0x81044000</dt></dl> | Máscara usada por la propiedad <a href="/windows/desktop/properties/props-system-sfgaoflags">PKEY_SFGAOFlags</a> para determinar los atributos que se consideran que provocan cálculos lentos o carecen de contexto: SFGAO_ISSLOW, SFGAO_READONLY, SFGAO_HASSUBFOLDER y SFGAO_VALIDATE. Normalmente, los llamadores no usan este valor.<br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IShellFolder::GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof)
</dt> <dt>

[**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)
</dt> <dt>

[**IShellItemArray::GetAttributes**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes)
</dt> </dl>

 

 
