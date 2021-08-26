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
ms.openlocfilehash: 0f639e5d68b11b6a7a65ccfe0d0c6465f822d591b0c4dfd0f4916072fde40856
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043775"
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

Puntero a una cadena de caracteres anchos terminada en NULL constante que identifica el pin. Debe ser L"In".

</dd> <dt>

*ppPin* 
</dt> <dd>

Dirección de una variable que recibe un puntero a la interfaz [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin. Si se produce un error en el método , *\* ppPin* se establece en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                       | Descripción                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Correcto.<br/>                   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>         | **Argumento de** puntero NULL.<br/> |
| <dl> <dt>**VFW \_ E \_ NO \_ ENCONTRADO**</dt> </dl> | Not found.<br/>                 |



 

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CBaseFilter::FindPin.**](cbasefilter-findpin.md) El único pin del filtro (el pin de entrada) se denomina "In".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




