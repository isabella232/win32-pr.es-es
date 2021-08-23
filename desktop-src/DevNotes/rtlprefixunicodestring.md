---
description: Compara dos cadenas Unicode para determinar si una cadena es un prefijo de la otra.
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: Función RtlPrefixUnicodeString (Ntddk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlPrefixUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 28997f3bc85dedb9a18139cec13b9a76a8dd975e4ff57f1380053178bfaab328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076009"
---
# <a name="rtlprefixunicodestring-function"></a>Función RtlPrefixUnicodeString

Compara dos cadenas Unicode para determinar si una cadena es un prefijo de la otra.

## <a name="syntax"></a>Sintaxis


```C++
BOOLEAN RtlPrefixUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*String1* \[ En\]
</dt> <dd>

Puntero a la primera cadena, que podría ser un prefijo de la cadena Unicode en búfer en *String2*.

</dd> <dt>

*String2* \[ En\]
</dt> <dd>

Puntero a la segunda cadena.

</dd> <dt>

*CaseInSensitive* \[ En\]
</dt> <dd>

Si **es TRUE,** se debe omitir el uso de mayúsculas y minúsculas al realizar la comparación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**TRUE** si *String1* es un prefijo de *String2.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                    |
| Plataforma de destino<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Header<br/>                   | <dl> <dt>Ntddk.h (incluir Ntddk.h)</dt> </dl>                                    |
| Biblioteca<br/>                  | <dl> <dt>Ntdll.lib</dt> </dl>                                                    |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RtlCompareUnicodeString**](rtlcompareunicodestring.md)
</dt> </dl>

 

 




