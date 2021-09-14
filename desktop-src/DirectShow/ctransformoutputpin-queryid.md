---
description: 'Método CTransformOutputPin.QueryId: el método QueryId recupera un identificador para el pin. Este método implementa el método IPin::QueryId.'
ms.assetid: 3d83db3a-b919-454d-a91a-91f33a952a22
title: Método CTransformOutputPin.QueryId (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4c2d222ca4dd184adfe41f9f610b10f15ee9f02
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255333"
---
# <a name="ctransformoutputpinqueryid-method"></a>Método CTransformOutputPin.QueryId

El `QueryId` método recupera un identificador para el pin. Este método implementa el [**método IPin::QueryId.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Id* 
</dt> <dd>

Recibe una cadena que contiene el identificador de pin.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>       |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | **Argumento de** puntero NULL<br/> |



 

## <a name="remarks"></a>Observaciones

El identificador de pin se usa para la persistencia del grafo. El identificador de pin de esta clase es Out. Esta clase invalida el comportamiento de la [**clase CBasePin.**](cbasepin.md) En la **clase CBasePin,** el identificador de pin es el mismo que el nombre del pin, especificado en el constructor de clase. En la **clase CTransformInputPin,** el identificador de pin y el nombre del pin no son los mismos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




