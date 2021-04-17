---
description: Método de constructor.
ms.assetid: a64c3e29-91f2-455f-aac1-1e4ecce6958d
title: Constructor CTransformFilter. CTransformFilter (Transfrm. h)
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
ms.openlocfilehash: 39569dff69c2ab1ebb635cb69a4c71602a7400d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660729"
---
# <a name="ctransformfilterctransformfilter-constructor"></a>Constructor CTransformFilter. CTransformFilter

Método de constructor.

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

Puntero al propietario de este objeto. Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación. De lo contrario, establezca este parámetro en **null**.

</dd> <dt>

*CLSID* 
</dt> <dd>

Identificador de clase del filtro.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El constructor no crea los PIN del filtro. Esto sucede durante la primera llamada al método [**GetPin**](ctransformfilter-getpin.md) . El constructor inicializa las variables de miembro [**m \_ pInput**](ctransformfilter-m-pinput.md) y [**m \_ pOutput**](ctransformfilter-m-poutput.md) en **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




