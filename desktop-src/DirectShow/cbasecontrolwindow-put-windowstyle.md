---
description: El \_ método put estiloVentana establece los estilos de ventana estándar.
ms.assetid: 3b3aa035-6aa1-4f11-80d8-03268fcf98e1
title: Método CBaseControlWindow.put_WindowStyle (Ctlutil. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661340"
---
# <a name="cbasecontrolwindowput_windowstyle-method"></a>CBaseControlWindow. put \_ estiloVentana (método)

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

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Tenga cuidado al cambiar los estilos de ventana. En la mayoría de los casos, una aplicación debe recuperar el estilo actual y, a continuación, agregar o quitar los bits inapropiados. Este procedimiento permite que los distintos estilos de ventana internos utilizados por Windows permanezcan intactos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




