---
title: Función UtilAssembleStringsWithAlloc (Ndattributils.h)
description: Asigna una cadena y le da formato mediante cadenas proporcionadas por la tabla de cadenas. Esta función usa StringCchPrintf para crear la cadena con formato.
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- Función NDF UtilAssembleStringsWithAlloc
topic_type:
- apiref
api_name:
- UtilAssembleStringsWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38473f45e2bd4c53b964bb38ec285cdf3eea091a96d72684c1d801b949f4d0a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801735"
---
# <a name="utilassemblestringswithalloc-function"></a>Función UtilAssembleStringsWithAlloc

La **función UtilAssembleStringsWithAlloc** asigna una cadena y le da formato mediante cadenas proporcionadas por la tabla de cadenas. Esta función usa [**StringCchPrintf para**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) crear la cadena con formato.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UtilAssembleStringsWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR InputFormat,
  _In_  LPCWSTR InputString,
  _In_  BOOLEAN AdditionalArgument,
  _In_  ULONG   AdditionalValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Búfer* \[ out\]
</dt> <dd>

Tipo: **LPWSTR \***

Ubicación donde se colocará la cadena recién asignada. Cuando la cadena ya no es necesaria, debe publicarse [**con CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*BufferMax* \[ En\]
</dt> <dd>

Tipo: **UINT**

Número máximo de caracteres permitido en la cadena asignada por *buffer*. Si la cadena con formato resultante es mayor que el número de caracteres especificado, se trunca y finaliza en NULL.

> [!Note]  
> Este parámetro no se puede establecer en cero.

 

</dd> <dt>

*InputFormat* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Recurso de cadena de la tabla de cadenas que representa un parámetro de formato pasado a [**StringCchPrintf.**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) Se construye mediante [**MAKEINTRESOURCE.**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)

El formato de cadena de recursos debe especificar un parámetro de formato que tome una cadena ancha o un parámetro de formato que tome una cadena larga y una cadena ancha sin signo.

</dd> <dt>

*InputString* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Recurso de cadena fuera de la tabla de cadenas que representa un argumento pasado a [**StringCchPrintf en**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) lugar de la cadena ancha en el parámetro format. Se construye mediante [**MAKEINTRESOURCE.**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)

</dd> <dt>

*AdditionalArgument* \[ En\]
</dt> <dd>

Tipo: **BOOLEAN**

True si *AdditionalValue* debe pasarse como primer argumento de formato a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); de lo contrario, false (y solo se pasará la cadena de recurso identificada por *InputString).*

</dd> <dt>

*AdditionalValue* \[ En\]
</dt> <dd>

Tipo: **ULONG**

Valor que se va a pasar como primer argumento de formato a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) si *AdditionalArgument* es true.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Los valores devueltos posibles incluyen, entre otros, lo siguiente.



| Código devuelto                                                                                  | Descripción                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | La operación se realizó correctamente.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | No se han proporcionado correctamente uno o varios parámetros.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**UtilStringCopyWithAlloc**](utilstringcopywithalloc.md)
</dt> <dt>

[**UtilLoadStringWithAlloc**](utilloadstringwithalloc.md)
</dt> <dt>

[**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)
</dt> <dt>

[**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

