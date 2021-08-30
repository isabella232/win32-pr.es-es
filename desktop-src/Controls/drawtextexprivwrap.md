---
title: Función DrawTextExPrivWrap
description: Dibuja texto con formato en el rectángulo especificado. Esta función encapsula una llamada a DrawTextEx.
ms.assetid: 3212282c-1adb-4f7e-b4d7-7d833b26ac60
keywords:
- Controles de Windows de función DrawTextExPrivWrap
topic_type:
- apiref
api_name:
- DrawTextExPrivWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3381cd7aef94556cf80ddfc3ad828477e3a29c0fd57601ad27ff735d7b2f58f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916335"
---
# <a name="drawtextexprivwrap-function"></a>Función DrawTextExPrivWrap

\[**DrawTextExPrivWrap** está disponible a través Windows XP con Service Pack 2 (SP2). Podría modificarse o no estar disponible en versiones posteriores. Se recomienda usar [**DrawTextEx directamente**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) en su lugar.\]

Dibuja texto con formato en el rectángulo especificado. Esta función encapsula una llamada a [**DrawTextEx.**](/windows/desktop/api/winuser/nf-winuser-drawtextexa)

## <a name="syntax"></a>Sintaxis


```C++
int WINAPI DrawTextExPrivWrap(
  _In_    HDC              hdc,
  _Inout_ LPTSTR           lpchText,
  _In_    int              cchText,
  _Inout_ LPRECT           lprc,
  _In_    UINT             dwDTFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hdc* \[ En\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Identificador del contexto del dispositivo en el que se va a dibujar.

</dd> <dt>

*lpchText* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntero a un búfer que contiene el texto que se dibujará. Si el *parámetro cchText* es -1, la cadena debe terminar en null.

Si *dwDTFormat* incluye DT \_ MODIFYSTRING, la función podría agregar hasta cuatro caracteres adicionales a esta cadena. El búfer que contiene la cadena debe ser lo suficientemente grande como para dar cabida a estos caracteres adicionales.

</dd> <dt>

*cchText* \[ En\]
</dt> <dd>

Tipo: **int**

Longitud de la cadena a la que apunta *lpchText.* Si *cchText* es -1, se supone que el parámetro *lpchText* es un puntero a una cadena terminada en NULL y [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) calcula automáticamente el recuento de caracteres.

</dd> <dt>

*lprc* \[ in, out\]
</dt> <dd>

Tipo: **LPRECT**

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que contiene el rectángulo, en coordenadas lógicas, en el que se va a dar formato al texto.

</dd> <dt>

*dwDTFormat* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Opciones de formato. Consulte la documentación de [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) para obtener una lista completa de opciones.

</dd> <dt>

*lpDTParams* \[ En\]
</dt> <dd>

Tipo: **LPDRAWTEXTPARAMS**

Puntero a una [**estructura DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) que especifica opciones de formato adicionales. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Si la función se realiza correctamente, el valor devuelto es el alto del texto en unidades lógicas. Si **se especifica DT \_ VCENTER** o **DT \_ BOTTOM,** el  valor devuelto es el desplazamiento desde el miembro superior de *lprc* hasta la parte inferior del texto dibujado.

Si la función no se realiza correctamente, el valor devuelto es cero.

Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

**DrawTextExPrivWrap** no se exporta por nombre ni se declara en un archivo de encabezado público. Para usarlo, debe usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y solicitar el ordinal 416 de ComCtl32.dll para obtener un puntero de función.

Para obtener comentarios adicionales, vea [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 6.0 o posterior)</dt> </dl> |



 

