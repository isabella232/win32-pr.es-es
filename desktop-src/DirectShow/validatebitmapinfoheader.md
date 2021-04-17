---
description: La función ValidateBitmapInfoHeader comprueba una estructura BITMAPINFOHEADER para detectar algunos errores comunes que pueden producir desbordamientos de búfer o desbordamientos de enteros.
ms.assetid: a797c286-ed77-437f-9ec1-1ef3a189bf62
title: Función ValidateBitmapInfoHeader (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateBitmapInfoHeader
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: c7242778a2ff16414b07f887dc1e71a1547a88e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681168"
---
# <a name="validatebitmapinfoheader-function"></a>ValidateBitmapInfoHeader función)

La `ValidateBitmapInfoHeader` función comprueba una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) para detectar algunos errores comunes que pueden producir desbordamientos de búfer o desbordamientos de enteros.

> [!Note]  
> Esta función no garantiza que la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) sea válida o que el código que usa la estructura sea seguro.

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL ValidateBitmapInfoHeader(
   const BITMAPINFOHEADER *pbmi,
         DWORD            cbSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbmi* 
</dt> <dd>

Puntero a la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que se va a validar.

</dd> <dt>

*cbSize* 
</dt> <dd>

Tamaño del bloque de memoria que contiene la estructura, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano. Si el valor es **false**, la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) no es válida.

## <a name="remarks"></a>Observaciones

Esta función protege contra los siguientes errores:

-   Desbordamiento aritmético en el tamaño de la estructura o un tamaño de estructura no válido.
-   Valor no válido para el miembro **biClrUsed** .
-   Desbordamiento aritmético en el tamaño de la imagen (**biSizeImage**).
-   Valores no válidos para el tamaño de la imagen (**biSizeImage**) para los formatos RGB.

La función no comprueba si la estructura describe un formato de vídeo válido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Checkbmi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de vídeo e imagen](video-and-image-functions.md)
</dt> </dl>

 

 




