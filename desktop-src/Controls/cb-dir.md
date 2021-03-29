---
title: Mensaje de CB_DIR (Winuser. h)
description: Agrega nombres a la lista mostrada por el cuadro combinado. El mensaje agrega los nombres de los directorios y archivos que coinciden con una cadena y un conjunto de atributos de archivo especificados. \_El directorio CB también puede Agregar Letras de unidad asignadas a la lista.
ms.assetid: 6082d12c-0af4-4a99-98c0-6a98d171f4d8
keywords:
- CB_DIR controles de mensajes de Windows
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
ms.openlocfilehash: 98cbea5bb88614d5606dd3d5cb165be59f632556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905246"
---
# <a name="cb_dir-message"></a>Mensaje de Dir. CB \_

Agrega nombres a la lista mostrada por el cuadro combinado. El mensaje agrega los nombres de los directorios y archivos que coinciden con una cadena y un conjunto de atributos de archivo especificados. **CB \_ DIR** también puede Agregar Letras de unidad asignadas a la lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Atributos de los archivos o directorios que se van a agregar al cuadro combinado. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                         | Significado                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <dt>**\_archivo DDL**</dt> </dl>       | Incluye archivos archivados.<br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <dt>**\_directorio DDL**</dt> </dl> | Incluye subdirectorios, que se incluyen entre corchetes ( \[ \] ).<br/>                                                             |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <dt>**\_unidades DDL**</dt> </dl>          | Todas las unidades asignadas se agregan a la lista. Las unidades se muestran en el formato \[ - *x* - \] , donde *x* es la letra de la unidad.<br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <dt>**DDL \_ exclusivo**</dt> </dl> | Incluye solo los archivos con los atributos especificados. De forma predeterminada, los archivos de lectura y escritura se enumeran incluso si \_ no se especifica DDL ReadWrite.<br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <dt>**DDL \_ oculto**</dt> </dl>          | Incluye archivos ocultos.<br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <dt>**DDL de \_ solo lectura**</dt> </dl>    | Incluye archivos de solo lectura.<br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <dt>**ReadWrite de DDL \_**</dt> </dl> | Incluye archivos de lectura/escritura sin atributos adicionales. Este es el valor predeterminado.<br/>                                                       |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <dt>**\_sistema DDL**</dt> </dl>          | Incluye archivos del sistema.<br/>                                                                                                              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Un puntero **LPCTSTR** a una cadena terminada en null que especifica una ruta de acceso absoluta, una ruta de acceso relativa o un nombre de archivo. Una ruta de acceso absoluta puede empezar con una letra de unidad (por ejemplo, d: \) o un nombre UNC (por ejemplo, \\ \\ *MachineName* \\ *ShareName*). Si la cadena especifica un nombre de archivo o un directorio que tiene los atributos especificados por el parámetro *wParam* , el nombre de archivo o el directorio se agregan a la lista. Si el nombre de archivo o el nombre de directorio contiene caracteres comodín (? o \* ), todos los archivos o directorios que coinciden con la expresión de carácter comodín y que tienen los atributos especificados por el parámetro *wParam* se agregan a la lista mostrada en el cuadro combinado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es el índice de base cero del último nombre agregado a la lista.

Si se produce un error, el valor devuelto es CB \_ error. Si no hay suficiente espacio para almacenar las nuevas cadenas, el valor devuelto es CB \_ ERRSPACE.

## <a name="remarks"></a>Observaciones

Si *wParam* incluye la \_ marca de directorio DDL y *lParam* especifica todos los subdirectorios de un directorio de primer nivel, como C: \\ temp \\ \* , el cuadro de lista incluirá siempre una entrada ".." para el directorio raíz. Esto es así incluso si el directorio raíz tiene atributos ocultos o del sistema, y \_ \_ no se especifican las marcas DDL ocultas y del sistema DDL. El directorio raíz de un volumen NTFS tiene atributos ocultos y del sistema.

La lista muestra los nombres de archivo largos, si los hay.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



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

 

 





