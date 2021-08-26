---
title: Función DrawTextWrap
description: Dibuja texto con formato en el rectángulo especificado. Da formato al texto según el método especificado (expandir pestañas, justificar caracteres, líneas de separación, entre otras). Esta función encapsula una llamada a DrawText.
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- DrawTextWrap , función Windows controles
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
ms.openlocfilehash: dcbd504955b6ae772ffb3db7bc4cc0223215d6d9ecf880fe7d7e3aa359c992ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878295"
---
# <a name="drawtextwrap-function"></a>Función DrawTextWrap

\[**DrawTextWrap** está disponible a través Windows XP con Service Pack 2 (SP2). Podría modificarse o no estar disponible en versiones posteriores. Se recomienda usar [**DrawText directamente**](/windows/desktop/api/winuser/nf-winuser-drawtext) en su lugar.\]

Dibuja texto con formato en el rectángulo especificado. Da formato al texto según el método especificado (expandir pestañas, justificar caracteres, líneas de separación, entre otras). Esta función encapsula una llamada a [**DrawText.**](/windows/desktop/api/winuser/nf-winuser-drawtext)

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

*hdc* \[ En\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Identificador del contexto del dispositivo.

</dd> <dt>

*lpString* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntero a un búfer que contiene el texto que se dibujará. Si el *parámetro nCount* es -1, la cadena debe terminar en null.

Si *uFormat* incluye DT \_ MODIFYSTRING, la función podría agregar hasta cuatro caracteres adicionales a esta cadena. El búfer que contiene la cadena debe ser lo suficientemente grande como para dar cabida a estos caracteres adicionales.

</dd> <dt>

*nCount* \[ En\]
</dt> <dd>

Tipo: **int**

Longitud de la cadena a la que apunta *lpString.* Si *nCount* es -1, se supone que el parámetro *lpString* es un puntero a una cadena terminada en NULL y [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) calcula automáticamente el recuento de caracteres.

</dd> <dt>

*lpRect* \[ in, out\]
</dt> <dd>

Tipo: **LPRECT**

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que contiene el rectángulo, en coordenadas lógicas, en el que se va a dar formato al texto.

</dd> <dt>

*uFormat* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Opciones de formato. Consulte la documentación de [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) para obtener una lista completa de opciones.

</dd> <dt>

*lpDTParams* \[ En\]
</dt> <dd>

Tipo: **LPDRAWTEXTPARAMS**

Puntero a una [**estructura DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) que especifica opciones de formato adicionales. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Si la función se realiza correctamente, el valor devuelto es el alto del texto en unidades lógicas. Si **se especifica DT \_ VCENTER** o **DT \_ BOTTOM,** el  valor devuelto es el desplazamiento desde el miembro superior de *lprc* hasta la parte inferior del texto dibujado Si se produce un error en la función, el valor devuelto es cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

**DrawTextWrap** no se exporta por nombre ni se declara en un encabezado público. Para usarlo, debe usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y solicitar ordinal 415 a ComCtl32.dll para obtener un puntero de función.

Para obtener comentarios adicionales, vea [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 6.0 o posterior)</dt> </dl> |



 

