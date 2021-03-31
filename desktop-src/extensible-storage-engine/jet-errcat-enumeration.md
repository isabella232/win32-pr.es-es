---
description: 'Más información acerca de: enumeración JET_ERRCAT'
title: Enumeración JET_ERRCAT (Microsoft. ISAM. esent. Interop. Windows8)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277114"
---
# <a name="jet_errcat-enumeration"></a>Enumeración JET_ERRCAT

La categoría de error. La jerarquía es la siguiente: JET_errcatError | |--JET_errcatOperation | |--JET_errcatFatal | |--JET_errcatIO//problemas de e/s incorrectos, pueden o no ser transitorios. | |--JET_errcatResource | |--JET_errcatMemory//sin memoria (todas las variantes) | |--JET_errcatQuota | |--JET_errcatDisk//espacio insuficiente en disco (todas las variantes) |--JET_errcatData | |--JET_errcatCorruption | |--JET_errcatInconsistent//suele deberse a un mal control del usuario | |--JET_errcatFragmentation |--JET_errcatApi |--JET_errcatUsage |--JET_errcatState |--JET_errcatObsolete

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

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

## <a name="members"></a>Miembros

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
<td>Una categoría genérica.</td>
</tr>
<tr class="odd">
<td></td>
<td>Operación</td>
<td>Errores que normalmente se pueden producir en cualquier momento debido a condiciones no controlables. Con frecuencia temporal, pero no siempre. Recuperación: probablemente inténtelo de nuevo o informará al operador.</td>
</tr>
<tr class="even">
<td></td>
<td>Crítico</td>
<td>Este error de ordenación se produce solo cuando ESE encuentra una condición de error tan grave, que no se puede continuar en un modo seguro (a menudo transaccional) y no en los datos dañados que se producen errores de esta categoría. Recuperación: reinicie la instancia o el proceso. Si el problema persiste, informe al operador.</td>
</tr>
<tr class="odd">
<td></td>
<td>IO</td>
<td>O los errores provienen del sistema operativo y están fuera del control de ESE, es posible que este tipo de error sea temporal, posiblemente no. Recuperación: Reintentar. Si no se resuelve, preguntar al operador sobre el problema del disco.</td>
</tr>
<tr class="even">
<td></td>
<td>Recurso</td>
<td>Esta es una categoría que indica una de las numerosas condiciones de recursos insuficientes.</td>
</tr>
<tr class="odd">
<td></td>
<td>Memory</td>
<td>Estado de memoria insuficiente clásico. Recuperación: Espere un poco y vuelva a intentarlo, libere memoria o salga.</td>
</tr>
<tr class="even">
<td></td>
<td>Quota</td>
<td>Determinados &quot; &quot; recursos especializados se encuentran en grupos de cierto tamaño, lo que facilita la detección de pérdidas de estos recursos. Recuperación: podría requerir algunos cambios de código secundarios. La aplicación debe tener una acción de solo depuración, como una aserción, en estas condiciones para detectarlas durante el desarrollo. En el caso de código comercial, se recomienda que trate este error como el error de categoría de memoria y que vuelva a intentarlo, libere memoria o salga de la operación.</td>
</tr>
<tr class="odd">
<td></td>
<td>Disco</td>
<td>Condiciones de disco insuficiente. Recuperación: puede volver a intentarlo más tarde con la esperanza de que haya más espacio disponible o pedir al operador que libere espacio en disco.</td>
</tr>
<tr class="even">
<td></td>
<td>Datos</td>
<td>Un error relacionado con datos.</td>
</tr>
<tr class="odd">
<td></td>
<td>Ocasiona</td>
<td>Mi unidad de disco duro comió mis deberes. Problemas de daños clásicos, permanentes con frecuencia sin acción correctiva. Recuperación: restaure desde una copia de seguridad, quizás la operación de reparación de utilidades de ese (que solo recupera los datos que se han dejado y se pierden). Además, en el caso de la recuperación (JetInit), quizás se pueda realizar una recuperación al permitir la pérdida de datos.</td>
</tr>
<tr class="even">
<td></td>
<td>Incoherente</td>
<td>Esto es similar a los daños en que los archivos de base de datos o de registro se encuentran en un estado incoherente y no se pueden reconciliar entre sí. A menudo, esto se debe a un mal control del administrador o la aplicación. Recuperación: restaure desde una copia de seguridad, quizás la operación de reparación de utilidades de ese (que solo recupera los datos que se han dejado y se pierden). Además, en el caso de la recuperación (JetInit), quizás se pueda realizar una recuperación al permitir la pérdida de datos.</td>
</tr>
<tr class="odd">
<td></td>
<td>Fragmentación</td>
<td>Se trata de una clase de errores en los que se ha agotado algún recurso interno persistente. Recuperación: en el caso de los errores de base de datos, la desfragmentación sin conexión rectificará el problema. en _primer lugar_ , los archivos de registro recuperan todas las bases de datos asociadas a un cierre correcto y, a continuación, eliminan todos los archivos de registro y el punto de control</td>
</tr>
<tr class="even">
<td></td>
<td>API</td>
<td>Un contenedor para el uso y el estado.</td>
</tr>
<tr class="odd">
<td></td>
<td>Uso</td>
<td>Error de uso clásico, esto significa que el código de cliente no ha pasado los argumentos correctos a la API de JET. Este error probablemente no desaparecerá con el reintento. Recuperación: en general, el código de cliente debe imponer () no se devuelve esta clase de errores, por lo que se pueden detectar problemas durante el desarrollo. En el comercio minorista, es probable que la aplicación tenga poca opción pero devolver el problema al operador.</td>
</tr>
<tr class="even">
<td></td>
<td>Estado</td>
<td>Esta es la clasificación para las diferentes señales que la API podría devolver describe el estado de la base de datos, un caso clásico es JET_errRecordNotFound que puede ser devuelto por JetSeek () cuando no se encuentra el registro que solicitó. Recuperación: no es realmente relevante, depende en gran medida de la API.</td>
</tr>
<tr class="odd">
<td></td>
<td>Obsoletos</td>
<td>El error se reconoce como un error válido, pero no se espera que sea devuelto por esta versión de la API.</td>
</tr>
<tr class="even">
<td></td>
<td>Máx.</td>
<td>Valor máximo de la enumeración. No debe usarse.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
