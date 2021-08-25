---
description: 'Constructor CTransformFilter.CTransformFilter: método constructor.'
ms.assetid: a64c3e29-91f2-455f-aac1-1e4ecce6958d
title: Constructor CTransformFilter.CTransformFilter (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 44061a753ef61c784298fe23e70f21fe410a9f0ad5f360acc10cb1fd16dd5f80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907695"
---
# <a name="ctransformfilterctransformfilter-constructor"></a>Constructor CTransformFilter.CTransformFilter

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CTransformFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   CLSID     clsid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pObjectName* 
</dt> <dd>

Cadena que contiene el nombre de depuración del filtro. Para obtener más información, vea [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*lpUnk* 
</dt> <dd>

Puntero al propietario de este objeto. Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación. De lo contrario, establezca este parámetro en **NULL.**

</dd> <dt>

*Clsid* 
</dt> <dd>

Identificador de clase del filtro.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El constructor no crea los pines del filtro. Esto sucede durante la primera llamada al [**método GetPin.**](ctransformfilter-getpin.md) El constructor inicializa las variables [**miembro m \_ pInput**](ctransformfilter-m-pinput.md) y [**m \_ pOutput**](ctransformfilter-m-poutput.md) en **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




