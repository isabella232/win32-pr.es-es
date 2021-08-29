---
description: 'Constructor CMemAllocator.CMemAllocator: método constructor.'
ms.assetid: 2340b39a-cab6-4524-b8cd-b22d4bdd24d0
title: Constructor CMemAllocator.CMemAllocator (Amfilter.h)
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
ms.openlocfilehash: 9ef77a05eefc84975539bdc4e61b534a7ed5ee71d00e029bdf7ef2af8c19e666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016243"
---
# <a name="cmemallocatorcmemallocator-constructor"></a>Constructor CMemAllocator.CMemAllocator

Método constructor.

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

*Punk* 
</dt> <dd>

Puntero al propietario de este objeto. Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación. De lo contrario, establezca este parámetro en **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o error del método.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMemAllocator (clase)**](cmemallocator.md)
</dt> </dl>

 

 




