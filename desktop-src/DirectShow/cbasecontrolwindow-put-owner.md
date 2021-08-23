---
description: El método put Owner establece la ventana primaria de la ventana de vídeo; a continuación, la ventana primaria \_ reenvía determinados mensajes a la ventana de vídeo.
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: CBaseControlWindow.put_Owner método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f33e0c26506faea93afc11f51aaba13007c443fc011839efafce436fe9f2b2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635904"
---
# <a name="cbasecontrolwindowput_owner-method"></a>CBaseControlWindow.put \_ Owner (método)

El método establece la ventana primaria de la ventana de vídeo; a continuación, la `put_Owner` ventana primaria reenvía determinados mensajes a la ventana de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Owner(
   OAHWND Owner
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Propietario* 
</dt> <dd>

Identificador de la ventana primaria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve NOERROR.

## <a name="remarks"></a>Comentarios

Internamente, este método llama a la función **SetParent** de Microsoft Win32 para establecer el nuevo propietario y establece el estilo de la ventana primaria en WS \_ CHILD. A continuación, la ventana primaria reenviará determinados conjuntos de mensajes (en particular, mensajes del mouse y del teclado) a la ventana de vídeo.

Después de establecer el propietario de la ventana de vídeo, debe establecer el propietario en **NULL** y el estilo de ventana del propietario en WS OVERLAPPED y WS CLIPCHILDREN antes de liberar el gráfico \_ \_ de filtros. Al establecer el propietario en **NULL,** este método desactiva el bit WS CHILD de la \_ ventana primaria. Si no establece el propietario en **NULL,** la ventana primaria seguirá pasando mensajes a la ventana de vídeo y es probable que se produzcan errores cuando se cierre la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




