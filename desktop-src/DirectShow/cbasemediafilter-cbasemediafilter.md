---
description: Método de constructor.
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: Constructor CBaseMediaFilter. CBaseMediaFilter (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498e9da88804291fc5cdb900ff1dbda212e8b0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670585"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a>Constructor CBaseMediaFilter. CBaseMediaFilter

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del objeto.

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

Identificador de clase del objeto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si otro objeto contiene o agrega el `CBaseMediaFilter` objeto, el bloqueo **CCritSec** podría ser externo al `CBaseMediaFilter` objeto. En ese caso, pase un puntero al bloqueo en *Plock*.

De lo contrario, puede:

-   Derive una clase que herede `CBaseMediaFilter` y **CCritSec**. En el caso de *Plock*, pase el puntero this.
-   Derive una clase que herede `CBaseMediaFilter` y contenga una variable miembro **CCritSec** . En el caso de *Plock*, pase la dirección de esa variable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




