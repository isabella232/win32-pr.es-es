---
description: Convierte una cadena de caracteres Unicode o un solo carácter en minúsculas.
ms.assetid: 09b7cf8e-6aed-40f4-9dfa-29be3559ae89
title: Función CharLowerWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharLowerWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: c9a02e89713dd82de63817c00d5402fabe991fed565ebe33fa40286ad30058d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710755"
---
# <a name="charlowerwrapw-function"></a>Función CharLowerWrapW

\[**CharLowerWrapW** está disponible para su uso en Windows XP. Es posible que no esté disponible en versiones posteriores. Debe usar [**CharLowerW en**](/windows/win32/api/winuser/nf-winuser-charlowera) su lugar.\]

Convierte una cadena de caracteres Unicode o un solo carácter en minúsculas. Si el operando es una cadena de caracteres, la función convierte los caracteres en su lugar.

> [!Note]  
> **CharLowerWrapW es** un contenedor para la **función CharLowerW.** Consulte la [**página CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) para obtener más notas de uso.

 

## <a name="syntax"></a>Sintaxis


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pch* \[ in, out\]
</dt> <dd>

Tipo: **LPWSTR**

Puntero a una cadena Unicode terminada en NULL o a un solo carácter. Si la palabra de orden superior de este parámetro es cero, la palabra de orden bajo debe contener solo un carácter que se va a convertir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LPWSTR**

Si *pch* es una cadena de caracteres, la función devuelve un puntero a la cadena convertida. Puesto que la cadena se convierte en su lugar, el valor devuelto es igual a *pch*.

Si *pch* es un carácter único, el valor devuelto es un valor de 32 bits cuya palabra de orden superior es cero y la palabra de orden bajo contiene el carácter convertido.

No hay ninguna indicación de éxito o error. El error es poco frecuente. No hay ninguna información de error extendida para esta función; no llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

El método preferido es usar [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) junto con la capa de Microsoft para Unicode (MSLU).

**Se debe llamar a CharLowerWrapW** directamente desde Shlwapi.dll, mediante el ordinal 38.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de \[ escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 
