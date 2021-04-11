---
description: Traduce la cadena de origen especificada en una cadena Unicode, usando la página de códigos del formato de transformación Unicode de 8 bits (UTF-8).
ms.assetid: 2871a81b-74f9-462e-9e5c-c59d06bb6841
title: Función RtlUTF8ToUnicodeN (WDM. h)
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
ms.openlocfilehash: 8b3de7192a9a26d367fc0b6ad231fbc046514ec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274905"
---
# <a name="rtlutf8tounicoden-function"></a>RtlUTF8ToUnicodeN función)

Traduce la cadena de origen especificada en una cadena Unicode, usando la página de códigos del formato de transformación Unicode de 8 bits (UTF-8).

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

*UnicodeStringDestination* \[ enuncia\]
</dt> <dd>

Puntero a un búfer asignado por el llamador que recibe la cadena traducida.

</dd> <dt>

*UnicodeStringMaxByteCount* \[ de\]
</dt> <dd>

Número máximo de bytes que se van a escribir en *UnicodeStringDestination*. Si este valor hace que la cadena traducida se trunque, **RtlUTF8ToUnicodeN** devuelve un estado de error.

</dd> <dt>

*UnicodeStringActualByteCount* \[ out, opcional\]
</dt> <dd>

Puntero a una variable asignada por el llamador que recibe la longitud, en bytes, de la cadena traducida. Este parámetro es opcional y puede ser **null**. Si la cadena se trunca, el número devuelto cuenta el recuento de cadenas truncadas real.

</dd> <dt>

*UTF8StringSource* \[ de\]
</dt> <dd>

Puntero a la cadena que se va a traducir.

</dd> <dt>

*UTF8StringByteCount* \[ de\]
</dt> <dd>

Tamaño, en bytes, de la cadena en *UTF8StringSource*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**RtlUTF8ToUnicodeN** devuelve uno de los siguientes valores de NTSTATUS:



| Código devuelto                                                                                                  | Descripción                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ESTADO \_ correcto**</dt> </dl>               | La cadena se convirtió a Unicode.<br/>                                                                 |
| <dl> <dt>**ESTADO \_ \_ no \_ asignado**</dt> </dl>     | Se encontró un carácter de entrada no válido y se ha reemplazado. Este estado se considera un estado correcto.<br/> |
| <dl> <dt>**ESTADO \_ parámetro no válido \_**</dt> </dl>    | Ambos punteros a *UnicodeStringDestination* y *UnicodeStringActualByteCount* eran **null**.<br/>       |
| <dl> <dt>**Parámetro de estado \_ no válido \_ \_ 4**</dt> </dl> | *UTF8StringSource* era **null**.<br/>                                                                 |
| <dl> <dt>**búfer de estado \_ \_ demasiado \_ pequeño**</dt> </dl>    | *UnicodeStringDestination* se truncó.<br/>                                                            |



 

## <a name="remarks"></a>Observaciones

Aunque *UnicodeStringActualByteCount* es opcional y puede ser **null**, los llamadores deben proporcionar almacenamiento para él, ya que la longitud recibida se puede usar para determinar si la conversión se realizó correctamente.

Si el resultado se trunca y se encuentra un carácter de entrada no válido, la función devuelve un error de búfer de estado \_ \_ demasiado \_ pequeño.

Si *UnicodeStringDestination* se establece en **null** , la función devolverá el número necesario de bytes para hospedar la cadena traducida sin ningún truncamiento en *UnicodeStringActualByteCount*.

**RtlUTF8ToUnicodeN** no modifica la cadena de origen a menos que los punteros *UnicodeStringDestination* y *UTF8StringSource* sean equivalentes. La cadena Unicode devuelta no termina en NULL.

Los autores de llamadas de **RtlUTF8ToUnicodeN** deben ejecutarse en el nivel de distribución de IRQL < \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>WDM. h</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RtlUnicodeToUTF8N**](rtlunicodetoutf8n.md)
</dt> </dl>

 

 




