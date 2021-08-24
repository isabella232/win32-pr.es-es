---
description: Convierte la cadena Unicode especificada en una nueva cadena de caracteres, mediante la página de códigos Formato de transformación Unicode de 8 bits (UTF-8).
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: Función RtlUnicodeToUTF8N (Wdm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUnicodeToUTF8N
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3580eb86deba77bcc214cf69fbd21f65fee2735ef3a5ff73319b415d2c814d88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538035"
---
# <a name="rtlunicodetoutf8n-function"></a>Función RtlUnicodeToUTF8N

Convierte la cadena Unicode especificada en una nueva cadena de caracteres, mediante la página de códigos Formato de transformación Unicode de 8 bits (UTF-8).

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI RtlUnicodeToUTF8N(
  _Out_     PCHAR  UTF8StringDestination,
  _In_      ULONG  UTF8StringMaxByteCount,
  _Out_opt_ PULONG UTF8StringActualByteCount,
  _In_      PCWSTR UnicodeStringSource,
  _In_      ULONG  UnicodeStringByteCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UTF8StringDestination* \[ out\]
</dt> <dd>

Puntero a un búfer asignado por el autor de la llamada para recibir la cadena traducida.

</dd> <dt>

*UTF8StringMaxByteCount* \[ En\]
</dt> <dd>

Número máximo de bytes que se van a escribir *en UTF8StringDestination.* Si este valor provoca el truncamiento de la cadena traducida, **RtlUnicodeToUTF8N** devuelve un estado de error.

</dd> <dt>

*UTF8StringActualByteCount* \[ out, opcional\]
</dt> <dd>

Puntero a una variable asignada por el autor de la llamada que recibe la longitud, en bytes, de la cadena traducida. Este parámetro es opcional y puede ser **NULL.** Si la cadena se trunca, el número devuelto cuenta el recuento real de cadenas truncadas.

</dd> <dt>

*UnicodeStringSource* \[ En\]
</dt> <dd>

Puntero a la cadena de origen Unicode que se va a traducir.

</dd> <dt>

*UnicodeStringByteCount * \[ en\]
</dt> <dd>

Especifica el número de bytes de la cadena de origen Unicode a la que apunta el parámetro *UnicodeStringSource.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**RtlUnicodeToUTF8N devuelve** uno de los siguientes valores NTSTATUS:



| Código devuelto                                                                                                  | Descripción                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ESTADO \_ CORRECTO**</dt> </dl>               | La cadena Unicode se convirtió a UTF-8.<br/>                                                           |
| <dl> <dt>**ESTADO \_ ALGUNOS \_ NO \_ ASIGNADOS**</dt> </dl>     | Se encontró y se reemplazó un carácter de entrada no válido. Este estado se considera un estado correcto.<br/> |
| <dl> <dt>**PARÁMETRO STATUS \_ INVALID \_**</dt> </dl>    | Ambos punteros a *UTF8StringDestination* y *UTF8StringActualByteCount* eran **NULL.**<br/>              |
| <dl> <dt>**PARÁMETRO \_ STATUS INVALID \_ \_ 4**</dt> </dl> | *UnicodeStringSource era* **NULL.**<br/>                                                              |
| <dl> <dt>**BÚFER DE \_ ESTADO \_ DEMASIADO \_ PEQUEÑO**</dt> </dl>    | *UTF8StringDestination* se ha truncado.<br/>                                                               |



 

## <a name="remarks"></a>Comentarios

Aunque *UTF8StringActualByteCount* es opcional y puede ser **NULL,** los llamadores deben proporcionar almacenamiento para él, ya que la longitud recibida se puede usar para determinar si la conversión se ha realizado correctamente. Esta rutina no modifica la cadena de origen. Devuelve una cadena UTF-8 terminada en NULL si el *UnicodeStringSource* determinado incluía un terminador NULL y si el *UTF8StringMaxByteCount* dado no provocaba truncamiento.

Si la salida se trunca y se encuentra un carácter de entrada no válido, la función devuelve el error STATUS \_ BUFFER \_ TOO \_ SMALL.

Si *UTF8StringDestination* se establece en **NULL,** la función devolverá el número necesario de bytes para hospedar la cadena traducida sin truncamiento en *UTF8StringActualByteCount.*

Los llamadores **de RtlUnicodeToUTF8N** deben ejecutarse en IRQL < DISPATCH \_ LEVEL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wdm.h</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RtlUTF8ToUnicodeN**](rtlutf8tounicoden.md)
</dt> </dl>

 

 




