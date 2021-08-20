---
description: 'Constructor CBaseReferenceClock.CBaseReferenceClock: método constructor.'
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: Constructor CBaseReferenceClock.CBaseReferenceClock (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ea08e5555aa6286dac80642f19969e6e669a4ec6ccddb4e530d13e0253b4bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954994"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a>Constructor CBaseReferenceClock.CBaseReferenceClock

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del objeto. Para obtener más información, vea [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*Punk* 
</dt> <dd>

Puntero al propietario de este objeto. Si el objeto se agrega, pase un puntero a la interfaz IUnknown del objeto de agregación. De lo contrario, establezca este parámetro en **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a un **valor HRESULT.** Si se produce un error, el método devuelve un código de error en este parámetro. No establezca este parámetro en **NULL.**

</dd> <dt>

*pSched* 
</dt> <dd>

Puntero a un [**objeto CAMSchedule.**](camschedule.md) Si **es NULL,** este método crea un **nuevo objeto CAMSchedule.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseReferenceClock (clase)**](cbasereferenceclock.md)
</dt> </dl>

 

 




