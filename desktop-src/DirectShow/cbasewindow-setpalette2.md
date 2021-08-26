---
description: El método SetPalette instala una paleta para la ventana. Este método no tiene parámetros.
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: 'Método CBaseWindow.SetPalette (Winutil.h): sin parámetros'
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
ms.openlocfilehash: f15df65f6e427e467c14654a0e2745b84d774a5226b9a526193fc546261c5a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052155"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a>Método CBaseWindow.SetPalette (Winutil.h): sin parámetros

El `SetPalette` método instala una paleta para la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Una llamada interna **a GdiFlush** devolvió un error.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                                            |



 

## <a name="remarks"></a>Comentarios

La paleta que proporciona la variable [**miembro \_ HPalette CBaseWindow::m**](cbasewindow-m-hpalette.md) está seleccionada. El autor de la llamada debe garantizar la validez **de m \_ hPalette**.

Si el valor de la variable miembro [**CBaseWindow::m \_ bNoRealize**](cbasewindow-m-bnorealize.md) es **FALSE** (valor predeterminado), este método selecciona la paleta y la realiza. De lo contrario, selecciona la paleta, pero no la reconoce. El objeto no elimina ninguna paleta anterior que estaba usando. El autor de la llamada es responsable de eliminar las paletas.

Cualquier subproceso puede llamar de forma segura a este método, no solo al subproceso que posee la ventana. La ventana envía un mensaje privado a sí mismo, lo que desencadena una llamada al método [**CBaseWindow::OnPaletteChange.**](cbasewindow-onpalettechange.md)

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Winutil.h (incluir Secuencias.h) |
| Biblioteca| Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




