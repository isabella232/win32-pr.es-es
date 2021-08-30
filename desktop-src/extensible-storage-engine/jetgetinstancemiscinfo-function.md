---
description: 'Más información sobre: JetGetInstanceMiscInfo (Función)'
title: Función JetGetInstanceMiscInfo
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
ms.openlocfilehash: 3fe6dbdc997b7c9f72094999aa852036c578dd99
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988508"
---
# <a name="jetgetinstancemiscinfo-function"></a>Función JetGetInstanceMiscInfo


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetinstancemiscinfo-function"></a>Función JetGetInstanceMiscInfo

La **función JetGetInstanceMiscInfo** recupera información sobre la instancia mientras la instancia está en línea.

**Windows Vista: JetGetInstanceMiscInfo** se presenta en Windows Vista.

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parámetros

*Ejemplo*

Identifica la instancia de base de datos que se usará para la llamada API.

*pvResult*

Puntero a un búfer que recibirá la información. El tipo del búfer depende de *InfoLevel.* El autor de la llamada es responsable de alinear el búfer correctamente.

*cbMax*

Tamaño, en bytes, del búfer pasado en *pvResult*.

*InfoLevel*

Determina qué tipo de información se recuperará para la instancia especificada por *la instancia*. El formato de los datos almacenados *en pvResult* depende de *InfoLevel*.

Las siguientes opciones están disponibles para su uso con este parámetro.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_InstanceMiscInfoLogSignature</p> | <p><em>pvResult</em> se interpreta como una estructura <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> de la secuencia del registro de transacciones asociada a esta instancia.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>El búfer era demasiado pequeño.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Se especificó <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> <em>infoLevel</em> no válido o no válido.</p> | 



#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SIGNATURE](./jet-signature-structure.md)
