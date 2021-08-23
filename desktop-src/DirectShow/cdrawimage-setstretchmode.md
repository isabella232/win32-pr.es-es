---
description: El método SetStretchMode calcula si se debe ajustar la imagen de vídeo.
ms.assetid: ffdcaf9c-e157-4557-9193-8430c1c451bf
title: Método CDrawImage.SetStretchMode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetStretchMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3886910bce57aca728f64ffbe9d660c1073d1281864a7721faa7e757c7c7d81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526495"
---
# <a name="cdrawimagesetstretchmode-method"></a>Método CDrawImage.SetStretchMode

El método calcula si se debe extender la imagen `SetStretchMode` de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
void SetStretchMode();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La **clase CDrawImage llama** automáticamente a este método cada vez que cambia el rectángulo de origen o de destino.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> </dl>

 

 




