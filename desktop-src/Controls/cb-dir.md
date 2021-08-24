---
title: CB_DIR mensaje (Winuser.h)
description: Agrega nombres a la lista mostrada por el cuadro combinado. El mensaje agrega los nombres de directorios y archivos que coinciden con una cadena y un conjunto de atributos de archivo especificados. CB \_ DIR también puede agregar letras de unidad asignadas a la lista.
ms.assetid: 6082d12c-0af4-4a99-98c0-6a98d171f4d8
keywords:
- CB_DIR controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: defa19ffdebfb448e1a89c141da0b275c1df1bffdcfa9e3914293400d706b7ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577125"
---
# <a name="cb_dir-message"></a>Mensaje \_ de dir. de CB

Agrega nombres a la lista mostrada por el cuadro combinado. El mensaje agrega los nombres de directorios y archivos que coinciden con una cadena y un conjunto de atributos de archivo especificados. **CB \_ DIR** también puede agregar letras de unidad asignadas a la lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Atributos de los archivos o directorios que se van a agregar al cuadro combinado. Este parámetro puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                         | Significado                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <dt>**DDL \_ ARCHIVE**</dt> </dl>       | Incluye archivos archivados.<br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <dt>**DIRECTORIO \_ DDL**</dt> </dl> | Incluye subdirectorios, que se incluyen entre corchetes ( \[ \] ).<br/>                                                             |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <dt>**UNIDADES \_ DDL**</dt> </dl>          | Todas las unidades asignadas se agregan a la lista. Las unidades se muestran con el \[ - *formato x* - \] , donde *x* es la letra de unidad.<br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <dt>**DDL \_ EXCLUSIVE**</dt> </dl> | Incluye solo los archivos con los atributos especificados. De forma predeterminada, los archivos de lectura y escritura se muestran incluso si no se especifica DDL \_ READWRITE.<br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <dt>**DDL \_ HIDDEN**</dt> </dl>          | Incluye archivos ocultos.<br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <dt>**DDL \_ READONLY**</dt> </dl>    | Incluye archivos de solo lectura.<br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <dt>**DDL \_ READWRITE**</dt> </dl> | Incluye archivos de lectura y escritura sin atributos adicionales. Este es el valor predeterminado.<br/>                                                       |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <dt>**DDL \_ SYSTEM**</dt> </dl>          | Incluye archivos del sistema.<br/>                                                                                                              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero **LPCTSTR** a una cadena terminada en NULL que especifica una ruta de acceso absoluta, una ruta de acceso relativa o un nombre de archivo. Una ruta de acceso absoluta puede comenzar con una letra de unidad (por ejemplo, d: o un nombre \) UNC (por ejemplo, \\ \\ *nombredeEquipo* \\ *nombreDeEquipo).* Si la cadena especifica un nombre de archivo o directorio que tiene los atributos especificados por el parámetro *wParam,* el nombre de archivo o directorio se agrega a la lista. Si el nombre de archivo o el nombre de directorio contiene caracteres comodín (? o ), todos los archivos o directorios que coinciden con la expresión comodín y tienen los atributos especificados por el parámetro wParam se agregan a la lista que se muestra en \* el cuadro combinado. 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es el índice de base cero del apellido agregado a la lista.

Si se produce un error, el valor devuelto es CB \_ ERR. Si no hay suficiente espacio para almacenar las nuevas cadenas, el valor devuelto es CB \_ ERRSPACE.

## <a name="remarks"></a>Comentarios

Si *wParam* incluye la marca DDL DIRECTORY y lParam especifica todos los subdirectorios de un directorio de primer nivel, como C: TEMP, el cuadro de lista siempre incluirá una \_ entrada  \\ \\ \* ".." para el directorio raíz. Esto es así incluso si el directorio raíz tiene atributos ocultos o del sistema y no se especifican las marcas DDL HIDDEN y \_ DDL \_ SYSTEM. El directorio raíz de un volumen NTFS tiene atributos ocultos y del sistema.

La lista muestra nombres de archivo largos, si los hay.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> <dt>

[**DlgDirListComboBox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)
</dt> </dl>

 

 





