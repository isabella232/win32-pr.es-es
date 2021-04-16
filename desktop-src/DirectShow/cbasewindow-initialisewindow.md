---
description: El método InitialiseWindow inicializa la ventana.
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: CBaseWindow.Inimétodo tialiseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75668846c700c33a26b7bb7ad2af2a3fd6e8eea2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679563"
---
# <a name="cbasewindowinitialisewindow-method"></a>CBaseWindow.Inimétodo tialiseWindow

El `InitialiseWindow` método inicializa la ventana.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT InitialiseWindow(
   HWND hwnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Identificador de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

De forma predeterminada, este método recupera un identificador para el contexto de dispositivo (DC) de la ventana y crea un controlador de dominio de memoria compatible. Sin embargo, si el valor de la marca [**CBaseWindow:: m \_ BDoGetDC**](cbasewindow-m-bdogetdc.md) es **false**, este método no recupera los contextos de dispositivo. El controlador de dominio de memoria es útil para seleccionar mapas de bits antes de blitting a la ventana.

El método [**CBaseWindow::D ocreatewindow**](cbasewindow-docreatewindow.md) llama a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




