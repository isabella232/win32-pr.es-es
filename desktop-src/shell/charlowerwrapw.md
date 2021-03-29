---
description: Convierte una cadena de caracteres Unicode o un carácter individual en minúsculas.
ms.assetid: 09b7cf8e-6aed-40f4-9dfa-29be3559ae89
title: CharLowerWrapW función)
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
ms.openlocfilehash: 3911e0366d30f3eb9420391f9d06867ded73530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540558"
---
# <a name="charlowerwrapw-function"></a>CharLowerWrapW función)

\[**CharLowerWrapW** está disponible para su uso en Windows XP. Puede que no esté disponible en versiones posteriores. Debe usar [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) en su lugar.\]

Convierte una cadena de caracteres Unicode o un carácter individual en minúsculas. Si el operando es una cadena de caracteres, la función convierte los caracteres en su lugar.

> [!Note]  
> **CharLowerWrapW** es un contenedor para la función **CharLowerW** . Vea la página [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) para obtener más notas de uso.

 

## <a name="syntax"></a>Sintaxis


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PCH* \[ in, out\]
</dt> <dd>

Tipo: **LPWStr**

Puntero a una cadena Unicode terminada en null o a un solo carácter. Si la palabra de orden superior de este parámetro es cero, la palabra de orden inferior debe contener solo un carácter que se va a convertir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LPWStr**

Si *PCH* es una cadena de caracteres, la función devuelve un puntero a la cadena convertida. Dado que la cadena se convierte en contexto, el valor devuelto es igual a *PCH*.

Si *PCH* es un carácter único, el valor devuelto es un valor de 32 bits cuya palabra de orden superior es cero y la palabra de orden inferior contiene el carácter convertido.

No hay ninguna indicación de si se ha realizado correctamente o no. El error es poco frecuente. No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Observaciones

El método preferido es usar [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) junto con la capa de Microsoft para Unicode (MSLU).

Se debe llamar a **CharLowerWrapW** directamente desde Shlwapi.dll, mediante el ordinal 38.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 
