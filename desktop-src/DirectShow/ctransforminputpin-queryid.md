---
description: 'Método CTransformInputPin.QueryId: el método QueryId recupera un identificador para el pin. Este método implementa el método IPin::QueryId.'
ms.assetid: 91fde383-0288-4307-9ca8-e117b6111769
title: Método CTransformInputPin.QueryId (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8bb7fa42453e15137be6770332496ea1f39c04c3a6055af00300da9bd6194961
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087005"
---
# <a name="ctransforminputpinqueryid-method"></a>Método CTransformInputPin.QueryId

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



 

## <a name="remarks"></a>Comentarios

El identificador de pin se usa para la persistencia del grafo. El identificador de pin de esta clase es In. Esta clase invalida el comportamiento de la [**clase CBasePin.**](cbasepin.md) En la **clase CBasePin,** el identificador de pin es el mismo que el nombre del pin, especificado en el constructor de clase. En la **clase CTransformInputPin,** el identificador de pin y el nombre del pin no son iguales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




