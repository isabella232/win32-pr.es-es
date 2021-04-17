---
description: Método de constructor.
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: Constructor CBaseFilter. CBaseFilter (const TCHAR *, LPUNKNOWN, CCritSec*, REFCLSID, HRESULT *) (Amfilter. h)
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
ms.openlocfilehash: b4d8806c9b4103c06eb58e11547e83fc933d5d3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660575"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a>Constructor CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID, HRESULT \* )

Método de constructor.

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

*pUnk* 
</dt> <dd>

Puntero al propietario de este objeto. Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación. De lo contrario, establezca este parámetro en **null**.

</dd> <dt>

*pLock* 
</dt> <dd>

Puntero a un bloqueo de [**CCritSec**](ccritsec.md) , que se usa para serializar los cambios de estado.

</dd> <dt>

*CLSID* 
</dt> <dd>

Identificador de clase (CLSID) del filtro.

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a un valor **HRESULT** . El constructor omite este parámetro.

</dd> </dl>

## <a name="remarks"></a>Observaciones

En el objeto de sección crítica, normalmente realizará una de las siguientes acciones:

-   Derive una clase que herede tanto **CBaseFilter** como **CCritSec**. En el caso de *Plock*, pase el `this` puntero.
-   Derive una clase que herede **CBaseFilter** y contenga una variable miembro de **CCritSec** . En el caso de *Plock*, pase la dirección de esa variable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




