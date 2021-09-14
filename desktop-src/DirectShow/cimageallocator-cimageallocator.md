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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170038"
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
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImageAllocator (clase)**](cimageallocator.md)
</dt> </dl>

 

 




