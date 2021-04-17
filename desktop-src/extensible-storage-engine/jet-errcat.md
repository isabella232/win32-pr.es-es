---
description: 'Más información acerca de: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: fe3f5ebad9f0838d089beb83b20b818b7faa4001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706452"
---
# <a name="jet_errcat"></a>JET_ERRCAT


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_errcat"></a>JET_ERRCAT

El **JET_ERRCAT** grupo de constantes describe las clasificaciones de nivel superior o las categorías de errores. Este grupo de constantes permite a las aplicaciones definir el tratamiento predeterminado para una clasificación de errores, en lugar de controlar cada caso de error de forma individual. También garantiza que la aplicación no tiene que controlar las nuevas condiciones de error que se incluyen en las clasificaciones existentes.

Nota: esta documentación se basa en una versión preliminar del motor de almacenamiento extensible. Esta información está sujeta a cambios.

Las constantes de **JET_ERRCAT** se organizan en una jerarquía específica de condiciones y subcondiciones, como se indica a continuación:

|---Error |---operación (al) | |---fatal | |---e/s | |---recurso | |---memoria | |---quota | |---el disco | |---datos | |---daños | |---incoherente | |---fragmentación | |---la API |---uso |---

En la tabla siguiente se enumeran las constantes de **JET_ERRCAT** y se proporciona una descripción e información de recuperación, según corresponda.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante o valor</p></th>
<th><p>Descripción</p></th>
<th><p>Recuperación</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errcatUnknown 0</p></td>
<td><p>Una categoría de error no válida.</p></td>
<td><p>N/D</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatError 1</p></td>
<td><p>La categoría de nivel superior (no hay errores de esta clase).</p></td>
<td><p>Vea las constantes de error específicas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatOperation 2</p></td>
<td><p>Representa los errores que pueden producirse en cualquier momento debido a condiciones no controlables y que suelen ser temporales. Vea subcategorías si se especifica.</p></td>
<td><p>Vuelva a intentarlo y, si el error continúa, informe al operador.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatFatal 3</p></td>
<td><p>Representa los errores irrecuperables que, cuando se producen, crean un riesgo de que ESE no pueda continuar de forma segura (a menudo transaccional) y los datos pueden resultar dañados.</p></td>
<td><p>Reinicie la instancia o el proceso. Si el problema persiste, informe al operador.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatIO 4</p></td>
<td><p>Representa los errores de e/s, que proceden del sistema operativo, y están fuera del control de ESE. Este tipo de error puede ser temporal.</p></td>
<td><p>Vuelva a intentarlo y, si el error continúa, pida al operador que compruebe el disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatResource 5</p></td>
<td><p>Representa una categoría de errores relacionados con la falta de condiciones de recursos.</p></td>
<td><p>Vea subcategorías.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatMemory 6</p></td>
<td><p>Representa un error causado por la falta de memoria.</p></td>
<td><p>Vuelva a intentarlo después de un período de tiempo, libere memoria o salga.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatQuota 7</p></td>
<td><p>Determinados &quot; &quot; recursos especializados se encuentran en grupos de cierto tamaño, lo que facilita la detección de pérdidas de estos recursos.</p></td>
<td><p>La aplicación debe <strong>validar ()</strong> para detectar estos problemas durante el desarrollo. Sin embargo, en el código comercial, la aplicación debe tratar esto como un error de memoria.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatDisk 8</p></td>
<td><p>Representa un error causado por la falta de espacio en disco.</p></td>
<td><p>Vuelva a intentarlo más tarde para determinar si hay más espacio en disco disponible o pida al operador que libere espacio en disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatData 9</p></td>
<td><p>Representa una categoría de nivel superior para los errores relacionados con los datos.</p></td>
<td><p>Vea subcategorías.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatCorruption 10</p></td>
<td><p>Representa un problema de daños, que suele ser permanente sin ninguna acción correctiva.</p></td>
<td><p>Restaurar desde la copia de seguridad mediante la operación de reparación de utilidades de ESE (esta operación restaura solo los datos que se han dejado/perdidos). Además, cuando se usa el método de recuperación (JetInit), se puede realizar la recuperación mediante la posibilidad de pérdida de datos (para obtener más información, vea <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatInconsistent 11</p></td>
<td><p>Representa un error en el que los archivos de base de datos o de registro se encuentran en un estado incoherente y no se pueden reconciliar. Este error puede deberse a un error de control de la aplicación o administrador.</p></td>
<td><p>Restaure desde una copia de seguridad mediante la operación de reparación de utilidades de ESE (que solo restaura los datos que se han dejado/perdidos). Además, en el caso de la operación de <strong>recuperación (JetInit)</strong> , se puede realizar la recuperación mediante la posibilidad de pérdida de datos (para obtener más información, vea <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatFragmentation 12</p></td>
<td><p>Representa una clase de errores en los que se ha agotado algún recurso interno persistente.</p></td>
<td><p>En el caso de los errores de base de datos, la desfragmentación sin conexión corregirá el problema. En el caso de los archivos de registro, recupere primero todas las bases de datos adjuntas en un cierre correcto y, a continuación, elimine todos los archivos de registro y el punto de control.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatApi 13</p></td>
<td><p>Vea subcategorías.</p></td>
<td><p>Vea subcategorías.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatUsage 14</p></td>
<td><p>Representa un error de uso. El código de cliente no ha pasado los argumentos correctos a la API de <strong>jet</strong> . Este error se conservará con el reintento.</p></td>
<td><p>El código de cliente debe utilizar el método <strong>Assert ()</strong> para asegurarse de que no se devuelve esta clase de errores, por lo que se pueden detectar problemas durante el desarrollo. En el comercio minorista, la aplicación debe notificar al operador el error.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatState 15</p></td>
<td><p>Representa una clase de mensajes que la API puede devolver para describir el estado de la base de datos. Por ejemplo, el método <a href="gg294103(v=exchg.10).md">JetSeek ()</a> puede devolver <strong>JET_errRecordNotFound</strong> cuando no se encontró el registro solicitado.</p></td>
<td><p>Varía en función de la API.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatObsolete 16</p></td>
<td><p>Representa los errores que proceden de una versión anterior del motor. El motor actual no debe devolver estos errores.</p></td>
<td><p>Desconocido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatMax 17</p></td>
<td><p>Constante que indica el final de la enumeración.</p></td>
<td><p>N/D</p></td>
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
<td><p>Requiere Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows 8 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>

