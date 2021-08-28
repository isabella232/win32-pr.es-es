---
description: 'Método CTransInPlaceOutputPin.EnumMediaTypes: el método EnumMediaTypes enumera los tipos de medios preferidos del pin. Este método implementa el método IPin::EnumMediaTypes.'
ms.assetid: 942c6594-3053-484a-a0f7-286dcd3f7550
title: Método CTransInPlaceOutputPin.EnumMediaTypes (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7a351f947b0526b8daf77b0b15ea0d2a2894ef6ff90390be484b5d0ce4b7fa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076175"
---
# <a name="ctransinplaceoutputpinenummediatypes-method"></a>Método CTransInPlaceOutputPin.EnumMediaTypes

El `EnumMediaTypes` método enumera los tipos de medios preferidos del pin. Este método implementa el [**método IPin::EnumMediaTypes.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnum* 
</dt> <dd>

Recibe un puntero a la [**interfaz IEnumMediaTypes.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                                         |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Memoria insuficiente.<br/>                     |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>             | **Puntero NULL.**<br/>                        |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | El pin de entrada del filtro no está conectado.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método devuelve la **interfaz IEnumMediaTypes** del pin de salida ascendente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransInPlaceOutputPin (clase)**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




