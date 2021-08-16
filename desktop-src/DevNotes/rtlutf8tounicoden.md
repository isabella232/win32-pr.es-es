---
description: Convierte la cadena de origen especificada en una cadena Unicode, mediante la página de códigos Formato de transformación Unicode (UTF-8) de 8 bits.
ms.assetid: 2871a81b-74f9-462e-9e5c-c59d06bb6841
title: Función RtlUTF8ToUnicodeN (Wdm.h)
ms.topic: reference
ms.date: 02/21/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUTF8ToUnicodeN
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8d6268857387d4caf4b024eb6dd308ac11349fe839173d307a311bf63ef84b56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119385565"
---
# <a name="rtlutf8tounicoden-function"></a>Función RtlUTF8ToUnicodeN

Convierte la cadena de origen especificada en una cadena Unicode, mediante la página de códigos Formato de transformación Unicode (UTF-8) de 8 bits.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI RtlUTF8ToUnicodeN(
  _Out_     PWSTR  UnicodeStringDestination,
  _In_      ULONG  UnicodeStringMaxByteCount,
  _Out_opt_ PULONG UnicodeStringActualByteCount,
  _In_      PCCH   UTF8StringSource,
  _In_      ULONG  UTF8StringByteCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UnicodeStringDestination* \[ out\]
</dt> <dd>

Puntero a un búfer asignado por el autor de la llamada que recibe la cadena traducida.

</dd> <dt>

*UnicodeStringMaxByteCount* \[ En\]
</dt> <dd>

Número máximo de bytes que se van a escribir *en UnicodeStringDestination*. Si este valor hace que la cadena traducida se trunca, **RtlUTF8ToUnicodeN** devuelve un estado de error.

</dd> <dt>

*UnicodeStringActualByteCount* \[ out, opcional\]
</dt> <dd>

Puntero a una variable asignada por el autor de la llamada que recibe la longitud, en bytes, de la cadena traducida. Este parámetro es opcional y puede ser **NULL.** Si la cadena se trunca, el número devuelto cuenta el recuento real de cadenas truncadas.

</dd> <dt>

*UTF8StringSource* \[ En\]
</dt> <dd>

Puntero a la cadena que se va a traducir.

</dd> <dt>

*UTF8StringByteCount* \[ En\]
</dt> <dd>

Tamaño, en bytes, de la cadena en *UTF8StringSource.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**RtlUTF8ToUnicodeN devuelve** uno de los siguientes valores NTSTATUS:



| Código devuelto                                                                                                  | Descripción                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ESTADO \_ CORRECTO**</dt> </dl>               | La cadena se ha convertido a Unicode.<br/>                                                                 |
| <dl> <dt>**ESTADO \_ ALGUNOS \_ NO \_ ASIGNADOS**</dt> </dl>     | Se encontró y se reemplazó un carácter de entrada no válido. Este estado se considera un estado correcto.<br/> |
| <dl> <dt>**PARÁMETRO \_ STATUS INVALID \_**</dt> </dl>    | Ambos punteros a *UnicodeStringDestination y* *UnicodeStringActualByteCount* eran **NULL.**<br/>       |
| <dl> <dt>**STATUS \_ INVALID \_ PARAMETER \_ 4**</dt> </dl> | *UTF8StringSource* era **NULL.**<br/>                                                                 |
| <dl> <dt>**BÚFER DE \_ ESTADO \_ DEMASIADO \_ PEQUEÑO**</dt> </dl>    | *UnicodeStringDestination* se ha truncado.<br/>                                                            |



 

## <a name="remarks"></a>Comentarios

Aunque *UnicodeStringActualByteCount* es opcional y puede ser **NULL,** los autores de la llamada deben proporcionar almacenamiento para él, ya que la longitud recibida se puede usar para determinar si la conversión se ha realizado correctamente.

Si la salida se trunca y se encuentra un carácter de entrada no válido, la función devuelve el error STATUS \_ BUFFER \_ TOO \_ SMALL.

Si *UnicodeStringDestination* se establece en **NULL,** la función devolverá el número necesario de bytes para hospedar la cadena traducida sin truncamiento en *UnicodeStringActualByteCount*.

**RtlUTF8ToUnicodeN** no modifica la cadena de origen a menos que los punteros *UnicodeStringDestination* y *UTF8StringSource* sean equivalentes. La cadena Unicode devuelta no termina en NULL.

Los llamadores **de RtlUTF8ToUnicodeN** deben ejecutarse en IRQL < DISPATCH \_ LEVEL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wdm.h</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RtlUnicodeToUTF8N**](rtlunicodetoutf8n.md)
</dt> </dl>

 

 




