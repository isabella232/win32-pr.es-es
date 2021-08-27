---
description: El método InitialiseWindow inicializa la ventana.
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: CBaseWindow.Inimétodo tialiseWindow (Winutil.h)
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
ms.openlocfilehash: f260f60111f715bfce357e264b65bb4b821c5ca890d39d4d54e7269a191df303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954664"
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

*Hwnd* 
</dt> <dd>

Identificador de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

De forma predeterminada, este método recupera un identificador en el contexto de dispositivo (DC) de la ventana y crea un controlador de dominio de memoria compatible. Si el valor de la [**marca CBaseWindow::m \_ bDoGetDC**](cbasewindow-m-bdogetdc.md) es **FALSE,** sin embargo, este método no recupera los contextos del dispositivo. El controlador de dominio de memoria es útil para seleccionar mapas de bits antes de su borrado en la ventana.

El [**método CBaseWindow::D oCreateWindow**](cbasewindow-docreatewindow.md) llama a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




