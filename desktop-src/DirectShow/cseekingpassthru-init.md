---
description: El método Init inicializa el objeto .
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: CSeekingPassThru.Init (Seekpt.h)
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
ms.openlocfilehash: 91d20477f83ec79c6ae6095e81810c98454f9c26521eda995c919867b3e3ac12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953823"
---
# <a name="cseekingpassthruinit-method"></a>CSeekingPassThru.Init (método)

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



 

## <a name="remarks"></a>Comentarios

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

 

 




