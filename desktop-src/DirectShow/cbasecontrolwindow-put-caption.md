---
description: El método put \_ Caption establece el título o el título de la ventana.
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: CBaseControlWindow.put_Caption método (Ctlutil.h)
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
ms.openlocfilehash: c7f0c9da5ad2c3ae409e14a1ca9918a0c1aa7ef04615ab4d647ce1a3467c7311
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983705"
---
# <a name="cbasecontrolwindowput_caption-method"></a>CBaseControlWindow.put \_ Caption (método)

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

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

La mayoría de las ventanas de nivel superior de Windows escritorio basado en aplicaciones tienen un título (título) asociado a ellas. Esta propiedad se puede consultar y establecer a través de la [**interfaz IVideoWindow.**](/windows/desktop/api/Control/nn-control-ivideowindow) Cualquier conjunto de títulos solo será visible si la ventana tiene aplicado el estilo WS \_ CAPTION. Si no es así, el título todavía se puede establecer (y recuperar), aunque no será visible para el usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




