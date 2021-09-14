---
description: El método GetPointer recupera un puntero de lectura y escritura al búfer. Este método implementa el método IMediaSample::GetPointer.
ms.assetid: dd797ad5-6066-4366-a56f-621132f2e6ea
title: Método CMediaSample.GetPointer (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe8d8785bd52fbe601d9980f8fc146a2c6f41e40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361376"
---
# <a name="cmediasamplegetpointer-method"></a>Método CMediaSample.GetPointer

El `GetPointer` método recupera un puntero de lectura y escritura al búfer. Este método implementa el [**método IMediaSample::GetPointer.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPointer(
   BYTE **ppBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppBuffer* 
</dt> <dd>

Dirección de una variable que recibe un puntero al búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




