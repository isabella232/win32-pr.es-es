---
description: Especifica si el color especificado es un color de texto especial.
ms.assetid: 527806f5-5046-48b0-a8db-86a5b8c0db08
title: Función FSpecialTextIMEColorStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialTextIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 6fa964ba5d1020a5d9ba35b7359d81d965778b8a1e1f546a0a6cac19d2611ebd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017733"
---
# <a name="fspecialtextimecolorstyle-function"></a>Función FSpecialTextIMEColorStyle

Especifica si el color especificado es un color de texto especial.

## <a name="syntax"></a>Sintaxis


```C++
BOOL __cdecl FSpecialTextIMEColorStyle(
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

Devuelve **TRUE** cuando el color es un color de texto especial.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md)
</dt> <dt>

[**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
