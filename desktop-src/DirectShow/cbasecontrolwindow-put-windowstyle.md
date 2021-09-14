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
ms.openlocfilehash: 3f98e6205a45530a0dbcce09d095dfaa2267ccbb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173849"
---
# <a name="cbasecontrolwindowput_windowstyle-method"></a>CBaseControlWindow.put \_ WindowStyle (método)

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

## <a name="remarks"></a>Observaciones

Al cambiar los estilos de ventana, debe tener cuidado. En la mayoría de los casos, una aplicación debe recuperar el estilo actual y, a continuación, agregar o quitar los bits inadecuados. Este procedimiento permite que varios estilos de ventana internos usados por Windows permanezcan intactos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




