---
description: El método ReceiveMultiple recibe una matriz de ejemplos. Este método implementa el método IMemInputPin::ReceiveMultiple.
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: Método CBaseInputPin.ReceiveMultiple (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63d71f47978a2eefdcbdacbe1c31bfe69c732c24a0479357b35aa1ddd2b0a9de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079405"
---
# <a name="cbaseinputpinreceivemultiple-method"></a>Método CBaseInputPin.ReceiveMultiple

El `ReceiveMultiple` método recibe una matriz de ejemplos. Este método implementa el [**método IMemInputPin::ReceiveMultiple.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReceiveMultiple(
   IMediaSample **pSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSamples* 
</dt> <dd>

Dirección de una matriz de [**punteros IMediaSample,**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de tamaño *nSamples*.

</dd> <dt>

*nSamples* 
</dt> <dd>

Número de muestras que se procesarán.

</dd> <dt>

*nSamplesProcessed* 
</dt> <dd>

Puntero a una variable que recibe el número de muestras que se procesaron.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                                             | Descripción                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Correcto.<br/>                                        |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                 | El pin se está vacíando actualmente; se rechazó el ejemplo.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>               | **Argumento de** puntero NULL.<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de medio no válido.<br/>                             |
| <dl> <dt>**ERROR EN TIEMPO DE EJECUCIÓN DE VFW \_ E \_ \_**</dt> </dl>   | Se produjo un error en tiempo de ejecución.<br/>                      |
| <dl> <dt>**VFW \_ E \_ ESTADO \_ INCORRECTO**</dt> </dl>     | El pin se detiene.<br/>                             |



 

## <a name="remarks"></a>Comentarios

Este método se comporta como el [**método CBaseInputPin::Receive,**](cbaseinputpin-receive.md) pero recibe una matriz de ejemplos. En la clase base, el método recorre en bucle la matriz y llama **a Receive** con cada ejemplo. Invalide esta función si el filtro puede procesar lotes de muestras de forma más eficaz que procesarlos de uno en uno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseInputPin (clase)**](cbaseinputpin.md)
</dt> </dl>

 

 




