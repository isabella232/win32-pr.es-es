---
title: LB_DIR mensaje (Winuser.h)
description: Agrega nombres a la lista mostrada por un cuadro de lista. El mensaje agrega los nombres de directorios y archivos que coinciden con una cadena y un conjunto de atributos de archivo especificados. LB \_ DIR también puede agregar letras de unidad asignadas al cuadro de lista.
ms.assetid: 5ec134e9-fe42-4cc0-bdea-fa5e66c218f6
keywords:
- LB_DIR controles de Windows mensaje
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
ms.openlocfilehash: f3add3c0ea14c637e0240ab296095bcc720aff9efb4c3e8e99a2f3de7019a711
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671677"
---
# <a name="lb_dir-message"></a>Mensaje \_ de dir. de carga de carga

Agrega nombres a la lista mostrada por un cuadro de lista. El mensaje agrega los nombres de directorios y archivos que coinciden con una cadena y un conjunto de atributos de archivo especificados. **LB \_ DIR** también puede agregar letras de unidad asignadas al cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Atributos de los archivos o directorios que se van a agregar al cuadro de lista. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                         | Significado                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <dt>**DDL \_ ARCHIVE**</dt> </dl>       | Incluye archivos archivados.<br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <dt>**DIRECTORIO \_ DDL**</dt> </dl> | Incluye subdirectorios. Los nombres de subdirectorio se incluyen entre corchetes ( \[ \] ).<br/>                                                |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <dt>**UNIDADES \_ DDL**</dt> </dl>          | Todas las unidades asignadas se agregan a la lista. Las unidades se muestran con el \[ - *formato x* - \] , donde *x* es la letra de unidad.<br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <dt>**DDL \_ EXCLUSIVE**</dt> </dl> | Incluye solo los archivos con los atributos especificados. De forma predeterminada, los archivos de lectura y escritura se muestran incluso si no se especifica DDL \_ READWRITE.<br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <dt>**DDL \_ HIDDEN**</dt> </dl>          | Incluye archivos ocultos.<br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <dt>**DDL \_ READONLY**</dt> </dl>    | Incluye archivos de solo lectura.<br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <dt>**DDL \_ READWRITE**</dt> </dl> | Incluye archivos de lectura y escritura sin atributos adicionales. Esta es la configuración predeterminada.<br/>                                               |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <dt>**DDL \_ SYSTEM**</dt> </dl>          | Incluye archivos del sistema.<br/>                                                                                                              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en NULL que especifica una ruta de acceso absoluta, una ruta de acceso relativa o un nombre de archivo. Una ruta de acceso absoluta puede comenzar con una letra de unidad (por ejemplo, d: o un nombre \) UNC (por ejemplo, \\ \\ *nombredeEquipo* \\ *nombreDeEquipo).*

Si la cadena especifica un nombre de archivo o directorio que tiene los atributos especificados por el parámetro *wParam,* el nombre de archivo o directorio se agrega a la lista. Si el nombre de archivo o directorio contiene caracteres comodín (? o ), todos los archivos o directorios que coinciden con la expresión comodín y tienen los atributos especificados por el parámetro \* *wParam* se agregan a la lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es el índice de base cero del apellido agregado a la lista.

Si se produce un error, el valor devuelto es LB \_ ERR. Si no hay suficiente espacio para almacenar las nuevas cadenas, el valor devuelto es LB \_ ERRSPACE.

## <a name="remarks"></a>Observaciones

El [**mensaje \_ LB INITSTORAGE**](lb-initstorage.md) ayuda a acelerar la inicialización de cuadros de lista que tienen un gran número de elementos (más de 100). Reserva la cantidad de memoria especificada para que los mensajes de **\_ dir.** de carga de carga posteriores tarden el menor tiempo posible. Puede usar estimaciones para los *parámetros wParam* *y lParam.* Si sobreestima, se asigna la memoria adicional; Si se infravalora, la asignación normal se usa para los elementos que superan la cantidad solicitada.

Si *wParam* incluye la marca DDL DIRECTORY y lParam especifica todos los subdirectorios de un directorio de primer nivel, como C: TEMP, el cuadro de lista siempre incluirá una \_ entrada  \\ \\ \* ".." para el directorio raíz. Esto es así incluso si el directorio raíz tiene atributos ocultos o del sistema y no se especifican las marcas DDL HIDDEN y \_ DDL \_ SYSTEM. El directorio raíz de un volumen NTFS tiene atributos ocultos y del sistema.

La lista muestra nombres de archivo largos, si los hay.

Para una aplicación ANSI, el sistema convierte el texto de un cuadro de lista en Unicode mediante CP \_ ACP. Esto puede causar problemas. Por ejemplo, los caracteres latinos acentuados en un cuadro de lista que no es Unicode en Windows japonés aparecerán desconsolados. Para solucionar este problema, compile la aplicación como Unicode o use un cuadro de lista dibujado por el propietario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> </dl>

 

 





