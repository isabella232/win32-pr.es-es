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
ms.openlocfilehash: 35443d212fc244c80da958f2f87d03363c59348be4189393c1c3493521a0439b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076585"
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

Cadena que contiene el nombre del objeto con fines de depuración.

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
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseObject (clase)**](cbaseobject.md)
</dt> </dl>

 

 




