---
description: 'Más información sobre: Función JetGetErrorInfoW'
title: JetGetErrorInfoW (Función)
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
ms.openlocfilehash: 867d96561459d009be8464f431307bfa373e8782
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983428"
---
# <a name="jetgeterrorinfow-function"></a>JetGetErrorInfoW (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgeterrorinfow-function"></a>JetGetErrorInfoW (Función)

La **función JetGetErrorInfoW** BAS_ del motor de base de datos.

Nota: Esta documentación se basa en una versión preliminar de Extensible Storage Engine. Esta información está sujeta a cambios.

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

Contexto o valor de error para el que se necesita la información de error extendida. El valor pasado depende del valor *del parámetro InfoLevel.*

*pvResult*

Puntero a un búfer que recibirá la información. El tipo del búfer depende del valor *del parámetro InfoLevel.* El autor de la llamada debe estar configurado para alinear el búfer correctamente.

*cbMax*

Tamaño máximo de la *estructura pvResult* que se pasa.

*InfoLevel*

El tipo de información que se recuperará para la información o el contexto de error se especifica mediante el *parámetro pvContext.* El formato de los datos almacenados en *pvResult* depende de *InfoLevel*.

En la tabla siguiente se enumeran los valores posibles para este parámetro.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_ErrorInfoSpecificErr</p> | <p><em>pvContext</em> se interpreta como un JET_ERR <a href="gg269297(v=exchg.10).md">/error</a>code, <em>pvResult</em> se interpreta como un <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>y los campos de la estructura <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> se rellenan correctamente.</p> | 



*grbit*

Reservado.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./extensible-storage-engine-error-codes.md) tipo de datos con uno de los códigos de retorno enumerados en la tabla siguiente. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contiene un valor inesperado o un valor que no tiene sentido cuando se combina con el valor de otro parámetro. Esto puede ocurrir para <strong>JetGetErrorInfo</strong> cuando se produce lo siguiente:</p><ul><li><p>El valor del <em>parámetro InfoLevel</em> especificado no es válido.</p></li><li><p>El valor <em>grbit especificado</em> no es válido.</p></li><li><p>El valor <em>cbMax del</em> búfer del parámetro <em>pvResult</em> especificado es menor que el tamaño necesario para la salida de <em>este parámetro InfoLevel.</em></p></li><li><p>Para <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, <a href="gg294092(v=exchg.10).md">el JET_ERR</a> de datos pasado es desconocido para el motor.</p></li></ul> | 
| <p>JET_errDisabledFunctionality</p> | <p>Si esta SKU de Windows no admite esta función, se devolverá este error.</p> | 



Si se ejecuta correctamente, el búfer de salida adecuado para el valor o contexto de error solicitado se establecerá en la información de error extendida solicitada.

En caso de error, el estado de los búferes de salida será indefinido.

### <a name="remarks"></a>Observaciones

La [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) y [el JET_ERRCAT](./jet-errcat.md) de constantes contienen documentación sobre la información de error extendida que se devuelve para *InfoLevel* = JET_ErrorInfoSpecificErr.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows 8 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Nota: Solo <strong>se implementa JetGetErrorInfoW</strong> (Unicode). Esta API no tiene una versión A (ANSI).</p> | 

