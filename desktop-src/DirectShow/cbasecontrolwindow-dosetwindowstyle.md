---
description: El método DoSetWindowStyle cambia los estilos de ventana típicos o extendidos.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Método CBaseControlWindow.DoSetWindowStyle (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoSetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3b1f72ace792f13f88fbf0ce1e0edaf7b08789ecba88aede0b4094e9e75ae52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640894"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a>CBaseControlWindow.DoSetWindowStyle (método)

El `DoSetWindowStyle` método cambia los estilos de ventana típicos o extendidos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Estilo* 
</dt> <dd>

Estilos de ventana adecuados.

</dd> <dt>

*WindowLong* 
</dt> <dd>

Valor que especifica los estilos que se establecerán. Debe ser una de las siguientes:



| Etiqueta | Value |
|--------------|--------------------------------------|
| ESTILO \_ GWL   | Recupere los estilos de ventana.          |
| GWL \_ EXSTYLE | Recupere los estilos de ventana extendidos. |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Esta función miembro llama a la función **SetWindowLong** de Win32 para establecer el estilo de ventana y, a continuación, vuelve a mostrar la ventana en la posición actual. Las funciones miembro [**CBaseControlWindow::p ut \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) y [**CBaseControlWindow::p ut \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) llaman a esta función miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




