---
description: Método de constructor.
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: Constructor CImagePalette. CImagePalette (Winutil. h)
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
ms.openlocfilehash: 38b5766617e1d17fa3917048c2fb845b5194cc42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681007"
---
# <a name="cimagepalettecimagepalette-constructor"></a>Constructor CImagePalette. CImagePalette

Método de constructor.

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

Puntero a un objeto **CBaseWindow** , que administra la ventana donde se realiza la paleta. Este parámetro puede ser **NULL**.

</dd> <dt>

*pDrawImage* 
</dt> <dd>

Puntero a un objeto **CDrawImage** que dibuja la imagen de vídeo. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




