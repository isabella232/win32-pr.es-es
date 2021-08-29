---
description: La función ValidateBitmapInfoHeader comprueba una estructura BITMAPINFOHEADER en busca de determinados errores comunes que pueden provocar saturaciones de búfer o desbordamientos de enteros.
ms.assetid: a797c286-ed77-437f-9ec1-1ef3a189bf62
title: Función ValidateBitmapInfoHeader (Checkbmi.h)
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
ms.openlocfilehash: a23bbb322da1effdb2246ee797b353d1af36e3b87cbb37bd89039d1aced994e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755835"
---
# <a name="validatebitmapinfoheader-function"></a>Función ValidateBitmapInfoHeader

La función comprueba una estructura BITMAPINFOHEADER en busca de determinados errores comunes que pueden provocar saturaciones de búfer o `ValidateBitmapInfoHeader` desbordamientos de [](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) enteros.

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

Puntero a la [**estructura BITMAPINFOHEADER que**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) se validará.

</dd> <dt>

*cbSize* 
</dt> <dd>

Tamaño del bloque de memoria que contiene la estructura, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano. Si el valor es **FALSE**, la [**estructura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) no es válida.

## <a name="remarks"></a>Comentarios

Esta función protege contra los errores siguientes:

-   Desbordamiento aritmético en el tamaño de la estructura o un tamaño de estructura no válido.
-   Valor no válido para el **miembro biClrUsed.**
-   Desbordamiento aritmético en el tamaño de la imagen (**biSizeImage**).
-   Valores no válidos para el tamaño de imagen (**biSizeImage**) para formatos RGB.

La función no comprueba si la estructura describe un formato de vídeo válido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Checkbmi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de vídeo e imagen](video-and-image-functions.md)
</dt> </dl>

 

 




