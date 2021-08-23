---
description: El Conectar de conexión conecta el pin a otro pin. Este método implementa el método IPin::Conectar.
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: CBasePin. Conectar método (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a134b87e9c7c4d0f665ae37df7ec9cd0ecb3a37c0d0548f27835ead7b8ecca21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074799"
---
# <a name="cbasepinconnect-method"></a>CBasePin. Conectar método

El `Connect` método conecta el pin a otro pin. Este método implementa el [**método IPin::Conectar.**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Connect(
         IPin          *pReceivePin,
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntero a la interfaz IPin del [**pin receptor.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

</dd> <dt>

*Pmt* 
</dt> <dd>

Puntero a una [**estructura \_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio para la conexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los de la tabla siguiente.



| Código devuelto                                                                                                  | Descripción                                                                        |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Correcto.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ YA \_ CONECTADO**</dt> </dl>    | El pin ya está conectado.<br/>                                           |
| <dl> <dt>**VFW \_ E \_ NO \_ ACCEPTABLE \_ TYPES**</dt> </dl> | No se encontró un tipo de medio aceptable.<br/>                                |
| <dl> <dt>**VFW \_ E \_ NOT \_ STOPPED**</dt> </dl>          | El filtro está activo y el pin no admite la reconexión dinámica.<br/> |
| <dl> <dt>**TIPO E VFW \_ \_ NO \_ \_ ACEPTADO**</dt> </dl>   | El tipo de medio especificado no es aceptable.<br/>                             |



 

## <a name="remarks"></a>Comentarios

El *parámetro pmt* puede ser **NULL.** También puede especificar un tipo de medio parcial, con un valor de GUID NULL para \_ el tipo principal, subtipo o formato.

En la clase base, este método comprueba si el pin ya está conectado y si el filtro está detenido. Delega el resto del proceso de conexión al [**método CBasePin::AgreeMediaType.**](cbasepin-agreemediatype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




