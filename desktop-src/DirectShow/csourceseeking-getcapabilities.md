---
description: 'Método CSourceSeeking.GetCapabilities: el método GetCapabilities recupera todas las funcionalidades de búsqueda de la secuencia. Este método implementa el método IMediaSeeking::GetCapabilities.'
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: Método CSourceSeeking.GetCapabilities (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96e3a637673a91ebc98e48777b8f42bdcbf02654a0c264037a66b4121f5b80ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054345"
---
# <a name="csourceseekinggetcapabilities-method"></a>Método CSourceSeeking.GetCapabilities

El `GetCapabilities` método recupera todas las funcionalidades de búsqueda de la secuencia. Este método implementa el [**método IMediaSeeking::GetCapabilities.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCapabilities* 
</dt> <dd>

Puntero a una variable que recibe una combinación bit a bit de marcas [**AM \_ SEEKING SEEKING \_ \_ CAPABILITIES.**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.



| Código devuelto                                                                               | Descripción                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto<br/>                |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | **Valor de** puntero NULL<br/> |



 

## <a name="remarks"></a>Comentarios

La variable miembro [**CSourceSeeking::m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) especifica las funcionalidades de búsqueda.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 




