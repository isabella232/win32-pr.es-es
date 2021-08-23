---
description: Recupera el estilo de color de texto del estilo especificado.
ms.assetid: 242c37af-5b39-4b18-9c8f-4e692f41c497
title: Función PColorStyleTextFromIMEStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleTextFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 58fb2c2830f016080ac27c48b188bbd1948406a6cb7516b3279c411c87d9c155
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955724"
---
# <a name="pcolorstyletextfromimestyle-function"></a>Función PColorStyleTextFromIMEStyle

Recupera el estilo de color de texto del estilo especificado.

## <a name="syntax"></a>Sintaxis


```C++
const IMECOLORSTY* __cdecl PColorStyleTextFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pimestyle* \[ En\]
</dt> <dd>

Estructura **IMESTYLE** devuelta desde [**la función PIMEStyleFromAttr.**](pimestylefromattr.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Puntero a una **estructura IMECOLORSTY** que representa el estilo de color del texto.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

La **estructura IMECOLORSTY** se define de la siguiente manera:

``` syntax
typedef struct {
    UINT colorId;
    union {
        COLORREF    rgb;
        UINT        colorWin;
        UINT        colorSpec;
        UINT        colorFund;
    };
} IMECOLORSTY;
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PIMEStyleFromAttr**](pimestylefromattr.md)
</dt> </dl>

 

 
