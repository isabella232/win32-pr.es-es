---
description: El método Invoke proporciona acceso a las propiedades y los métodos expuestos por el objeto .
ms.assetid: 3c03751d-239b-4cc5-bfab-8d1aed1074b8
title: Método CMediaPosition.Invoke (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6dac439b94a62e9dbd11ca9e12ab80023071fc00cf22abcf6b9b4b93b07c356c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156861"
---
# <a name="cmediapositioninvoke-method"></a>Método CMediaPosition.Invoke

El `Invoke` método proporciona acceso a las propiedades y los métodos expuestos por el objeto .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dispidMember* 
</dt> <dd>

Identificador del miembro. Use [**CMediaPosition::GetIDsOfNames**](cmediaposition-getidsofnames.md) para obtener el identificador de distribución.

</dd> <dt>

*riid* 
</dt> <dd>

Reservado para uso futuro. Debe ser IID \_ NULL.

</dd> <dt>

*lcid* 
</dt> <dd>

Contexto de configuración regional en el que se interpretarán los argumentos.

</dd> <dt>

*wFlags* 
</dt> <dd>

Marcas que describen el contexto de la llamada.

</dd> <dt>

*pdispparams* 
</dt> <dd>

Puntero a una **estructura DIPPARAMS** que contiene los argumentos.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Puntero a **una VARIANT que** recibe el resultado o **NULL** si el autor de la llamada no espera ningún resultado.

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

Puntero a una estructura que recibe información de excepción.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Puntero a una variable que recibe el índice del primer argumento que produce un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                              | Descripción                                      |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Correcto.<br/>                              |
| <dl> <dt>**DISP \_ E \_ UNKNOWNINTERFACE**</dt> </dl> | El *parámetro riid* no es IID \_ NULL<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaPosition (clase)**](cmediaposition.md)
</dt> </dl>

 

 




