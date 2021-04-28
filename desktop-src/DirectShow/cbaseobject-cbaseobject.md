---
description: 'Constructor CBaseObject.CBaseObject: método constructor.'
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: Constructor CBaseObject.CBaseObject (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14fa2d3d38d42fa0feb387b477205cc51e0b6b87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099623"
---
# <a name="cbaseobjectcbaseobject-constructor"></a>Constructor CBaseObject.CBaseObject

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Cadena que contiene el nombre del objeto, con fines de depuración.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Este método incrementa el recuento de objetos activos. (Vea [**CBaseObject::ObjectsActive).**](cbaseobject-objectsactive.md)

Asigne el *parámetro pName* en la memoria estática:


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



La [**macro NAME**](name.md) se compila en NULL **en** las compilaciones comerciales, de modo que las cadenas estáticas solo aparecen en las compilaciones de depuración. Para obtener más información, [**vea DbgDumpObjectRegister**](dbgdumpobjectregister.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseObject (clase)**](cbaseobject.md)
</dt> </dl>

 

 




