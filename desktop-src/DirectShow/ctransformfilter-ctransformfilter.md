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
ms.openlocfilehash: fce67bbe22361bdbae0cd3e51768e0cf0743d97d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098723"
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
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




