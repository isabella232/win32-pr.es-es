---
description: El método FindPin recupera el pin con el identificador especificado.
ms.assetid: d07a298f-ddb0-44eb-85ca-81735875cdf3
title: Método CBaseRenderer.FindPin (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6e6789a91f34d95933ae7869e1588eeb14b6006
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061335"
---
# <a name="cbaserendererfindpin-method"></a>Método CBaseRenderer.FindPin

El `FindPin` método recupera el pin con el identificador especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Id* 
</dt> <dd>

Puntero a una cadena de caracteres anchos constante terminada en NULL que identifica el pin. Debe ser L"In".

</dd> <dt>

*ppPin* 
</dt> <dd>

Dirección de una variable que recibe un puntero a la interfaz [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin. Si se produce un error en el *\* método, ppPin* se establece en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                       | Descripción                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Correcto.<br/>                   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>         | **Argumento de** puntero NULL.<br/> |
| <dl> <dt>**VFW \_ E \_ NO \_ ENCONTRADO**</dt> </dl> | Not found.<br/>                 |



 

## <a name="remarks"></a>Observaciones

Este método invalida el [**método CBaseFilter::FindPin.**](cbasefilter-findpin.md) El único pin del filtro (el pin de entrada) se denomina "In".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




