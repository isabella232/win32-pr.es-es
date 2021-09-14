---
description: El método Next recupera un número especificado de pines en la secuencia de enumeración. Este método implementa el método IEnumPins::Next.
ms.assetid: c38fbd32-7d83-43ec-a105-4a7cb515b471
title: Método CEnumPins.Next (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 612dcd638939b34803b7296babf7445a07cdad22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973877"
---
# <a name="cenumpinsnext-method"></a>CEnumPins.Next (método)

El método Next recupera un número especificado de pines en la secuencia de enumeración. Este método implementa el [**método IEnumPins::Next.**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Next(
   ULONG cPins,
   IPin  **ppPins,
   ULONG *pcFetched
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cPins* 
</dt> <dd>

Número de pines que se recuperarán.

</dd> <dt>

*ppPins* 
</dt> <dd>

Matriz de *cPins de tamaño* que se rellena con [**punteros IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

</dd> <dt>

*pcFetched* 
</dt> <dd>

Puntero a una variable que recibe el número de pines recuperados. Puede ser **NULL** si *cPins* es 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                                | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | No recuperó tantas patillas como se solicitó.<br/>                                 |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Correcto.<br/>                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Argumento no válido.<br/>                                                           |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>                  | **Argumento de** puntero NULL.<br/>                                                  |
| <dl> <dt>**VFW \_ E \_ ENUM \_ OUT \_ OF \_ SYNC**</dt> </dl> | El estado del filtro ha cambiado y ahora es incoherente con el enumerador.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método recupera punteros al número especificado de pines, empezando en la posición actual de la enumeración, y los coloca en la matriz especificada.

Este método llama al método [**CBaseFilter::GetPin**](cbasefilter-getpin.md) del filtro para recuperar los pines.

Si el método se realiza correctamente, todos los punteros **IPin** tienen recuentos de referencias pendientes. Asegúrese de liberarlos cuando haya terminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CEnumPins (clase)**](cenumpins.md)
</dt> </dl>

 

 




