---
description: 'Más información sobre: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: bd72ecab62eeccb3ed7e586e2e793bdb9796f09a57686e70d9177eb496316760
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118254327"
---
# <a name="jet_errcat"></a>JET_ERRCAT


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_errcat"></a>JET_ERRCAT

El **JET_ERRCAT** de constantes describe las clasificaciones de nivel superior o las categorías de errores. Este grupo de constantes permite a las aplicaciones definir el tratamiento predeterminado para una clasificación de errores, en lugar de controlar cada caso de error individualmente. También garantiza que la aplicación no tenga que controlar las nuevas condiciones de error que se incluyen en las clasificaciones existentes.

Nota: Esta documentación se basa en una versión preliminar de Extensible Storage Engine. Esta información está sujeta a cambios.

Las **JET_ERRCAT** constantes se organizan en una jerarquía específica de condiciones y subcondiciones, como se muestra a continuación:

|--- Error |--- Operation(al) | |--- Fatal | |--- IO | |--- Resource | |--- Memory | |--- Quota | |--- Disk | |--- Data | |--- Corruption | |--- Inconsistent | |--- Fragmentation | |--- Api |--- Usage |--- State

En la tabla siguiente se enumeran **JET_ERRCAT** constantes y se proporciona una descripción e información de recuperación, según corresponda.

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
<td><p>Categoría de error no válida.</p></td>
<td><p>N/D</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatError 1</p></td>
<td><p>Categoría de nivel superior (ningún error debe ser de esta clase).</p></td>
<td><p>Vea las constantes de error específicas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatOperation 2</p></td>
<td><p>Representa errores que pueden producirse en cualquier momento debido a condiciones incontrolables y que suelen ser temporales. Si se especifica, consulte subcategorías.</p></td>
<td><p>Vuelva a intentarlo y, si el error continúa, informe al operador.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatFatal 3</p></td>
<td><p>Representa errores irreales que, cuando se producen, crean un riesgo de que ese no pueda continuar de forma segura (a menudo transaccional) y que los datos se puedan dañar.</p></td>
<td><p>Reinicie la instancia o el proceso. Si el problema persiste, informe al operador.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatIO 4</p></td>
<td><p>Representa los errores de E/S, que proceden del sistema operativo y están fuera del control de ESE. Este tipo de error puede ser temporal.</p></td>
<td><p>Vuelva a intentarlo y, si el error continúa, pida al operador que compruebe el disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatResource 5</p></td>
<td><p>Representa una categoría de errores relacionados con la falta de condiciones de recursos.</p></td>
<td><p>Consulte subcategorías.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatMemory 6</p></td>
<td><p>Representa un error causado por falta de memoria.</p></td>
<td><p>Vuelva a intentarlo después de un período de tiempo, liberar memoria o salir.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatQuota 7</p></td>
<td><p>Algunos recursos especializados están en grupos de un tamaño determinado, lo que &quot; &quot; facilita la detección de pérdidas de estos recursos.</p></td>
<td><p>La aplicación debe <strong>Assert() para</strong> detectar estos problemas durante el desarrollo. Sin embargo, en el código comercial, la aplicación debe tratar esto como un error de memoria.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatDisk 8</p></td>
<td><p>Representa un error causado por la falta de espacio en disco.</p></td>
<td><p>Vuelva a intentarlo más tarde para determinar si hay más espacio en disco disponible o pida al operador que liberará espacio en disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatData 9</p></td>
<td><p>Representa una categoría de nivel superior para los errores relacionados con los datos.</p></td>
<td><p>Consulte subcategorías.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatCorruption 10</p></td>
<td><p>Representa un problema de daños, que a menudo es permanente sin acción correctiva.</p></td>
<td><p>Restaurar desde la copia de seguridad mediante la operación de reparación de utilidades de ESE (esta operación solo restaura los datos que quedan o pierden). Además, cuando se usa el método recovery(JetInit), la recuperación se puede realizar permitiendo la pérdida de datos (para obtener más información, <a href="gg269296(v=exchg.10).md">vea JET_bitReplayIgnoreLostLogs</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatInconsistent 11</p></td>
<td><p>Representa un error en el que la base de datos o los archivos de registro están en un estado incoherente y no se puede conciliar. Este error puede deberse a un error de administración o aplicación.</p></td>
<td><p>Restaure desde la copia de seguridad mediante la operación de reparación de utilidades de ESE (que solo restaura los datos que quedan o pierden). También en el caso de la operación <strong>recovery(JetInit),</strong> la recuperación se puede realizar permitiendo la pérdida de datos (para obtener más información, <a href="gg269296(v=exchg.10).md">vea JET_bitReplayIgnoreLostLogs</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatFragmentation 12</p></td>
<td><p>Representa una clase de errores en la que se ha ejecutado algún recurso interno persistente.</p></td>
<td><p>En el caso de los errores de base de datos, la desfragmentación sin conexión corregirá el problema. Para los archivos de registro, recupere primero todas las bases de datos adjuntas a un apagado limpio y, a continuación, elimine todos los archivos de registro y el punto de control.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatApi 13</p></td>
<td><p>Consulte subcategorías.</p></td>
<td><p>Consulte subcategorías.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatUsage 14</p></td>
<td><p>Representa un error de uso. El código de cliente no pasó los argumentos correctos a la API <strong>jet.</strong> Este error se conservará con reintento.</p></td>
<td><p>El código de cliente debe usar <strong>el método Assert()</strong> para asegurarse de que no se devuelve esta clase de errores, por lo que se pueden capturar problemas durante el desarrollo. En el comercio minorista, la aplicación debe notificar al operador sobre el error.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatState 15</p></td>
<td><p>Representa una clase de mensajes que la API puede devolver para describir el estado de la base de datos. Por ejemplo, el <a href="gg294103(v=exchg.10).md">método JetSeek()</a> podría devolver JET_errRecordNotFound <strong>cuando</strong> no se encontró el registro solicitado.</p></td>
<td><p>Varía en función de la API.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatObsolete 16</p></td>
<td><p>Representa los errores que son de una versión anterior del motor. El motor actual no debe devolver estos errores.</p></td>
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
<td><p>Declarado en Esent.h.</p></td>
</tr>
</tbody>
</table>

