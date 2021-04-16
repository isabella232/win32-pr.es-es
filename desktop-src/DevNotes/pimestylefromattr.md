---
description: Recupera estilos para un atributo determinado.
ms.assetid: 206c69b9-981b-49ef-9f71-1c65e08637bb
title: PIMEStyleFromAttr función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PIMEStyleFromAttr
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 27673ebb74c1dca3e686542a541735cfc515bee9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649544"
---
# <a name="pimestylefromattr-function"></a>PIMEStyleFromAttr función)

Recupera estilos para un atributo determinado.

## <a name="syntax"></a>Sintaxis


```C++
const IMESTYLE* __cdecl PIMEStyleFromAttr(
  _In_ const  UINT attr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ATTR* \[ de\]
</dt> <dd>

Este parámetro puede ser uno de los valores siguientes.

<dl> <dt>

<span id="IMESATTR_FIXEDCONVERTED"></span><span id="imesattr_fixedconverted"></span>**IMESATTR \_ FIXEDCONVERTED** (5)
</dt> <dt>

<span id="IMESATTR_INPUT"></span><span id="imesattr_input"></span>**IMESATTR \_ ENTRADA** (0)
</dt> <dt>

<span id="IMESATTR_INPUT_ERROR"></span><span id="imesattr_input_error"></span>**IMESATTR \_ \_Error de entrada** (4)
</dt> <dt>

<span id="IMESATTR_MAX"></span><span id="imesattr_max"></span>**IMESATTR \_ MÁX** . (5)
</dt> <dt>

<span id="IMESATTR_MIN"></span><span id="imesattr_min"></span>**IMESATTR \_ MÍN** . (0)
</dt> <dt>

<span id="IMESATTR_TARGET_CONVERTED"></span><span id="imesattr_target_converted"></span>**IMESATTR \_ DESTINO \_ convertido** (1)
</dt> <dt>

<span id="IMESATTR_TARGET_NOTCONVERTED"></span><span id="imesattr_target_notconverted"></span>**IMESATTR \_ DESTINO \_ NOTCONVERTED** (4)
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a una estructura **IMESTYLE** que representa la configuración de color y no color.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

La estructura **IMESTYLE** se define de la siguiente manera:

``` syntax
typedef struct {
    union {
        GRFSTY  grfsty;
        struct {
            UINT    fBold:1;
            UINT    fItalic:1;
            UINT    fUl:1;
            UINT    idUl:(sizeof(UINT) * 8 - 3);
        };
    };

    union {
        IMECOLORSTY colorstyText;
        struct {
            UINT    colorIdText;
            union {
                COLORREF    rgbText;
                UINT        colorWinText;
                UINT        colorSpecText;
                UINT        colorFundText;
            };
        };
    };

    union {
        IMECOLORSTY colorstyBack;
        struct {
            UINT    colorIdBack;
            union {
                COLORREF    rgbBack;
                UINT        colorWinBack;
                UINT        colorSpecBack;
                UINT        colorFundBack;
            };
        };
    };

    union {
        IMECOLORSTY colorstyUl;
        struct {
            UINT    colorIdUl;
            union {
                COLORREF    rgbUl;
                UINT        colorWinUl;
                UINT        colorSpecUl;
                UINT        colorFundUl;
            };
        };
    };
} IMESTYLE;
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



 

 
