---
description: Envía una cadena Unicode al depurador para su presentación.
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: Función OutputDebugStringWrapW (Shlwapip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OutputDebugStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: cce8754b01ddf156951964b7189b4a7189759c52cdcd08e08091ca62b2e950bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858794"
---
# <a name="outputdebugstringwrapw-function"></a>Función OutputDebugStringWrapW

\[Esta función está disponible para su uso en Windows XP. Es posible que no esté disponible en versiones posteriores. Use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) en su lugar.\]

Envía una cadena Unicode al depurador para su presentación.

> [!Note]  
> **OutputDebugStringWrapW es** un contenedor de la **función OutputDebugStringW.** Vea la [**página OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) para obtener más notas de uso.

 

## <a name="syntax"></a>Sintaxis


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpOutputString* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a la cadena Unicode terminada en NULL que se va a mostrar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

**OutputDebugStringWrapW proporciona** la capacidad de usar cadenas Unicode en sistemas operativos antes de Windows XP. El método preferido es usar [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) junto con la capa de Microsoft para Unicode (MSLU).

**Se debe llamar a OutputDebugStringWrapW** directamente Shlwapi.dll, mediante ordinal 115.

Si la aplicación no tiene ningún depurador, el depurador del sistema muestra la cadena. Si la aplicación no tiene ningún depurador y el depurador del sistema no está activo, **OutputDebugStringWrapW no** hace nada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shlwapip.h</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
