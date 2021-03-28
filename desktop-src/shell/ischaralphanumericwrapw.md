---
description: Determina si un carácter es un carácter alfabético o numérico.
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: IsCharAlphaNumericWrapW función)
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
ms.openlocfilehash: bf7f1b4db54cc5374214ff45b51579556dc22062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984722"
---
# <a name="ischaralphanumericwrapw-function"></a>IsCharAlphaNumericWrapW función)

\[**IsCharAlphaNumericWrapW** está disponible para su uso en Windows XP. No estará disponible en las versiones posteriores. Debe usar [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) en su lugar.\]

Determina si un carácter es un carácter alfabético o numérico. Esta determinación se basa en la semántica del idioma seleccionado por el usuario durante la instalación o a través del panel de control.

> [!Note]  
> **IsCharAlphaNumericWrapW** es un contenedor para la función **IsCharAlphaNumericW** . Vea la página [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) para obtener más notas de uso.

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CH* \[ de\]
</dt> <dd>

Tipo: **WCHAR**

Carácter Unicode que se va a probar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **bool**

Si el carácter es alfanumérico, el valor devuelto es distinto de cero.

Si el carácter no es alfanumérico, el valor devuelto es cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

**IsCharAlphaNumericWrapW** ofrece la posibilidad de usar cadenas Unicode en sistemas operativos anteriores a Windows XP. El método preferido es usar [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) junto con la capa de Microsoft para Unicode (MSLU).

Se debe llamar a **IsCharAlphaNumericWrapW** directamente desde Shlwapi.dll, mediante el ordinal 28.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
