---
description: El método DoRealisePalette se da cuenta de la paleta actual de la ventana.
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: Método CBaseWindow.DoRealisePalette (Winutil.h)
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
ms.openlocfilehash: ce593939ec9f8aa3f2675c95e7a70363465aabb6f501fde79de839c533a1d249
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757485"
---
# <a name="cbasewindowdorealisepalette-method"></a>Método CBaseWindow.DoRealisePalette

El `DoRealisePalette` método se da cuenta de la paleta actual de la ventana.

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

Valor booleano que especifica si la paleta se ve forzada a ser una paleta de fondo. Para obtener más información, consulte **SelectPalette** en el SDK de plataforma.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Una llamada interna a **GdiFlush** devolvió un error.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                                            |



 

## <a name="remarks"></a>Comentarios

El [**método CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) llama a este método. Para establecer una nueva paleta, llame al [**método CBaseWindow::SetPalette.**](cbasewindow-setpalette.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




