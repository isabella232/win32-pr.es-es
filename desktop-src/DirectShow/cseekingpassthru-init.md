---
description: El método init inicializa el objeto.
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: Método CSeekingPassThru.Init (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78176a6966f379240b5b7edd1ef5b73d7fa75b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660179"
---
# <a name="cseekingpassthruinit-method"></a>CSeekingPassThru.Init (método)

El `Init` método inicializa el objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bSupportRendering* \[ de\]
</dt> <dd>

Valor booleano que especifica si el filtro es un representador. Use el valor **true** si el filtro es un representador o **false** en caso contrario.

</dd> <dt>

*pPin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) en el PIN de entrada del filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>                                |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | El objeto ya se ha inicializado.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente para crear el objeto.<br/> |



 

## <a name="remarks"></a>Observaciones

Si el valor de *bSupportRendering* es **true**, este método crea una instancia de la clase [**CRendererPosPassThru**](crendererpospassthru.md) . De lo contrario, crea una instancia de la clase [**CPosPassThru**](cpospassthru.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Seekpt. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSeekingPassThru**](cseekingpassthru.md)
</dt> </dl>

 

 




