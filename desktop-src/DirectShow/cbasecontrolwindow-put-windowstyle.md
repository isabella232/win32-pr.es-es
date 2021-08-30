---
description: El método put \_ WindowStyle establece los estilos de ventana estándar.
ms.assetid: 3b3aa035-6aa1-4f11-80d8-03268fcf98e1
title: CBaseControlWindow.put_WindowStyle método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 416f222b3b4a3f3d10c12baf482d1c94687ba23596fcfbc92e59e1b7dab731e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056733"
---
# <a name="cbasecontrolwindowput_windowstyle-method"></a>CBaseControlWindow.put \_ (método WindowStyle)

El `put_WindowStyle` método establece los estilos de ventana estándar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_WindowStyle(
   long WindowStyle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*WindowStyle* 
</dt> <dd>

Nuevos estilos de ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Tener cuidado al cambiar los estilos de ventana. En la mayoría de los casos, una aplicación debe recuperar el estilo actual y, a continuación, agregar o quitar los bits inadecuados. Este procedimiento permite que varios estilos de ventana internos usados por Windows permanezcan intactos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




