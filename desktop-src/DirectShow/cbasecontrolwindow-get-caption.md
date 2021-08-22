---
description: El método get \_ Caption recupera el título de la ventana actual.
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: CBaseControlWindow.get_Caption método (Ctlutil.h)
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
ms.openlocfilehash: 0f05501adbd486eaa60e939aacfdd5896c0fbcae059673029f04fcca8aeb742a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640895"
---
# <a name="cbasecontrolwindowget_caption-method"></a>CBaseControlWindow.get \_ Caption (método)

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

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

La mayoría de las ventanas de nivel superior de un Windows basado en el escritorio tienen un título (título) asociado a ellas. Esta propiedad se puede consultar y establecer a través de la [**interfaz IVideoWindow.**](/windows/desktop/api/Control/nn-control-ivideowindow) Cualquier conjunto de títulos solo será visible si la ventana tiene aplicado el estilo WS \_ CAPTION. Si no es así, el título todavía se puede establecer (y recuperar), aunque no será visible para el usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




