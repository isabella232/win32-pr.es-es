---
title: GetTextExtentPoint32Wrap función)
description: Calcula el ancho y el alto de la cadena de texto especificada. Esta función contiene una llamada a GetTextExtentPoint.
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- GetTextExtentPoint32Wrap (función) controles de Windows
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
ms.openlocfilehash: b6a0db92ad019950cf8be0a72260da75acc06779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801232"
---
# <a name="gettextextentpoint32wrap-function"></a>GetTextExtentPoint32Wrap función)

\[**GetTextExtentPoint32Wrap** está disponible a través de Windows XP con Service Pack 2 (SP2). Podría modificarse o no estar disponible en versiones posteriores. Se recomienda usar [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) directamente en su lugar.\]

Calcula el ancho y el alto de la cadena de texto especificada. Esta función contiene una llamada a [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

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

*HDC* \[ de\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Identificador del contexto del dispositivo.

</dd> <dt>

*lpString* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntero a un búfer que contiene el texto que se va a dibujar. No es necesario que la cadena termine en cero, ya que *cbCount* especifica la longitud de la cadena.

</dd> <dt>

*cbCount* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

La longitud, en bytes, de la cadena a la que apunta *lpString*.

</dd> <dt>

*lpSize* \[ enuncia\]
</dt> <dd>

Tipo: **LPSIZE**

Cuando este método devuelve un valor, contiene un puntero a una estructura de [**tamaño**](/previous-versions//dd145106(v=vs.85)) que contiene las dimensiones de la cadena, en unidades lógicas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

Devuelve un valor distinto de cero si es correcto; de lo contrario, es 0.

Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

**GetTextExtentPoint32Wrap** no se exporta por nombre o se declara en un archivo de encabezado público. Para usarlo, debe utilizar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y el ordinal de solicitud 420 de ComCtl32.dll para obtener un puntero de función.

Para obtener más comentarios, vea [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                            |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 5,81 o posterior)</dt> </dl> |



 

