---
description: 'Más información sobre: enumeración JET_ERRCAT datos'
title: JET_ERRCAT enumeración (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: JET_ERRCAT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errcat(v=EXCHG.10)
ms:contentKeyID: 55104419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e08ec4ce308003dc30edaa32a07000e244dc9f37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360118"
---
# <a name="jet_errcat-enumeration"></a>JET_ERRCAT enumeración

Categoría de error. La jerarquía es la siguiente: JET_errcatError | |-- JET_errcatOperation | |-- JET_errcatFatal | |-- JET_errcatIO // problemas de E/S no son transitorios. | |-- JET_errcatResource | |-- JET_errcatMemory // falta de memoria (todas las variantes) | |-- JET_errcatQuota | |-- JET_errcatDisk // falta de espacio en disco (todas las variantes) |-- JET_errcatData | |-- JET_errcatCorruption | |-- JET_errcatInconsistent // normalmente causado por un control | |-- JET_errcatFragmentation |-- JET_errcatApi |-- JET_errcatUsage |-- JET_errcatState |-- JET_errcatObsolete

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Enumeration JET_ERRCAT
'Usage
Dim instance As JET_ERRCAT
```

``` csharp
public enum JET_ERRCAT
```

## <a name="members"></a>Members

<table>
<thead>
<tr class="header">
<th></th>
<th>Nombre del miembro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Unknown</td>
<td>Categoría desconocida.</td>
</tr>
<tr class="even">
<td></td>
<td>Error</td>
<td>Categoría genérica.</td>
</tr>
<tr class="odd">
<td></td>
<td>Operación</td>
<td>Errores que normalmente pueden producirse en cualquier momento debido a condiciones incontrolables. Con frecuencia es temporal, pero no siempre. Recuperación: probablemente vuelva a intentarlo o, finalmente, informe al operador.</td>
</tr>
<tr class="even">
<td></td>
<td>Grave</td>
<td>Este error de ordenación solo se produce cuando ese encuentra una condición de error tan grave que no podemos continuar de forma segura (a menudo transaccional) y, en lugar de datos dañados, se producen errores de esta categoría. Recuperación: reinicie la instancia o el proceso. Si el problema persiste, informe al operador.</td>
</tr>
<tr class="odd">
<td></td>
<td>IO</td>
<td>Los errores de sistema operativo proceden del sistema operativo y están fuera del control de ESE, este tipo de error es posiblemente temporal, posiblemente no. Recuperación: vuelva a intentarlo. Si no se resuelve, pregunte al operador sobre el problema del disco.</td>
</tr>
<tr class="even">
<td></td>
<td>Recurso</td>
<td>Se trata de una categoría que indica una de las muchas posibles condiciones de falta de recursos.</td>
</tr>
<tr class="odd">
<td></td>
<td>Memoria</td>
<td>Condición clásica de memoria fuera de memoria. Recuperación: espere un tiempo y vuelva a intentarlo, liberar memoria o salir.</td>
</tr>
<tr class="even">
<td></td>
<td>Quota</td>
<td>Algunos recursos especializados están en grupos de un tamaño determinado, lo que &quot; &quot; facilita la detección de pérdidas de estos recursos. Recuperación: puede requerir algunos cambios menores en el código. La aplicación solo debe tener una acción de depuración, como assert, en estas condiciones para detectarlas durante el desarrollo. Para el código comercial, se recomienda tratar este error como el error de categoría Memoria y reintentar, liberar memoria o salir de la operación.</td>
</tr>
<tr class="odd">
<td></td>
<td>Disco</td>
<td>Condiciones fuera del disco. Recuperación: puede volver a intentarlo más adelante con la esperanza de que haya más espacio disponible, o bien pedir al operador que libera espacio en disco.</td>
</tr>
<tr class="even">
<td></td>
<td>Datos</td>
<td>Error relacionado con los datos.</td>
</tr>
<tr class="odd">
<td></td>
<td>Corrupción</td>
<td>Mi unidad de disco duro se comió mi deber. Problemas de daños clásicos, con frecuencia permanentes sin acción correctiva. Recuperación: restauración a partir de la copia de seguridad, quizás la operación de reparación de utilidades de ese (que solo recupera qué datos quedan o pierden). También en el caso de la recuperación (JetInit), quizás se puede realizar la recuperación permitiendo la pérdida de datos.</td>
</tr>
<tr class="even">
<td></td>
<td>Inconsistente</td>
<td>Esto es similar a Daños en que la base de datos o los archivos de registro están en un estado incoherente y no conciliable entre sí. A menudo, esto se debe a un uso desacertado de la aplicación o el administrador. Recuperación: restauración a partir de la copia de seguridad, quizás la operación de reparación de utilidades de ese (que solo recupera los datos que se quedan o pierden). También en el caso de la recuperación (JetInit), quizás se puede realizar la recuperación permitiendo la pérdida de datos.</td>
</tr>
<tr class="odd">
<td></td>
<td>Fragmentación</td>
<td>Se trata de una clase de errores donde se ha ejecutado algún recurso interno persistente. Recuperación: en el caso de los errores de la  base de datos, la desfragmentación sin conexión corregirá el problema; en primer lugar, los archivos de registro recuperarán todas las bases de datos adjuntas a un apagado limpio y, a continuación, eliminarán todos los archivos de registro y el punto de control.</td>
</tr>
<tr class="even">
<td></td>
<td>API</td>
<td>Un contenedor para Usage y State.</td>
</tr>
<tr class="odd">
<td></td>
<td>Uso</td>
<td>Error de uso clásico, esto significa que el código de cliente no pasó los argumentos correctos a la API de JET. Este error probablemente no desaparecerá con el reintento. Recuperación: por lo general, el código de cliente debe assert() esta clase de errores no se devuelve, por lo que se pueden capturar problemas durante el desarrollo. En el comercio minorista, es probable que la aplicación tenga pocas opciones, pero devolver el problema al operador.</td>
</tr>
<tr class="even">
<td></td>
<td>State</td>
<td>Esta es la clasificación de las distintas señales que la API podría devolver y describe el estado de la base de datos; un caso clásico es JET_errRecordNotFound que JetSeek() puede devolver cuando no se encuentra el registro que solicitó. Recuperación: no es realmente relevante, depende en gran medida de la API.</td>
</tr>
<tr class="odd">
<td></td>
<td>Obsoletos</td>
<td>El error se reconoce como un error válido, pero no se espera que lo devuelva esta versión de la API.</td>
</tr>
<tr class="even">
<td></td>
<td>Max</td>
<td>Valor máximo de la enumeración. No se debe usar.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
