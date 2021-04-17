---
description: El \_ método put Caption establece el título o el título de la ventana.
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: Método CBaseControlWindow.put_Caption (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aca8e5e7ad04acae9fab1cfe2d44f982266805e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660627"
---
# <a name="cbasecontrolwindowput_caption-method"></a>CBaseControlWindow. put ( \_ método de leyenda)

El `put_Caption` método establece el título o el título de la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Caption(
   BSTR strCaption
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strCaption* 
</dt> <dd>

Nuevo título de ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

La mayoría de las ventanas de nivel superior de un escritorio basado en Windows tienen un título (título) asociado. Esta propiedad se puede consultar y establecer a través de la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Cualquier conjunto de títulos solo será visible si la ventana tiene aplicado el \_ estilo de leyenda de WS. Si no es así, el título se puede establecer (y recuperar), aunque no será visible para el usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




