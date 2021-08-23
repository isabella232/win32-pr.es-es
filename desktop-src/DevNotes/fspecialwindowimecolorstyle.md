---
description: Especifica si el color especificado es un color de ventana especial.
ms.assetid: 41f7d4fb-9718-42a8-89df-c29bd8c0665b
title: Función FSpecialWindowIMEColorStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialWindowIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: c42a8f4cf61b2b61d228dc243d06e902d825040570f4baa6502f2feba0322ae2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691345"
---
# <a name="fspecialwindowimecolorstyle-function"></a>Función FSpecialWindowIMEColorStyle

Especifica si el color especificado es un color de ventana especial.

## <a name="syntax"></a>Sintaxis


```C++
BOOL __cdecl FSpecialWindowIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcolorstyle* \[ En\]
</dt> <dd>

Estructura **IMECOLORSTY** devuelta desde una [**función PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) o [**PColorStyleTextFromIMEStyle.**](pcolorstyletextfromimestyle.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** cuando el color es un color de ventana especial (uno de color especial).

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md)
</dt> <dt>

[**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
