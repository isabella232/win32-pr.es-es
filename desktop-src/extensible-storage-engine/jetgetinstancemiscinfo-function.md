---
description: 'Más información acerca de: JetGetInstanceMiscInfo (función)'
title: JetGetInstanceMiscInfo función)
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed63c6a5c6d3b2488f7226da0a1f23e1adb39e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083042"
---
# <a name="jetgetinstancemiscinfo-function"></a>JetGetInstanceMiscInfo función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetinstancemiscinfo-function"></a>JetGetInstanceMiscInfo función)

La función **JetGetInstanceMiscInfo** recupera información sobre la instancia, mientras que la instancia está en línea.

**Windows Vista: JetGetInstanceMiscInfo** se presentó en Windows Vista.

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parámetros

*repetición*

Identifica la instancia de base de datos que se utilizará para la llamada API.

*pvResult*

Puntero a un búfer que recibirá la información. El tipo de búfer depende de *InfoLevel*. El autor de la llamada es responsable de alinear el búfer adecuadamente.

*cbMax*

Tamaño, en bytes, del búfer pasado en *pvResult*.

*InfoLevel*

Determina qué tipo de información se recuperará para la instancia especificada por la *instancia* de. El formato de los datos almacenados en *pvResult* depende de *InfoLevel*.

Las siguientes opciones están disponibles para su uso con este parámetro.

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
<td><p>JET_InstanceMiscInfoLogSignature</p></td>
<td><p><em>pvResult</em> se interpreta como una estructura <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> de la secuencia de registro de transacciones asociada a esta instancia.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>El búfer era demasiado pequeño.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Se especificó una <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> no válida o un <em>InfoLevel</em> no válido.</p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008.</p></td>
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
[JET_SIGNATURE](./jet-signature-structure.md)
