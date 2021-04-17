---
description: El método SetPalette instala una paleta para la ventana.
ms.assetid: 64fa0d3a-c2eb-4e58-8b8d-c8e5ec3bb479
title: Método CBaseWindow. SetPalette (Winutil. h)
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
ms.openlocfilehash: f246fe8401e1f671f5935ff7d7454093ea1d3179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660313"
---
# <a name="cbasewindowsetpalette-method-winutilh"></a>Método CBaseWindow. SetPalette (Winutil. h)

El `SetPalette` método instala una paleta para la ventana.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT SetPalette(
   HPALETTE hPalette
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPalette* 
</dt> <dd>

Identificador de la nueva paleta. No puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Una llamada interna a **GdiFlush** devolvió un error.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto.<br/>                                            |



 

## <a name="remarks"></a>Observaciones

Si el valor de la variable miembro [**CBaseWindow:: m \_ BNoRealize**](cbasewindow-m-bnorealize.md) es **false** (valor predeterminado), este método selecciona la paleta y la realiza. De lo contrario, selecciona la paleta pero no la detecta. El objeto no elimina ninguna de las paletas anteriores que estaba usando. El autor de la llamada es responsable de eliminar las paletas.

Cualquier subproceso puede llamar con seguridad a este método, no solo al subproceso que posee la ventana. La ventana envía un mensaje privado a sí mismo, lo que desencadena una llamada al método [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




