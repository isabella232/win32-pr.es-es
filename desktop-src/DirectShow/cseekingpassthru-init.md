---
description: El método Init inicializa el objeto .
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: Método CSeekingPassThru.Init (Seekpt.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070052"
---
# <a name="cseekingpassthruinit-method"></a>Método CSeekingPassThru.Init

El `Init` método inicializa el objeto .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bSupportRendering* \[ En\]
</dt> <dd>

Valor booleano que especifica si el filtro es un representador. Use el valor **TRUE si** el filtro es un representador o **FALSE** en caso contrario.

</dd> <dt>

*pPin* 
</dt> <dd>

Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) en el pin de entrada del filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto.<br/>                                |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | El objeto ya se ha inicializado.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay suficiente memoria para crear el objeto.<br/> |



 

## <a name="remarks"></a>Observaciones

Si el valor de *bSupportRendering* es **TRUE,** este método crea una instancia de la [**clase CRendererPosPassThru.**](crendererpospassthru.md) De lo contrario, crea una instancia de la [**clase CPosPassThru.**](cpospassthru.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Seekpt.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSeekingPassThru (clase)**](cseekingpassthru.md)
</dt> </dl>

 

 




