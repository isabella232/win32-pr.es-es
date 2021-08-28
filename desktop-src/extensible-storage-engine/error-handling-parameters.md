---
description: 'Más información sobre: Parámetros de control de errores'
title: Parámetros de control de errores
TOCTitle: Error Handling Parameters
ms:assetid: 014996a1-5674-40c7-9538-54cae1681fec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269173(v=EXCHG.10)
ms:contentKeyID: 32765476
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 698854aa81ddd7a44fcf58dd250444e657d44a0c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982018"
---
# <a name="error-handling-parameters"></a>Parámetros de control de errores


_**Se aplica a:** Windows | Windows Servidor_

## <a name="error-handling-parameters"></a>Parámetros de control de errores

Este tema contiene parámetros que se usan para el control de errores.

*JET_paramErrorToString* 70  

Este parámetro se puede usar para convertir un [JET_ERR](./jet-err.md) en una cadena. Esto se realiza mediante una llamada especial a [JetGetSystemParameter](./jetgetsystemparameter-function.md) donde el búfer de salida entero contiene el valor [JET_ERR que](./jet-err.md) se va a convertir (como parámetro de entrada) y el búfer de salida de cadena devuelve la cadena de error correspondiente. La cadena tendrá un aspecto parecido al siguiente: "JET_errSuccess operación correcta". La cadena se compone del nombre simbólico de la cadena, después una coma y, a continuación, una descripción de texto simple del error. La cadena de descripción puede contener comas. Si no se reconoce el error, la cadena será "Error desconocido,Error desconocido".

**Nota**  Este parámetro es de solo lectura.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>Especial</p> | 
| <p>Escriba:</p> | <p>Especial</p> | 
| <p>Intervalo válido:</p> | <p>Especial</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>No</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>No</p> | 
| <p>Afecta al rendimiento:</p> | <p>No</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 


*JET_paramExceptionAction*  
98  

Este parámetro controla lo que sucede cuando el motor de base de datos o el código al que llama el motor de base de datos produce una excepción. Cuando se establece en JET_ExceptionMsgBox, se producirá cualquier excepción en el Windows de excepciones no controladas. Esto dará lugar a que la excepción se controle como un error de la aplicación. La intención es evitar que el código de la aplicación intente detectar y omitir erróneamente una excepción generada por el motor de base de datos. Esto no se puede permitir porque podría producirse un daño en la base de datos. Si la aplicación desea controlar correctamente estas excepciones, la protección se puede deshabilitar estableciendo este parámetro en JET_ExceptionNone.


| Etiqueta | Value |
|--------|-------|
| <p>Valor predeterminado:</p> | <p>JET_ExceptionMsgBox</p> | 
| <p>Escriba:</p> | <p>Entero</p> | 
| <p>Intervalo válido:</p> | <p>JET_ExceptionMsgBox, JET_ExceptionNone</p> | 
| <p>Ámbito:</p> | <p>Global</p> | 
| <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  No</p><p><strong>Windows Vista:</strong>  Sí</p> | 
| <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  No</p><p><strong>Windows Vista:</strong>  Sí</p> | 
| <p>Afecta al diseño físico:</p> | <p>No</p> | 
| <p>Afecta a la confiabilidad:</p> | <p>Sí</p> | 
| <p>Afecta al rendimiento:</p> | <p>No</p> | 
| <p>Afecta a los recursos:</p> | <p>No</p> | 
| <p>Disponibilidad:</p> | <p>All</p> | 


### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 


### <a name="see-also"></a>Consulte también

[Constantes de control de errores](./error-handling-constants.md)  
[Códigos de error Storage motor extensibles](./extensible-storage-engine-error-codes.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JetInit](./jetinit-function.md)
