---
description: 'Constructor CBaseFilter.CBaseFilter(const \* TCHAR, LNOWN, CCritSec \* , REFCLSID): método constructor.'
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: Constructor CBaseFilter.CBaseFilter(const *TCHAR, LNOWN, CCritSec*, REFCLSID) (Amfilter.h)
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
ms.openlocfilehash: 8455e78096af7bc2ca82a2b7634ceac14b2bdf6e918f62f8ae0fa64308f4b9a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640655"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a>Constructor CBaseFilter.CBaseFilter(const \* TCHAR, LNOWN, CCritSec \* , REFCLSID)

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBaseFilter(
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

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para el objeto de sección crítica, normalmente haría una de las siguientes acciones:

-   Derive una clase que herede **tanto CBaseFilter** como **CCritSec.** Para *pLock*, pase el `this` puntero.
-   Derive una clase que hereda **CBaseFilter** y contiene una variable **miembro CCritSec.** Para *pLock*, pase la dirección de esa variable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




