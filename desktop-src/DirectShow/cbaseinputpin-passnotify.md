---
description: El método PassNotify pasa un mensaje de control de calidad al objeto adecuado.
ms.assetid: dbc9a4b7-a522-4fbf-8e3a-af50e11c1d80
title: Método CBaseInputPin.PassNotify (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.PassNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 760ec066a9d4876dd6ef754783c41ae12765db10c1595d08aef0a73258de087f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017003"
---
# <a name="cbaseinputpinpassnotify-method"></a>Método CBaseInputPin.PassNotify

El `PassNotify` método pasa un mensaje de control de calidad al objeto adecuado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PassNotify(
   Quality q
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Q* 
</dt> <dd>

[**Estructura**](/windows/win32/api/strmif/ns-strmif-quality) de calidad que contiene el mensaje de control de calidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                                       | Descripción                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Correcto.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ NO \_ ENCONTRADO**</dt> </dl> | No se encontró un objeto para aceptar el mensaje.<br/> |



 

## <a name="remarks"></a>Comentarios

Llame a este método si el filtro no controla los mensajes de control de calidad. Este método pasa el mensaje a uno de los siguientes objetos, en orden de preferencia:

-   Un administrador de control de calidad externo, si se llamó al método [**IQualityControl::SetSink.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink)
-   El pin de salida ascendente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseInputPin (clase)**](cbaseinputpin.md)
</dt> <dt>

[Administración de control de calidad](quality-control-management.md)
</dt> </dl>

 

 




