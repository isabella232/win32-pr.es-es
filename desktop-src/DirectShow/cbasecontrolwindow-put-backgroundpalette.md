---
description: El método \_ put BackgroundPalette establece una marca para realizar la paleta en segundo plano.
ms.assetid: db420e75-e300-41fa-bae4-fb267cc99c7c
title: CBaseControlWindow.put_BackgroundPalette método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 295889510b96a085865eeff45ba976278519670adbd596b24e6aea829a29df4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966725"
---
# <a name="cbasecontrolwindowput_backgroundpalette-method"></a>CBaseControlWindow.put \_ BackgroundPalette (método)

El `put_BackgroundPalette` método establece una marca para realizar la paleta en segundo plano.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_BackgroundPalette(
   long BackgroundPalette
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*BackgroundPalette* 
</dt> <dd>

Marca booleana de Automation (0 está desactivada, 1 está desactivada).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Para reproducir un vídeo dentro de otra aplicación o documento, es posible que la aplicación quiera usar su propia paleta. Puede pedir que el vídeo use la paleta de primer plano actual en lugar de la suya propia como paleta de fondo estableciendo esta marca en 1. Si se establece en 0, la ventana se instalará y se dará cuenta de su propia paleta preferida. Pedir a la ventana que use una paleta diferente provocará graves penalizaciones de rendimiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




