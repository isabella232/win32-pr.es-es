---
description: 'Más información acerca de: JET_CBTYP'
title: JET_CBTYP
TOCTitle: JET_CBTYP
ms:assetid: babbfa11-01a7-477b-a525-cff27a983b60
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294071(v=EXCHG.10)
ms:contentKeyID: 32765686
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b01bafad091ed17e018793ea701596aef6d0d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678327"
---
# <a name="jet_cbtyp"></a>JET_CBTYP


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_cbtyp"></a>JET_CBTYP

El **JET_CBTYP** grupo de constantes describe todos los puntos posibles en una operación que el motor de base de datos notificará a una aplicación mediante una llamada a la función de devolución de llamada [JET_CALLBACK](./jet-callback-callback-function.md) . El motor de base de datos pasa una de estas constantes en el parámetro *cbtyp* de la función de devolución de llamada. El significado de los demás parámetros pasados por el motor de base de datos en esta llamada depende de la **JET_CBTYP** específica que se pasa.

**Windows XP:**  El **JET_CBTYP** grupo de constantes se introduce en Windows XP.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante o valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_cbtypNull<br />
0x00000000</p></td>
<td><p>Esta devolución de llamada está reservada y siempre se considera no válida.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFinalize<br />
0x00000001</p></td>
<td><p>Esta devolución de llamada se reserva para uso futuro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeInsert<br />
0x00000002</p></td>
<td><p>Esta devolución de llamada se producirá inmediatamente antes de que se inserte un nuevo registro en una tabla mediante una llamada a <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</p>
<p>El puntero de función para esta razón de devolución de llamada se pasa a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por medio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o se configura en tiempo de ejecución por medio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Para obtener más información, vea <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Los parámetros de devolución de llamada tendrán los valores siguientes:</p>
<ul>
<li><p><em>sesid</em>: la sesión que tiene el registro que se va a insertar.</p></li>
<li><p><em>DBID</em>: el identificador de base de datos de la tabla que contiene el registro que se va a insertar.</p></li>
<li><p><em>TABLEID</em>: el cursor que ha preparado el nuevo registro que se va a insertar. Es importante tener en cuenta que el valor de cualquier columna de versión o de incremento automático puede no ser correcto en este momento.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: el puntero de contexto pasado a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong> si la devolución de llamada devuelve un error, se producirá un error en la operación que origina la devolución de llamada.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterInsert<br />
0x00000004</p></td>
<td><p>Esta devolución de llamada se producirá inmediatamente después de que se haya insertado un nuevo registro en una tabla mediante una llamada a <a href="gg269288(v=exchg.10).md">JetUpdate</a> pero antes de que <a href="gg269288(v=exchg.10).md">JetUpdate</a> vuelva a su llamador.</p>
<p>El puntero de función para esta razón de devolución de llamada se pasa a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por medio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o se configura en tiempo de ejecución por medio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Para obtener más información, vea <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Los parámetros de devolución de llamada tendrán los valores siguientes:</p>
<ul>
<li><p><em>sesid</em>: la sesión que tiene el registro que se acaba de insertar.</p></li>
<li><p><em>DBID</em>: el identificador de base de datos de la tabla que contiene el registro que se acaba de insertar.</p></li>
<li><p><em>TABLEID</em>: cursor en la tabla en la que se acaba de insertar el registro. Observe que el cursor sigue situado en la misma entrada de índice que estaba en la devolución de llamada antes de la inserción. Tenga en cuenta que es posible que esta entrada de índice no esté relacionada de ninguna forma con el registro que se está insertando.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: el puntero de contexto pasado a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong> si la devolución de llamada devuelve un error, se omitirá.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeReplace<br />
0x00000008</p></td>
<td><p>Esta devolución de llamada se producirá justo antes de un registro existente en una tabla que se va a cambiar mediante una llamada a <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</p>
<p>El puntero de función para esta razón de devolución de llamada se pasa a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por medio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o se configura en tiempo de ejecución por medio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Para obtener más información, vea <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Los parámetros de devolución de llamada tendrán los valores siguientes:</p>
<ul>
<li><p><em>sesid</em>: la sesión que tiene el registro que se va a cambiar.</p></li>
<li><p><em>DBID</em>: el identificador de base de datos de la tabla que contiene el registro que se va a cambiar.</p></li>
<li><p><em>TABLEID</em>: cursor situado en una entrada de índice asociada al registro que se va a cambiar. Es importante tener en cuenta que el valor de cualquier columna de versión o de incremento automático puede no ser correcto en este momento.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: el puntero de contexto pasado a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong> si la devolución de llamada devuelve un error, se producirá un error en la operación que origina la devolución de llamada.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterReplace<br />
0x00000010</p></td>
<td><p>Esta devolución de llamada se producirá inmediatamente después de que un registro existente en una tabla se haya modificado mediante una llamada a <a href="gg269288(v=exchg.10).md">JetUpdate</a> pero antes de que <a href="gg269288(v=exchg.10).md">JetUpdate</a> vuelva a su llamador.</p>
<p>El puntero de función para esta razón de devolución de llamada se pasa a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por medio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o se configura en tiempo de ejecución por medio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Para obtener más información, vea <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Los parámetros de devolución de llamada tendrán los valores siguientes:</p>
<ul>
<li><p><em>sesid</em>: la sesión que tiene el registro que se acaba de cambiar.</p></li>
<li><p><em>DBID</em>: el identificador de base de datos de la tabla que contiene el registro que se acaba de cambiar.</p></li>
<li><p><em>TABLEID</em>: cursor situado en una entrada de índice asociada al registro que se acaba de cambiar.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: el puntero de contexto pasado a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong> si la devolución de llamada devuelve un error, se omitirá.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeDelete<br />
0x00000020</p></td>
<td><p>Esta devolución de llamada se producirá inmediatamente antes de que se elimine un registro existente de una tabla mediante una llamada a <a href="gg269315(v=exchg.10).md">JetDelete</a>.</p>
<p>El puntero de función para esta razón de devolución de llamada se pasa a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por medio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o se configura en tiempo de ejecución por medio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Para obtener más información, vea <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Los parámetros de devolución de llamada tendrán los valores siguientes:</p>
<ul>
<li><p><em>sesid</em>: la sesión que tiene el registro que se va a eliminar.</p></li>
<li><p><em>DBID</em>: el identificador de base de datos de la tabla que contiene el registro que se va a eliminar.</p></li>
<li><p><em>TABLEID</em>: cursor situado en una entrada de índice asociada al registro que se va a eliminar.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: el puntero de contexto pasado a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong> si la devolución de llamada devuelve un error, se producirá un error en la operación que origina la devolución de llamada.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterDelete<br />
0x00000040</p></td>
<td><p>Esta devolución de llamada se producirá inmediatamente después de que un registro existente en una tabla se haya eliminado mediante una llamada a <a href="gg269315(v=exchg.10).md">JetDelete</a> pero antes de que <a href="gg269315(v=exchg.10).md">JetDelete</a> vuelva a su llamador.</p>
<p>El puntero de función para esta razón de devolución de llamada se pasa a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por medio de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o se configura en tiempo de ejecución por medio de <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Para obtener más información, vea <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>Los parámetros de devolución de llamada tendrán los valores siguientes:</p>
<ul>
<li><p><em>sesid</em>: la sesión que tiene el registro que se acaba de eliminar.</p></li>
<li><p><em>DBID</em>: el identificador de base de datos de la tabla que contiene el registro que se acaba de eliminar.</p></li>
<li><p><em>TABLEID</em>: cursor situado en una entrada de índice asociada al registro que se acaba de eliminar.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: el puntero de contexto pasado a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong></p></li>
</ul>
<p>Si la devolución de llamada devuelve un error, se omitirá.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypUserDefinedDefaultValue<br />
0x00000080</p></td>
<td><p>Esta devolución de llamada se producirá cuando el motor necesite recuperar el valor predeterminado definido por el usuario de una columna de la aplicación. Esta devolución de llamada es esencialmente una implementación limitada de <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> evaluada por la aplicación. Se puede devolver un valor máximo de una columna para un valor predeterminado definido por el usuario.</p>
<p>El puntero de función para esta razón de devolución de llamada se pasa a <a href="gg294122(v=exchg.10).md">JetAddColumn</a> por medio de una estructura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> o se pasa a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> por medio de una estructura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> en una estructura de <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> en una estructura de <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> .</p>
<p>Los parámetros de devolución de llamada tendrán los valores siguientes:</p>
<ul>
<li><p><em>sesid</em>: la sesión que está calculando el valor predeterminado definido por el usuario</p></li>
<li><p><em>DBID</em>: el identificador de base de datos de la tabla que contiene el valor predeterminado definido por el usuario</p></li>
<li><p><em>TABLEID</em>: cursor situado en el registro para el que se recupera el valor predeterminado definido por el usuario.</p></li>
<li><p><em>pvArg1</em>: el búfer de salida para el valor predeterminado definido por el usuario</p></li>
<li><p><em>pvArg2</em>: en la entrada, es el tamaño del búfer de salida. En la salida, es el tamaño real del valor predeterminado definido por el usuario. en cualquier caso, el tamaño es un entero de 32 bits sin signo.</p></li>
<li><p><em>pvContext</em>: puntero a un búfer que contiene los datos de usuario especificados en la estructura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> cuando se creó la columna o null si no se proporcionó ningún contexto.</p></li>
<li><p><em>ulUnused</em>: el ID. de columna de la columna para la que se recupera el valor predeterminado definido por el usuario.</p></li>
</ul>
<p>Si la devolución de llamada devuelve un error, se producirá un error en la operación que origina la devolución de llamada.</p>
<p>Si la devolución de llamada devuelve JET_wrnBufferTruncated, la operación continuará, pero no se recuperará el valor completo durante la devolución de llamada.</p>
<p>Si la devolución de llamada devuelve JET_wrnColumnNull, la operación continuará, pero el valor predeterminado definido por el usuario para la columna es NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypOnlineDefragCompleted<br />
0x00000100</p></td>
<td><p>Esta devolución de llamada se producirá cuando la desfragmentación con conexión de una base de datos tal como la inicia <a href="gg269317(v=exchg.10).md">JetDefragment</a> se haya detenido debido a que el proceso se ha completado o hasta que se alcanza el límite de tiempo.</p>
<p>El puntero de función para esta razón de devolución de llamada se pasa a <a href="gg269317(v=exchg.10).md">JetDefragment</a>. Para obtener más información, vea <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</p>
<p>Los parámetros de devolución de llamada tendrán los valores siguientes:</p>
<ul>
<li><p><em>sesid</em>: la sesión que se usa para realizar la desfragmentación en línea de la base de datos o JET_sesidNil para un archivo de streaming.</p></li>
<li><p><em>DBID</em>: el identificador de la base de datos que se está desfragmentando o JET_dbidNil para un archivo de streaming.</p></li>
<li><p><em>TABLEID</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: <strong>null</strong></p></li>
<li><p><em>ulUnused</em>: <strong>null</strong></p></li>
</ul>
<p>Si la devolución de llamada devuelve un error, se omitirá.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypFreeCursorLS<br />
0x00000200</p></td>
<td><p>Esta devolución de llamada se producirá cuando la aplicación necesite limpiar el identificador de contexto para el almacenamiento local asociado a un cursor que el motor de base de datos está liberando. Para obtener más información, vea <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</p>
<p>El puntero de función para esta razón de devolución de llamada se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</p>
<p>Los parámetros de devolución de llamada tendrán los valores siguientes:</p>
<ul>
<li><p><em>sesid</em>: JET_sesidNil</p></li>
<li><p><em>DBID</em>: JET_dbidNil</p></li>
<li><p><em>TABLEID</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1</em>: el conjunto de identificadores de contexto con <a href="gg269243(v=exchg.10).md">JetSetLS</a></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: <strong>null</strong></p></li>
<li><p><em>ulUnused</em>: <strong>null</strong></p></li>
</ul>
<p>Si la devolución de llamada devuelve un error, se omitirá.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFreeTableLS<br />
0x00000400</p></td>
<td><p>Esta devolución de llamada se producirá como resultado de la necesidad de que la aplicación Limpie el identificador de contexto para el almacenamiento local asociado a una tabla que el motor de base de datos está liberando. Para obtener más información, vea <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</p>
<p>El puntero de función para esta razón de devolución de llamada se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</p>
<p>Los parámetros de devolución de llamada tendrán los valores siguientes:</p>
<ul>
<li><p><em>sesid</em>: JET_sesidNil</p></li>
<li><p><em>DBID</em>: JET_dbidNil</p></li>
<li><p><em>TABLEID</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1</em>: el conjunto de identificadores de contexto con <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: <strong>null</strong></p></li>
<li><p><em>ulUnused</em>: <strong>null</strong></p></li>
</ul>
<p>Si la devolución de llamada devuelve un error, se omitirá.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_CALLBACK](./jet-callback-callback-function.md)
