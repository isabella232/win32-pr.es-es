---
description: Método de constructor.
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: Constructor CBaseAllocator. CBaseAllocator (Amfilter. h)
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
ms.openlocfilehash: 98a1ba1163058f92fba666177d0ff82331dd528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660116"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a>Constructor CBaseAllocator. CBaseAllocator

Método de constructor.

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

*pUnk* 
</dt> <dd>

Puntero al propietario de este objeto. Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación. De lo contrario, establezca este parámetro en **null**.

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a un valor **HRESULT** . Establezca el valor en es \_ correcto antes de crear el objeto. Si se produce un error en el constructor, el valor se establece en un código de error.

</dd> <dt>

*ventilación* 
</dt> <dd>

Valor booleano que indica si se va a crear un semáforo. Si **es true**, el asignador crea un semáforo ([**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md)), que se señala cada vez que una muestra está disponible. Establezca el valor en **false** si está implementando una clase derivada que no requiere un semáforo.

</dd> <dt>

*fEnableReleaseCallback* 
</dt> <dd>

Valor booleano que indica si está habilitado el mecanismo de devolución de llamada de versión. Establezca el valor en **true** si desea proporcionar una interfaz de devolución de llamada, a la que se llama cuando se liberan los búferes. Especifique la devolución de llamada mediante una llamada al método [**CBaseAllocator:: SetNotify**](cbaseallocator-setnotify.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




