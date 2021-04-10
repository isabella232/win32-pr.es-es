---
description: Traduce la cadena Unicode especificada en una nueva cadena de caracteres, usando la página de códigos del formato de transformación Unicode de 8 bits (UTF-8).
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: Función RtlUnicodeToUTF8N (WDM. h)
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
ms.openlocfilehash: 46153dd152ed5a45a65de50ca214fbb24a6dc2ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152962"
---
# <a name="rtlunicodetoutf8n-function"></a>RtlUnicodeToUTF8N función)

Traduce la cadena Unicode especificada en una nueva cadena de caracteres, usando la página de códigos del formato de transformación Unicode de 8 bits (UTF-8).

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

*UTF8StringDestination* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer asignado por el llamador para recibir la cadena traducida.

</dd> <dt>

*UTF8StringMaxByteCount* \[ de\]
</dt> <dd>

Número máximo de bytes que se van a escribir en *UTF8StringDestination*. Si este valor hace que la cadena traducida se trunque, **RtlUnicodeToUTF8N** devuelve un estado de error.

</dd> <dt>

*UTF8StringActualByteCount* \[ out, opcional\]
</dt> <dd>

Puntero a una variable asignada por el llamador que recibe la longitud, en bytes, de la cadena traducida. Este parámetro es opcional y puede ser **null**. Si la cadena se trunca, el número devuelto cuenta el recuento de cadenas truncadas real.

</dd> <dt>

*UnicodeStringSource* \[ de\]
</dt> <dd>

Puntero a la cadena de origen Unicode que se va a traducir.

</dd> <dt>

* UnicodeStringByteCount * \[ en\]
</dt> <dd>

Especifica el número de bytes de la cadena de origen Unicode a los que apunta el parámetro *UnicodeStringSource* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**RtlUnicodeToUTF8N** devuelve uno de los siguientes valores de NTSTATUS:



| Código devuelto                                                                                                  | Descripción                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ESTADO \_ correcto**</dt> </dl>               | La cadena Unicode se convirtió a UTF-8.<br/>                                                           |
| <dl> <dt>**ESTADO \_ \_ no \_ asignado**</dt> </dl>     | Se encontró un carácter de entrada no válido y se ha reemplazado. Este estado se considera un estado correcto.<br/> |
| <dl> <dt>**ESTADO \_ parámetro no válido \_**</dt> </dl>    | Ambos punteros a *UTF8StringDestination* y *UTF8StringActualByteCount* eran **null**.<br/>              |
| <dl> <dt>**Parámetro de estado \_ no válido \_ \_ 4**</dt> </dl> | *UnicodeStringSource* era **null**.<br/>                                                              |
| <dl> <dt>**búfer de estado \_ \_ demasiado \_ pequeño**</dt> </dl>    | *UTF8StringDestination* se truncó.<br/>                                                               |



 

## <a name="remarks"></a>Observaciones

Aunque *UTF8StringActualByteCount* es opcional y puede ser **null**, los llamadores deben proporcionar almacenamiento para él, ya que la longitud recibida se puede usar para determinar si la conversión se realizó correctamente. Esta rutina no modifica la cadena de origen. Devuelve una cadena UTF-8 terminada en NULL si el *UnicodeStringSource* dado incluye un terminador null y si el *UTF8StringMaxByteCount* determinado no ha provocado el truncamiento.

Si el resultado se trunca y se encuentra un carácter de entrada no válido, la función devuelve un error de búfer de estado \_ \_ demasiado \_ pequeño.

Si *UTF8StringDestination* se establece en **null** , la función devolverá el número necesario de bytes para hospedar la cadena traducida sin ningún truncamiento en *UTF8StringActualByteCount*.

Los autores de llamadas de **RtlUnicodeToUTF8N** deben ejecutarse en el nivel de distribución de IRQL < \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>WDM. h</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RtlUTF8ToUnicodeN**](rtlutf8tounicoden.md)
</dt> </dl>

 

 




