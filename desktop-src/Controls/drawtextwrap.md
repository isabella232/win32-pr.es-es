---
title: DrawTextWrap función)
description: Dibuja texto con formato en el rectángulo especificado. Da formato al texto según el método especificado (expandir pestañas, justificar caracteres, líneas de división, etc.). Esta función contiene una llamada a DrawText.
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- DrawTextWrap (función) controles de Windows
topic_type:
- apiref
api_name:
- DrawTextWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfc5eb707b4016a592ad339223e0f32ab21d4a29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995983"
---
# <a name="drawtextwrap-function"></a>DrawTextWrap función)

\[**DrawTextWrap** está disponible a través de Windows XP con Service Pack 2 (SP2). Podría modificarse o no estar disponible en versiones posteriores. En su lugar, se recomienda usar [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) directamente.\]

Dibuja texto con formato en el rectángulo especificado. Da formato al texto según el método especificado (expandir pestañas, justificar caracteres, líneas de división, etc.). Esta función contiene una llamada a [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).

## <a name="syntax"></a>Sintaxis


```C++
int WINAPI DrawTextWrap(
  _In_    HDC              hdc,
  _Inout_ LPCTSTR          lpString,
  _In_    int              nCount,
  _Inout_ LPRECT           lpRect,
  _In_    UINT             uFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HDC* \[ de\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Identificador del contexto del dispositivo.

</dd> <dt>

*lpString* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Un puntero a un búfer que contiene el texto que se va a dibujar. Si el parámetro *nCount* es-1, la cadena debe terminar en NULL.

Si *uFormat* incluye DT \_ MODIFYSTRING, la función podría agregar hasta cuatro caracteres adicionales a esta cadena. El búfer que contiene la cadena debe ser lo suficientemente grande como para dar cabida a estos caracteres adicionales.

</dd> <dt>

*nCount* \[ de\]
</dt> <dd>

Tipo: **int**

La longitud de la cadena a la que apunta *lpString*. Si *nCount* es-1, se supone que el parámetro *lpString* es un puntero a una cadena terminada en NULL y [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) calcula el recuento de caracteres automáticamente.

</dd> <dt>

*lpRect* \[ in, out\]
</dt> <dd>

Tipo: **LPRECT**

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene el rectángulo, en coordenadas lógicas, en la que se va a dar formato al texto.

</dd> <dt>

*uFormat* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Opciones de formato. Consulte la documentación de [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) para obtener una lista completa de opciones.

</dd> <dt>

*lpDTParams* \[ de\]
</dt> <dd>

Tipo: **LPDRAWTEXTPARAMS**

Puntero a una estructura [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) que especifica opciones de formato adicionales. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Si la función se ejecuta correctamente, el valor devuelto es el alto de texto en unidades lógicas. Si se especifica **DT \_ vCenter** o **DT \_ Bottom** , el valor devuelto es el desplazamiento desde el miembro **superior** de *LPRC* hasta la parte inferior del texto dibujado si se produce un error en la función, el valor devuelto es cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

**DrawTextWrap** no se exporta por nombre o se declara en un encabezado público. Para usarlo, debe utilizar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y el ordinal de solicitud 415 de ComCtl32.dll para obtener un puntero de función.

Para obtener más comentarios, consulte [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 6,0 o posterior)</dt> </dl> |



 

