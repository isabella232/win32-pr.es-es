---
description: 'Constructor CImagePalette.CImagePalette: método constructor.'
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: Constructor CImagePalette.CImagePalette (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CImagePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5021b165a8fa47bedc7961657d7cdbfa07af301d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063340"
---
# <a name="cimagepalettecimagepalette-constructor"></a>Constructor CImagePalette.CImagePalette

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBaseFilter* 
</dt> <dd>

Puntero al filtro propietario.

</dd> <dt>

*pBaseWindow* 
</dt> <dd>

Puntero a un **objeto CBaseWindow,** que administra la ventana donde se realiza la paleta. Este parámetro puede ser **NULL**.

</dd> <dt>

*pDrawImage* 
</dt> <dd>

Puntero a un **objeto CDrawImage,** que dibuja la imagen de vídeo. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CImagePalette (clase)**](cimagepalette.md)
</dt> </dl>

 

 




