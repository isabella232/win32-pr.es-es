---
title: DrawTextExPrivWrap función)
description: Dibuja texto con formato en el rectángulo especificado. Esta función contiene una llamada a DrawTextEx.
ms.assetid: 3212282c-1adb-4f7e-b4d7-7d833b26ac60
keywords:
- DrawTextExPrivWrap (función) controles de Windows
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
ms.openlocfilehash: eba496a121af3ba88ed24ab6c9c7834c90153ec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997113"
---
# <a name="drawtextexprivwrap-function"></a>DrawTextExPrivWrap función)

\[**DrawTextExPrivWrap** está disponible a través de Windows XP con Service Pack 2 (SP2). Podría modificarse o no estar disponible en versiones posteriores. Se recomienda usar [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) directamente en su lugar.\]

Dibuja texto con formato en el rectángulo especificado. Esta función contiene una llamada a [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).

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

*HDC* \[ de\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Identificador del contexto de dispositivo en el que se va a dibujar.

</dd> <dt>

*lpchText* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPTSTR**](/windows/desktop/WinProg/windows-data-types)**

Un puntero a un búfer que contiene el texto que se va a dibujar. Si el parámetro *cchText* es-1, la cadena debe terminar en NULL.

Si *dwDTFormat* incluye DT \_ MODIFYSTRING, la función podría agregar hasta cuatro caracteres adicionales a esta cadena. El búfer que contiene la cadena debe ser lo suficientemente grande como para dar cabida a estos caracteres adicionales.

</dd> <dt>

*cchText* \[ de\]
</dt> <dd>

Tipo: **int**

La longitud de la cadena a la que apunta *lpchText*. Si *cchText* es-1, se supone que el parámetro *lpchText* es un puntero a una cadena terminada en NULL y [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) calcula el recuento de caracteres automáticamente.

</dd> <dt>

*LPRC* \[ in, out\]
</dt> <dd>

Tipo: **LPRECT**

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene el rectángulo, en coordenadas lógicas, en la que se va a dar formato al texto.

</dd> <dt>

*dwDTFormat* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Opciones de formato. Consulte la documentación de [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) para obtener una lista completa de opciones.

</dd> <dt>

*lpDTParams* \[ de\]
</dt> <dd>

Tipo: **LPDRAWTEXTPARAMS**

Puntero a una estructura [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) que especifica opciones de formato adicionales. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Si la función se ejecuta correctamente, el valor devuelto es el alto de texto en unidades lógicas. Si se especifica **DT \_ vCenter** o **DT \_ Bottom** , el valor devuelto es el desplazamiento desde el miembro **superior** de *LPRC* hasta la parte inferior del texto dibujado.

Si la función no se realiza correctamente, el valor devuelto es cero.

Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

**DrawTextExPrivWrap** no se exporta por nombre o se declara en un archivo de encabezado público. Para usarlo, debe utilizar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y el ordinal de solicitud 416 de ComCtl32.dll para obtener un puntero de función.

Para obtener más comentarios, vea [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 6,0 o posterior)</dt> </dl> |



 

