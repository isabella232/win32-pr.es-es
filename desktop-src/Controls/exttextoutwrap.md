---
title: Función ExtTextOutWrap
description: Dibuja texto con la fuente, el color de fondo y el color de texto seleccionados actualmente. Opcionalmente, puede proporcionar dimensiones que se usarán para el recorte, la opacidad o ambos. Esta función encapsula una llamada a ExtTextOut.
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- ExtTextOutWrap function Windows Controls
topic_type:
- apiref
api_name:
- ExtTextOutWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 934a8d203cf232a339db46e97783e87c075e5bb949ec5d23e20a7b1874ea6ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047275"
---
# <a name="exttextoutwrap-function"></a>Función ExtTextOutWrap

\[**ExtTextOutWrap** está disponible a través Windows XP con Service Pack 2 (SP2). Podría modificarse o no estar disponible en versiones posteriores. Se recomienda usar [**ExtTextOut directamente**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) en su lugar.\]

Dibuja texto con la fuente, el color de fondo y el color de texto seleccionados actualmente. Opcionalmente, puede proporcionar dimensiones que se usarán para el recorte, la opacidad o ambos. Esta función encapsula una llamada a [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).

## <a name="syntax"></a>Sintaxis


```C++
BOOL ExtTextOutWrap(
  _In_       HDC     hdc,
  _In_       int     X,
  _In_       int     Y,
  _In_       UINT    uOptions,
  _In_ const RECT    *lprc,
  _In_       LPCTSTR lpString,
  _In_       UINT    cbCount,
  _In_ const INT     *lpDx
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hdc* \[ En\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Identificador del contexto del dispositivo.

</dd> <dt>

*X* \[ en\]
</dt> <dd>

Tipo: **int**

Coordenada x, en coordenadas lógicas, del punto de referencia utilizado para colocar la cadena.

</dd> <dt>

*Y* \[ en\]
</dt> <dd>

Tipo: **int**

Coordenada y, en coordenadas lógicas, del punto de referencia utilizado para colocar la cadena.

</dd> <dt>

*uOptions* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Valores que especifican cómo usar el rectángulo definido por la aplicación. Consulte [**ExtTextOut para**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) obtener una lista completa de opciones.

</dd> <dt>

*lprc* \[ En\]
</dt> <dd>

Tipo: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Puntero a una estructura [**RECT**](/previous-versions//dd162897(v=vs.85)) opcional que especifica las dimensiones, en coordenadas lógicas, de un rectángulo que se usa para el recorte, la opacidad o ambos.

</dd> <dt>

*lpString* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntero a un búfer que contiene el texto que se va a dibujar. No es necesario que la cadena termine en cero, ya *que cbCount* especifica la longitud de la cadena.

</dd> <dt>

*cbCount* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Longitud de la cadena, en bytes, a la que apunta *lpString.*

</dd> <dt>

*lpDx* \[ En\]
</dt> <dd>

Tipo: **const [**INT**](/windows/desktop/WinProg/windows-data-types) \***

Puntero a una matriz opcional de valores que indican la distancia entre los orígenes de las celdas de caracteres adyacentes. Por ejemplo, *las unidades* lógicas lpDx x separan los orígenes de la celda de caracteres x y la celda \[ de caracteres \] (x + 1).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

Devuelve un valor distinto de cero si la cadena se dibuja correctamente. Sin embargo, si se llama a la versión ANSI de [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) con ETO GLYPH INDEX, la función devuelve TRUE aunque la \_ función no haga \_ nada. 

Si la función no se realiza correctamente, el valor devuelto es cero.

Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

**ExtTextOutWrap** no se exporta por nombre ni se declara en un archivo de encabezado público. Para usarlo, debe usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y solicitar ordinal 417 a ComCtl32.dll obtener un puntero de función.

Para obtener comentarios adicionales, vea [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 6.0 o posterior)</dt> </dl> |



 

