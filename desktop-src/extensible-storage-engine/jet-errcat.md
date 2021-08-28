---
description: 'Más información sobre: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: dee8dc7850cf69957c360253b942117739fe405b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987558"
---
# <a name="jet_errcat"></a>JET_ERRCAT


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_errcat"></a>JET_ERRCAT

El **JET_ERRCAT** de constantes describe las clasificaciones de nivel superior o las categorías de errores. Este grupo de constantes permite a las aplicaciones definir el tratamiento predeterminado para una clasificación de errores, en lugar de controlar cada caso de error individualmente. También garantiza que la aplicación no tenga que controlar las nuevas condiciones de error que se incluyen en las clasificaciones existentes.

Nota: Esta documentación se basa en una versión preliminar de Extensible Storage Engine. Esta información está sujeta a cambios.

Las **JET_ERRCAT** constantes se organizan en una jerarquía específica de condiciones y subcondiciones, como se muestra a continuación:

|--- Error |--- Operation(al) | |--- Fatal | |--- IO | |--- Resource | |--- Memory | |--- Quota | |--- Disk | |--- Data | |--- Corruption | |--- Inconsistent | |--- Fragmentation | |--- API |--- Usage |--- State

En la tabla siguiente se enumeran **JET_ERRCAT** constantes y se proporciona una descripción e información de recuperación, según corresponda.


| <p>Constante o valor</p> | <p>Descripción</p> | <p>Recuperación</p> | 
|-----------------------|--------------------|-----------------|
| <p>JET_errcatUnknown 0</p> | <p>Categoría de error no válida.</p> | <p>N/D</p> | 
| <p>JET_errcatError 1</p> | <p>Categoría de nivel superior (ningún error debe ser de esta clase).</p> | <p>Vea las constantes de error específicas.</p> | 
| <p>JET_errcatOperation 2</p> | <p>Representa errores que pueden producirse en cualquier momento debido a condiciones incontrolables y que a menudo son temporales. Si se especifica, consulte subcategorías.</p> | <p>Vuelva a intentarlo y, si el error continúa, informe al operador.</p> | 
| <p>JET_errcatFatal 3</p> | <p>Representa errores irreales que, cuando se producen, crean un riesgo de que ESE no pueda continuar de forma segura (a menudo transaccional) y los datos se puedan dañar.</p> | <p>Reinicie la instancia o el proceso. Si el problema persiste, informe al operador.</p> | 
| <p>JET_errcatIO 4</p> | <p>Representa los errores de E/S, que proceden del sistema operativo y están fuera del control de ESE. Este tipo de error puede ser temporal.</p> | <p>Vuelva a intentarlo y, si el error continúa, pida al operador que compruebe el disco.</p> | 
| <p>JET_errcatResource 5</p> | <p>Representa una categoría de errores relacionados con la falta de condiciones de recursos.</p> | <p>Consulte subcategorías.</p> | 
| <p>JET_errcatMemory 6</p> | <p>Representa un error causado por la falta de memoria.</p> | <p>Vuelva a intentarlo después de un período de tiempo, liberar memoria o salir.</p> | 
| <p>JET_errcatQuota 7</p> | <p>Algunos recursos "especializados" están en grupos de un tamaño determinado, lo que facilita la detección de pérdidas de estos recursos.</p> | <p>La aplicación debe <strong>Assert() para</strong> detectar estos problemas durante el desarrollo. Sin embargo, en el código comercial, la aplicación debe tratar esto como un error de memoria.</p> | 
| <p>JET_errcatDisk 8</p> | <p>Representa un error causado por la falta de espacio en disco.</p> | <p>Vuelva a intentarlo más tarde para determinar si hay más espacio en disco disponible o pida al operador que liberara espacio en disco.</p> | 
| <p>JET_errcatData 9</p> | <p>Representa una categoría de nivel superior para los errores relacionados con los datos.</p> | <p>Consulte subcategorías.</p> | 
| <p>JET_errcatCorruption 10</p> | <p>Representa un problema de daños, que a menudo es permanente sin acción correctiva.</p> | <p>Restaurar a partir de la copia de seguridad mediante la operación de reparación de utilidades ese (esta operación solo restaura los datos que quedan o pierden). Además, cuando se usa el método recovery(JetInit), la recuperación se puede realizar permitiendo la pérdida de datos (para obtener más información, <a href="gg269296(v=exchg.10).md">vea JET_bitReplayIgnoreLostLogs</a>.</p> | 
| <p>JET_errcatInconsistent 11</p> | <p>Representa un error en el que la base de datos o los archivos de registro están en un estado incoherente y no se pueden conciliar. Este error puede deberse a un error de administración o aplicación.</p> | <p>Restaure a partir de la copia de seguridad mediante la operación de reparación de utilidades ese (que solo restaura los datos que se quedan o pierden). También en el caso de la operación <strong>recovery(JetInit),</strong> la recuperación se puede realizar permitiendo la pérdida de datos (para obtener más información, <a href="gg269296(v=exchg.10).md">vea JET_bitReplayIgnoreLostLogs</a>.</p> | 
| <p>JET_errcatFragmentation 12</p> | <p>Representa una clase de errores en la que se ha ejecutado algún recurso interno persistente.</p> | <p>En el caso de los errores de base de datos, la desfragmentación sin conexión corregirá el problema. En el caso de los archivos de registro, recupere primero todas las bases de datos adjuntas a un apagado limpio y, a continuación, elimine todos los archivos de registro y el punto de control.</p> | 
| <p>JET_errcatApi 13</p> | <p>Consulte subcategorías.</p> | <p>Consulte subcategorías.</p> | 
| <p>JET_errcatUsage 14</p> | <p>Representa un error de uso. El código de cliente no pasó los argumentos correctos a la API <strong>jet.</strong> Este error se conservará con reintento.</p> | <p>El código de cliente debe usar <strong>el método Assert()</strong> para asegurarse de que no se devuelve esta clase de errores, por lo que se pueden capturar problemas durante el desarrollo. En el comercio minorista, la aplicación debe notificar al operador sobre el error.</p> | 
| <p>JET_errcatState 15</p> | <p>Representa una clase de mensajes que la API puede devolver para describir el estado de la base de datos. Por ejemplo, el <a href="gg294103(v=exchg.10).md">método JetSeek()</a> podría devolver JET_errRecordNotFound <strong>cuando</strong> no se encontró el registro solicitado.</p> | <p>Varía en función de la API.</p> | 
| <p>JET_errcatObsolete 16</p> | <p>Representa los errores que son de una versión anterior del motor. El motor actual no debe devolver estos errores.</p> | <p>Desconocido.</p> | 
| <p>JET_errcatMax 17</p> | <p>Constante que indica el final de la enumeración.</p> | <p>N/D</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows 8 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 


