---
description: Dada una lista de tipos de medios, el método TryMediaTypes intenta completar una conexión mediante uno de esos tipos.
ms.assetid: cc437e44-bc59-494e-8669-7f539353a794
title: Método CBasePin.TryMediaTypes (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.TryMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a4d4e33ca339c1ade344bb2ca9531bea381d14b4381773673b07e522437e90a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108625"
---
# <a name="cbasepintrymediatypes-method"></a>Método CBasePin.TryMediaTypes

Dada una lista de tipos de medios, `TryMediaTypes` el método intenta completar una conexión mediante uno de esos tipos.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT TryMediaTypes(
         IPin            *pReceivePin,
   const CMediaType      *pmt,
         IEnumMediaTypes *pEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin receptor.

</dd> <dt>

*Pmt* 
</dt> <dd>

Puntero a un [**objeto CMediaType**](cmediatype.md) que limita los posibles tipos multimedia, o **NULL.**

</dd> <dt>

*pEnum* 
</dt> <dd>

Puntero a una [**interfaz IEnumMediaTypes,**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) que se usa para enumerar la lista de tipos de medios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los de la tabla siguiente.



| Código devuelto                                                                                                  | Descripción                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Correcto.<br/>                               |
| <dl> <dt>**VFW \_ E NO HAY TIPOS \_ \_ \_ ACEPTABLES**</dt> </dl> | No se encontró un tipo de medio aceptable.<br/> |



 

## <a name="remarks"></a>Comentarios

Para cada tipo de medio devuelto por la interfaz **IEnumMediaTypes,** este método intenta una conexión llamando al [**método CBasePin::AttemptConnection.**](cbasepin-attemptconnection.md)

Si el *parámetro pmt* no es **NULL,** el pin omite los tipos de medios que no coinciden con este tipo. El *parámetro pmt* puede especificar un tipo de medio parcial. Un tipo de medio parcial tiene un valor de GUID \_ NULL para el tipo principal, el subtipo o el formato. El valor \_ NULL de GUID coincide con cualquier tipo, similar a un valor de "carácter comodín".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




