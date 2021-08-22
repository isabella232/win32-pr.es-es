---
description: Recupera el estilo de color de fondo del estilo especificado.
ms.assetid: 1b0acac1-c36d-49b6-8154-f69bda008e9a
title: Función PColorStyleBackFromIMEStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleBackFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 86f7c5774767cf410f67fe79a741872c32874cbb92aafcefc2b08dbdc2904989
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386645"
---
# <a name="pcolorstylebackfromimestyle-function"></a>Función PColorStyleBackFromIMEStyle

Recupera el estilo de color de fondo del estilo especificado.

## <a name="syntax"></a>Sintaxis


```C++
const IMECOLORSTY* __cdecl PColorStyleBackFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pimestyle* \[ En\]
</dt> <dd>

Estructura **IMESTYLE devuelta** por [**la función PIMEStyleFromAttr.**](pimestylefromattr.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Puntero a una **estructura IMECOLORSTY que** representa el estilo de color de fondo.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

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

 

 
