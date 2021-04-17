---
description: Método de constructor.
ms.assetid: 2340b39a-cab6-4524-b8cd-b22d4bdd24d0
title: Constructor CMemAllocator. CMemAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b650e23761c3fe5b3f5014666f90c679f088c4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670757"
---
# <a name="cmemallocatorcmemallocator-constructor"></a>Constructor CMemAllocator. CMemAllocator

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CMemAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del asignador.

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntero al propietario de este objeto. Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación. De lo contrario, establezca este parámetro en **null**.

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a una variable que recibe un valor **HRESULT** que indica si el método se ha ejecutado correctamente o no.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




