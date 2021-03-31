---
description: 'Más información acerca de: JetCloseFile (función)'
title: JetCloseFile función)
TOCTitle: JetCloseFile Function
ms:assetid: e8930915-8102-44b0-ae42-abedbd3e0512
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294127(v=EXCHG.10)
ms:contentKeyID: 32765741
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFile
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29fc2c76bf8528956d3e3331b3c2f23bf52f929f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423648"
---
# <a name="jetclosefile-function"></a>JetCloseFile función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetclosefile-function"></a>JetCloseFile función)

La función **JetCloseFile** cierra un archivo que se abrió con [JetOpenFile](./jetopenfile-function.md) después de que los datos de ese archivo se hayan extraído con [JetReadFile](./jetreadfile-function.md).

```cpp
    JET_ERR JET_API JetCloseFile(
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a>Parámetros

*hfFile*

Identificador del archivo que se va a leer.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código devuelto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>La operación se ha completado correctamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p>Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro. Esto puede ocurrir para <strong>JetCloseFile</strong> cuando:</p>
<ul>
<li><p>El identificador de instancia especificado no es válido (Windows XP y versiones posteriores),</p></li>
<li><p>El identificador de archivo especificado no es válido.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia cuando en realidad existen varias instancias.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se cierra el identificador de archivo. Si se ha cerrado un archivo de base de datos, se destruye el archivo de revisión de la base de datos asociado (si existe).

En caso de error, no se produce ningún cambio.

#### <a name="remarks"></a>Observaciones

Actualmente, el motor de base de datos solo admite un archivo abierto a través de [JetOpenFile](./jetopenfile-function.md) a la vez. Si se abre un identificador de archivo con [JetOpenFile](./jetopenfile-function.md) , se debe cerrar con **JetCloseFile** antes de que se pueda abrir otro archivo.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_HANDLE](./jet-handle.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopService](./jetstopservice-function.md)
