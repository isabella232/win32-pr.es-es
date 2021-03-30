---
description: Envía una cadena Unicode al depurador para su presentación.
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: Función OutputDebugStringWrapW (Shlwapip. h)
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
ms.openlocfilehash: e8213aee48a90a816e2968aac115159472ed7b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997777"
---
# <a name="outputdebugstringwrapw-function"></a>OutputDebugStringWrapW función)

\[Esta función está disponible para su uso en Windows XP. Puede que no esté disponible en versiones posteriores. Use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) en su lugar.\]

Envía una cadena Unicode al depurador para su presentación.

> [!Note]  
> **OutputDebugStringWrapW** es un contenedor para la función **OutputDebugStringW** . Vea la página [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) para obtener más notas de uso.

 

## <a name="syntax"></a>Sintaxis


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpOutputString* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a la cadena Unicode terminada en null que se va a mostrar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

**OutputDebugStringWrapW** ofrece la posibilidad de usar cadenas Unicode en sistemas operativos anteriores a Windows XP. El método preferido es usar [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) junto con la capa de Microsoft para Unicode (MSLU).

Se debe llamar a **OutputDebugStringWrapW** directamente desde Shlwapi.dll, mediante el ordinal 115.

Si la aplicación no tiene ningún depurador, el depurador del sistema muestra la cadena. Si la aplicación no tiene ningún depurador y el depurador del sistema no está activo, **OutputDebugStringWrapW** no hace nada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shlwapip. h</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
