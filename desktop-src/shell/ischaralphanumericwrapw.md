---
description: Determina si un carácter es alfabético o numérico.
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: Función IsCharAlphaNumericWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCharAlphaNumericWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bf0a9752162c1593928e1bed270859ec4166230fe1f7e2d46d979c5c989ca237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118453000"
---
# <a name="ischaralphanumericwrapw-function"></a>Función IsCharAlphaNumericWrapW

\[**IsCharAlphaNumericWrapW** está disponible para su uso en Windows XP. No estará disponible en versiones posteriores. Debe usar [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) en su lugar.\]

Determina si un carácter es alfabético o numérico. Esta determinación se basa en la semántica del idioma seleccionado por el usuario durante la instalación o a través Panel de control.

> [!Note]  
> **IsCharAlphaNumericWrapW es** un contenedor para la **función IsCharAlphaNumericW.** Consulte la [**página IsCharAlphaNumeric para**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) obtener más notas de uso.

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ch* \[ En\]
</dt> <dd>

Tipo: **WCHAR**

Carácter Unicode que se va a probar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **BOOL**

Si el carácter es alfanumérico, el valor devuelto es distinto de cero.

Si el carácter no es alfanumérico, el valor devuelto es cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

**IsCharAlphaNumericWrapW** proporciona la capacidad de usar cadenas Unicode en sistemas operativos anteriores a Windows XP. El método preferido es usar [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) junto con la capa de Microsoft para Unicode (MSLU).

**Se debe llamar a IsCharAlphaNumericWrapW** directamente desde Shlwapi.dll, mediante el ordinal 28.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de \[ escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
