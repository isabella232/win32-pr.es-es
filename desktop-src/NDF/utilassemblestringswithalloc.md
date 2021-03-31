---
title: Función UtilAssembleStringsWithAlloc (Ndattributils. h)
description: Asigna una cadena y le da formato mediante las cadenas proporcionadas por la tabla de cadenas. Esta función usa StringCchPrintf para crear la cadena con formato.
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- UtilAssembleStringsWithAlloc función NDF
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
ms.openlocfilehash: dae121b1d5f2d968f696190c64828be91adc71da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804063"
---
# <a name="utilassemblestringswithalloc-function"></a>UtilAssembleStringsWithAlloc función)

La función **UtilAssembleStringsWithAlloc** asigna una cadena y le da formato mediante las cadenas proporcionadas por la tabla de cadenas. Esta función usa [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) para crear la cadena con formato.

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

*Búfer* \[ de enuncia\]
</dt> <dd>

Tipo: **LPWStr \** _

Ubicación donde se colocará la cadena recién asignada. Cuando la cadena ya no es necesaria, se debe liberar con [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*BufferMax* \[ de\]
</dt> <dd>

Tipo: **uint**

Número máximo de caracteres permitidos en la cadena asignada por el *búfer*. Si la cadena con formato resultante es mayor que el número de caracteres especificado, se trunca y termina en NULL.

> [!Note]  
> Este parámetro no se puede establecer en cero.

 

</dd> <dt>

*Formatodeentrada* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Recurso de cadena fuera de la tabla de cadenas que representa un parámetro de formato pasado a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa). Se construye mediante [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).

El formato de la cadena de recursos debe especificar un parámetro de formato que toma una cadena de caracteres anchos, o un parámetro de formato que toma una longitud sin signo y una cadena de caracteres anchos.

</dd> <dt>

*InputString* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Recurso de cadena fuera de la tabla de cadenas que representa un argumento pasado a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) en lugar de la cadena ancha en el parámetro Format. Se construye mediante [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).

</dd> <dt>

*AdditionalArgument* \[ de\]
</dt> <dd>

Tipo: **booleano**

True si *AdditionalValue* debe pasarse como el primer argumento de formato a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); de lo contrario, es false (y solo se pasará la cadena de recursos identificada por *InputString* ).

</dd> <dt>

*AdditionalValue* \[ de\]
</dt> <dd>

Tipo: **ULong**

Valor que se va a pasar como primer argumento de formato a [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) si *AdditionalArgument* es true.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Los valores devueltos posibles incluyen, entre otros, lo siguiente.



| Código devuelto                                                                                  | Descripción                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | La operación se realizó correctamente.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | No se ha proporcionado correctamente uno o más parámetros.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



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

 

