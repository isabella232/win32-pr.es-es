---
description: El método DoRealisePalette observa la paleta actual de la ventana.
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: Método CBaseWindow. DoRealisePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoRealisePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be1e02d355ab5991c9d0e95dbff30d4c8e0162ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660229"
---
# <a name="cbasewindowdorealisepalette-method"></a>CBaseWindow. DoRealisePalette, método

El `DoRealisePalette` método se obtiene de la paleta actual de la ventana.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT DoRealisePalette(
   BOOL bForceBackground
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bForceBackground* 
</dt> <dd>

Valor booleano que especifica si la paleta se ve obligada a ser una paleta de fondo. Para obtener más información, vea **SelectPalette** en el SDK de la plataforma.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Una llamada interna a **GdiFlush** devolvió un error.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto.<br/>                                            |



 

## <a name="remarks"></a>Observaciones

El método [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) llama a este método. Para establecer una nueva paleta, llame al método [**CBaseWindow:: SetPalette**](cbasewindow-setpalette.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




