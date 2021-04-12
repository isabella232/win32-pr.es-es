---
description: El método SetPalette instala una paleta para la ventana. Este método no tiene parámetros.
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: 'Método CBaseWindow. SetPalette (Winutil. h): no hay parámetros'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1203b6aeedd39eb82d7188c4e5d5503b01d167fe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104280536"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a>Método CBaseWindow. SetPalette (Winutil. h): no hay parámetros

El `SetPalette` método instala una paleta para la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Una llamada interna a **GdiFlush** devolvió un error.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto.<br/>                                            |



 

## <a name="remarks"></a>Observaciones

La paleta proporcionada por la variable miembro [**CBaseWindow:: m \_ hPalette**](cbasewindow-m-hpalette.md) está seleccionada. El autor de la llamada debe garantizar la validez de **m \_ hPalette**.

Si el valor de la variable miembro [**CBaseWindow:: m \_ BNoRealize**](cbasewindow-m-bnorealize.md) es **false** (valor predeterminado), este método selecciona la paleta y la realiza. De lo contrario, selecciona la paleta pero no la detecta. El objeto no elimina ninguna de las paletas anteriores que estaba usando. El autor de la llamada es responsable de eliminar las paletas.

Cualquier subproceso puede llamar con seguridad a este método, no solo al subproceso que posee la ventana. La ventana envía un mensaje privado a sí mismo, lo que desencadena una llamada al método [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) .

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Winutil. h (incluir streams. h) |
| Biblioteca| Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




