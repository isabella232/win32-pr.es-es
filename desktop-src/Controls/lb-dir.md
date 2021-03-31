---
title: Mensaje de LB_DIR (Winuser. h)
description: Agrega nombres a la lista mostrada por un cuadro de lista. El mensaje agrega los nombres de los directorios y archivos que coinciden con una cadena y un conjunto de atributos de archivo especificados. LB \_ dir también puede Agregar Letras de unidad asignadas al cuadro de lista.
ms.assetid: 5ec134e9-fe42-4cc0-bdea-fa5e66c218f6
keywords:
- LB_DIR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80abddbce13adec2e66824057fc5e873def306ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151059"
---
# <a name="lb_dir-message"></a>Mensaje de LB \_ dir

Agrega nombres a la lista mostrada por un cuadro de lista. El mensaje agrega los nombres de los directorios y archivos que coinciden con una cadena y un conjunto de atributos de archivo especificados. **Lb \_ DIR** también puede Agregar Letras de unidad asignadas al cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Atributos de los archivos o directorios que se van a agregar al cuadro de lista. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                         | Significado                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <dt>**\_archivo DDL**</dt> </dl>       | Incluye archivos archivados.<br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <dt>**\_directorio DDL**</dt> </dl> | Incluye subdirectorios. Los nombres de subdirectorios se incluyen entre corchetes ( \[ \] ).<br/>                                                |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <dt>**\_unidades DDL**</dt> </dl>          | Todas las unidades asignadas se agregan a la lista. Las unidades se muestran en el formato \[ - *x* - \] , donde *x* es la letra de la unidad.<br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <dt>**DDL \_ exclusivo**</dt> </dl> | Incluye solo los archivos con los atributos especificados. De forma predeterminada, los archivos de lectura y escritura se enumeran incluso si \_ no se especifica DDL ReadWrite.<br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <dt>**DDL \_ oculto**</dt> </dl>          | Incluye archivos ocultos.<br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <dt>**DDL de \_ solo lectura**</dt> </dl>    | Incluye archivos de solo lectura.<br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <dt>**ReadWrite de DDL \_**</dt> </dl> | Incluye archivos de lectura/escritura sin atributos adicionales. Esta es la configuración predeterminada.<br/>                                               |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <dt>**\_sistema DDL**</dt> </dl>          | Incluye archivos del sistema.<br/>                                                                                                              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en null que especifica una ruta de acceso absoluta, una ruta de acceso relativa o un nombre de archivo. Una ruta de acceso absoluta puede empezar con una letra de unidad (por ejemplo, d: \) o un nombre UNC (por ejemplo, \\ \\ *MachineName* \\ *ShareName*).

Si la cadena especifica un nombre de archivo o directorio que tiene los atributos especificados por el parámetro *wParam* , el nombre de archivo o directorio se agrega a la lista. Si el nombre de archivo o de directorio contiene caracteres comodín (? o \* ), todos los archivos o directorios que coinciden con la expresión comodín y que tienen los atributos especificados por el parámetro *wParam* se agregan a la lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es el índice de base cero del último nombre agregado a la lista.

Si se produce un error, el valor devuelto es LB \_ Err. Si no hay suficiente espacio para almacenar las nuevas cadenas, el valor devuelto es LB \_ ERRSPACE.

## <a name="remarks"></a>Observaciones

El mensaje [**lb \_ INITSTORAGE**](lb-initstorage.md) ayuda a acelerar la inicialización de cuadros de lista que tienen un gran número de elementos (más de 100). Reserva la cantidad de memoria especificada para que los mensajes de **lb \_ dir** posteriores tarden el menor tiempo posible. Puede usar estimaciones para los parámetros *wParam* e *lParam* . Si sobrestima, se asigna la memoria adicional; Si se subestima, se usa la asignación normal para los elementos que superan la cantidad solicitada.

Si *wParam* incluye la \_ marca de directorio DDL y *lParam* especifica todos los subdirectorios de un directorio de primer nivel, como C: \\ temp \\ \* , el cuadro de lista incluirá siempre una entrada ".." para el directorio raíz. Esto es así incluso si el directorio raíz tiene atributos ocultos o del sistema, y \_ \_ no se especifican las marcas DDL ocultas y del sistema DDL. El directorio raíz de un volumen NTFS tiene atributos ocultos y del sistema.

La lista muestra los nombres de archivo largos, si los hay.

En el caso de una aplicación ANSI, el sistema convierte el texto de un cuadro de lista en Unicode mediante CP \_ ACP. Esto puede causar problemas. Por ejemplo, los caracteres romanos acentuados en un cuadro de lista no Unicode en las ventanas japonesas se desactivarán. Para solucionar este error, compile la aplicación como Unicode o use un cuadro de lista dibujado por el propietario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> </dl>

 

 





