---
description: 'Constructor CBaseMediaFilter.CBaseMediaFilter: método constructor.'
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: Constructor CBaseMediaFilter.CBaseMediaFilter (Amfilter.h)
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
ms.openlocfilehash: 264363ebb7194504dd16a94c0835bab0a4fe0163edd31329b77853510c9523db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917015"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a>Constructor CBaseMediaFilter.CBaseMediaFilter

Método constructor.

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

Identificador de clase del objeto.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si otro objeto contiene o agrega el `CBaseMediaFilter` objeto, el **bloqueo CCritSec** podría ser externo al `CBaseMediaFilter` objeto . En ese caso, pase un puntero al bloqueo en *pLock*.

De lo contrario, puede:

-   Derive una clase que herede y `CBaseMediaFilter` **CCritSec**. Para *pLock*, pase el puntero this.
-   Derive una clase que hereda `CBaseMediaFilter` y contiene una variable miembro **CCritSec.** Para *pLock*, pase la dirección de esa variable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseMediaFilter (clase)**](cbasemediafilter.md)
</dt> </dl>

 

 




