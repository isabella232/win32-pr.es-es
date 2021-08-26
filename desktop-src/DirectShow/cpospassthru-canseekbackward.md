---
description: El método CanSeekBackward determina si la secuencia se puede buscar hacia atrás. Este método implementa el método IMediaPosition::CanSeekBackward.
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: Método CPosPassThru.CanSeekBackward (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekBackward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1d989acf074eb20e6ea3387c37129700320ce782e3c5d7c8bd4320641839ca1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108435"
---
# <a name="cpospassthrucanseekbackward-method"></a>Método CPosPassThru.CanSeekBackward

El `CanSeekBackward` método determina si se puede buscar la secuencia hacia atrás. Este método implementa el [**método IMediaPosition::CanSeekBackward.**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CanSeekBackward(
   LONG *pCanSeekBackward
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCanSeekBackward* 
</dt> <dd>

Puntero a una variable que recibe el valor OATRUE si el filtro puede buscar hacia atrás o OAFALSE en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el **valor HRESULT** del pin conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> </dl>

 

 




