---
title: ExtTextOutWrap función)
description: Dibuja texto con la fuente, el color de fondo y el color de texto seleccionados actualmente. Opcionalmente, puede proporcionar dimensiones que se usarán para el recorte, la opacidad o ambos. Esta función contiene una llamada a ExtTextOut.
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- ExtTextOutWrap (función) controles de Windows
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
ms.openlocfilehash: a173fedb7d8534dbd926a8a147e833435a7710b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149942"
---
# <a name="exttextoutwrap-function"></a>ExtTextOutWrap función)

\[**ExtTextOutWrap** está disponible a través de Windows XP con Service Pack 2 (SP2). Podría modificarse o no estar disponible en versiones posteriores. Se recomienda usar [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) directamente en su lugar.\]

Dibuja texto con la fuente, el color de fondo y el color de texto seleccionados actualmente. Opcionalmente, puede proporcionar dimensiones que se usarán para el recorte, la opacidad o ambos. Esta función contiene una llamada a [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).

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

*HDC* \[ de\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Identificador del contexto del dispositivo.

</dd> <dt>

*X* \[ en\]
</dt> <dd>

Tipo: **int**

La coordenada x, en coordenadas lógicas, del punto de referencia utilizado para colocar la cadena.

</dd> <dt>

*Y* \[ en\]
</dt> <dd>

Tipo: **int**

La coordenada y, en coordenadas lógicas, del punto de referencia utilizado para colocar la cadena.

</dd> <dt>

*uOptions* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Valores que especifican cómo usar el rectángulo definido por la aplicación. Consulte [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) para obtener una lista completa de opciones.

</dd> <dt>

*LPRC* \[ de\]
</dt> <dd>

Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \** _

Puntero a una estructura [_ *Rect* *](/previous-versions//dd162897(v=vs.85)) opcional que especifica las dimensiones, en coordenadas lógicas, de un rectángulo que se usa para el recorte, la opacidad o ambos.

</dd> <dt>

*lpString* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntero a un búfer que contiene el texto que se va a dibujar. No es necesario que la cadena termine en cero, ya que *cbCount* especifica la longitud de la cadena.

</dd> <dt>

*cbCount* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Longitud de la cadena, en bytes, a la que apunta *lpString*.

</dd> <dt>

*lpDx* \[ de\]
</dt> <dd>

Tipo: **const [**int**](/windows/desktop/WinProg/windows-data-types) \** _

Puntero a una matriz opcional de valores que indican la distancia entre los orígenes de las celdas de caracteres adyacentes. Por ejemplo, _lpDx \[ unidades lógicas * x separan \] los orígenes de la celda de carácter x y la celda de carácter (x + 1).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

Devuelve un valor distinto de cero si la cadena se dibuja correctamente. Sin embargo, si se llama a la versión ANSI de [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) con el índice del GLIFO de ETO \_ \_ , la función devuelve **true** aunque la función no hace nada.

Si la función no se realiza correctamente, el valor devuelto es cero.

Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

**ExtTextOutWrap** no se exporta por nombre o se declara en un archivo de encabezado público. Para usarlo, debe utilizar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y el ordinal de solicitud 417 de ComCtl32.dll para obtener un puntero de función.

Para obtener más comentarios, vea [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 6,0 o posterior)</dt> </dl> |



 

