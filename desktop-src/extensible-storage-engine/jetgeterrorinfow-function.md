---
description: 'Más información acerca de: JetGetErrorInfoW (función)'
title: JetGetErrorInfoW función)
TOCTitle: JetGetErrorInfoW Function
ms:assetid: 7a84f937-7a16-434e-896d-789f316ee833
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475859(v=EXCHG.10)
ms:contentKeyID: 37033565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetErrorInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bf4db5d8d34a741e57f72e8f237f1497de0bacf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104157281"
---
# <a name="jetgeterrorinfow-function"></a>JetGetErrorInfoW función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgeterrorinfow-function"></a>JetGetErrorInfoW función)

La función **JetGetErrorInfoW** BAS_ del motor de base de datos.

Nota: esta documentación se basa en una versión preliminar del motor de almacenamiento extensible. Esta información está sujeta a cambios.

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a>Parámetros

*pvContext*

El valor de contexto o error para el que se necesita la información de error extendida. El valor que se pasa depende del valor del parámetro *InfoLevel* .

*pvResult*

Un puntero a un búfer que recibirá la información. El tipo del búfer depende del valor del parámetro *InfoLevel* . El autor de la llamada debe estar configurado para alinear el búfer adecuadamente.

*cbMax*

Tamaño máximo de la estructura *pvResult* que se pasa.

*InfoLevel*

El tipo de información que se recuperará para el contexto o la información de error se especifica mediante el parámetro *pvContext* . El formato de los datos que se almacenan en *pvResult* depende de *InfoLevel*.

En la tabla siguiente se enumeran los posibles valores para este parámetro.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_ErrorInfoSpecificErr</p></td>
<td><p><em>pvContext</em> se interpreta como un <a href="gg269297(v=exchg.10).md">JET_ERR</a>/error Code, <em>pvResult</em> se interpreta como un <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>y los campos de la estructura <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> se rellenan de forma adecuada.</p></td>
</tr>
</tbody>
</table>


*grbit*

Reservado.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de datos [JET_ERR](./extensible-storage-engine-error-codes.md) con uno de los códigos de retorno que se enumeran en la tabla siguiente. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

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
<td><p>Uno de los parámetros proporcionados contiene un valor inesperado o contiene un valor que no tiene sentido cuando se combina con el valor de otro parámetro. Esto puede ocurrir para <strong>JetGetErrorInfo</strong> cuando se produce lo siguiente:</p>
<ul>
<li><p>El valor del parámetro <em>InfoLevel</em> especificado no es válido.</p></li>
<li><p>El valor de <em>grbit</em> especificado no es válido.</p></li>
<li><p>El valor de <em>cbMax</em> del búfer del parámetro <em>pvResult</em> especificado es menor que el tamaño necesario para la salida de este parámetro <em>InfoLevel</em> .</p></li>
<li><p>En el caso de <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, el motor no conoce el valor de <a href="gg294092(v=exchg.10).md">JET_ERR</a> pasado.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errDisabledFunctionality</p></td>
<td><p>Si esta SKU de Windows no admite esta función, se devolverá este error.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, el búfer de salida adecuado para el contexto o valor de error solicitado se establecerá en la información de error extendida solicitada.

En caso de error, el estado de los búferes de salida será undefined.

### <a name="remarks"></a>Observaciones

La función [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) y [JET_ERRCAT](./jet-errcat.md) grupo de constantes contienen documentación sobre la información de error extendida que se devuelve para *InfoLevel* = JET_ErrorInfoSpecificErr.

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
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Nota: solo se implementa <strong>JetGetErrorInfoW</strong> (Unicode). Esta API no tiene una versión A (ANSI).</p></td>
</tr>
</tbody>
</table>
