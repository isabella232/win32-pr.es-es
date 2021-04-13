---
description: Compara dos cadenas Unicode para determinar si una cadena es un prefijo del otro.
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: Función RtlPrefixUnicodeString (Ntddk. h)
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
ms.openlocfilehash: 47382daab1bac5e71098f79a601d89255f1cf0e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496103"
---
# <a name="rtlprefixunicodestring-function"></a>RtlPrefixUnicodeString función)

Compara dos cadenas Unicode para determinar si una cadena es un prefijo del otro.

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

*Cadena1* \[ de\]
</dt> <dd>

Puntero a la primera cadena, que puede ser un prefijo de la cadena Unicode almacenada en el búfer en *cadena2*.

</dd> <dt>

*Cadena2* \[ de\]
</dt> <dd>

Puntero a la segunda cadena.

</dd> <dt>

*CaseInSensitive* \[ de\]
</dt> <dd>

Si **es true**, se debe pasar por alto la distinción de mayúsculas y minúsculas al realizar la comparación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**True** si *string1* es un prefijo de *cadena2*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                    |
| Plataforma de destino<br/>          | <dl> <dt>[Mundo](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Encabezado<br/>                   | <dl> <dt>Ntddk. h (incluye Ntddk. h)</dt> </dl>                                    |
| Biblioteca<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RtlCompareUnicodeString**](rtlcompareunicodestring.md)
</dt> </dl>

 

 




