---
description: El método CanSeekForward determina si la secuencia se puede buscar hacia delante. Este método implementa el método IMediaPosition::CanSeekForward.
ms.assetid: ccb2db8d-b52e-4e3d-b49b-9689197a974a
title: Método CPosPassThru.CanSeekForward (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekForward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f07491a94522280357c85d773d28ea4732f2f85879b55cf5d1b5a99ec72d23f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073569"
---
# <a name="cpospassthrucanseekforward-method"></a>Método CPosPassThru.CanSeekForward

El `CanSeekForward` método determina si la secuencia se puede buscar hacia delante. Este método implementa el [**método IMediaPosition::CanSeekForward.**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CanSeekForward(
   LONG *pCanSeekForward
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCanSeekForward* 
</dt> <dd>

Puntero a una variable que recibe el valor OATRUE si el filtro puede buscar hacia delante o OAFALSE en caso contrario.

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

 

 




