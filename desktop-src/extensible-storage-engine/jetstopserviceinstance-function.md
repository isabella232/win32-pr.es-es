---
description: 'Más información sobre: JetStopServiceInstance (Función)'
title: Función JetStopServiceInstance
TOCTitle: JetStopServiceInstance Function
ms:assetid: d8d3d047-91d6-4054-b3e1-44174666900e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294108(v=EXCHG.10)
ms:contentKeyID: 32765723
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopServiceInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e82f7b3ea85ffb76f58dd0ada8c56b83ecdf40a4b40e799b7ae482f307d1f916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614635"
---
# <a name="jetstopserviceinstance-function"></a>Función JetStopServiceInstance


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetstopserviceinstance-function"></a>Función JetStopServiceInstance

La **función JetStopServiceInstance** prepara una instancia para la terminación.

**Windows XP:****JetStopServiceInstance** se introdujo en Windows XP.  

```cpp
    JET_ERR JET_API JetStopServiceInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parámetros

*Ejemplo*

Instancia en ejecución que se usará para la llamada API.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>El parámetro de instancia especificado tiene un valor no válido (no una instancia que se está ejecutando actualmente).</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
</tbody>
</table>


Si esta función se realiza correctamente, se prepara para una terminación futura. Los pasos necesarios para prepararse para una terminación incluyen los siguientes:

  - Detenga la desfragmentación en línea si se está ejecutando.

  - Inicie una limpieza del almacén de versiones.

  - Para reducir la profundidad del punto de control, empiece a vaciar las páginas desatendcidas en el administrador de búferes.

  - Evitar llamadas futuras a la mayoría de las funciones de esa instancia.

Si se produce un error en esta función, no se realizará ninguno de los pasos para prepararse para la terminación de una instancia, por lo que no se producirá ningún cambio en el estado de la instancia.

#### <a name="remarks"></a>Comentarios

Esta función reducirá el trabajo que tendrá que realizar la instancia cuando finalice, pero no finalizará la instancia. Como resultado, esta función es simplemente una optimización y no es obligatoria de usar. Tenga en cuenta que la cantidad de trabajo realizado en preparación fue menor Windows 2000 y Windows XP. Una vez que la función se realiza correctamente, la llamada a funciones que ya no se permiten devolverá JET_errClientRequestToStopJetService. Las funciones que todavía se permiten después de esta llamada son: [JetRollback,](./jetrollback-function.md) [JetCloseTable,](./jetclosetable-function.md) [JetEndSession,](./jetendsession-function.md) [JetCloseDatabase,](./jetclosedatabase-function.md) [JetDetachDatabase](./jetdetachdatabase-function.md) y [JetResetSessionContext.](./jetresetsessioncontext-function.md)

#### <a name="requirements"></a>Requisitos

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
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
