---
description: El \_ método get Caption recupera el título de la ventana actual.
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: Método CBaseControlWindow.get_Caption (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8d743c746f833007d91afd4346f7f48c6218dde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660407"
---
# <a name="cbasecontrolwindowget_caption-method"></a>CBaseControlWindow. Get \_ Caption (método)

El `get_Caption` método recupera el título de la ventana actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Caption(
   BSTR *pstrCaption
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pstrCaption* 
</dt> <dd>

Puntero al título de la ventana actual.

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

 

 




