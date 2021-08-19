---
title: Función GetTextExtentPoint32Wrap
description: Calcula el ancho y alto de la cadena de texto especificada. Esta función encapsula una llamada a GetTextExtentPoint.
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- GetTextExtentPoint32Wrap , función Windows controles
topic_type:
- apiref
api_name:
- GetTextExtentPoint32Wrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0217d1708764ec33dd76ea35ff330f0d411697b5e9be3a6bd148377002a1f127
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047215"
---
# <a name="gettextextentpoint32wrap-function"></a>Función GetTextExtentPoint32Wrap

\[**GetTextExtentPoint32Wrap** está disponible a través Windows XP con Service Pack 2 (SP2). Podría modificarse o no estar disponible en versiones posteriores. Se recomienda usar [**GetTextExtentPoint directamente en**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) su lugar.\]

Calcula el ancho y alto de la cadena de texto especificada. Esta función encapsula una llamada a [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

## <a name="syntax"></a>Sintaxis


```C++
BOOL GetTextExtentPoint32Wrap(
  _In_  HDC     hdc,
  _In_  LPCTSTR lpString,
  _In_  UINT    cbCount,
  _Out_ LPSIZE  lpSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hdc* \[ En\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Identificador del contexto del dispositivo.

</dd> <dt>

*lpString* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntero a un búfer que contiene el texto que se va a dibujar. No es necesario que la cadena termine en cero, ya *que cbCount* especifica la longitud de la cadena.

</dd> <dt>

*cbCount* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Longitud, en bytes, de la cadena a la que apunta *lpString.*

</dd> <dt>

*lpSize* \[ out\]
</dt> <dd>

Tipo: **LPSIZE**

El resultado que devuelve este método contiene un puntero a una [**estructura SIZE**](/previous-versions//dd145106(v=vs.85)) que contiene las dimensiones de la cadena, en unidades lógicas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

Devuelve un valor distinto de cero si se realiza correctamente; de lo contrario, 0.

Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

**GetTextExtentPoint32Wrap** no se exporta por nombre ni se declara en un archivo de encabezado público. Para usarlo, debe usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y solicitar ordinal 420 a ComCtl32.dll obtener un puntero de función.

Para obtener comentarios adicionales, [**vea GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                            |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 5.81 o posterior)</dt> </dl> |



 

