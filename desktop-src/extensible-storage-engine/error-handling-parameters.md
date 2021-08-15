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
ms.openlocfilehash: 01e2f8cbdec9defb2e277f20d186937120ff4f50a85110793833fa33a65b4112
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119365425"
---
# <a name="error-handling-parameters"></a>Parámetros de control de errores


_**Se aplica a:** Windows | Windows Servidor_

## <a name="error-handling-parameters"></a>Parámetros de control de errores

Este tema contiene parámetros que se usan para el control de errores.

*JET_paramErrorToString* 70  

Este parámetro se puede usar para convertir un [JET_ERR](./jet-err.md) en una cadena. Esto se hace mediante una llamada especial a [JetGetSystemParameter,](./jetgetsystemparameter-function.md) donde el búfer de salida entero contiene el valor [JET_ERR que](./jet-err.md) se va a convertir (como parámetro de entrada) y el búfer de salida de cadena devuelve la cadena de error correspondiente. La cadena tendrá un aspecto parecido a este: "JET_errSuccess, Operación correcta". La cadena se compone del nombre simbólico de la cadena, después una coma y, a continuación, una descripción de texto simple del error. La cadena de descripción puede contener comas. Si no se reconoce el error, la cadena será "Error desconocido,Error desconocido".

**Nota**  Este parámetro es de solo lectura.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>Especial</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Especial</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>Especial</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Todo</p></td>
</tr>
</tbody>
</table>

*JET_paramExceptionAction*  
98  

Este parámetro controla lo que sucede cuando el motor de base de datos o el código a los que llama el motor de base de datos inician una excepción. Cuando se establece en JET_ExceptionMsgBox, se producirá cualquier excepción en el Windows de excepciones no controladas. Esto dará lugar a que la excepción se controle como un error de aplicación. La intención es evitar que el código de la aplicación intente detectar y omitir erróneamente una excepción generada por el motor de base de datos. Esto no se puede permitir porque podría producirse un daño en la base de datos. Si la aplicación desea controlar correctamente estas excepciones, la protección se puede deshabilitar estableciendo este parámetro en JET_ExceptionNone.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>JET_ExceptionMsgBox</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>JET_ExceptionMsgBox, JET_ExceptionNone</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p></td>
<td><p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  No</p>
<p><strong>Windows Vista:</strong>  Sí</p></td>
</tr>
<tr class="even">
<td><p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p></td>
<td><p><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  No</p>
<p><strong>Windows Vista:</strong>  Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Todo</p></td>
</tr>
</tbody>
</table>

### <a name="requirements"></a>Requisitos

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
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
</tbody>
</table>

### <a name="see-also"></a>Consulte también

[Constantes de control de errores](./error-handling-constants.md)  
[Códigos de error Storage motor extensible](./extensible-storage-engine-error-codes.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JetInit](./jetinit-function.md)
