---
description: 'Constructor CBaseFilter.CBaseFilter(const TCHAR \* , LNOWNOWN, CCritSec, \* REFCLSID, HRESULT \* ): método constructor.'
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: Constructor CBaseFilter.CBaseFilter(const *TCHAR, LNOWNOWN, CCritSec,* REFCLSID, HRESULT*) (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f85fc666d299d5e120f71cfeaec5fc2f88e72761
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120113"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a>Constructor CBaseFilter.CBaseFilter(const \* TCHAR, LNOWNOWN, CCritSec, \* REFCLSID, HRESULT \* )

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid,
         HRESULT   *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del filtro, con fines de depuración.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntero al propietario de este objeto. Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación. De lo contrario, establezca este parámetro en **NULL.**

</dd> <dt>

*Plock* 
</dt> <dd>

Puntero a un [**bloqueo CCritSec,**](ccritsec.md) que se usa para serializar los cambios de estado.

</dd> <dt>

*Clsid* 
</dt> <dd>

Identificador de clase (CLSID) del filtro.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a un **valor HRESULT.** El constructor omite este parámetro.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para el objeto de sección crítica, normalmente realizaría una de las siguientes acciones:

-   Derive una clase que herede **tanto CBaseFilter** como **CCritSec.** Para *pLock*, pase el `this` puntero.
-   Derive una clase que hereda **CBaseFilter** y contiene una variable **miembro CCritSec.** Para *pLock*, pase la dirección de esa variable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




