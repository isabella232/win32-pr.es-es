---
description: Compara dos cadenas Unicode.
ms.assetid: D2703180-946C-4762-AFBA-1E882B01B944
title: Función RtlCompareUnicodeString (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlCompareUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9de12f218c37916c7e30393c0701efcf1889973f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907194"
---
# <a name="rtlcompareunicodestring-function"></a>RtlCompareUnicodeString función)

Compara dos cadenas Unicode.

## <a name="syntax"></a>Sintaxis


```C++
LONG RtlCompareUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cadena1* \[ de\]
</dt> <dd>

Puntero a la primera cadena.

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

Valor con signo que proporciona los resultados de la comparación:



| Código devuelto                                                                               | Descripción                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**Nulo**</dt> </dl>       | *String1* es igual a *cadena2*.<br/>          |
| <dl> <dt>**< cero**</dt> </dl>  | *String1* es menor que *cadena2*.<br/>    |
| <dl> <dt>**> cero**</dt> </dl> | *String1* es mayor que *cadena2*.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                    |
| Plataforma de destino<br/>          | <dl> <dt>[Mundo](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Encabezado<br/>                   | <dl> <dt>WDM. h (incluir WDM. h, Ntddk. h o Ntifs. h)</dt> </dl>                   |
| Biblioteca<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RtlCompareString**](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlcomparestring)
</dt> <dt>

[**RtlEqualString**](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlequalstring)
</dt> </dl>

 

 
