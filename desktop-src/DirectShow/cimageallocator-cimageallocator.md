---
description: 'Constructor CImageAllocator.CImageAllocator: método constructor.'
ms.assetid: 8c215b16-98e5-42fb-a95b-b6df1ade180e
title: Constructor CImageAllocator.CImageAllocator (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f17ae78b668f6cc35e454c5e4e83d38727077ef7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085763"
---
# <a name="cimageallocatorcimageallocator-constructor"></a>Constructor CImageAllocator.CImageAllocator

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFilter* 
</dt> <dd>

Puntero al filtro propietario.

</dd> <dt>

*pName* 
</dt> <dd>

Puntero a una cadena que contiene el nombre de depuración del asignador. Para obtener más información, vea [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a un **valor HRESULT.** Establezca el valor en S \_ OK antes de crear el objeto. Si se produce un error en el constructor, el valor se establece en un código de error.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CImageAllocator (clase)**](cimageallocator.md)
</dt> </dl>

 

 




