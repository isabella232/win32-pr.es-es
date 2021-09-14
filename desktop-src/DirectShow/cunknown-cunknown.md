---
description: 'Constructor CUnknown.CUnknown: método constructor.'
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: Constructor CUnknown.CUnknown (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32859871f8ef69ce357fe204f0741356314fbb06
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255272"
---
# <a name="cunknowncunknown-constructor"></a>Constructor CUnknown.CUnknown

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Cadena que contiene el nombre del objeto; se usa en el constructor [**CBaseObject**](cbaseobject.md) para la depuración.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntero al propietario de este objeto. Si el objeto se agrega, pase un puntero a la interfaz IUnknown del objeto de agregación. De lo contrario, establezca este parámetro en **NULL.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

El objeto se inicializa con un recuento de referencias de cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




