---
description: El método Invoke proporciona acceso a las propiedades y los métodos expuestos por el objeto.
ms.assetid: 3c03751d-239b-4cc5-bfab-8d1aed1074b8
title: Método CMediaPosition. Invoke (Ctlutil. h)
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
ms.openlocfilehash: 3955848bf2a87e0983ddd7dc3bef48f157ae6648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671555"
---
# <a name="cmediapositioninvoke-method"></a>CMediaPosition. Invoke (método)

El `Invoke` método proporciona acceso a las propiedades y los métodos expuestos por el objeto.

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

Identificador del miembro. Use [**CMediaPosition:: GetIDsOfNames**](cmediaposition-getidsofnames.md) para obtener el identificador de envío.

</dd> <dt>

*riid* 
</dt> <dd>

Reservado para uso futuro. Debe ser un IID \_ null.

</dd> <dt>

*lcid* 
</dt> <dd>

Contexto de configuración regional en el que se interpretan los argumentos.

</dd> <dt>

*wFlags* 
</dt> <dd>

Marcas que describen el contexto de la llamada.

</dd> <dt>

*pdispparams* 
</dt> <dd>

Puntero a una estructura **DIPPARAMS** que contiene los argumentos.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Puntero a una **variante** que recibe el resultado, o **null** si el llamador no espera ningún resultado.

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

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                              | Descripción                                      |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                     | Correcto.<br/>                              |
| <dl> <dt>**DISP \_ E \_ UNKNOWNINTERFACE**</dt> </dl> | El parámetro *riid* no es un IID \_ nulo<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




