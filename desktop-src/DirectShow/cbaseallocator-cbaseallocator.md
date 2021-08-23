---
description: 'Constructor CBaseAllocator.CBaseAllocator: método constructor.'
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: Constructor CBaseAllocator.CBaseAllocator (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21da9f5dda7f60fd4a88e85eb28f2197bdc9847d0b56d413bd6b49cb5abfe658
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641005"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a>Constructor CBaseAllocator.CBaseAllocator

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBaseAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   BOOL      bEvent = TRUE,
   BOOL      fEnableReleaseCallback = FALSE
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Puntero a una cadena que contiene el nombre de depuración del asignador. Para obtener más información, vea [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*Punk* 
</dt> <dd>

Puntero al propietario de este objeto. Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación. De lo contrario, establezca este parámetro en **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a un **valor HRESULT.** Establezca el valor en S \_ OK antes de crear el objeto. Si se produce un error en el constructor, el valor se establece en un código de error.

</dd> <dt>

*bEvent* 
</dt> <dd>

Valor booleano que indica si se debe crear un semáforo. Si **es TRUE,** el asignador crea un semáforo ([**CBaseAllocator::m \_ hSem**](cbaseallocator-m-hsem.md)), que se señala cada vez que hay disponible un ejemplo. Establezca el valor en **FALSE** si va a implementar una clase derivada que no requiere un semáforo.

</dd> <dt>

*fEnableReleaseCallback* 
</dt> <dd>

Valor booleano que indica si el mecanismo de devolución de llamada de versión está habilitado. Establezca el valor en **TRUE si** desea proporcionar una interfaz de devolución de llamada, a la que se llama cuando se liberan búferes. Especifique la devolución de llamada llamando al [**método CBaseAllocator::SetNotify.**](cbaseallocator-setnotify.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




